[![CircleCI](https://circleci.com/gh/noosenergy/noos-circleci-orb.svg?style=svg&circle-token=a0075b2b31e38b369f818e7bc5638ae11f5a2b61)](https://circleci.com/gh/noosenergy/noos-circleci-orb)

# Noos CircleCI Orb

Custom CircleCI Orb for working with Docker and Helm CI/CD pipelines.

## Resources

[CI/CD Noos CircleCI Orb](https://circleci.com/developer/orbs/orb/noosenergy/noos-ci) - The official registry page of this orb for all versions, executors, commands, and jobs described.

[CI/CD Noos Invoke SDK](https://pypi.org/project/noos-inv) - Software development kit for managing CI/CD pipelines, shipped with this orb.

### How to Contribute

We welcome [issues](https://github.com/noosenergy/noos-circleci-orb/issues) to and [pull requests](https://github.com/noosenergy/noos-circleci-orb/pulls) against this repository!

### How to Publish

* Create and push a branch with your new features.
* When ready to publish a new production version, create a Pull Request from your _feature branch_ to `master`.
* Request manual approval to run the integration tests against your _feature branch_.
* Once your features have been merged, the final merge commit onto the `master` branch should be tagged as `v<version>` where:

| increment | version|
| ----------| -----------|
| major     | 1.0.0 incremented release|
| minor     | x.1.0 incremented release|
| patch     | x.x.1 incremented release|

### Known Issue

You may encounter this CircleCI error when pushing a new PR:

```
The dev version of noosenergy/noos-ci@dev:<version> has expired. Dev versions of orbs are only valid for 90 days after publishing.
```

You may need to publish a [`dev:<version>`](https://github.com/noosenergy/noos-circleci-orb/blob/master/.circleci/config.yml#L21) version manually:

    $ circleci orb pack ./src | circleci orb validate -
    $ circleci orb pack ./src | circleci orb publish - noosenergy/noos-ci@dev:<version>

You may also get such an error if the dev version is out of date and there are config changes in the latest orb that aren't in the dev version.
