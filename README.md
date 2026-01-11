Download Instructions:
1. Click "QuickWaypointEnemyCapper.zip"
2. Click the "..." button in the top right of page.
3. Select "Download"
# Quick Waypoint Enemy Capper
Provides a keybind to waypoint the most recent enemy player to grab your flag from the flagstand (using T2's built-in waypoint system).

### Important Note - This Script Does Not Work on Taco's Server
It is most important to know that this script does *not* work on server's running Taco's server config (https://github.com/ChocoTaco1/TacoServer). The reason for this is that the data required to create the capper waypoint is not exposed to clients on Taco's servers. This means that, for the most common community use cases, this script is non-functional. However, I am still sharing this script for reference. I fully completed it before realizing it was not compatible. 

### Summary
The purpose of this script is to provide a keybind that quickly allows the script user to waypoint the most recent enemy player which grabbed  the flag off of your flagstand. The script uses T2's built-in "AttackPlayer" task (as opposed to using the "createWaypoint()" function used by scripts like BuddyPoints). This means that one and only one waypoint can be created at any time. It also means that this waypoint will be removed if the user accepts *any other* task. 

In other words, it's the exact same functionality as a) right-clicking an enemy player via the command map, b) selecting "Attack" via the menu option,  and then c) using the quickchat menu to accept that task (using VCA). All of these actions are shortcutted into a single keybind.

The goal is to support quick enemy capper waypointing with at least some restrictions. If one were to use the "createWaypoint()" function, then that action essentially bypasses the way T2 intended players to waypoint enemies.

Beyond all of the above, the following additional points are important to know:
1. The script will only waypoint the most recent enemy player to grabbed your flag off the flag stand. If a player has not yet grabbed the flag, then no waypoint can be created. If a player grabs the flag in the field, then a waypoint will *not* be created for that player.
2. The purposeful goal is to help defense map one and only one capper from the enemy team. Ideally, a person would waypoint the capper they feel is most dangerous.
3. Given that this uses T2's built-in task system, the capper waypoint will be cleared / removed according to the exact same logic that T2 uses to clear / remove tasks. This applies for switching teams, leaving a match, matches ending, and loading a new match.
