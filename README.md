# codeship-env-var-showcase

Codeship environment `CI_COMMIT_DESCRIPTION` variable contains a newline character.

This repo is a simple showcase of the bug.

Shell script:
```
echo "-CI_COMMIT_DESCRIPTION-=-${CI_COMMIT_DESCRIPTION}-"
```

Codeship run output:
```
2017-01-24T22:44:10.196Zshowcasebuild/pull started
2017-01-24T22:44:10.310Zshowcasebuild/pull finished successfully
2017-01-24T22:44:11.437Zshowcase-CI_COMMIT_DESCRIPTION-=-the_description_tag_should_not_contain_a_newline_character
2017-01-24T22:44:11.437Zshowcase-
```

I've been told the issue is queued to fix, shout when it is :)

