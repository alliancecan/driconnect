# test-site

This repo simply automates application of [Hugo](https://gohugo.io/) to stuff in driconnect/content, and propagates rendered results to a [live website](https://driconnect.alliancecan.ca) 

This operates via git-ops - namely, anything checked in goes through a CI process,
described in .gitlab-ci.yml, which uses Hugo to build site content, and copies the
content to the VM (a Rocky instance in Arbutus).

You can use git commands or the git.computecanada.ca site to change or add content.
If you have an LDAP account (as member of cc_staff), you can clone and push to the repo.
(Please ask @hahn or @plstonge to be added to the git membership).  Git workflows like
cloning and merge requests are fine, as well.  Currently, there are no branches or tags -
every commit to main triggers the CI run.

Here's the simplest example of using CLI git:

```
git clone gitlab@git.computecanada.ca:hahn/test-site.git
cd test-site
edit driconnect/content/program.en.md
git commit -a -m "my update"
git push
```

If desired, we can introduce a "prod" tag, and have non-prod changes show up on a different URL.
