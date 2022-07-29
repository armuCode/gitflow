armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git init
Initialized empty Git repository in C:/Users/armjo/OneDrive/Escritorio/gitflow/.git/

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        demo.js

nothing added to commit but untracked files present (use "git add" to track)

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git add .

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   demo.js


armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git commit -m 'feature(function) add suma AB'
[main (root-commit) 56b3361] feature(function) add suma AB
 1 file changed, 3 insertions(+)
 create mode 100644 demo.js

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git status
On branch main
nothing to commit, working tree clean

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git checkout -b develop
Switched to a new branch 'develop'

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (develop)
$ git status
On branch develop
nothing to commit, working tree clean

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (develop)
$ git status
On branch develop
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   demo.js

no changes added to commit (use "git add" and/or "git commit -a")

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (develop)
$ git add .

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (develop)
$ git status
On branch develop
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   demo.js


armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (develop)
$ git log
commit 56b336189152bb15c8bb14e9ec991150ed231081 (HEAD -> develop, main)
Author: Armando Bermudez <armucode@gmail.com>
Date:   Fri Jul 29 11:33:12 2022 -0500

    feature(function) add suma AB

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (develop)
$ git status
On branch develop
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   demo.js


armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (develop)
$ git add .

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (develop)
$ git status
On branch develop
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   demo.js


armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (develop)
$ git commit -m 'feature(carpeta)add resta AB'
[develop b095665] feature(carpeta)add resta AB
 1 file changed, 4 insertions(+)

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (develop)
$ git status
On branch develop
nothing to commit, working tree clean

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (develop)
$ git status
On branch develop
nothing to commit, working tree clean

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (develop)
$ git checkout main
Switched to branch 'main'

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git merge develop
Updating 56b3361..b095665
Fast-forward
 demo.js | 4 ++++
 1 file changed, 4 insertions(+)

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git branch
  develop
* main

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git status
On branch main
nothing to commit, working tree clean

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git remote add origin https://github.com/armuCode/gitflow.git

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git push origin main
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (6/6), 545 bytes | 272.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/armuCode/gitflow.git
 * [new branch]      main -> main

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git branch
  develop
* main

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git branch release

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git branch
  develop
* main
  release

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git branch feature

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git branch
  develop
  feature
* main
  release

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (main)
$ git switch develop
Switched to branch 'develop'

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (develop)
$ touch .gitignore

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (develop)
$ git switch feature
Switched to branch 'feature'

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (feature)
$ git merge develop
Updating b095665..8966c12
Fast-forward
 .gitignore |   0
 flow.md    | 180 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 prueba.js  |   7 +++
 3 files changed, 187 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 flow.md
 create mode 100644 prueba.js

---------------------------

armjo@Armando-Laptop MINGW64 ~/OneDrive/Escritorio/gitflow (feature)
$ git log
commit 0b3746f205bc3da04eba7e9651976567cb72b197 (HEAD -> feature)
Author: Armando Bermudez <armucode@gmail.com>
Date:   Fri Jul 29 12:11:37 2022 -0500

    Feature(FunArrayFeature) add function AB

commit 8966c126facaad67843690b666e5a838836b81b6 (develop)
Author: Armando Bermudez <armucode@gmail.com>
Date:   Fri Jul 29 12:05:54 2022 -0500

    Feature(prueba.js) add sumaArray AB

commit b095665430815ceb8ff4002c13eaef51d8767ac9 (origin/main, release, main)
Author: Armando Bermudez <armucode@gmail.com>
Date:   Fri Jul 29 11:37:43 2022 -0500

    feature(carpeta)add resta AB

commit 56b336189152bb15c8bb14e9ec991150ed231081
Author: Armando Bermudez <armucode@gmail.com>
Date:   Fri Jul 29 11:33:12 2022 -0500

    feature(function) add suma AB