# hubspot-dev-kit

## Tech Stack
Hubspot Dev Kit uses [TailwindCSS V4](https://tailwindcss.com/) (CSS framework)

## Hubspot Local Development

Please check KB Articles:

- [Local Development Tooling: CLI Reference](https://developers.hubspot.com/docs/guides/cms/tools/hubspot-cli/cli-v7)
- [Quick start guide tp developing on the HubSpot CMS](https://developers.hubspot.com/docs/guides/cms/quickstart/classic-hubl-quickstart)

## Setup local environment

Clone repository to your local machine

```bash
git clone git@github.com:freshjuice-dev/hubspot-dev-kit.git
```

Change current directory

```bash
cd ./hubspot-dev-kit
```

Install Packages
```bash
npm install
```

### Configure the local development tools (Hubspot Cli)

Run ``hs init`` to connect the tools to your HubSpot account. This command will walk you through the following steps:

1. First you’ll be guided to create a personal CMS access key to enable authenticated access to your account via the local development tools. You’ll be prompted to press "Enter" when you’re ready to open the [Personal CMS Access Key](https://app.hubspot.com/l/personal-access-key) page in your default browser. This page will allow you to view or generate your personal access key, if necessary. (Note: You’ll need to select at least the "Design Manager" permission in order to complete this tutorial.) Copy your access key and paste it in the terminal.
2. Next, you’ll enter a name for the account. This name is only seen and used by you, For example, you might use " sandbox" if you're using a developer sandbox or "company.com" if you’re using a full customer account. This name will be used when running commands.

Once you've completed this simple ``init`` flow, you'll see a success message confirming that a configuration file, ``hubspot.config.yml``, has been created in your current directory.

File **hubspot.config.yml** contains your personal access keys
Please be sure you are not track file **hubspot.config.yml** and its include to **.gitignore**

## NPM Scripts
- ``prepare`` - Initializes husky.
- ``npm run fetch`` - Fetch files from HubSpot (Be sure you commit local changes first before run this command, bc its override your local files and any changes)
- ``npm run upload`` - Upload local files to HubSpot
- ``npm run watch`` - Run watch process to upload files to HubSpot when you save the file or create a new one.
- ``start`` - Initialize local instance of repo.
- ``build`` - Initialize build of local version repo.

## Workflow

1. Always First commit your local changes
2. Second step use ``npm run fetch`` to be sure, your local files up to date
3. Two ways:

    - ``npm run upload``
    - ``npm run watch``
