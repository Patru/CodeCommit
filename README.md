CodeCommit
==========

This is an experimental project to show how to commit code to a maglev server when all the test cases run fine.

Maglev (https://github.com/MagLev/maglev) is a ruby implementation that allows you to persist ruby objects
transparently. However, this comes with an added responsibility, you have to commit the classes you want to persist
to the server too. During the process of committing a file it is parsed and and compiled, this catches your most
obvious programming errors. Those classes will then be committed and they add to the persistent codebase of the
server.

However, this code can still contain a lot of bugs and you would like to run your tests on it. In this project
I would like to explore if it is possible to load my classes to a MagLev-server, run the tests, figure out if they
worked and only commit my code changes if the tests ran well.