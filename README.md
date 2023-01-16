```bash
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v $(pwd):/opt \
    -w /opt \
    laravelsail/php80-composer:latest \
    composer install --ignore-platform-reqs
```

This command uses a small Docker container containing PHP and Composer to install the application's dependencies:

In the first terminal window, use the ```sail up``` command to start Laravel Sail. This will execute your application within a Docker container and is isolated from your local computer.

```bash
./vendor/bin/sail up
```

![Terminal 1](https://i.imgur.com/WIWp3mC.png)

In our second terminal, we will use the ```npm run watch``` command. The npm run watch command will continue running in your terminal and watch all relevant CSS and JavaScript files for changes. Webpack will automatically recompile your assets when it detects a change to one of these files:

```bash
npm install
npm run watch
```

