# Git Workflow

## Branches
Most projects have a three-pronged git repository, with feature branches:

|Name|Use|
|---|---|
|`develop`|Active development|
|`master`|Production-ready code|
|`production`|(Nearly) identical to production environment|
|`issue/{#}`|Project development|

### Typical Project Workflow
`issue/{#}` => `develop` => `master` => `production`

1. Issue is created to manage the project
1. Branch of `develop` is created, named after issue's number
1. Development starts on new branch: local and development environments used
1. Pull request for feature branch submitted against `origin:develop`
1. Code and UI/UX reviews
1. Feature branch merged into `develop` branch
1. Testing of `develop` branch
1. Fixes made on `develop`, or merge reverted
1. `develop` merged into `master` branch
1. Merged code uploaded to staging environment and tested
1. Fixes made on `master`, or merge reverted
1. Release to production environment
1. Test on production
1. Fixes made on `master`, or release rolled back and merge reverted
1. `master` merged into `develop` and `production`
1. Branches pushed to `origin` and appropriate forks