# Lab04 Screenshots

---

## workAround
````powershell
npx mocha test_login.spec.js
````

````js
// func
const fs = require('fs');

async function smartSleep(driver, arg) {
  if (arg === "take_screenshot" || arg === take_screenshot) {
    let screenshot = await driver.takeScreenshot();
    fs.writeFileSync(`screenshot_${Date.now()}.png`, screenshot, 'base64');
  } else {
    await driver.sleep(arg);
  }
}

module.exports = { smartSleep };
````
