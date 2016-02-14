# toggl-cli
[![Build Status](https://travis-ci.org/meeDamian/toggl-cli.svg?branch=master)](https://travis-ci.org/meeDamian/toggl-cli) [ ![Codeship Status for meeDamian/toggl-cli](https://codeship.com/projects/4651ffa0-ae14-0133-e229-0eeab60c84ba/status?branch=master)](https://codeship.com/projects/132211) [![npm version](https://badge.fury.io/js/toggl-cli.svg)](https://badge.fury.io/js/toggl-cli) [![XO code style](https://img.shields.io/badge/code_style-XO-5ed9c7.svg)](https://github.com/sindresorhus/xo)

Manage your Toggl.com time entries from the familiarity of the nearby CLI.

## Download (node v5.0+)

```
$ npm install -g toggl-cli
```

## Usage (Simple)

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
		c current            - see details of currently running time entry (if any).
		l list [number]      - list last <number> of time entries (default: 8)
		s smart [name]       - start or stop the entry, whatever makes more sense.
			start [name]       - start new time entry with the given name.
			stop               - stop running entry.
		r rename <new-name>  - rename currently running entry to <new name>.
		b browser            - open Toggl timer in default browser.

	Note:
		→ Values in [square brackets] are optional.


$ toggl --examples

	Set default token for all future launches:
		$ toggl --save-token d9db051bf06be16c2027d3cb08769451

	List last 17 time entries for a different account:
		$ toggl --token a1ad615af03be16c2027d3dc08291457 list 17

	Run interactive mode with a different token:
		$ toggl --token a1ad615af03be16c2027d3dc08291457

	Start a new task named "Writing toggl-cli docs":
		$ toggl start Writing toggl-cli docs

	Alias toggl for work:
		$ echo "toggl2='toggl --token <work-token>'" >> ~/.bashrc
		$ toggl list   # last 8 entries from your private account
		$ toggl2 list  # last 8 entries from your work account


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

```
	Time entry
	  c ⇾ current          r ⇾ rename        l ⇾ list last 8
	  s ⇾ start or stop    p ⇾ add project   L ⇾ list last 16
	  d ⇾ discard

	Other
	  x ⇾ clear         h, ? ⇾ help          v ⇾ version
	  b ⇾ open in browser  q ⇾ quit

	What do you want to do [c,s,r,d,p,l,L,b,v,h,?,q]?
```

## Notice

* This module is in no way supported nor developed by Toggl.com .
* It's still WIP, any and all PRs highly appreciated (esp. tests ;))


## Bugs and feedback

If you discover a bug please report it [here](https://github.com/meeDamian/toggl-cli/issues/new).

Mail me at bugs@meedamian.com, on twitter I'm [@meeDamian](http://twitter.com/meedamian).


## License

MIT @ [Damian Mee](https://meedamian.com)
