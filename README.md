# Repositories 

**This is my preferred way to make a project in which I have access to Git & GitHub**
- Have your project (or at least your workspace set up)
- Run the ```git init``` command to initialise a local repo on your project.
- Then run ```gh repo create``` to create your remote repo.
  - If you simply do this command above, the name of the repo will be the name of the directory in which this project lives.
  - Else, you can specify a name for your repository using ```gh repo create [newRepoName]```

This is taken right from the github cli [site](https://cli.github.com/manual/gh_repo_create). en gros, it is a visual of the commands that correlate with what I am trying to explain above
```bash
  # create a repository under your account using the current directory name
  $ git init my-project
  $ cd my-project
  $ gh repo create

  # create a repository with a specific name
  $ gh repo create my-project

  # create a repository in an organization
  $ gh repo create cli/my-project

  # disable issues and wiki
  $ gh repo create --enable-issues=false --enable-wiki=false
```
## Creating a new repository
- Type the command: ```gh repo create [newRepoName]```
- The above is to create a repo for my personal account, which is the one I will most often use, This said,to create a repository for your organisation: ```gh repo [organisationName]/[newRepoName]```
- You'll then be asked a few questions:
  - Visibilty: (Public, Private or Internal)
  - then you will see: ```This will create [newRepoName] in your current directory. Continue?```
    - Yes will proceed to the next step
    - No will stop the process altogether
  -  Create a local project directory for [repoOwnerName]/[newRepoName]?
     -  Yes will create a new directory, with the same name as your repo name, in your current directory. that is, a folder inside your current folder. It will also automatically create and initialise a git repository in this folder. This is the same as when we manually do ```git init```.
     -  No will not create a folder, but the git repository will not be initialised. So when you go to github, you will see your empty git repository waiting to be attached to a folder (like how I've been regularly doing it). This is very counter-intuitive.

## Cloning a Repository
- To clone a repository: ```gh repo clone [organisationName]/[repositoryName]```
- So for example, if I wanted to clone [vuejs] repository, it would look like this: ```gh repo clone vuejs/vue```

## Forking a Repository
- Let's say we wanted to make changes and have the capability of pushing and pulling our cloned vuejs repository. We can't do that as it is as we don't own it. Solution? Forking it: ```gh repo fork```
- It will then ask: Would you like to add a remote to the fork? 
  - Yes will take the current remote, change it's name from origin to upstream. It will Make a new remote and name that one origin
  - No, will not create a new remote. Don't know the repurcussions of this
- We can also fork a repo without cloning it. This is much more preferable: ```gh repo fork vuejs/vue```





[vuejs]: https://github.com/vuejs/vue




ill sort this l8r

gh cli useful commands

gh —help 
gh auth login - will probably never need to use this one again
gh auth status

create repository on gh cli
gh repo create <repositoryName>

gh clone <ownerName>/<repoName>

gh fork (I need to come back to this one)

gh repo view
gh repo view <userName>/<repoName>

IMPORTANT: if you need more help on commands (maybe even subcommands too) do this:
gh <commandName> help
so if I need more info on managing my repos. I can do:
gh repo help