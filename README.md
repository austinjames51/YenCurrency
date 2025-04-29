# YenCurrency
This is just a repository for the types.xml for psyopgirl's Yen Currency mod which can be found here: ttps://steamcommunity.com/sharedfiles/filedetails/?id=3434475139&searchtext=yen+currency

# 💴 Yen Currency Types file for DayZ

This types file adds Yen currency items to your DayZ server's economy using a standalone `types.xml` configuration. It does NOT include the mod. You will need to download that and add it to your server using the instructions on the modpage.

---

## 📂 Files Included

- `Yen_Currency_types.xml`

---

## 🛠️ Installation Guide

Follow these steps to install the Yen Currency mod on your DayZ server:

### 1. Navigate to Your Mission Folder

Go to: 

mpmissions\yourmapname\

### 2. Create a Custom Economy Folder

If you haven't already, create a folder named:

mods_ce

### 3. Add the Types File

Place `Yen_Currency_types.xml` inside the `mods_ce` folder.

### 4. Edit `cfgeconomycore.xml`

Open the file located at:

mpmissions\yourmapname\cfgeconomycore.xml


Scroll to the bottom and add the following before the closing `</economy>` tag:

<ce folder="mods_ce">
    <file name="Yen_Currency_types.xml" type="types" />
</ce>

### 5. Restart Your Server
After saving your changes and uploading the updated files, restart your server to apply the new economy data.


### Notes
The types file does not add any spawn points or loot tables — it simply defines Yen currency item types. It also will not spawn ANY of the currency. You will need to change the min and nominal values to have them spawn. Adding 10 for example to the nominal will make it spawn initially and when the amount in the min is 0 it will be replaced when there are 0 left in the world. I've also changed the value to last 6 hours on the ground/stored somewhere and 3 hours between spawning the items in so that players won't loot an area, run away, and have them spawn back. The whole point of this repository types.xml is that currency will not despawn if dropped onto the ground or stored somewhere. 

You can integrate these items with your loot spawn system or traders manually if needed with psyopgirl's instructions in the mod page.

