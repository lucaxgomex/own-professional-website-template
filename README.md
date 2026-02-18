<img align="right" width="150" alt="logo" src="https://user-images.githubusercontent.com/5889006/190859553-5b229b4f-c476-4cbd-928f-890f5265ca4c.png">

# Hugo Theme Stack Starter Template

This is a quick start template for [Hugo theme Stack](https://github.com/CaiJimmy/hugo-theme-stack). It uses [Hugo modules](https://gohugo.io/hugo-modules/) feature to load the theme.

It comes with a basic theme structure and configuration. GitHub action has been set up to deploy the theme to a public GitHub page automatically. Also, there's a cron job to update the theme automatically everyday.

## Get started

1. Click *Use this template*, and create your repository as `<username>.github.io` on GitHub.
![Step 1](https://user-images.githubusercontent.com/5889006/156916624-20b2a784-f3a9-4718-aa5f-ce2a436b241f.png)

2. Once the repository is created, create a GitHub codespace associated with it.
![Create codespace](https://user-images.githubusercontent.com/5889006/156916672-43b7b6e9-4ffb-4704-b4ba-d5ca40ffcae7.png)

3. And voila! You're ready to go. The codespace has been configured with the latest version of Hugo extended, just run `hugo server` in the terminal and see your new site in action.

4. Check `config` folder for the configuration files. You can edit them to suit your needs. Make sure to update the `baseurl` property in `config/_default/config.toml` to your site's URL.

5. Open Settings -> Pages. Change the build branch from `master` to `gh-pages`.
![Build](https://github.com/namanh11611/hugo-theme-stack-starter/assets/16586200/12c763cd-bead-4923-b610-8788f388fcb5)

6. Once you're done editing the site, just commit it and push it. GitHub action will deploy the site automatically to GitHub page asociated with the repository.
![GitHub action](https://user-images.githubusercontent.com/5889006/156916881-90b8bb9b-1925-4e60-9d7a-8026cda729bf.png)

---

In case you don't want to use GitHub codespace, you can also run this template in your local machine. **You need to install Git, Go and Hugo extended locally.**

## Update theme manually

Run:

```bash
hugo mod get -u github.com/CaiJimmy/hugo-theme-stack/v3
hugo mod tidy
```

> This starter template has been configured with `v3` version of theme. Due to the limitation of Go module, once the `v4` or up version of theme is released, you need to update the theme manually. (Modifying `config/module.toml` file)

## Deploy to another static page hostings

If you want to build this site using another static page hosting, you need to make sure they have Go installed in the machine. 

<details>
  <summary>Vercel</summary>
  
You need to overwrite build command to install manually Go:

```
amazon-linux-extras install golang1.11 && hugo --gc --minify
```

![](https://user-images.githubusercontent.com/5889006/156917172-01e4d418-3469-4ffb-97e4-a905d28b8424.png)

If you are using Node.js 20, you need to overwrite the install command to install manually Go:

```
dnf install -y golang
```

![image](https://github.com/zhi-yi-huang/hugo-theme-stack-starter/assets/83860323/777c1109-dfc8-4893-9db7-1305ec027cf5)


Make sure also to specify Hugo version in the environment variable `HUGO_VERSION` (Use the latest version of Hugo extended):

![Environment variable](https://user-images.githubusercontent.com/5889006/156917212-afb7c70d-ab85-480f-8288-b15781a462c0.png)
</details>

# terminalCV

[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/go-semantic-release/semantic-release)
[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-%23FE5196?logo=conventionalcommits&logoColor=white)](https://conventionalcommits.org)
![GitHub Tag](https://img.shields.io/github/v/tag/coolapso/hugo-theme-terminalcv?logo=semver&label=semver&labelColor=gray&color=green)
![terminalCV](https://raw.githubusercontent.com/coolapso/hugo-theme-terminalcv/master/images/screenshot.png)

# General Information

An easy to setup and (almost) fully hackable command line style CV theme with blogging capabilities

Live example at: <https://coolapso.sh>

# Features

* Blogging:
  * Toggle support, don't want blog features? just disable them!
  * Support for images
  * Supoort for [hugo shortcodes](https://gohugo.io/content-management/shortcodes/) (not fully tested, but should work!)
* Custom Greeting
  * Multi line text is respected
* Customizable prompt
  * Custom before & after prompt text
  * Custom before & after prompt colors
  * Custom prompt text
  * Custom prompt text Color
  * custom separator text
  * custom separator color
  * custom before & after symbols text
  * custom before & after symbols colors
  * Custom symbols
  * Custom symbols color
  * Custom extra text
  * Custom extra text color
* Multiple sections with individual commands:
  * **Whois:** General information about the individual
  * **social:** shows social networks
    * Any social network is supported, even the ones that don't exist! just provide a name and a URL
    * The social network name can be hidden and show only the URL
  * **work:** shows work experience information
    * Title can have custom color
  * **education:** shows education information
    * Title can have custom color
  * **sklls:** Shows skills information
    * Skill name can have custom color
  * **softskills:** shows softskills information
    * Skill name can have custom color
  * **languages:** Shows languages skills information
    * Language name can have custom color
  * **projects:** Shows projects information
    * Project title can have custom color
  * **misc:** Free text
    * misc command can be overriden and given another name
    * Title can have custom color
    * Content can have custom color
* Extra commands:
  * **startx:** Shows "loading..." progress bar and redirects to another website
    * Disabled by default
    * only enabled if provided a location to send to
  * **exit:** Shows "terminating..." progress bar and redirects to another website
    * Disabled by default
    * only enabled if provided a location to send to
  * **source:** Shows the glider and the theme github repo URL
    * Enabled by default
    * Can be disabled
  * **version:** Shows the website version
    * Disabled by default
    * only enabled if provided a version parameter
* Less, print commands output with less
  * Global, all commands use less instead of standard output
  * Per command, only defined commands use less as output method
  * `less <command>`, will output using less instead of standard output
* Command auto completion
* progression bars can be interrupted by pressing `ctrl+d`
* Favicons
* Bootsequence:
  * Option for a custom bootsequence to mimic the boot process of the terminal
  * If the parameter is not set, the bootsequence is skipped.
# How to start

This theme is far more simplistic than most themes therefore running `hugo new site` creates a lot of things that are not necessary.

```
mkdir -p myterminalcv/themes
cd myterminalcv
git clone https://github.com/coolapso/hugo-theme-terminalcv themes/terminalcv
cp themes/terminalcv/exampleSite/config.yml .
hugo server
```

Now you can start personalizing it by changing the config.yml and when you are happy just build the site with `hugo`

## Recommended way

If you are using git (which you should be!) for your website and don't want to make any radical changes to the theme itself, it's recommended that you add the theme as a submodule. This way, you can easily get new updates when they are available.

``` bash
git submodule add https://github.com/coolapso/hugo-theme-terminalcv.git themes/terminalcv
```

# How to configure

All the content and configuration is done through the [config.yml](config.yml).

you can just copy the existing example file and change it to your liking.

# Faviconss

[RealFaviconGenerator](https://realfavicongenerator.net/) and put the generated files into the static your folder

# Blog posts

blog post functionalities are enabled/disabled with the `blog` key in the params section

```yaml
params:
  blog: true
```

The theme supports blog posts, site visitors can find the posts with the `posts` or `ls` commands, and can view posts with `cat <filename>` to see how it works you can read the [example post](/exampleSite/content/posts/examplepost/index.md). 



![terminalCV](https://raw.githubusercontent.com/coolapso/hugo-theme-terminalcv/main/images/blogdemo.gif)


The live demo may not be making use of the blogging capabilities, but you can always see it in action like this:

> [!IMPORTANT]  
> Be sure to have hugo installed before proceeding

```
git clone https://github.com/coolapso/hugo-theme-terminalcv
cd hugo-theme-terminalcv
make server
```

Now a demo will be available at http://localhost:1313

# Contributions

Improvements and suggestions are always welcome, feel free to open an Issue or Pull Request

If you like this theme and want to support / contribute in a different way you can always:

<a href="https://www.buymeacoffee.com/coolapso" target="_blank">
  <img src="https://cdn.buymeacoffee.com/buttons/default-yellow.png" alt="Buy Me A Coffee" style="height: 51px !important;width: 217px !important;" />
</a>

# Development

If you just want to make any changes and be able to test them as you progress, or if you simply just want to test the module wihtou having to create a new hugo website you can just run

```
git clone https://github.com/coolapso/hugo-theme-terminalcv
cd hugo-theme-terminalcv
make server
```

if you don't have make, then you can just run:

```
hugo server --config exampleSite/config.yml --theme ""
```

# jcubic/Jquery.Terminal

terminalCV makes use [jcubic/jquery.terminal](https://github.com/jcubic/jquery.terminal)

# Using this theme?

Let me know and feel free to open a Pull Request and add it to this list:

|link                 | Description       |
|---------------------|-------------------|
|<https://coolapso.sh>  | Simple CV         |
