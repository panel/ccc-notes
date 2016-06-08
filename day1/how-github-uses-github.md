# How Github Uses Github

### Repo Navigation
Viewing commits by a specific user
* `<user>/<repo>/commits?author=<user>`
* `<user>/<repo>/commits/<branch>?author=<user>`

Diff any two points in time on a project
* `<user>/<repo>/compare`
* `<user>/<repo>/compare/<commit-ish>...<commit-ish>`
    commit*ish is githubs way to specify any point in time: commits, time, etc.

Suppress whitespace changes in diff (git diff -w)
* `diff-url?w=1`

Point out specific lines in a file
* `<user>/<repo>/blob/<commit-ish>/path#L<line-number>-L<line-number>`

Keyboard shortcuts
* `shift` + `?` (context sensitive menu for shortcuts)
    similar to gmail shortcuts apparently

Fuzzy file finder
* `t`

Github on Command Line
* `hub`
* `hub checkout pull-request-url`

### Managing Projects
Set up teams in an organization
* github has more teams than people
* send @ mentions to whole teams with @teamname

Share guidelines
* `contributing.md`
* `issue_template.md`
* `pull_request_template.md`
* Put them in a `.github` folder

Markdown
* use it

Be smart w/ binaries
* don't commit build artifacts, use LFS
* LFS: Large File Storage, an open source extension

### Finding all the things
help.github.com/categories/search

flags:
* mentions:user
* team:org/team
* `<emoji-name> in:comment` (can't do this in Bitbucket!)
* base=target-branch
* is:state
* status:combined-status
* updated:date
* `git log -L :<function-name>:<file-path>`
* `git log -S <string>`
* `git log -G <regex>`
* `git log -L <line1>,<line2>:<file-path>`

### Better Pull Requests
Start a conversation on changes not just when you're ready to merge
* The biggest barrier here is psychological
* Don't be afraid to show incomplete work
* `git commit --allow-empty`

Automatically close issues
* `Fixes #<issue-number`
* `Closes #<issue-number>`
* `Resolves #<issue-number>`

Status API
* associate visible state w/ commits

Deployments API
* Shipit Squirrel, shows where code is deployed

### API & Integrations
Wrapper libraries and API to accomplish things programmatically
* developer.github.com

### ChatOps
Started at Github

Integrate with Github via a chat interface (Hubot)
* visibility for deployment and devops in a public channel

### What About Non-Devs?
Github Legal, uses github for organizing docs and issues
* issues are objectively better than email for a lot of reasons

### Further Reading
* Github Blog
* developer.github.com/changes
* githubengineering.com

*Github does not merge anything to master that has not been deployed to production*
