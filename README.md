# hubspot-dev-kit

## Tech Stack
Hubspot Dev Kit is a theme boilerplate and uses [TailwindCSS V4](https://tailwindcss.com/) (CSS framework).

## Hubspot Local Development

Please check documentation and articles for information on Hubspot Local Development.

- [Local Development Tooling: CLI Reference](https://developers.hubspot.com/docs/guides/cms/tools/hubspot-cli/cli-v7)
- [Quick start guide tp developing on the HubSpot CMS](https://developers.hubspot.com/docs/guides/cms/quickstart/classic-hubl-quickstart)
- [Hubl Functions](https://developers.hubspot.com/docs/reference/cms/hubl/functions)
- [Hubl Variables](https://developers.hubspot.com/docs/reference/cms/hubl/variables)
- [Hubl Filters](https://developers.hubspot.com/docs/reference/cms/hubl/filters)
- [HubDB](https://developers.hubspot.com/docs/guides/cms/storage/hubdb/overview)

It is recommended to develop using the [Official Hubspot Developer Extension](https://chromewebstore.google.com/detail/hubspot-developer-extensi/gebemkdecnlgbcanplbgdpcffpdnfdfo), as it gives you a plethora of tools for your own convenience, such as hsDebug toggle.

## Setup local environment

1. Clone the repository to your local machine

```bash
git clone git@github.com:freshjuice-dev/hubspot-dev-kit.git
```

2. Change current directory

```bash
cd ./hubspot-dev-kit
```

3. Install Packages

```bash
npm install
```

### Configure the local development tools (Hubspot Cli)

Run ``hs init`` to connect the tools to your HubSpot account. This command will walk you through the following steps:

1. The command will guide you to create a personal CMS access key to enable authenticated access to your account via the local development tools.
2. It will prompt you to press "Enter" once you’re ready to open the [Personal CMS Access Key](https://app.hubspot.com/l/personal-access-key) page in your default browser. This page will allow you to view or generate your personal access key if necessary. (Note: You’ll need to select at least the "Design Manager" permission to complete this tutorial.)
3. Copy your access key and paste it in the terminal.
4. Enter a name for the account. This name is only seen and used by you. For instance, you might use "sandbox" if you're using a developer sandbox or "company.com" if you’re using a full customer account. This name will be used when running commands.

Once you've completed this simple ``init`` flow, you'll see a success message confirming that a configuration file, ``hubspot.config.yml``, has been created in your current directory.

File **hubspot.config.yml** contains your personal access keys
Please be sure you are not track file **hubspot.config.yml** and its include to **.gitignore**

## NPM Scripts
- ``prepare`` - Initializes husky.
- ``fetch:hubspot`` - Fetches the current saved files on hubspot.
- ``upload:hubspot`` - Updates hubspot saved files with local changes.
- ``watch:hubspot`` - When initialized, watches for changes to local repo, and updates hubspot files on saving.
- ``watch:tailwind`` - When initialized, watches for changes to tailwind.css and updates the compiled theme's tailwind.css file.
- ``build:tailwind`` - Updates hubspot compiled tailwind.css file with local changes.
- ``watch:js`` - When initialized, watches for changes to main.js and updates the compiled theme's main.js file.
- ``build:js`` - Updates hubspot compiled main.js file with local changes.
- ``start`` - Initialize local instance of repo.
- ``build`` - Initialize build of local version repo.

## Workflow

1. Use ``npm run fetch:hubspot`` to be sure your local files match the contents on hubspot.
2. Once changes are done, always commit.
3. To upload your changes:

   - ``npm run upload:hubspot``
   - ``npm run start``

Please note that when you execute ``npm run start``, if you do not terminate the process, it will keep watching for any changes you make and publish said changes on your corresponding hubspot files.
