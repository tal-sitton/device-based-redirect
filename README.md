# Device-Based Redirection

A simple, lightweight solution that dynamically redirects users to different URLs based on their device type, such as Android, iOS, Windows, or other platforms.

## Optional Usage

- 📲 Redirect users to download your app from the relevant app store based on their device type
- 🔗 Send mobile users to a mobile-optimized version of your website.

## Features

- 📡 **Platform Detection**: Detects the user's platform (Android, iOS, Windows) automatically through the browser's user agent string.
- 🔀 **Dynamic Redirection**: Enables flexible redirection by allowing you to specify destination URLs via query parameters without modifying code.
- ⚡ **Lightweight**: The entire project is contained within a single HTML file that you can easily deploy on any server.

## How It Works

🖥️, 📱, 💻 When users visit the page, the system checks their device type using the browser's user agent string and redirects them to the appropriate URL. You specify which URLs should be used for Android, iOS, Windows, and other platforms directly via the URL parameters.

### Supported Platforms:
- **Android**: Redirects users to a URL specified for Android devices.
- **iOS**: Redirects users to a URL specified for iPhones, iPads, and iPods.
- **Windows**: Redirects users on both Windows desktop and Windows phones.
- **Other Devices**: For devices that do not match the above platforms (e.g., desktop browsers on macOS or Linux), a default URL can be provided.

## How to Use It

1. **Determine your wanted URLs**: 
   - determine which device type should redirect to what URL.
   
2. **Pass the URLs for each platform via query parameters**:
   - When you link to this page, include the URLs for the different platforms in the query string.

### URL Parameters

- **`android`**: The URL for Android devices (smartphones and tablets).
- **`ios`**: The URL for iOS devices, such as iPhones, iPads, and iPods.
- **`windows`**: The URL for Windows devices, including desktops and Windows phones.
- **`other`**: A fallback URL for any other devices or platforms.
- 
### Example URL:

```
https://code.sitton.dev/device-based-redirect?android=https://android-app.com&ios=https://ios-app.com&windows=https://windows-site.com&other=https://desktop-site.com
```

In this example:
- Android users will be redirected to `https://android-app.com`.
- iOS users will be redirected to `https://ios-app.com`.
- Windows users will be redirected to `https://windows-site.com`.
- All other users will be redirected to `https://desktop-site.com`.

## Deployment

The site is deployed using Github Pages to the URL: [code.sitton.dev/device-based-redirect](https://code.sitton.dev/device-based-redirect).

If you want to deploy your own, simply upload the HTML file to your server. No server-side logic is required, so it works with any basic hosting solution.
