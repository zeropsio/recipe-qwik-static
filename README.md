# Zerops x Qwik - Static

Qwik is a web framework for building instead loading web applications at any size or complexity. [Zerops](https://zerops.io) makes deploying and running Qwik apps, both server side rendered and static, a breeze. This recipe showcases the Static version, see [zeropsio/recipe-qwik-nodejs](https://github.com/zeropsio/recipe-qwik-nodejs) for the Node.js version.

![qwik](https://github.com/zeropsio/recipe-shared-assets/blob/main/covers/svg/cover-qwik.svg)

<br/>

## Deploy on Zerops

You can either click the deploy button to deploy directly on Zerops, or manually copy the [import yaml](https://github.com/zeropsio/recipe-qwik-static/blob/main/zerops-project-import.yml) to the import dialog in the Zerops app.

<br/>

[![Deploy on Zerops](https://github.com/zeropsio/recipe-shared-assets/blob/main/deploy-button/green/deploy-button.svg)](https://app.zerops.io/recipe/qwik-static)

<br/>

## Recipe features

- Latest version of **Qwik** with SSG running on a **Zerops Static** service.

<br/>

## Production vs. development

This recipe is ready for production as is, and will scale horizontally by adding more containers in case of high traffic surges. If you want to achieve the highest baseline reliability and resiliace, start with at least two containers (add `minContainers: 2` in recipe YAML in the `app` service section, or change the minimum containers in "Automatic Scaling configuration" section of service detail).

<br/>

## Changes made over the default installation

If you want to modify your existing Qwik app to efficiently run on Zerops, follow these steps:

1. Install the necessary adapter with:
   `sh
    npm run qwik add static
    `
   Running this command will make the following changes

- A build.server script will be automatically added to your package.json file.
- A adapters/static/vite.config.ts file will be created.

Now, just add the [zerops.yml](https://github.com/zeropsio/recipe-qwik-static/blob/main/zerops.yml) file to the root of your project, and make sure to check `package.json` for the scripts.

<br/>

Need help setting your project up? Join [Zerops Discord community](https://discord.com/invite/WDvCZ54).
