# Lovelace Soft UI 
![license](https://img.shields.io/github/license/N-l1/home-assistant-config?style=flat-square) ![user_friendly](https://img.shields.io/badge/new%20user-friendly-brightgreen?style=flat-square&)

![lovelace_soft_UI](images/lovelace_soft_UI.jpg)

## Introduction

First and foremost **thank you** for finding you way to my Home Assistant repo. This is my [Home Assistant](https://github.com/home-assistant/home-assistant) Lovelace user interface configuration. I've been using Home Assistant for a little less than a year now (not so long), and it has brought me a huge amount of joy! This repo is to inspire and potentially be implemented into you UI! **Enjoy**! 

## Lovelace UI
Lovelace is the primary interface for Home Assistant, it is used to display all sorts of information. My take on Lovelace is for it to be **simple**. I'm trying to make it easy for **you** to implement my UI into yours! Look below for further details. 

My theme of the UI is based on [Soft UI](https://dribbble.com/shots/8027871-Soft-UI/attachments/531358?mode=media)

![ui_home_page](images/UI_home_page.png)

### Advanced Users
Thanks for taking you time to visit my repo! I have posted the yaml for my Lovelace and themes above, I have also listed the custom cards I used below. If you require further assistance, please check below.

# Prerequisites
These are some of the things you need before getting started.

## Custom Cards
You will need the following custom cards to be installed, it is easily done via [**HACS**](https://hacs.xyz). Please read HACS documentations and install the following cards.

#### Required

* [**Custom Header**](https://github.com/maykar/custom-header), by **@maykar**
* [**Button Card**](https://github.com/custom-cards/button-card), by **@RomRider**
* [**Card Mod**](https://github.com/thomasloven/lovelace-card-mod), by **@thomasloven**

#### Optional

* [**Search Card**](https://github.com/postlund/search-card) and [**Card Tools**](https://github.com/thomasloven/lovelace-card-tools), by **@postlund** and **@thomasloven**
* [**Simple Weather Card**](https://github.com/kalkih/simple-weather-card), by **@kalkih**
* [**Mini Media Player**](https://github.com/kalkih/mini-media-player), by **@kalkih**
* [**Mini Graph Card**](https://github.com/kalkih/mini-graph-card), also by **@kalkih**

## sun.sun
If you would like to use the light/dark automatic version, pleas make sure you have the sun.sun entity (should come preinstalled). If you don't have it please add the following to your `configuration.yaml`.

``` markdown
# Example configuration.yaml entry
sun:
```
# Themes
Themes can also be installed with [HACS](https://hacs.xyz), manual installation docs are [here](https://www.home-assistant.io/integrations/frontend/). **@JuanMTech** also made a great [video](https://www.youtube.com/watch?v=3Xpd4zB2eRM) explaining how to setup themes. 

### Light Themes
Any light theme consisting a **milky white background** should work.

**Please note the background cannot be pure white.**

### Dark Themes
Any dark theme consisting a **dark grey/black background** should work.

**Please note the background of the theme cannot be compeletly black.** 

The following themes are available in [**HACS**](https://hacs.xyz).

<p align="left">
  <img src="images/slate_theme_UI.png" alt="Slate theme UI" width="425">
  <img src="images/grey_night_theme_UI.png" alt="Grey Night theme UI" width="425">
  <br>
  <a href="https://github.com/seangreen2/slate_theme"><b>Slate theme</b></a> and <a href="https://github.com/home-assistant-community-themes/grey-night"><b>Grey Night theme</b></a>, by <b>@seangreen2</b> and <b>@ksya</b>
</p>
<p align="left">
  <img src="images/midnight_theme_UI.png" alt="Midnight theme UI" width="425">
  <img src="images/dark_mint_theme_UI.png" alt="Dark Mint theme UI" width="425">
  <br>
  <a href="https://github.com/home-assistant-community-themes/midnight"><b>Midnight theme</b></a> and <a href="https://github.com/home-assistant-community-themes/dark-mint"><b>Dark Mint theme</b></a>, by <b>@Marcel Hoffs</b> and <b>@lambtho</b>
</p>

### Comapct Header
You can either have the header match the background color or display it's own color.
</p>
<p align="left">
  <img src="images/dark_mint_w:color_header.png" alt="Dark mint theme with color header" width="425">
  <img src="images/dark_mint_no_color_header.png" alt="Dark mint theme without color header" width="425">
  <br>
  <a href="https://github.com/home-assistant-community-themes/dark-mint"><b>Dark Mint theme</b></a> header with and without color.
</p>

Click on the three dots on the top right, then go to `Configure UI` then `Raw config editor`. 

Add the following if you would like the header to match the background color:

``` markdown
# Example entry
custom_header:
  background: var(--primary-background-color);
  compact_mode: true
```
Only add the following if you would like the header to display it's own color:

``` markdown
# Example entry
custom_header:
  compact_mode: true
```

# Cards
Finally we've arrived on how to configure the cards themselves.

## Text Header Card
