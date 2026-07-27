# Slack Setup 
Open your web browser and navigate to slack.com. On the homepage, click on the "GET STARTED" button to begin creating your Slack workspace.
Enter your work email address and click "Continue", or sign up quickly using your Google or Apple account.
Enter a name for your Slack workspace (e.g., your company or team name) and click "Next" to proceed.
Slack will prompt you to upgrade to a Pro plan. To continue for free, click "Start with the Limited Free Version" at the bottom of the page.
Your Slack workspace is now ready! You will see default channels in the sidebar. You can start creating channels, inviting teammates, and collaborating right away.
# Create a Slack APP
Open api.slack.com/apps in a new browser tab and click the "Create an App" button to start building your Slack app.
Create an App from scratch or from a maifest file.
Select your workspace from the dropdown (e.g., "Personal_Workspace") and click "Next" to proceed.
Ensure to select Chat:Write and Channel:read oauth permission scopes. Review all the details and click on Create.
You’ll be redirected to the "Basic Information" page showing your app’s credentials (App ID, Client ID, Client Secret, Signing Secret). From the left sidebar, click "Install App" to install it to your workspace.
# Install App on slack workspace
On the "Install App" page, click the "Install to <Your Workspace>" button to install the app and generate access tokens.
Review the app permissions, select your workspace from the dropdown, and click "Allow" to authorize the app to access your Slack workspace.
Your app is successfully installed! Copy the "Bot User OAuth Token" (starts with xoxb-) by clicking "Copy" — this token is used to authenticate your app with Slack.
Go back to your Slack workspace and verify that your app (e.g., "ProjectBot") appears under the "Apps" section in the left sidebar. This confirms your Slack app is successfully installed and ready to use.

# n8n Setup
Open your n8n instance (n8n.io) in the browser and log in to your account.
Navigate to the "Credentials" tab from the top menu bar.

*OpenAI* - Click the "Create credential" button (orange button in the top-right corner) to start adding a new credential.
In the "Add new credential" dialog, type "OpenAI" in the search bar to filter the list.
Select "OpenAI" from the dropdown results and click "Continue" to proceed.Add your OpenAI API key and save.After saving, n8n will automatically test the connection. You should see a green "Connection tested successfully" banner confirming the API key is valid.

*GSheet* - Click "Create credential" again, search for "Google Sheets OAuth2 API" in the search bar and select it. Click "Continue" to proceed with the Google Sheets setup.
Click the "Sign in with Google" button to authenticate with your Google account and grant n8n access to your Google Sheets.You should see a green "Account connected" banner confirming the Google Sheets credential is linked successfully.
Click "Create credential" again, and search for "Slack" in the search bar.Select "Slack API" from the dropdown (not "Slack OAuth2 API") and click "Continue".

*Slack* - Click "Create credential" again, and search for "Slack" in the search bar.Select "Slack API" from the dropdown (not "Slack OAuth2 API") and click "Continue".
Go back to your Slack API page at api.slack.com/apps and navigate to "Install App" in the left sidebar. Click "Copy" next to the Bot User OAuth Token (the xoxb- token generated in Phase 2) to copy it to your clipboard.
Paste the copied Bot User OAuth Token into the "Access Token" field. Optionally, add a Signature Secret for verifying request authenticity (recommended by n8n). Click "Save" (orange button, top-right) to store the credential.
After saving, n8n will automatically test the connection. You should see a green "Connection tested successfully" banner confirming the Slack token is valid. The status will show "Saved" in the top-right corner. Your Slack credential is now ready to use in workflows.

# Slack Channels

Open your Slack workspace. You’ll see existing channels in the left sidebar.
Click the "+" button next to "Channels" in the sidebar and select "Create a channel". Enter the channel name as **project_updates**( this will be your main channel where you can ask questions and upon successful workflow execution the agent's response  is sent back on the same channel )and click "Next". Set the visibility to "Public" and click "Create".On the "Add people" screen, click "Skip for now".
Similarly create one more channel as **Errors** (this is used for error handling, in case there is an issue in the workflow the details will be published in this channel).
Open each newly created channel (#project_updates and #errors).In the message box, type /invite @ProjectBot (replace with your bot’s name) and hit Enter.
You should see a confirmation message that the bot was added to the channel.



