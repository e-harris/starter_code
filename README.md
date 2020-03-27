# Jenkins

Jenkins is a program that automates testing and can merge your branch with master on GitHub

### New Freestyle Project

Mostly self explanatory

 - Discard old builds to stop the server from clogging up
 - use https github link
 - restrict where this project can run - if test environment has already been built - sparta-ubuntu-node

 **Source Code Management**

  - use SSH link to your GitHub
  - Use private SSH key on your Jenkins credentials.
  - Use public key on your GitHub
  - Use `*/dev*` in branch to build
    - Searches for all branches beginning with dev - is a good naming convention for branches

**SHH KEYS**

  ALWAYS generate your keys in .shh

  `ssh-keygen -t rsa -b 4096`

  no passcode



  - Git hook trigger - change to GitHub starts Jenkins
  - Provide Node & npm bin/ folder to PATH

**Build**
Where/how you run your tests (bash), for sparta app:
```
cd app
npm install
npm test
```

**Git Publisher** - plugin
 - push only if build succeeds
 - Merge results
 - branch to push - master
 - target remote name - origin
