# Steps to deploy
## Preparation
1. Run tests
   ```bash
   py.test configcatclienttests
   ```
2. Increase the version in `setup.py`.
2. Increase the version in `configcatclient/version.py`.
3. Commit & Push
## Publish
Use the **same version** for the git tag as in `configcatclient/version.py` and `setup.py`.
- Via git tag
    1. Create a new version tag.
       ```bash
       git tag v[MAJOR].[MINOR].[PATCH]
       ```
       > Example: `git tag v2.5.5`
    2. Push the tag.
       ```bash
       git push origin --tags
       ```
- Via Github release 

  Create a new [Github release](https://github.com/configcat/python-sdk/releases) with a new version tag and release notes.

## Python Package
Make sure the new version is available on [PyPI](https://pypi.org/project/configcat-client/).

## Update samples
Update and test sample apps with the new SDK version.
