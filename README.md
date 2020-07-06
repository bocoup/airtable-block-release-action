# Airtable Release Block Github Action

This action allows you to release your block to Airtable.

## Usage

You need to add your Block Api Key your github repository as a secret. You can
find your key on your [Airtable Account Page](https://airtable.com/account).
Follow [these instructions](https://docs.github.com/en/actions/configuring-and-managing-workflows/creating-and-storing-encrypted-secrets#creating-encrypted-secrets-for-a-repository) for adding the `BlockApiKey` to your repo.

Setup the action to run on whenever you want to create a release. For example
add the following file as `.github/worksflows/release.yml` to your block repo to release
every time the master branch is pushed.

```
on:
  push:
    branches:
      - master

steps:
  - uses: airtable/airtable-block-release-action@master
```
