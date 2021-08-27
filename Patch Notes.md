8/26/21 v1.0.5: Important fixes: Completely re-did the transfers page, was a lot of work but it should be much more reliable now.
* Place cursor into auth code box automatically for two-factor when reaching the step (so you can complete 2-factor with keyboard only)
* Listen for enter key on license entry page.(edited)
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


8/23/21 v1.0.4: Important fixes: Added new Two-Factor Authentication option.  If enabled (see settings sliders to disable), you'll be taken to the new two factor screen during the login process.  Your two-factor code is the same as the password short-cut you can enter at least six characters and ends with zero to proceed to the bank.  This update has many great improvements:
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


8/21/21  v1.0.3
Important fixes: corrected issue with re-generating account's (account balance and acct minimum were stuck at 1,000)
changes: added "re-generate ALL" button in the reset menu.  This will re-generate all checking/savings/credit/billpay
transactions in one single click, for the current profile.
Added: Software version notices, starting with v1.0.3 you will now be alerted when there is a new version in the
controller's pop-up menu.  When installing new versions, be sure to replace both your controller and bait plug-in's.

8/19/21  v1.0.2
Changed Bank of america code for better reliability and function.
Changed Bank of america login for better reliability and function.





8/19/21  v1.0.1

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

