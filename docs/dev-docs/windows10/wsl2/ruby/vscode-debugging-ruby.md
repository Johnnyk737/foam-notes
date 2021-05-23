# Debugging for Ruby on Rails in VScode.

## Installation
We first need to install some gems. They will be slightly different based on your ruby version.


### Ruby 2.x
```shell
gem install ruby-debug-ide
gem install debase
```

## Setting up
There have been many articles that have this set up with a very easy launch.json file. However, I have not been able to get these to work. A workaround that I found and use all the time is a combination of a VScode configuration and a shell command.

### VSCode configuration
You will need to create a configuration for this in your launch.json file. The value for `remoteWorkspaceRoot` will be the project directory on the mounted on WSL, for example: `/mnt/c/Users/johnn/foam-notes`. The `cwd` value will be the same directory but direct on the C drive. The difference will be that the backslashes will need to be escaped, for example: `C:\\Users\johnn\foam-notes`.
```json
{
  "name": "Listen for rdebug-ide",
  "type": "Ruby",
  "request": "attach",
  "remoteHost": "127.0.0.1",
  "remotePort": "1234",
  "remoteWorkspaceRoot": <project directory on mount>,
  "cwd": <project directory on C drive>,
  "showDebuggerOutput" : true
}
```

### Shell command
This command uses the `ruby-debug-ide` gem to start the debug session.
`rdebug-ide --host 0.0.0.0 --port 1234 -d -x -- ./bin/rails s -b 0.0.0.0 -p 3000 -e development"`

## Running the Debugger
1. Run the debugger shell command.
2. Start the `Listen for rdebug-ide' debugger profile and wait for the server to start.
3. Make sure you have breakpoints set.
4. Go to `localhost:3000` and go to a page that should hit your breakpoints.
5. You should be able to see the breakpoints get hit in the IDE.
6. To stop debugging, just use `Ctrl + c` which will shut down the server.

> Note: This will not hot-reload your changes into the server, so if you need to make changes, you'll need to restart this process. 
