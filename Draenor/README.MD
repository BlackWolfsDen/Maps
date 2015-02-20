----------------------------------------------------------------------------------------------------------------------
this adds area name above mini-map.
----------------------------------------------------------------------------------------------------------------------
required software:

 * mpq editor
 
 * CASCExplorer
 
 * MS excel
 
 * notepad
 
 * Bulk Rename Utility
 
 * dbc->cvs->dbc converter
 
----------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------
After downloading Anthony's Toolbox map, open the patch and create a folder named "DBFilesClient" 
inside it and save the patch.
Now create 2 folders on your c: drive.

 * 1 temporary folder called C:/WoD

 * 1 temporary folder called C:/Wotlk

----------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------
now with CASCExplorer pointing at your WoD wow.exe folder, open CASCExplorer. this will take a short bit.

now navigate to the DBFilesClient folder in the CASCExplorer screen and extract these 4 dbc files to your C:/WoD temp folder.

 * AreaTable.dbc

 * Map.dbc

 * WorldMapArea.dbc

 * WorldMapContinent.dbc

now navigate to the DBc folder of your 3.3.5a Trinity Core server and extract these same 4 dbc files to your C:/wotlk working folder.

 * AreaTable.dbc

 * Map.dbc

 * WorldMapArea.dbc

 * WorldMapContinent.dbc

----------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------

now first conver C:/WoD/Map.dbc to a .cvs file. once its converted , open it up with notepad and search for the map name you want to add the minimaps to.
i will use Draenor as an example:

"1116,"Draenor",0,8404573,1,"Draenor",,,,,,,,,,,,,,,,0xFF01FE,0,"",,,,,,,,,,,,,,,,0xFF01FC,"",,,,,,,,,,,,,,,,0xFF01FC,360,1.0,0,0.0,0.0,-1,0x2,0x0,0x0,"

entry id 1116 is for Draenor. this id is the WoD map id. rather than changing everything over to id 900 like Anthony says in his tutorial i will leave everything using this map id instead. so remember this map id (1116).

now copy the entry 1116 to your clipboard(Ctrl+C).
now convert C:/WotlK/Map.dbc to a cvs file and open it up in notepad. scroll to the bottom and add entry 1116. close Map.dbc.cvs.
Open the C:/WotlK/Map.dbc.cvs with MS Excel and scroll to the new entry at the bottom and confirm the data lines up wwith the Wotlk map entries.
entry 1116 should now look like this:
 * "1116,"Draenor",0,1,0,"Draenor",,,,,,,,,,,,,,,,0xFF01FE,0,"",,,,,,,,,,,,,,,,0xFF01FC,"",,,,,,,,,,,,,,,,0xFF01FC,360,1.0,0,0.0,0.0,-1,0x2,0x0,0x0,"

In Excel save the file as a cvs (comma delimited).
convert C:/Map.dbc.cvs back into a dbc file.

----------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------
NOW extracting everything that deals with the map id you want.(1116)
----------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------

convert C:/WoD/WorldMapContinent.dbc to a cvs. open it with notepad and scroll down until you find the entry that contains the map id(1116) in the second column entry:
"13,1116,0,0,0,0,0.0,0.0,1.0,-4771.0,-6276.0,11630.0,10120.0,0,1,"

copy this entry to your clipboard.

now convert C:/WotlK/WorldMapContinent.dbc to a cvs and add this entry at the bottom and save.
now open the C:/WotlK/WorldMapContinent.dbc.cvs with MS Excel and verify the data lines up properly with the Wotlk data entries.

It should look like this now:
"13,1116,0,0,0,0,0.0,0.0,1.0,-4771.0,-6276.0,11630.0,10120.0,0,"

In Excel save the file as a cvs (comma delimited).
convert C:/WotlK/WorldMapContinent.dbc.cvs back into a dbc file.

----------------------------------------------------------------------------------------------------------------------

convert C:/WoD/WorldMapArea.dbc to a cvs and open.
now open word pad off to the side.
now search and extract every line that has the map id (1116) for column 2 and paste to your . 

 + 941,1116,6720,"Frostfire Ridge",7506.25,1391.67004395,8275.0,4197.91992188,-1,0,962,0x0,90,93,
 + 9945,1116,6723,"Tanaan Jungle",1506.25,-3481.25,5760.41992188,2435.41992188,-1,0,962,0x0,100,100,
 + 9946,1116,6662,"Talador",5833.33007813,-129.166000366,4429.16992188,454.165985107,-1,0,962,0x0,94,96,
 + 9947,1116,6719,"Shadowmoon Valley DR",2268.75,-4431.25,2660.41992188,-1806.25,-1,0,962,0x0,90,93,
 + 9948,1116,6722,"Spires Of Arak",4681.25,-1379.17004395,1383.32995605,-2656.25,-1,0,962,0x0,96,98,
 + 9949,1116,6721,"Gorgrond",5066.66992188,-3110.41992188,9589.58007813,4139.58007813,-1,0,962,0x0,92,94,
 + 9950,1116,6755,"Nagrand Draenor",9308.33007813,3633.33007813,4922.91992188,1139.57995605,-1,0,962,0x0,98,100,
 + 9962,1116,0,"Draenor",12242.34375,-10493.4384766,11193.0,-3964.1875,-1,0,0,0,0,
 + 9971,1116,7078,"garrison smv alliance",545.833984375,-137.5,2091.66699219,1635.41699219,-1,0,947,0x1820,0,0,
 + 9973,1116,7078,"garrison smv alliance_tier1",545.833984375,-137.5,2091.66699219,1635.41699219,-1,0,947,0x822,0,0,
 + 9974,1116,7078,"garrison smv alliance_tier3",545.833984375,-137.5,2091.66699219,1635.41699219,-1,0,947,0x822,0,0,
 + 9975,1116,7078,"garrison smv alliance_tier4",545.833984375,-137.5,2091.66699219,1635.41699219,-1,0,947,0x822,0,0,
 + 9976,1116,7004,"garrison ff horde",4885.41601563,4183.33300781,5814.58300781,5345.83300781,-1,0,941,0x1820,0,0,
 + 9978,1116,6941,"Ashran",-2672.91992188,-5795.83007813,5577.08007813,3495.83007813,-1,0,0,0x0,100,100,
 + 9980,1116,7004,"garrison ff horde_tier1",4885.41601563,4183.33300781,5814.58300781,5345.83300781,-1,0,941,0x822,0,0,
 + 9981,1116,7004,"garrison ff horde_tier3",4885.41601563,4183.33300781,5814.58300781,5345.83300781,-1,0,941,0x822,0,0,
 + 9982,1116,7004,"garrison ff horde_tier4",4885.41601563,4183.33300781,5814.58300781,5345.83300781,-1,0,941,0x822,0,0,
 + 9990,1116,7004,"garrison ff horde_tier2",4885.41601563,4183.33300781,5814.58300781,5345.83300781,-1,0,941,0x822,0,0,
 + 9991,1116,7078,"garrison smv alliance_tier2",545.833984375,-137.5,2091.66699219,1635.41699219,-1,0,947,0x822,0,0,
 + 91009,1116,7332,"Ashran Alliance Faction Hub",-3625.0,-4312.5,3908.33300781,3450.0,-1,0,978,0x0,0,0,
 + 91011,1116,7333,"Ashran Horde Faction Hub",-3589.58398438,-4389.58398438,5541.66601563,5008.33300781,-1,0,978,0x0,0,0,

convert C:/WotlK/WorldMapArea.dbc to a cvs and open. now scroll to the bottom and add these entries and save.
now open C:/WotlK/WorldMapArea.dbc.cvs with MS Excel and edit/verify new entries line up properly with Wotlk Entries.
In Excel save the file as a cvs (comma delimited).
convert C:/WotlK/WorldMapArea.dbc.cvs back into a dbc file.

----------------------------------------------------------------------------------------------------------------------
convert C:/WoD/WorldMapArea.dbc to a cvs and open.
now open a new word pad off to the side.

now search and extract every line that has the map id (1116) for column 2 and paste to your .
column 3 may be recursive so go line by line of each map id (1116) and verify column 3 entry is an entry that also exsists with the 
extracted entries . if column 3 entry was not extracted then find it and extract it with the rest. 
missing entries WILL cause client to crash when player enters the missing entry area. i.e entry gets recursive call from column 3 but entry doesnt exsist.
so go thru and triple check that you have extracted EVERY entry that has map id (1116) in column 2.

convert C:/WotlK/AreaTable.dbc to a cvs and open. now scroll to the bottom and ALL add these entries and save.
now open C:/WotlK/AreaTable.dbc.cvs with MS Excel and edit/verify new entries line up properly with Wotlk Entries.
In Excel save the file as a cvs (comma delimited).
convert C:/WotlK/AreaTable.dbc.cvs back into a dbc file.

now go back to your custom map patch you downloaded from Anthony's Toolbox open it and add these 4 files to the DBFilesClient folder you created in it.
 * C:/WotlK/AreaTable.dbc
 * C:/WotlK/Map.dbc
 * C:/WotlK/WorldMapArea.dbc
 * C:/WotlK/WorldMapContinent.dbc
 
 close the patch. rename it patch-4.mpq and add it to your folder /world of warcraft/data/
 start WoW and enjoy.

----------------------------------------------------------------------------------------------------------------------
AreaTable.dbc example:
----------------------------------------------------------------------------------------------------------------------
 + 96662,1116,0,5296,0x40,0,0,84,1143,1498,0,Talador,,,,,,,,,,,,,,,,0xFF01FE,0x0,0,,,0,-500.0,0.0,
 + 96719,1116,0,5351,0x40,0,0,96,1148,1455,-1,Shadowmoon Valley DR,,,,,,,,,,,,,,,,0xFF01FE,0x0,0,,,0,-500,0,
 + 96720,1116,0,5352,0x41,0,0,96,1147,1478,-1,Frostfire Ridge,,,,,,,,,,,,,,,,0xFF01FE,0x0,0,,,0,-500,0,

----------------------------------------------------------------------------------------------------------------------
