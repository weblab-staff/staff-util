# staff-util

utility scripts for web.lab staff

## workshop-cherry-pick

Mass cherry-picks the specified commit to all workshops. Ensures that all branches are up-to-date with origin before cherry-picking. After running this script, use `git push --all` to push all local branches.

Usage: `./workshop-cherry-pick [commit] --start [start-branch]`

- `commit`: (optional) the hash of the commit to cherry-pick. Uses the most recent commit on the current branch if not specified
- `start-branch`: (optional) first branch to cherry-pick to (any branches before `start-branch` will not receive the changes). Applies to all branches if not specified.
- `end-branch`: (optional) last branch to cherry-pick to (inclusive)

e.g. to apply commit `a1b2c3` to all of workshop 0

```bash
./workshop-cherry-pick a1b2c3 --start workshop0-starter --end workshop0-complete

# short option also supported
./workshop-cherry-pick a1b2c3 -s workshop0-starter -e workshop0-complete
```

## environment-setup-grader

Can give this to students to make sure they set up their development environment. Checks:

- node installed to version 12 or 13
- npm installed
- git installed
- they have a MongoDB SRV
