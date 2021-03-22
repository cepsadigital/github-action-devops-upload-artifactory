# Upload Python Library to Artifactory 1.0.0

The `github-action-devops-python-upload-artifactory` Github Action will upload your python library to a repository in JFrog Artifactory

## Inputs

| Name | Description | Required |Default |
| --- | --- | --- | --- |
| `repository-name` | Artifactory Virtual Repository Name | :heavy_check_mark: | |
| `artifactory-user` | Artifactory username | :heavy_check_mark: | |
| `artifactory-psw` | Artifactory password | :heavy_check_mark: | |
| `artifactory-host` | Artifactory host | :heavy_check_mark: | |


## Usage

```yaml
on:
  workflow_dispatch:
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - name: Upload Python Library to Artifactory
      uses: cepsadigital/github-action-devops-upload-artifactory@1.0.0
      with:
        repository-name: td-pypi
        artifactory-user: ${{ secrets.TD_ARTIFACTORY_USER }}
        artifactory-psw: ${{ secrets.TD_ARTIFACTORY_PSW }}
        artifactory-host: https://example.example.xxx
```

## Secrets

- `TD_ARTIFACTORY_USER` - **_(Required)_** this is the Cepsa Artifactory user.
- `TD_ARTIFACTORY_PSW` - **_(Required)_** this is the Cepsa Artifactory password.

## Contact

DevOps Team - [Devops Documentation Portal](https://doc.devops.cepsacorp.com/) - devops@cepsa.com

More GitHub Actions in Cepsa TD: [https://github.com/cepsadigital?q=github-action-&type=&language=&sort=](https://github.com/cepsadigital?q=github-action-&type=&language=&sort=)
