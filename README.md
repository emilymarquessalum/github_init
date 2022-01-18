# github_init
Project that communicates with github API, creating and uploading to a repository. 
It is quite simple, but it allowed me to simplify a few things I had to do in a few projects of mine.
Mainly written to work with my [Portfolio Builder](https://github.com/emilymarquessalum/portfolio-builder). Go there to know more details. 
And yes, I know you can setup github to push files on change. If you dont though,
[read this](https://gist.github.com/darencard/5d42319abcb6ec32bebf6a00ecf99e86).


## Development stage: Concluded / Open for extension. 

## Functionalities:

1. Creates repository with a given name
2. Adds files in specified paths 
3. Ignores specific files as instructed.
4. Within every path it visits, it will look for a 'build_configurations.json' file, which specifies actions that need to be made in that folder. This was mainly used in the past when I was not aware of the ability to use environment variables and wanted to send my projects to github, but they had secretive data on it. Specifically, you can use:
    1. "Replace": Replaces content in specific file to be something different inside github. 
    2. "Create": Creates file in github. 

## How to use:

- Install the package. 
- Add your github information to the info.json file
- You now have direct access to the functionalities!

You can use them already through the following files: 

- main.js

This file works with [Builder Helper](https://github.com/emilymarquessalum/builder_helper).
Running main.js will get the latest project submitted to the loaders connection, using that information
to build the repository. 

- github_args.py

This file uses sys arguments to run the commands. This was made to connect to javascrypt code using 
[Python Shell](https://www.npmjs.com/package/python-shell).


- Otherwise, connect directly to 'github_behaviour.py' and use your own methods.

## Example Of Usage

Inside the project you will find:
- a .py file called "release"
- a 'build_configurations.json' file

Both were used to specify the creation of this repository. It shows how to copy files, and you can also see me replacing the github key and password used for connection inside my info.json file with mock data.

### Why this matters to me:

- Github communication can be done through any program that connects to this. 

For Project Builder for example (see below), by calling this it can setup a repository for a newly started project while doing other processes, 
which for the purposes of project builder is great! 

- Offers specific commands and possibility for expansion. 

Although not many are implemented, the ones that are can be usefull to me.

## Associated Programs:

- [Builder Helper](https://github.com/emilymarquessalum/builder_helper).
- [project_builder]().
- [portfolio_builder](https://github.com/emilymarquessalum/portfolio-builder).
