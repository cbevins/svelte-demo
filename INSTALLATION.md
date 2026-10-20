#  Svelte Installation Process

Below are the steps I use to create this Sveltekit project with a remote Github repository.

## 1 - Create a Blank Remote Github Repository

First, go to Github and create a new repository *without* a README, .gitignore, or license file.  I usually use the same name for both the Github.com remote repository and the Sveltekit project directory.  In this example, the project and repo names are **svelte-demo**.


## 2 - Create a Sveltekit Project

From the parent directory of the new project (**projects/**),
enter the following command to run the installation script:

```bash
> npx sv create svelte-demo
```

Then change into the project directory and install the required packages:

```bash
cd svelte-demo
npm install
```

## 3 - Create a Local Git Repository and Connect it to the Remote Github Repo

```bash
Initialize the local Git repository:
echo "# sem2026" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/cbevins/svelte-demo.git
git push -u origin main
```

Open VScode, add the new project folder to the Workspace, and ensure the **SOURCE CONTROL REPOSITORY** for the folder is attached to **main**.

I then edit the existing README.md to add the new project's actual info.

Whenever I commit changes to the local repo, I also use VScode to 'push' or sync'
the changes with the remote repo.

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://svelte.dev/docs/kit/adapters) for your target environment.
