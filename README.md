## Supported tags and respective `Dockerfile` links

* [`2.1.0`, `latest`](https://github.com/herloct/docker-phpmetrics/blob/2.1.0/Dockerfile)
* [`2.0.0`](https://github.com/herloct/docker-phpmetrics/blob/2.0.0/Dockerfile)

## What is PhpMetrics?

PhpMetrics is a static analysis tool for PHP. It provides tons of metrics:

* **Complexity**: Cyclomatic complexity, Myer's interval, Relative system complexity
* **Volume**: Vocabulary, Data complexity, Lines of code, Readability...
* **Object Oriented**: Lack of cohesion of methods, Coupling, Abstraction...
* **Maintainability**: Maintainability index, Halstead's metrics, Effort...
* [And more !](http://www.phpmetrics.org//documentation/index.html)

> http://www.phpmetrics.org/

## How to use this image

Basic usage using current user.

```sh
docker run --rm \
    --user $(id -u):$(id -g) \
    --volume /local/path:/project \
    herloct/phpmetrics[:tag] [<options>]
```

For example, to generate metrics of our `src` directory.

```sh
docker run --rm \
    --user $(id -u):$(id -g) \
    --volume /local/path:/project \
    herloct/phpmetrics --report-html=build/metrics src
```

## Volumes

* **/project**: Your PHP project directory.
