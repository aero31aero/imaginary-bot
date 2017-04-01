# Imaginary Bot for Zulip

This Repository contains sample files that a bot using the proposed deployment system would need to have.

## Structure

There are four main files that need to be made:

### 1. `package.json`

This file, similar to Node's `package.json`, should contain information like(but not limmited to):

- Bot Name
- Brief Desctiption/Tag Line
- Author Name
- Author Email
- Tags
- Path to Main Python File

### 2. `config.json`

This file is an array of objects, each defining one parameter to be taken from the user by the Configuration Management System. Each object should contain the following properties:

- Variable Name - *string*
- Display Name - *string*
- Description - *string*
- Validator - *boolean function*

Each variable will be stored as an environment variable for the deployment environment in the following format: `ZULIP_BOTNAME_VARIABLENAME`

### 3. `user-guide.md`

This file would be where the bot would be documented. The integrations documentation currently in `zulip/zulip` repository in `templates/zerver/integrations.html` would be migrated to this file. Zulip's markdown parser would be used to render this markdown in the package manager frontend.

### 4. `icon.png`

As the name implies, this would be the icon for the bot.
