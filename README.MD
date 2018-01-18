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


## Start project
- If it is a React project, start your front-end React server with `npm start` ffrom the project folder.
- If it has a Node back end, run `nodemon` from the project folder. 
    #### Notes and troubleshooting
    - When you simply run `nodemon` with nothing else in the command, it assumes your server file is named `index.js` and that it is located at the top of your project folder (in the same folder where you ran `nodemon`). 
    If your server file is named something else or it is located in a folder (like a `server` folder), you will have to add a path to the `nodemon` command, such as `nodemon server/index.js`. This tells nodemon where the file is.
    - If you get errors in the console saying things saying it "cannot resolve" the path to your