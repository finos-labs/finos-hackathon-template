# Contributing to FINOS Hackathons

All FINOS Hackathon projects are [Apache 2.0 licensed](LICENSE) and accept contributions via git pull requests. Each commit must be properly signed an include a DCO line in the git commit message.

## Developer Certificate of Origin (DCO)

All contributions to this project must be accompanied by a **Developer Certificate of Origin**
sign-off. This is a FINOS requirement that certifies you have the right to submit
the contribution under the project's license. 

>[!IMPORTANT]
>**All commits must be signed with a DCO signature to avoid being flagged by the DCO Bot.**
>The DCO check will fail if even a single commit in your branch is missing the Signed-off-by line.

This sign-off means you agree the commit satisfies the [Developer Certificate of Origin (DCO).](https://developercertificate.org/)

> Pull requests that contain unsigned commits will not be merged.

This means that your commit log message must contain a line that looks like the following one, with your actual name and email address:

```
Signed-off-by: John Doe <john.doe@example.com>
```

### Configuring Git to sign off 

```bash
git config --global user.name  "Your Name"
git config --global user.email "your.email@example.com"
# Then use: git commit -s -m "your message"
```
>[!NOTE]
>The email must match with the email linked to your GitHub profile (and must be set to public, see https://github.com/settings/emails to configure your email and for special configurations if keeping your email private).

Adding the -s flag to your git commit `git commit -s` will add that line automatically. You can also add it manually as part of your commit log message or add it afterwards with git commit --amend -s.

To avoid having to remember the -s flag every time, you can configure Git to sign every commit automatically on your workstation (make sure you configured your name and email correctly):

```
git config --global format.signoff true
```

### How to fix a failing DCO check

If the DCO bot flags your PR, you don't need to start over or re-open the PR. It is likely one or more of the commits inside your PR was not properly signed. You can bulk-sign your previous commits using an interactive rebase:

1. Start the rebase (Replace 'X' with the number of commits in your PR)

  ```git rebase -i HEAD~X --signoff```

2. An editor will open listing your commits. Simply save and close it without making changes.

3. Force push the corrected commits to your branch:

  ```git push --force```

### Helpful DCO Resources
- [Git Tools - Signing Your Work](https://git-scm.com/book/en/v2/Git-Tools-Signing-Your-Work)
- [Signing commits
](https://docs.github.com/en/github/authenticating-to-github/signing-commits)
