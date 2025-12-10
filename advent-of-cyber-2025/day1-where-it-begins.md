
## Overview
day1 is not too bad! Mojorly it testing if you can navigate through linux file system. The side quest in Day1, however, is a little hard. I had no idea how to solve it. I had to do a lot of researching on google and youtube. 

## Description
## Some important linux command: 
- sudo su
	- log in as root
- cat file 
	- peek file
- ls 
	- check what't inside the directory

## Some new linux knowledge for me: 
- root directory
	- only root user can access (the most secured folder)
- .bash_history
	- stored command history
	- this can expose some sensitive information

### side quest 

- So we were given credential: 
	- password: eddi_knapp:S0mething1Sc0ming
- we were supposed to use the credential to find the fragment of password
- we ere given these clues:

```
1)
I ride with your session, not with your chest of files.
Open the little bag your shell carries when you arrive.

2)
The tree shows today; the rings remember yesterday.
Read the ledger’s older pages.

3)
When pixels sleep, their tails sometimes whisper plain words.
Listen to the tail.

Find the fragments, join them in order, and use the resulting passcode
to decrypt the message I left. Be careful — I had to be quick,
and I left only enough to get help.
  
```

- so first we switch to the user eddi_knapp by typing `su eddi_knapp`
- The first clue is hinting on `env`. (keyword: session)
	- In linux, each session typically has its own set of environment variables, which define parameters like the user's home directory, path to executables, and locale settings. `3ast3r`
- THe second clue is hinting on `git`. (keyword: tree, ledger)
	- we go to `.secret` file and type `git log -p` 
	- the command allows us to see the git commit history
	- `-1s-`
- The last clue says the fragment is in a picture. We navigate to the Pictures folder. Run `ls -la` we found a hidden file. Open it and we found the frgment. 
	- `c0M1nG`
	
## We got the whole fragment 
3ast3r-1s-c0M1nG

## Tried to use this to decrypt the .gpg file in siade .secrect folder but ran into issues. 

```
gpg: problem with the agent: Permission denied
gpg: encrypted with 1 passphrase
gpg: decryption failed: Bad session key
```