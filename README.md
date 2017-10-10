# Sonarlint docker image

This is a docker image for running sonarlint cli.

## Usage

### Running on standalone mode

To run this on a *standalone* mode, run the command below. This will perform scan based on its default configuration.
	```shell
	docker run --rm -ti -v $PWD:/app travissouth/sonarlint
	```

### Running on connected mode

*Connected* mode is usually used if you have a SonarQube server where you want to retrieve all the configurations from the server. To do this, you need to setup first your global configuration (refer to this [link](http://www.sonarlint.org/commandline#Connected)).

If you followed that, most likely your global config is located in `~/.sonarlint/conf/global.json`.

Once done with global configuration, you can now run this using:
	```shell
	docker run --rm -ti -v $PWD:/app -v $HOME/.sonarlint:/root/.sonarlint travissouth/sonarlint -u
	```

## License

MIT
