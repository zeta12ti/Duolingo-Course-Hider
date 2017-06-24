# Extra Course Hider
NOTE: This script may no longer be needed. It seems that Duolingo will now automatically hide courses with 0 xp (other than the current course).

On 2017/06/19, the new site received an update that caused all your current courses to be shown by default. This basically makes the Duolingo Course Switcher script obselete. If you still prefer the layout used there (with each base language listed separately) you can continue to use the script. It may break due to the changes to the site, and I probably won't update it dramatically.

However, this new update introduced a new annoyance. Since it's impossible to remove the last course for a given base language, there may be extraneous courses shown. I've added a new script (HideExtraCourses.user.js) to remove those courses. For now, it'll take a bit of manual work to get it set up.

### Installing

1. If you haven't already, install the appropriate extension for your browser (restarting your browser afterwards if necessary):
 * Chrome: [Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en)
 * Chromium: [Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en)
 * Firefox: [Greasemonkey](https://addons.mozilla.org/en-US/firefox/addon/greasemonkey/)
 * Safari: [JavaScript Blocker](http://javascript-blocker.toggleable.com/)
2. Click [here](https://github.com/zeta12ti/DuolingoCourseSwitcher/raw/master/HideExtraCourses.user.js) to install the userscript.
3. Confirm the installation when prompted.

### Set Up

1. Go to https://www.duolingo.com/ and take note of which courses are unnecessary. 
2. For each extra course, copy down the flag code for the base language. A complete list of flag codes can be found [here](https://github.com/zeta12ti/DuolingoCourseSwitcher/blob/master/FlagCodes.txt).
3. Edit the user script. The way to do this varies by browser. Google is your friend.
 * In Firefox, open the Add-ons menu, click on the User Scripts tab, find the HideExtraCourses script, click preferences, then click Edit this User Script.
 * In Chrome and Chromium, open the Extensions menu, find the Tampermonkey extension. Click on Options to open the Tampermonkey interface. Click on the Installed User Scripts tab, then click on the HideExtraCourses script.
4. Edit lines 13-15 to include only the flag codes for the courses you want hidden. By default, three courses are hidden and you may delete them if you wish. Every line except the last should have a comma. Everything after the // is optional.
5. If you ever wish to show courses from a specific base language again, delete the corresponding flag code in the script source. Make sure every line but the last has a comma.
