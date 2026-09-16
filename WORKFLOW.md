Workflow Documentation
Task 1
commit hash: 
c99fb4209e6fb6e5ed2789893fdb2f893d61d6c6

This commit broke the BULK20 discount code in pricing.js so it no longer applies 20% off when buying 5 or more items.

Task 6 

# If a team of 4 were building this further, which branching strategy would you recommend (trunk-based, GitHub Flow, Git Flow) and why?
- I recommend GitHub Flow. It is easy to use for small teams because everyone works on short feature branches and uses Pull Requests to merge back into main. Git Flow is too complicated for a team of 4, and trunk-based can get messy if people push unfinished code directly to main.

# The secret you removed in Task 4 is still visible in old commits if someone digs through history. What would you actually need to do to fully remove it, and why didn't this assignment require that step?
- To completely wipe a secret from history, you have to use a tool like git filter-repo or BFG Repo-Cleaner to rewrite every old commit, and then force-push to GitHub. This assignment didn't require that because rewriting public git history changes all commit hashes, which breaks the repository for anyone else who already cloned or pulled it.

# Why was it acceptable to rewrite history in Task 2, but would NOT be acceptable to do the same thing to a commit your teammates had already pulled?
- It was fine in Task 2 because those commits were only on my local computer and hadn't been shared with anyone yet. Doing this to a commit that teammates already pulled breaks their local setups and causes major merge conflict errors when they try to pull updates.