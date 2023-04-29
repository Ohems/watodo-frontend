# ![Watodo](./docs/images/logo.png) [WIP]

Community event and responsibility management tool. Work in progress and currently unusable.

## Requirements

- [Node.js](https://nodejs.org/en/) 18 LTS or newer
- [npm](https://www.npmjs.com/) 6.14.0 or newer

For the test environment:

- [Docker and Docker Compose](https://docs.docker.com/compose/install/)

**NOTE:** Some of the console commands in this documentation may not run in batch or Powershell! When developing on Windows, Git Bash or Linux subsystem is recommended.

## Installation

In order to install the dependencies, navigate to the project folder and run

```bash
npm install
```

## API documentation

When the Node.js server is running, the Swagger documentation can be viewed at path `/api/api-docs`.

### PostgreSQL database

This app uses a single PostgreSQL database to store its data. It can be hosted separately, but the easiest way to host is with a Docker container. To start the container, make sure that the Docker daemon is running and run

```bash
docker-compose up -d
```

In order to stop the container, run

```bash
docker-compose stop
```

In order to stop and destroy the container, run

```bash
docker-compose down
```

## Run tests

```bash
npm test
```

## Run development

Copy the environment variable sample file with

```bash
cp .env-sample .env
```

and fill in the correct environment variables. Then source the file with

```bash
source .env
```

or use [autoenv](https://github.com/kennethreitz/autoenv). Make sure that the database is migrated with

```bash
knex migrate:latest
```

Finally, start the server with

```bash
npm run watch
```

The development server detects saved changes and automatically refreshes the content.

## Run production

Ensure that all required environment variables are correctly set and the database is up and migrated. Then run

```bash
npm start
```

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

**NOTE:** Project is currently in its earliest stages and actively developed all around without clear organization. Contributing at this stage isn't recommended.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/Ohems/mlc/releases).

## Authors

- [Ohems](https://github.com/Ohems) - *Initial work*

See also the list of [contributors](https://github.com/Ohems/mlc/graphs/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
