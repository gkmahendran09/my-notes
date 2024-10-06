# how to make cronicle starts when I restart the mac

To make **Cronicle** start automatically when you restart your Mac, you can set it up as a **launch agent** using a `plist` (property list) file. Here's a step-by-step guide:

### 1. Create a `plist` file

You’ll need to create a **launch agent** file that will instruct macOS to start Cronicle at boot.

- Open Terminal and create a directory for the LaunchDaemons if it doesn’t already exist:

  ```bash
  mkdir -p /Library/LaunchDaemons
  ```

- Now, create a `plist` file (e.g., `com.cronicle.start.plist`):

  ```bash
  nano /Library/LaunchDaemons/com.cronicle.start.plist
  ```

### 2. Edit the `plist` file

Inside the `plist` file, add the following content. Adjust the paths and commands based on where Cronicle is installed and how it’s started:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple Computer//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>Label</key>
    <string>com.cronicle.start</string>
    <key>ProgramArguments</key>
    <array>
        <string>/usr/local/bin/node</string>
        <string>/opt/cronicle/bin/control.sh</string>
        <string>start</string>
    </array>
    <key>RunAtLoad</key>
    <true/>
    <key>KeepAlive</key>
    <true/>
    <key>StandardOutPath</key>
    <string>/tmp/cronicle.stdout</string>
    <key>StandardErrorPath</key>
    <string>/tmp/cronicle.stderr</string>
</dict>
</plist>
```

- Replace `/opt/cronicle/bin/control.sh` with the actual path to the `control.sh` script that starts Cronicle.

### 3. Load the Launch Agent

After creating and saving the `plist` file, load it into **launchctl** (macOS's service manager):

```bash
launchctl load /Library/LaunchDaemons/com.cronicle.start.plist
```

This will load and start Cronicle automatically when your Mac restarts.

### 4. Test the Launch Agent

You can test the launch agent by unloading and loading it again:

```bash
launchctl unload /Library/LaunchDaemons/com.cronicle.start.plist
launchctl load /Library/LaunchDaemons/com.cronicle.start.plist
```

This ensures that Cronicle starts properly as defined by the `plist`.

Let me know if you need further assistance with setting up!
