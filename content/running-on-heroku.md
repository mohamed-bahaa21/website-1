# Running on Heroku

> [Heroku](https://www.heroku.com/) is a container-based cloud Platform as a Service (PaaS). Developers use Heroku to deploy, manage, and scale modern apps. The platform is elegant, flexible, and easy to use, offering developers the simplest path to getting their apps to market.
>
> From the ["What is Heroku?" section](https://www.heroku.com/about) of their website

Heroku provides a free hosting service which works with Umami as well as databases through add-ons.
You don't need to have a database set up before this setup guide.

## Setup [![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/umami-software/umami)
_Automate all steps using the button above_

### Website

1. Fork a copy of the [umami repository](https://github.com/umami-software/umami).
1. Create an account on [Heroku](https://heroku.com/).
1. From the dashboard page click **New > Create new app**.
1. Choose an **App name** and then click **Create app**.
1. Under **Deployment method** click **GitHub** and follow the instructions to connect Heroku to GitHub.
1. Search for the repository and click **Connect**.

### Database

1. Navigate to the **Resources** tab and click on the **Find more add-ons** button.
1. Search for **Heroku Postgres** and follow its instructions to install the add-on.
1. The add-on will set the `DATABASE_URL` automatically; you should not have to manually set it.
1. You will need to set up the database tables by following the **Create database tables** section of the [Install](/docs/install) docs. You can find temporary connection details by following the **Resources > Heroku Postgres > Settings > Database Credentials** path.

### Build and Deploy

1. Under the **Settings > Config Vars** section, set the `HASH_SALT` environment variable. Read the [Install](/docs/install) section for information about the `HASH_SALT` environment variable.
1. With the environment variables and database set up, click the **Deploy > Manual Deploy > Deploy Branch** button.
1. Once the build has finished, the website should be live. Follow the **Open app** button at the top of the dashboard to view it.
1. Follow the **Getting started** guide starting from the [Login](/docs/login) step.
