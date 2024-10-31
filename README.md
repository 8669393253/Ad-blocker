# Ad Blocker Tampermonkey Userscript

## Overview

This repository contains a Tampermonkey userscript designed to block advertisements on a specified webpage. Tampermonkey is a popular browser extension that allows users to run custom JavaScript code on web pages, enabling enhanced functionality such as ad blocking.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation Steps](#installation-steps)
- [Script Explanation](#script-explanation)
- [Customization](#customization)
- [Usage](#usage)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Before using this script, ensure that you have the following:

- A web browser that supports extensions (e.g., Google Chrome, Firefox).
- The **Tampermonkey** extension installed on your browser.

## Installation Steps

1. **Install Tampermonkey**:
   - Open the [Chrome Web Store](https://chrome.google.com/webstore/category/extensions).
   - Search for **Tampermonkey** and click **Add to Chrome**.
   - Confirm the installation by clicking **Add Extension**.

2. **Open the Tampermonkey Dashboard**:
   - Click on the Tampermonkey icon in the Chrome toolbar (usually located in the top-right corner).
   - Click on the three dots (menu icon) in the dropdown.
   - Select **Dashboard** from the options.

3. **Add a New Script**:
   - In the Tampermonkey Dashboard, click on the **+** (plus) icon or **Add a new script** button.

4. **Paste the Script Logic**:

5. **Customize the Script**:
   - Replace `https://example.com/*` in the `@match` line with the URL of the website where you want to block ads.
   - Update the `adSelectors` array with the actual CSS selectors for the ad elements you wish to block.

6. **Save the Script**:
   - Click **File** and then **Save** (or click the save icon).
   - Your script is now active and will run automatically on the specified website.

## Script Explanation

The userscript consists of the following sections:

- **Metadata Block**: This section includes various fields that describe the script, including its name, version, and match URL.
  - `@name`: The name of the script.
  - `@namespace`: A unique identifier for the script.
  - `@version`: The version number of the script.
  - `@description`: A brief description of what the script does.
  - `@author`: The author's name.
  - `@match`: The URL pattern where the script should be applied.
  - `@grant`: Specifies the permissions that the script requires (none in this case).

- **Functionality**:
  - The script uses an immediately invoked function expression (IIFE) to run the code as soon as the script loads.
  - An array called `adSelectors` is defined to store CSS selectors for ad elements.
  - The script selects elements matching these selectors and removes them from the DOM using the `remove()` method.

## Customization

To tailor the script for your needs:

1. **Update the `@match` Field**:
   - Replace `https://example.com/*` with the actual URL of the webpage where you want to block ads. The asterisk (*) allows for blocking on all paths under that domain.

2. **Modify the Ad Selectors**:
   - Add or remove selectors in the `adSelectors` array based on the specific ad elements you wish to target. Use your browser's Developer Tools to inspect elements and find their classes or IDs.

## Usage

After saving the script, visit the specified website to verify that ads are being blocked. The script will automatically execute whenever you load that page.

## Troubleshooting

- **Ads Still Showing**: Ensure that you have correctly identified the CSS selectors for the ads. You may need to adjust the selectors in the `adSelectors` array.
- **Script Not Running**: Double-check the URL in the `@match` field to ensure it matches the webpage you are visiting.
- **Tampermonkey Disabled**: Make sure Tampermonkey is enabled in your browser's extensions settings.

## Contributing

If you wish to contribute to this script or enhance its functionality, feel free to fork the repository and submit a pull request. Contributions are welcome!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
