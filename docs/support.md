# Support

Need help? Email us at **< contact _at_ enlazor.com >**.

## Quick start
1. Set Enlazor as your default browser (macOS: System Settings → Desktop & Dock → *Default web browser*).
2. Create your config file and add rules (see [configuration](#configuration) below).

## Configuration
- **Location:** `~/Library/Containers/com.enlazor.Enlazor/Data/Library/Application\ Support/Enlazor/config.json`
- **Example:**
```json
{
  "defaultBrowserBundleID" : "com.apple.Safari",
  "rules" : [
    {
      "browserBundleID" : "com.google.Chrome",
      "id" : "0AFF54A5-96C0-41A6-827E-EC1122607230",
      "pattern" : "youtube.com"
    },
    {
      "browserBundleID" : "com.apple.Safari",
      "pattern" : "apple.com"
    }
  ]
}
```

* **Notes:**: The first matching rule is applied. If no rules match, the `defaultBrowserBundleID` is used.

## Troubleshooting

* Link not opening in the expected browser?
  - Check your config file for typos or errors.
  - Ensure the target browser is installed.
  - Verify that Enlazor is set as the default browser.

* Still having issues? Contact us at **< contact _at_ enlazor.com >** for further assistance.
