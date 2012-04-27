This repository is used for testing composer's version invalidation feature.

To test it, use this composer.json on your project.

    {
        "repositories": [
            {
                "type": "vcs",
                "url": "https://github.com/igorw/composer-version-invalidation"
            },
            {
                "packagist": false
            }
        ],
        "require": {
            "igorw/foobar": "1.0.0"
        }
    }

There are 3 versions: 1.0.0, 1.0.1, 1.0.2. And the 1.0.3-dev version.

1.0.2 has been invalidated. To test it, try changing the constraint on your project's composer.json and installing 1.0.* or 1.0.2. Also try installing it with the `--dev` flag.

It should not be possible to install 1.0.2.
