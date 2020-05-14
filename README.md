# Pr_automate

Automate your Pull Request checks.
It does all your basic rule checks like :

- (should add the rules)
- 

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Installing

A step by step series of examples that tell you how to get a development env running

There are two methods available, 1st one being the simpler one

1. Directly Installing the Github Package with pip:

    ```shell
    python -m pip install git+https://github.com/ps011/automated-pull-request
    ```
2. Directly Download the Github Package, execute the following command inside the downloaded folder:

    ```shell
    pip install .
    ```

You can check the correct installation by executing following command:

	 pr_automate

And the default correct output will be this:

```
scm payload needs to be present like Github or Bit_bucket.
```

## Deployment

Download the [Generic Webhook Plugin](https://plugins.jenkins.io/generic-webhook-trigger/), follow the setup instructions present there.

Add a Post content parameter during the setup above with

```
Variable       :   payload
Expression   :   $
```

After configuring the plugin, just add the following line to your shell/batch script in the trigger job:

```
pr_automate
```

you should be seeing comments with warnings on future pull requests in that repo like this:

(Add some png's  here)

## Built With

(add something here if you want.) 

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details


## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
