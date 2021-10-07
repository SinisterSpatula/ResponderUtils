### How To Update ###
`
On the controller head to database -> reset and click the download button, so that you have a current backup of your database.  Next, find the viewcontent/download link from your purchase email to download the newest version.  Then, replace both of your plug-in folders (controller AND utilities) with the new version.  If needed, go back to database -> reset screen and click upload to restore your database backup file.
`
<br/>
<br/>

## 10/7/21 v1.0.12 ##
Important fixes: Added Stun/Turn servers to make connections establish more reliably.  This should make a large improvement especially for users with NAT/firewall/VPN blocking issues.  The plug-ins will still use a direct connection over LAN if possible, but now has stun/turn as a fallback when direct connections aren't working.
* Added the flag graphic to the header at the top of every bank page.
* fix issue with target redeem sometimes not displaying balance.
* fixed "unexpected end of json" error when the tool was checking to see if a new version was available.
* (see new fixes under 1.0.11 also as those are included in this version). 

## 10/1/21 v1.0.11 ##
Important fixes: Added merril edge investing accounts.  They will have quickview, but no real account page.  Visit the Loan Mortage and Investing Accounts on your profile dashboard to create the accounts and they will appear on the main bank page under investments.
* added 11 more walmart giftcards to the GC database.
* Zelle: change newly created zelle transfers status from completed to processing.
* Add support for target balance (from gift redeems): it will remember your redeem balance for up to 30 minutes from the last redemption and then reset back to zero.  Also made target redeem more reliable, and more spoofing of customer info. 
* Added Transfers to the database section.  You can edit existing transfers and give them some fun new status options: (ex: fraud, refunded, rejected, disputed, etc)
<br/>
<br/>


## 9/21/21 v1.0.10 ##
Important fixes: (bank transfers screen) swapped location of From/To and expand amount box, change text inside amount box to left-align, and remove notes box, it now compares much better to the real screen.
* logs/captures: Add Saved Logs (from controller) to the logs screen, so now both logs and captures will have a local backup on the controller.
* logs/captures: Logs will be sent to the controller also when they occur (to ensure we get a copy onto the controller if there is a connection established), previously it was just the red indicator that was sent.
* Zelle: Will now show an over the limit error if scammer tries to transfer more than 1,000 (previously the page would just reload).
<br/>
<br/>


## 9/17/21 v1.0.9 ##
Important fixes: Controller will start keeping backup's of captures (logs screen), so if you revert vm snapshots you won't lose your captures.  You can delete the backed up captures by clicking the delete all button on the logs screen.
* logs/captures: changed user number to user name.
* captures: will be sent to the controller also when they occur (to ensure we get a copy onto the controller if there is a connection established).
* help: add giftcard redeem info to FAQ.
* giftcard generator: apple gift cards will now start with 'X' and  no longer generate with a pin (they don't use a pin).
* giftcard generator: added ebay cards and more goolge play cards to the giftcard database.
* amazon: hide the sign-in 'flyout' better.
<br/>
<br/>


## 9/8/21 v1.0.8 ##
Important fixes: Controller will attempt to reconnect to bait if it loses connection. (This won't happen unless the bait previously was connected, in the same session).
* permit * X and x as censor characters in the phone number (don't strip them) so you can mask your bait profiles phone number if you wish to just edit it and replace the numbers you want to hide with any one of: "*", "X", or "x".
* bank: add "Wire amount" field at bottom of external account adding form, let's help law enforcement by capturing a transfer amount in conjunction with captured account details, this will help the reports be much more impactful and useful.
* controller: Bait commands will acknowledge if successful instead of blindly saying 'done'.
* redirect Receive money Zelle screen to the Send money zelle screen.
* controller: logs screen captures section is now human readable, to aid in reporting accounts easier.
* bank: Move bank agent chat-box more towards screen-center.
* bank: on the add external bank acct form, changed "add account" button  to "submit" button.
* controller: import profile now properly closes fakenamegenerator tab(s) when saving the imported data.
<br/>
<br/>


## 9/6/21 v1.0.7 ##
Important fixes: Two-factor code shows on the admin panel (if connected).  Made settings sliders un-slide if unsuccessful in changing a setting, and disable them from being clicked if the admin panel is opened but the connection is disconnected.  (bait will send confirmation that it changed back to the admin before the slider will stay slid.)  Tested conditions where the controller was connected, but is no longer connected, improved error handling and usability to more clearly communicate to the user when things are failing to be performed, hopefully less scenarios where you thought something took effect but it really didn't.  BTC.com integration, see new FAQ in help section of controller in v1.0.7 for details.  Paypal.com support, see new FAQ in help section of controller in v1.0.7 for details.
* Added account routing numbers based on profile state to the account information page per each account: checking, savings, billpay and Credit. Thanks Toby!
* Re-worked account information and services tab for each account.  Displays acct number as hidden with a reveal link.  And nicknames properly display as nicknames and account type displays properly as account type with authentic bofa arbitrary type descriptors.
* bank: "Hello, USER" is now normal capitalization.  The real site does not capitalize it.
* phone number is handled better now.  You can have improper formatting or extra stuff like country code (+11, +44 etc) and it will still be able to get the last four numbers for two-factor page, and be able to pick out the proper sets of numbers for the bank pages.
* fixed browser breaker manifest error preventing the plug-in from being installed.
* corrected spelling mistake in two-factor page.  Thanks recon!
* target card generator, cards will now start with 041.  Thanks Harvey!
* bank: remove iphone/android/ipad entries from recent sign-in (changed them to chrome).
* remove duplicate google play cards from giftcard database.
* bank: fixed bank-logout now works even if there is a different active tab or multiple windows  and tabs open (it will find the bank tab no matter where it is now).
* Bank is more stealthy - remove simulator stuff instead of just hiding it.  Now when a scammer saves the page, and opens the saved copy it will not reveal the demo.
* improved google-play redeem, fixed issue with netherlands region site, added bait email address and faded backdrop to the pop-up  for more realism.
* amazon: improve order history links to be more reliable.
* fix bug with amazon prices that include a comma, increased reliability of clicking the buy-now button (will now remove submit type from the button so it doesn't try to submit as a form causing a log-in prompt.
* add FAQ about paypal to help section of admin panel.
* capture, log, and alert scammer accounts transferred from paypal.
* bank: You will now get your login two-factor code on the admin panel (if connected).  You can still use the alternative method. (see FAQ in admin panel help section).
<br/>
<br/>


## 9/1/21 v1.0.6 ##
Important fixes: You can now make backup's of your database and restore them!  (You could also share them with other users, if you like.  After upgrading both your bait and controller plugin's, simply go to the Database side menu, and select Reset.  Scroll to the bottom and you'll find a Download button (save a copy of the database on your host machine), and an Upload button (Restore the database from your backup file).  Advanced users can modify these backup's in a text editor if they wish, but be careful not to break the formatting of it, or you'll not be able to re-import it until you correct the formatting symbols (JSON).
Other fixes in this version:
* Added a forced reload when clicking the accounts button on bank so it won't show old data. (Thanks modder!)
* Database backup/restore feature (mentioned above).
* make top navigation menu's in bofa look more real/live.
* New redeem!!!: bestbuy
* target website will now show profile name and profile city on all pages (without sign-in).
* Remove auto-fill for passcode/username changes on bank (so it looks less like a demo).
* Give the appearance that the scammer can change the account password, account username, etc. (Sign-in settings page)
* Add missing deal names to deal's tile possibilities (fixes wrong/undefined deal name when drilling down on the deal tile).  Let me know if deals tile is still not loading any picture occasionally.
* Add system log's for bank username/password "changes", and capture the 'changed' information.
* bestbuy website will now show profile name and profile city on all pages (without sign-in).
* Alerts History now shows profile email on the alerts.
* Add giftcard database to gift cards generator page (cards that will validate but have no money). (Thank you OJAS!)
* Add Starbucks to gift card generator options.  Hide money dropdown when generating cards that do not use it.
* Re-did the way the plug-in's display their connection status, it should be more true and accurate to what the connection state between them really is.  Slowed the controller's aggressiveness towards making the connection with the bait at startup.  Also the controller will now try to re-use the same ID number.
* Revised some FAQ's in the help section.
<br/>
<br/>


## 8/26/21 v1.0.5 ##
Important fixes: Completely re-did the transfers page, was a lot of work but it should be much more reliable now.
* Place cursor into auth code box automatically for two-factor when reaching the step (so you can complete 2-factor with keyboard only)
* Listen for enter key on license entry page.
* Get rid of the $100.00 auto populating amount in account transfers (both tile and page)
* transfer limits adjusted: changed to 500 overdraft limit, xfer amounts can go as high as the account balance + a bit over.)
* Use expired deals as current deals (add them to possible deals)
* Make bank username case insensitive
* Slow down savings transactions... 1 per month.
* Change browser breaker to ONLY break bankofamerica/paypal and not every site.
* Added code for database migrations during updates, store current software version in database, and if database is old, will run migration.
* Prevent two-factor page from loading directly without involving the log-in process.
* Transfer page having some troubles in some cases.  Tore down the existing system and replaced it.
* Fixed savings re-generate not working, only when doing re-generate all.
* change internal transfers "from" field to be the acct it was transfered from rather than the user who did it.
* change transfer tile to limit of 500 overdraft, no longer going to lock the account, just reject transfer.
* Add page refresh when clicking accounts top button to ensure fresh data. (part of 1.0.5 re-upload)
<br/>
<br/>


## 8/23/21 v1.0.4 ##
Important fixes: Added new Two-Factor Authentication option.  If enabled (see settings sliders to disable), you'll be taken to the new two factor screen during the login process.  Your two-factor code is the same as the password short-cut you can enter at least six characters and ends with zero to proceed to the bank.  This update has many great improvements:
* Fix email key code entry is now case insensitive.
* Deals page, credit card account now displays.
* Deals Tile will switch to a new deal every day.
* Clicking Logo at the top no longer reveals the simulator.
* Fixed bugs in external transfers screen when some accounts were set to disabled.
* add/cancel buttons on the add an external account page will light up 6 seconds after page display now.
* External transfer page fully set to guide them to add accounts.  Impossible to transfer out (except zelle).
* remove console.log messages, so scammer won't see the activity when they try to inspect element.
* Make security center sign-in history look recent.
* Zelle: scammer can add zelle recipients now, the system will "add it" to the list, log it to admin, and alert admin panel.
* Zelle now has transfer limit of 1,000
* Add refresh button to logs screen.
* Expand width of profile name on bank header, in-case of very long names.
* Fixed pagination row's (Newest, Next, Previous, Oldest) links appearing disabled on load.
* Fixed Additional tabbed pages under each account are now being modified too.
*  Made Fake Two-Factor page for sign-in, also could be used for high value transfers (in the future). This is done, it needs at least 6 characters and ends in zero just like password.
* replace the page title at 0 milliseconds to ensure simulator does not appear.
* replace simulator rewards badge with platinum (top right).
<br/>
<br/>


## 8/21/21  v1.0.3 ##
Important fixes: corrected issue with re-generating account's (account balance and acct minimum were stuck at 1,000)
changes: added "re-generate ALL" button in the reset menu.  This will re-generate all checking/savings/credit/billpay
transactions in one single click, for the current profile.
Added: Software version notices, starting with v1.0.3 you will now be alerted when there is a new version in the
controller's pop-up menu.  When installing new versions, be sure to replace both your controller and bait plug-in's.
<br/>
<br/>

## 8/19/21  v1.0.2 ##
Changed Bank of america code for better reliability and function.
Changed Bank of america login for better reliability and function.
<br/>
<br/>


## 8/19/21  v1.0.1 ##

Fixed: Acctmin7 not found, preventing changes to acct data.
Fixed: Sidebar toggle-close button disppearing when window gets too small.
Fixed: Paypal Balance not saving.
Fixed: unable to change "recent" field on database add/edit.
Fixed: Walmart Giftcards now generate with "6" as first number.

Vastly improved the reg code entry, it no longer prevents the plugin from establishing connection.  Also improved the pop-up connection status display.  Moved key code registration to new tab instead of pop-up (part of what solved the problems).  Will be updating the other plug-in the same way, and testing it, and making other fixes before posting fixed version.

Fixed: zelle transfers Not working.

Registration is on both plug-in's now, and requires purchase email.
The email is only used to verify your code.

Thank you for your support!
-SS

## Links
* [Link to store page](https://sinisterspatula.gumroad.com/l/UgtPr/r7pjv7i)
* [Sinister Spatula's Discord Server](https://discord.gg/Jt4XSxBfvG)
* [Sinister Spatula's YouTube Channel](https://www.youtube.com/channel/UCL1X9tYwaNBZm_Ry-Grj4ug)
* [Sinister Spatula's Twitter](https://twitter.com/SinisterSpatula)
