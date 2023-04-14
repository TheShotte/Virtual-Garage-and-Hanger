# Virtual-Garage-and-Hanger
Adds the ability to save invetory, and adds a public virtual hanger


             
	License
	--------------------------
	All the code and information provided here is provided under an Attribution Non-Commercial ShareAlike 4.0 Commons License.

	http://creativecommons.org/licenses/by-nc-sa/4.0/
	
Credits: Based on the virtual garage released by Shix

Description: modified to add ability to store inventory, skins, and a nickname
             Capacity to have virtual hangers for aircraft added as well.
	     
Requires: you must run a 64 bit Exile server using extDB3.

https://github.com/BrettNordin/Exile

Difficulty: significant expertise with scripting required.

Installation:

[This one is a bit complicated, be sure to make backups before starting]

Mission Integration:

Merge the contents of the "Exile.Altis\addons" folder with your mission folder.

Merge the contents of "Exile.Altis\config.hpp" with your mission's config.cpp

Merge the contents of "Exile.Altis\description.ext" with your mission's description.ext

Merge the contents of "Exile.Altis\init.sqf" with your mission's init.sqf.

Copy the "Exile.Altis\GRG_Exile_Server_Overrides" directory into your mission folder.

An example of virtual hanger terminals and spawn points I use is included.

Server:

Pack the "@ExileServer\addons\VirtualGarage_Server" folder and move the resulting VirtualGarage_Server.pbo to your @ExileServer\addons directory.

Backup your MySQL Exile database, then run the "database\virtual_garage.sql" and "database\exileDBupdate.sql" database queries respectively
- "database\virtual_garage.sql" adds the virtual garage table
- "database\exileDBupdate.sql" adds a field for weapons loadouts to the existing vehicles table
Merge the contents of "@ExileServer\extDB\sql_custom_v2\exile.ini" with your existing extDB3 exile.ini (be sure to make a backup first).

SPECIAL NOTES.

The virtual garage / hanger / boatrack does require one set of functions from my rearm / repair / refuel scripts.
If you have already installed that set of scripts you do not need to include the code listed in init.sqf to make virtualGarage run.
