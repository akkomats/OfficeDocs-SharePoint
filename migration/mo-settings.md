---
title: "Migration Manager settings"
ms.reviewer: 
ms.author: jhendr
author: JoanneHendrickson
manager: pamgreen
audience: ITPro
ms.topic: article
ms.prod: sharepoint-server-itpro
localization_priority: Priority
ms.collection: 
- IT_Sharepoint_Server_Top
- SPMigration
- M365-collaboration
description: "A complete listing of the Migration Manager basic and advanced settings." 
---

# Migration Manager Settings

The following table details the settings available in the Migration Manager. Advanced settings should only be changed or managed by your IT professional. 

**General**
 
|**Setting**|**Description**|
|:-----|:-----|
|Only perform scanning|If you wish to scan the files as a pre-assessment to migration, turn **Only perform scanning** on.|
|Start migration automatically if no scan issue found |If set to **On**, migration will start automatically if no scan issues are found. |
|Preserve file share permissions.|Preserve permissions on the files migrated.|


**Users**

|**Setting**|**Description**|
|:-----|:-----|
|Azure Active Directory lookup |By default, this is set to **On**. If no user mapping file is provided by the user, then Azure Active Directory is used as the default for user mapping.|
|User mapping file|By default,  *Azure AD lookup*  is used to map users when submitting migration jobs. If you wish to use your own mapping file, select the file to be used by clicking **Choose file**. If you choose to use a custom user mapping file and want to preserve user permissions, turn off  *Azure Active Directory lookup*. By doing so, if a user isn't found in the mapping file, the tool won't look it up in AAD.|


**Filters**

|**Setting**|**Description**|
|:-----|:-----|
|Migrate file version history |If set to **Off**, only the most recent version of the file will be migrated. If set to **On**, you can choose whether to keep all versions, or limit it to a specific number.|
|Keep all versions|If set to **On**, all versions of a file will be migrated.|
|Number of versions to migrate|Enter a number to limit the number of file versions migrated.|
|Migrate hidden files|If set to **Off**, hidden system files will **not** be migrated. |
|Migrate files created after|Only migrate files created after the selected date. This may be to limit the number of files migrated or to adhere to overall company governance policy regarding file retention.|
|Migrate files modified after|Only migrate files modified after the selected date. This may be to limit the number of files migrated or to adhere to overall company governance policy regarding file retention. |
|Do not migrate files with these extensions|Enter a list of file extensions of file types you do not want to migrate. Separate each extension entered with a colon. Do not include the dot.  Example: TXT:EXE:JPEP: </br> **Note** For files with multiple file extensions, eg. .ext1.ext2, add only the last extension, ext2, to the exclusion list.|
|Migrate files and folders with invalid characters|By default, the setting is set to **On**. This is the recommended setting. The tool will attempt to move all the files without filtering on characters. If any file can't be accepted into SPO, a failure message will be generated for that file.  <br/><br/>  If set to **Off**, the tool will skip any potential special characters. While this can improve performance when the source potentially contains a high number of files containing invalid characters, it also has drawbacks. To prevent malicious activities, source packages that generate more than 100 errors to the destination server will be blocked. As a result, all valid files in that package would also be blocked.  <br/> |
|Migrate OneNote folder as OneNote notebook <br/>|By default, this is set to **Off**. When set to **Off**, OneNote folders will not migrate over as a notebook.  At this time the ability to migrate notebooks on SharePoint on-premises is disabled.<br/>|
|Filter subsites|Enter any subsite names you want to exclude from migration.|
|Filter lists and libraries|Enter the names of the lists and libraries you want to exclude from migration.|
|Filter content type|Enter the content types you want to exclude from migration.|


**Advanced**

|**Setting**|**Description**|
|:-----|:-----|
|Migration auto re-run|Choose if you want to automatically rerun a migration task to look for changes or additions. Select either Run once, or Run up to 5 successive times.|
|Migration Manager work folder  <br/> |Choose if you want to create your own working folder.  By default, a temp folder will be created. <br/> **Note:** By default, the working folder is `%appdata%\Microsoft\MigrationTool`. Please make sure that your working folder has a minimum of 150 GB of free space. It may need more depending on the size of the data you plan to migrate.|
|Use custom Azure storage|If you wish to use your own Azure storage, set this value to **On**.  Enter your account and key, select if you want to enable or disable encryption, and if you want temporary working files to be deleted when migration is complete.  <br/> **Note:** This feature is supported only for *General Purpose storage accounts*  as General Purpose accounts support Azure blobs and queues. This feature is not available for Blob Storage accounts.|
   


