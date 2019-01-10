---
seo-title: Updating a DRM policy with the Java API
title: Updating a DRM policy with the Java API
uuid: ec21351c-900e-48f5-845a-c0b430c210d7
index: y
internal: n
snippet: y
---

# Updating a DRM policy with the Java API{#updating-a-drm-policy-with-the-java-api}

To update a DRM policy with the Java API:

1. Set up your development environment and include in your project all of the JAR files listed in [Setting up the development environment](../../protecting-content/setting-up-the-sdk/setting-up-the-sdk.md#c_content-setting-up-the-sdk). 
1. Create a DRM `Policy` instance and read the DRM policy from a file or database. 

   ```
   Policy policy = new Policy(policyBytes);
   ```

1. Update the DRM `Policy` object by setting its properties, such as its name and usage rules. 

   ```java
   // Change the DRM policy name.  
   policy.setName("UpdatedDemoPolicy");  
     
   // Add DRM module restrictions to the play right  
   for (Right r: policy.getRights()) {  
       if (r instanceof PlayRight) {  
           PlayRight pr = (PlayRight) r;  
           // Disallow Linux versions up to and including 1.9.  Allow  
           // all other OSes and Linux versions above 1.9  
           VersionInfo toExclude = new VersionInfo();  
           toExclude.setOS("Linux");  
           toExclude.setReleaseVersion("1.9");  
           Collection<VersionInfo> exclusions = new ArrayList<VersionInfo>();  
           exclusions.add(toExclude);  
           ModuleRequirements drmRestrictions = new ModuleRequirements();  
           drmRestrictions.setExcludedVersions(exclusions);  
           pr.setDRMModuleRequirements(drmRestrictions);  
           break;  
       }  
   }
   ```

1. Serialize the updated DRM `Policy` object and store it in a file or database. 

   ```java
   // Serialize the DRM policy.  
   byte[] policyBytes = policy.getBytes();  
   System.out.println("New DRM policy revision number: "  
       +  policy.getRevision());      
   // Write the DRM policy to a file.   
   // Alternatively, the DRM policy may be stored in a database.  
   FileOutputStream out = new FileOutputStream("demopolicy-updated.pol");  
   out.write(policyBytes);  
   out.close();
   ```

See `com.adobe.flashaccess.samples.policy.UpdatePolicy` in the Reference Implementation Command Line Tools [!DNL samples] directory for the source of this sample code. 
