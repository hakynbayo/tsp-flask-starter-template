# Team Software Project Starter Template - Flask

This example shows how to implement a basic app using:

- [Flask](https://flask.palletsprojects.com/en/3.0.x/) 
- [Prisma Client](https://prisma-client-py.readthedocs.io/en/stable/) as the ORM
- A SQLite database file with some initial dummy data which you can find at [`./prisma/dev.db`](./prisma/dev.db)
- [Bootstrap](https://getbootstrap.com/) for basic CSS Styling.
<!-- - [Jest](https://jestjs.io/) and [Supertest](https://github.com/ladjs/supertest) for unit testing
- [ESLint](https://eslint.org/) to statically analyze your code and find problems
- [Prettier](https://prettier.io/) to format your code -->

It is intended to serve as a starting point for your Team Software Project course if you choose to use ExpressJS. It
provides examples for performing basic tasks with different types of endpoints (GET, POST, etc.)

## Getting started

### 1. Download example and install dependencies

Clone this repository:

git clone git@github.com:kiboschool/tsp-flask-starter-template.git

Install npm dependencies:

```bash
cd tsp-flask-starter-template
pip3 install -r requirements.txt
```

### 2. Create and seed the database

Run the following command to create your SQLite database file. This also creates the `User` and `Post` tables that are
defined in [`prisma/schema.prisma`](./prisma/schema.prisma):

```bash
prisma db push
```

Seed the database by running the `./prisma/seed.py` file
```bash
python3 seed.py
```

### 3. Interacting with the Starter Template

```bash
flask run
```

The server is now running on `http://localhost:3000`. You can send the API requests implemented in `index.js`, e.g.
[`http://localhost:3000/feed`](http://localhost:3000/feed).

## Using the Starter Template

- Visit `http://127.0.0.1:5000` to be presented with the login page.
- If you have seeded the database per the above instructions, you can use one of the logins from `prisma/seed.js` to log
  in.
- Click on the `Register here` link to create a new user.

Once logged in, you can see that user's posts. Posts have Titles and Contents.

### Additional Commands

**ESLint configuration is stored in the `.eslintrc.json` file.**

Check if the formatting matches Prettier’s rules by using:

``` bash
npm run format:check
```

Apply the formatting recommendations using this command:

``` bash
npm run format:write
```

**Prettier configuration is stored in the `.prettierrc.json` file.**

Lint your code with ESLint using this command:

``` bash
npm run lint:check
```

Auto-fixing errors with this command:

``` bash
npm run lint:fix
```

Run unit tests with this command:

```bash
pytest tests
```

### Deploying To Render

You can deploy this application to Render using the following steps:

1. Once you have pushed the remote to a GitHub repository, go to render.com and select 'Get Started For Free'.
2. Log in using your GitHub account.
3. Select the option to deploy a new Web Service
4. Choose the option to 'Build and deploy from a Git repository'.  If you don't see your repository in the list, select
   the option to "Configure account" on the right-hand side of the screen.  You can then select which repo you would
   like to link.
5. Click on 'Connect' to the right of the correct repository.
6. Choose a name and region of your choice.  Since you are using `npm` locally, I recommend using `npm` as the 'Build
   Command'
7. For the 'Start Command' enter `npm run dev`.
8. Select the Free Plan option.
9. Click 'Create Web Service'.
    