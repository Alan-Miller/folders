# Folders

## Create project by either:

### cloning someone else's repo (not making your own)
- OPTIONAL: Fork the repo (if you want your own copy of the repo on your GitHub account that you can commit changes to).
- Clone the repo.
    - Copy the repo URL.
    - Use `cd` to navigate to the projects folder on your computer where you want this project to exist.
    - Use `git clone [repo-URL]` to clone the site to your projects folder.
    - Use `cd [repo-name]` to navigate into the repo folder.
- Install necessary dependencies into your project.
    - Run `npm install`. 
    - NOTE: Since the repo creator didn't push their node_modules folder to GitHub, you won't have the necessary node modules installed until you run this line, which looks in your package.json file and downloads all listed dependencies.

### OR

### creating your own React project from scratch
- Use `create-react-app [your-project-name]` to make a new project on your laptop.
- NOTE: By running the `create-react-app` command, you now have a working front-end React app with basic dependencies installed, so you do not need to run `npm install` to download anything.
- Create your own repo.
    1. Go to your GitHub account and click the button for a new repo. Name it.
    1. Either:
        1. Click the checkbox to initialize the repo with a README file. 
            - Do this if you want to clone down a project folder with a README file in it and then add your own files to this folder.
            - This is not a great option if you plan to create your own React app from scratch because `create-react-app` makes its own project folder, so you will end up with one of two situations. Either:
                1. Your top folder is the repo folder. Other than containing the README, this folder is basically just an extra folder with your React project folder nested inside. Since `npm start` expects you to be in the React folder when run, you either have to `cd` into the React folder or run `npm start --prefix [react-folder-name]` to tell it where to run. You also have to be careful which folder you are in when running `nodemon` for similar reasons.
                
                OR
                
                2. You can copy all the contents of your `create-react-app` folder directly into your cloned repo folder. But the `create-react-app`folder has at least one hidden file, the `.gitignore` file, so you will have to know how to move a hidden file or you will have to recreate the `.gitignore` file in the repo folder and have it ignore your `node_modules` folder so you are not pushing node modules to GitHub.
            - As you can see, clicking the checkbox to make a README can be a messy solution when you are trying to add your own `create-react-app` project to a GitHub repo.
        1. Do not click the checkbox to create a README file. 
            - This option works more smoothly when you already have local files you want to add to the repo (like when you make a React app with `create-react-app`).
            - You will notice that when you do not click the checkbox for a README, the next page shows a list of commands you can use to connect your local files to the new repo you made. Here are some recommended steps:
                1. Run `git init` inside the project folder. This tells git that your local folder is a repository. It stores a hidden folder called `.git` in your project folder. (If you ever have to undo `git init`, you can just delete this hidden folder.) 
                1. Run `git remote add origin [your-repo-URL]` to connect your local folder to the correct repo on your GitHub account.
    1. Commit changes to your code.
        1. Run `git add [file names or .]` and `git commit -m "commit message"` to add and commit changes.
        1. Run `git push -u origin master` to push commited changes. Normally, you just need `git push`, but your first push needs to specify which branch on GitHub you are pushing your local branch to. If you forget this commit and simply run `git push`, the console will simply remind you what command to run.


## Start project
- If it is a React project, start your front-end React server with `npm start` ffrom the project folder.
- If it has a Node back end, run `nodemon` from the project folder. 
    #### Notes and troubleshooting
    - When you simply run `nodemon` with nothing else in the command, it assumes your server file is named `index.js` and that it is located at the top of your project folder (in the same folder where you ran `nodemon`). 
    If your server file is named something else or it is located in a folder (like a `server` folder), you will have to add a path to the `nodemon` command, such as `nodemon server/index.js`. This tells nodemon where the file is.
    - If you get errors in the console saying it "cannot resolve" the path to your index.js file, you are probably not running `nodemon` from the right folder or you need to give `nodemon` the path to your server file.