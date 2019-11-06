# toggl-cli
###This is a fork from [meeDamian](https://github.com/meeDamian/toggl-cli) 
Manage your Toggl.com time entries from the familiarity of the nearby CLI.

## Download (node v5.0+)

```
$ npm install -g @dirdmaster/toggl-cli
```

## Usage (Simple)

![Simple Mode demo](/gifs/simple.gif)

```
$ toggl --help

  Manage your Toggl.com time entries from the familiarity of the nearby CLI.

  Usage:
    Interactive mode:
      $ toggl

    Single request:
      $ toggl <cmd>

  Flags:
    -v --version     - output version
    -h --help        - output this help
    --examples       - show usage examples
    --no-colors      - disable colors
    --save-token     - save provided token and exit
    -t --token       - run with a custom token (will not be saved)
    --set-background - set color theme. Choose more readible: dark or light

  Commands:
    c current 				- see details of currently running time entry (if any).
    l list [amount|when] 		- list last <amount> of time entries (default: 8) or <when> (see Notes)
    s smart [properties] [name|number]	- start or stop the entry, whatever makes more sense.
      start [properties] [name|number]	- start new time entry with the given name, or resume if number is given.
      stop  				- stop running entry.
    r rename <new-name> 		- rename currently running entry to <new-name>.
    pr projects  			- list existing projects.
    cl clients				- list existing clients.
    b browser				- open Toggl timer in default browser.

  Properties:
    New tasks can have properties defined as the first parameters after "start"
    → project:, proj: - set the project for this task, can be either a number, or partial name of the project
    → billable:, bill: - if passed "yes", will mark the task as billable
    → tag: - can add tags to the task, can be called multiple times

  Notes:
    → Values in [square brackets] are optional.
    → <when> is one of:
        today, yesterday, last Monday, last tue, etc…

$ toggl --examples

  Set default token for all future launches:
    $ toggl --save-token d9db051bf06be16c2027d3cb08769451

  List last 17 time entries for a different account:
    $ toggl --token a1ad615af03be16c2027d3dc08291457 list 17

  Run interactive mode with a different token:
    $ toggl --token a1ad615af03be16c2027d3dc08291457

  Start a new task named "Writing toggl-cli docs":
    $ toggl start Writing toggl-cli docs

  Resume last running time entry:
    $ toggl start 1

  List entries from the last Friday:
    $ toggl list last friday

  Alias toggl for work:
    $ echo "toggl2='toggl --token <work-token>'" >> ~/.bashrc
    $ toggl list yesterday  # yesterday entries from your private account
    $ toggl2 list           # last 8 entries from your work account


$ toggl --logo

              NN
           .: NN :.
         cX0l NN l0Nc
        xM;   NN   ;Mx
        WK    OO    KW
        oMc        cMo
         ;0Xd:,,:dX0;
           .xNMMNx.
```

## Usage (Interactive)

![Interactive Mode demo](/gifs/interactive.gif)

```
  Time entry
    c ⇾ current        1-9 ⇾ resume from the list
    s ⇾ start or stop    r ⇾ rename        l ⇾ list last 8
    d ⇾ discard          p ⇾ add project   L ⇾ list last 16

  Other
    x ⇾ clear         h, ? ⇾ help          v ⇾ version
    b ⇾ open in browser  q ⇾ quit

  What do you want to do [c,1-9,s,r,d,p,l,L,b,v,h,?,q]?
```

## Notice

* This module is in no way supported nor developed by Toggl.com .
* The original author doesn't seem to maintain this anymore, which is the reason of this fork 
* Special thanks to [nethunter](https://github.com/nethunter) who added the possibility to use properties




## License

MIT @ [Damian Mee](https://meedamian.com)
