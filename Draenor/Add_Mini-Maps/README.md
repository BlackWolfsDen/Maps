----------------------------------------------------------------------------------------------------------------------
This adds the mini-maps.
----------------------------------------------------------------------------------------------------------------------
required software:

 * mpq editor
 
 * CASCExplorer
 
 * MS excel
 
 * notepad
 
 * Bulk Rename Utility
 
 * Anthony'sToolbox Draenor patch -> http://adf.ly/w9AwQ . Private request me for non AdF.ly link.
 
----------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------

After downloading Anthony's toolbox Draenor map patch, rename it to patch-4 and save it to your "c:/world of warcraft WotlK/data/" folder.

 * create a folder named C:/WotlK/

----------------------------------------------------------------------------------------------------------------------

open patch-3.mpq with mpqeditor:
 * C:/world of warcraft/data/patch-3.mpq

navigate:
 * Textures/Minimap/

extract:
 * md5translate.trs to your folder(C:/WotLK/).

----------------------------------------------------------------------------------------------------------------------

open CASCExplorer.exe.xml:

 * edit wow path = proper location of WoD wow.exe
 * edit OnlineMode = false

run CASCExplorer pointing to your WoD .exe

 * navigate /Textures/minimaps/Draenor/
 * extract Draenor folder to your folder(C:/WotLK/).

open C:/WotLK/World/minimaps/md5translate.trs with note pad.

 * add line "dir: Dreanor" no gaps and then save.

----------------------------------------------------------------------------------------------------------------------

go to folder C:/WotLK/World/minimaps/.
 * open command prompt in same folder and type "dir /a-d /b /s > z1.txt
 * a new file will appear z1.txt

open file z1.txt
 * delete first useless data lines.

 * use  ctrl+H Replace "x:\xxx\xxx\xxx\" `long folder address` and `Replace ALL` with "" so the folder address is just the "MAP_FOLDER\MAP_NAME.blp"

 * save file.

 * select all entries (Ctrl+A) and copy (Ctrl+C).

 * open MS Excel and paste entries to column A1.

open BulkRenameUtility:
 * Action menu // Jump To Path // enter "C:/WotLK/World/minimaps/Draenor/" now you should see all the .blp files in the Bulk Rename Utility

 * select all .blp's(Ctrl+A) and replace(3) Replace "map" With "Draenor"

 * click Rename button then click ok, wait then close Bulk Rename Utility.

----------------------------------------------------------------------------------------------------------------------

go to folder C:/WoD/World/minimaps/.
 * open command prompt in same folder and type "dir /a-d /b /s > z2.txt"

 * a new file will appear z2.txt

 * open z2.txt and select all (Ctrl+A) and copy all (Ctrl+C)

 * delete first to data lines

 * use  ctrl+H Replace "x:\xxx\xxx\xxx\" `long folder address` and replace ALL with "" so the address is just the "MAP_NAME.blp"
and copy all lines (Ctrl+C)

 * go back to MS Excel window and add those lines to column B1

 * then copy BOTH columns (CTRL+A)

 * open C:/WotLK/Textures/Minimap/md5translate.trs with note pad.

 * Paste those 2 columns after line "dir: Dreanor" . no gaps.

 * save md5translate.TRS

 * DELETE z1.txt and z2.txt

----------------------------------------------------------------------------------------------------------------------

now copy ALL minimaps blp files form C:/WotLK/WORLD/Minimaps/Draenor/ and save with md5translate.TRS file in C:/WotLK/Texture/Minimaps/.

now add the 2 folders in "C:/WotLK/" (DBFilesClient, Textures and WORLD) to the patch patch-4.mpq in your C:/world of warcraft/data/ folder.

close the patch-4.mpq

start wow.

enjoy





