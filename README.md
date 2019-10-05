# docker-context

OS X wrapper script for `docker context`, creating colored Terminal sessions for different docker contexts.

If you use docker-machine instead of docker contexts, please see [docker-env](https://github.com/robbertkl/docker-env).

## Installation

* Install the [docker-context](docker-context) script to any `bin/` directory in your `$PATH`, for example:

```
curl -sSL https://raw.githubusercontent.com/robbertkl/docker-context/master/docker-context > /usr/local/bin/docker-context
chmod +x /usr/local/bin/docker-context
```

* In order to have custom Terminal colors for your docker contexts, create profiles for them in Terminal preferences. Duplicate your favorite/default profile and modify their background color. Change the profile names to their corresponding docker context name.

* Optionally, you can create convenient shortcut symlinks for each of your contexts:

```
cd $(dirname $(which docker-context))
docker context ls -q | xargs -n 1 ln -s docker-context
```

## Usage

To use it, you can either call it with an argument:

```
docker-context dev
```

or, if you created the shortcut symlinks, just use the context name:

```
dev
```

### Default context

Aside from using `default`, you can use any non-existent context name to use the default context.

You can use this, for example, to let `dev` go to your local Docker Desktop installation.

## Authors

* Robbert Klarenbeek, <robbertkl@renbeek.nl>

## License

This repo is published under the [MIT License](http://www.opensource.org/licenses/mit-license.php).
