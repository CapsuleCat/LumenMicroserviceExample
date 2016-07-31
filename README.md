# Circle Flock


## Getting Started

### Virtual Environment

Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads).

Download and install [Vagrant](https://www.vagrantup.com/downloads.html).

We recommend using [Laravel Homestead](https://laravel.com/docs/5.2/homestead),
which comes with PHP 7.0, HHVM, Postgres, and Redis build in.

Update your etc host file:

```
vi /etc/hosts
```

And add the line:

```
192.168.10.10   match.circleflock.app
```

Install Homestead using:

```
vagrant box add laravel/homestead
cd homestead
vagrant up
```

Once install, simply ssh into the vagrant box in order to work on your PHP stuff:

```
vagrant ssh
```

## Running Tests

Each microservice in the project has it's own set of tests. You can run the tests
for each service by ssh'ing into the box. Example:

```
vagrant ssh
cd circle-flock/match
phpunit
```
