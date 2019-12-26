# staff-util

utility scripts for web.lab staff

## workshop-cherry-pick

Mass cherry-picks the specified commit to all workshops.

Usage: `./workshop-cherry-pick [commit] --start [start-branch]`

- `commit`: (optional) the hash of the commit to cherry-pick. Uses the most recent commit on the current branch if not specified
- `start-branch`: (optional) first branch to cherry-pick to (any branches before `start-branch` will not receive the changes). Applies to all branches if not specified.
