# how to make cronicle starts when I restart the mac

To configure **Yahoo Mail** in **Thunderbird**, follow these steps:

### 1. Enable Yahoo Mail for third-party apps

Ensure your Yahoo account allows access for third-party email clients like Thunderbird:

1. Sign in to your Yahoo account via a browser.
2. Go to **Account Security** under **Account Info**.
3. If two-step verification is enabled, you'll need to generate an **app password**:
   - Click **Generate app password**.
   - Select **Other app**, type **Thunderbird**, and click **Generate**.
   - Copy the app password, as you'll use it in Thunderbird instead of your regular Yahoo password.

### 2. Open Thunderbird and add your Yahoo account

1. **Open Thunderbird**.
2. Click on the **Menu** button (≡) in the top-right corner and go to **Account Settings**.
3. Select **Account Actions** > **Add Mail Account**.

### 3. Enter your Yahoo Mail account details

- **Your name**: The name you want to display on sent emails.
- **Email address**: Your Yahoo Mail address (e.g., `yourname@yahoo.com`).
- **Password**: Use the app password you generated from Yahoo (if applicable).

Then click **Continue**.

### 4. Thunderbird will attempt to configure automatically

Thunderbird may auto-detect the Yahoo Mail server settings. If not, you can enter them manually:

### Manual Settings

#### Incoming Mail Server (IMAP)

- **Protocol**: IMAP
- **Server**: `imap.mail.yahoo.com`
- **Port**: 993
- **Connection Security**: SSL/TLS
- **Authentication Method**: OAuth2 (preferred) or Normal password (if you're using an app password)

#### Outgoing Mail Server (SMTP)

- **Server**: `smtp.mail.yahoo.com`
- **Port**: 465 or 587
- **Connection Security**: SSL/TLS
- **Authentication Method**: OAuth2 (preferred) or Normal password (if you're using an app password)

Click **Done** once the settings are entered.

### 5. Finalize and Test

Thunderbird should now sync your Yahoo Mail. You can check if the setup is correct by sending and receiving test emails.

Let me know if you run into any issues during the configuration!
