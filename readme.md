# Laravel Valet

[![Build Status](https://travis-ci.org/laravel/valet.svg)](https://travis-ci.org/laravel/valet)
[![Total Downloads](https://poser.pugx.org/laravel/valet/d/total.svg)](https://packagist.org/packages/laravel/valet)
[![Latest Stable Version](https://poser.pugx.org/laravel/valet/v/stable.svg)](https://packagist.org/packages/laravel/valet)
[![Latest Unstable Version](https://poser.pugx.org/laravel/valet/v/unstable.svg)](https://packagist.org/packages/laravel/valet)
[![License](https://poser.pugx.org/laravel/valet/license.svg)](https://packagist.org/packages/laravel/valet)

## Introduction

Valet is a Laravel development environment for Mac minimalists. No Vagrant, No Apache, No Nginx, No `/etc/hosts` file. You can even share your sites publicly using local tunnels. _Yeah, we like it too._

Laravel Valet configures your Mac to always run [Caddy](https://caddyserver.com/) in the background when your machine starts. Then, using [DnsMasq](https://en.wikipedia.org/wiki/Dnsmasq), Valet proxies all requests on the `*.dev` domain to point to sites installed on your local machine.

In other words, a blazing fast Laravel development environment that uses roughly 7mb of RAM. Valet isn't a complete replacement for Vagrant or Homestead, but provides a great alternative if you want flexible basics, prefer extreme speed, or are working on a machine with a limited amount of RAM.

## Official Documentation

Documentation for Valet can be found on the [Laravel website](http://laravel.com/docs/5.2/valet).

## Requirements

 - Ubuntu >= 15.05 
 - PHP >= 5.6
 - PHP Packages: `php*-cli php*-common php*-curl php*-json php*-mbstring php*-mcrypt php*-mysql php*-opcache php*-readline php*-xml php*-zip`

## Installation

1. `composer global require cpriego/valet-ubuntu`
2. `valet install`

## Usage

**`valet park`**
You can use `valet park` inside the directory where you store your projects (like Sites or Code) and then you can open `http://projectname.dev` in your browser. This command will allow you to access all the projects in the *parked* folder.

**`valet link`**
If you just want to serve a single site you can use `valet link [your-desired-url]` and then open `http://your-desired-url.dev` in the browser.

To check the status of the **Caddy** Server just type **`valet status`**.

## Update

To update your Valet package just run: `composer global update`

## F.A.Q.

**Why can't I run `valet install`?**
Check that you've added the `.composer/vendor/bin` directory to your `PATH` in either `~/.bashrc` or `~/.zshrc`.

## License

Laravel Valet is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)
