# PC Startups and DeepFreeze

Ok, this really is kinda our Bread-and-Butter, and we need to make sure they're all working correctly. No PCs, no teaching, sad students, crap NSS.

## Aims
To ensure all PCs are starting up and working correctly, and that DeepFreeze is correctly communicating with them.

## Gotchas!
* **WoL (as of the time of writing) doesn't work correctly ~~in INB2102/2B~~ anywhere - you'll have to run around manually**

## Procedure 
* Log in to DeepFreeze and navigate to the "Computers" tab
* We will be using the built in Wake-on-LAN feature to turn on and test communication with all PCs
   * Due to the nature of WoL, we have to stagger the startup of all PCs - we do this manually 
   * Using the search bar under "Computer Name" search 1 row of desks at a time, like 1A-A
   * Select all PCs under that search term and click "Wakeup" from the actions row
   * **Repeat for all rows in all labs! It doesn't take long, promise!**
* Once that has been done for all PCs, visit each lab and check everything is on
  * Is a PC off? It could be a case of the WoL packet didn't reach the PC - try turning on manually and checking network connections. Sometimes it just doesn't work for some reason
  * If a PC fails to turn on or boot at all, quickly investigate as to why, and prepare it for a repair if needed
  * Because lab sessions are _sometimes_ underbooked, have absences or have people using BYOD, a PC being out of action for a day is not a huge issue. However, to maintain appearances we do need to ensure we get a fix sorted ASAP
* Nothing turned on at all?
  * Is the power actually working? If no PC turns on it could be an issue with some of our circuits - a diagnostic will be outlined in an upcoming docs page
  * If PCs do turn on manually, it could be an issue with DeepFreeze, or, Networks