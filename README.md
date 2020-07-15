# MigraHub

[![Author](https://img.shields.io/badge/author-MigraHub-D54F44?style=flat-square)](https://github.com/migrahub)
[![Languages](https://img.shields.io/github/languages/count/migrahub/migrahub-backend?color=%23D54F44&style=flat-square)](#)
[![Stars](https://img.shields.io/github/stars/migrahub/migrahub-backend?color=D54F44&style=flat-square)](https://github.com/migrahub/migrahub-backend/stargazers)
[![Forks](https://img.shields.io/github/forks/migrahub/migrahub-backend?color=%23D54F44&style=flat-square)](https://github.com/migrahub/migrahub-backend/network/members)
[![Contributors](https://img.shields.io/github/contributors/migrahub/migrahub-backend?color=D54F44&style=flat-square)](https://github.com/migrahub/migrahub-backend/graphs/contributors)


> 🏖️ MigraHub is a hub that connects immigrants to the base care and services they need.

---

# :pushpin: Table of Contents

* [Introduction](#rocket-introduction)
* [Setup](#construction_worker-Setup)
* [FAQ](#postbox-faq)
* [Found a bug? Missing a specific feature?](#bug-issues)
* [Contributing](#tada-contributing)
* [License](#closed_book-license)


# :rocket: Introduction

MigraHub is a hub that connects immigrants to the base care and services they need.

It is developed under the GNU General Public License version 3, meaning you can copy, modify and host your own MigraHub if you need to.

However, you are the owner of your data - (e.g. everything that is stored in your database), and only you can access it.

This repository holds all of the code that provides the backend of MigraHub. This includes a *GraphQL API powered by Stripe*, which MigraHub consumes.

# :construction_worker: Setup

In order to configure your backend, you need to:

### 1. Install Heroku locally

Follow [this guide](https://devcenter.heroku.com/articles/heroku-cli) to install heroku-cli locally.

### 2. Create your heroku project

In your terminal, run:

```bash
heroku create migrahub
```

### 3. Setup your heroku project

First, add the free [heroku postgreSQL addon](https://elements.heroku.com/addons/heroku-postgresql):

```bash
heroku addons:create heroku-postgresql:hobby-dev
```

Then, retrieve your database credentials:

```bash
heroku config
```

This should print something like this:

> DATABASE_URL: postgres://ebitxebvixeeqd:dc59b16dedb3a1eef84d4999sb4baf@ec2-50-37-231-192.compute-2.amazonaws.com: 5432/d516fp1u21ph7b.

Where the URL is setup as:

> *postgres:// USERNAME : PASSWORD @ HOST : PORT : DATABASE_NAME*

Now, you need to setup your environment variables. Grab the values you got from the URL above, and create the command line below by replacing them.

```bash
heroku config:set DATABASE_USERNAME=<database_username>
heroku config:set DATABASE_PASSWORD=<database_password>
heroku config:set DATABASE_HOST=<database_host>
heroku config:set DATABASE_PORT=<database_port>
heroku config:set DATABASE_NAME=<database_name>
```

### 4. Publish your heroku project

Finally, just run:

```bash
git push heroku master
```

And then, to access your newly deployed backend:

```bash
heroku open
```

You will now need to set-up your `admin user` by accessing `/admin` in your heroku project URL, and you're ready to go!

### 5. Maintenance, fixes & new features

Have you changed anything?

If so, don't forget to commit your changes and repeat step 4 to deploy them to Heroku.

# :postbox: Faq

**Question:** What are the tecnologies used in this project?

**Answer:** The tecnologies used in this project are [NodeJS](https://nodejs.org/en/) + [Strapi](https://strapi.io/) to handle the server & GraphQL API, and [Heroku](https://heroku.com) to handle deployment and hosting.

##

**Question:** Can I host MigraHub?

**Answer:** Yes! You can host it, use it, modify it, as you wish. It's entirely up to you and your responsibility. However, you are the only one who owns the data generated by the project, and it is also your responsibility to keep it safe.


# :bug: Issues

Feel free to **file a new issue** with a respective title and description on the the [MigraHub Backend](https://github.com/migrahub/migrahub-backend) repository.

If you already found a solution to your problem, **I would love to review your pull request**!

# :tada: Contributing

Feel free to contribute to the project, and make it grow!

Check the [issues page](https://github.com/migrahub/migrahub-backend/issues) to see ongoing isses and [pull requests](https://github.com/migrahub/migrahub-backend/pulls).

# :closed_book: License

Released in 2020.

This project is under the [MIT license](https://github.com/migrahub/migrahub-backend/blob/master/LICENSE).

Made with love by [MigraHub team](https://github.com/orgs/migrahub/people) 💙🚀
