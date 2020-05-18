# Pr_automate

Automate your Pull Request checks.
It does all your basic rule checks like :

- Description should be added in a PR.
- LOC in a file should not be more than 1000.
- PR should not contain large changes(more than 10 files).
- Commits with only commented code should be discouraged.
- check if the test folder is modified/ new tests should be added when source code is changed.

## Getting Started

### Installing

There are two methods available, 1st one being the simpler one

1. Directly Installing the Github Package with pip:

    ```shell
    python -m pip install git+https://github.com/ps011/automated-pull-request
    ```
2. Directly Download the [Github Package](https://github.com/ps011/automated-pull-request), execute the following command inside the folder pr_automate, containing setup.py file:

    ```shell
    pip install .
    ```

You can check the correct installation by executing following command in your terminal:

	 pr_automate

And the default correct output will be this:

```
scm payload needs to be present like Github or Bit_bucket.
```

## Deployment

Download the [Generic Webhook Plugin](https://plugins.jenkins.io/generic-webhook-trigger/), follow the setup instructions present there.

Add a Post content parameter during the setup above with

```
Variable     :   payload
Expression   :   $
```

After configuring the plugin, just add the following line to your shell/batch script in the trigger job:

```
pr_automate
```

you should be seeing comments with warnings on future pull requests in that repo like this:


![gif](./github_2_edited.gif?raw=true)


