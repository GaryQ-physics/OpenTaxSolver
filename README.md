# Open Tax Solver
fork of
`https://svn.code.sf.net/p/opentaxsolver/SrcCodeRepo/`
just so I have it on git.

Their main website: `http://opentaxsolver.sourceforge.net/`

Have subversion, git, and git-svn packages apt installed.

Workflow
```
$ cd OpenTaxSolver/git/
$ git branch
* master
  svnrebase
$
$ git checkout svnrebase
$ git svn rebase
$ git checkout master
$ git merge svnrebase
$ git push
$ git checkout svnrebase
$ git push
$ git checkout master
```
