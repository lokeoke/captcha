Readme file for the CAPTCHA module for Drupal
---------------------------------------------

[![Build Status](https://travis-ci.org/M1r1k/captcha.svg)](https://travis-ci.org/M1r1k/captcha)

captcha.module is the basic CAPTCHA module, offering general CAPTCHA
administration and a simple math challenge.

Submodule image_captcha.module offers an image based challenge.

Installation:
  Installation is like with all normal drupal modules:
  extract the 'captcha' folder from the tar ball to the
  modules directory from your website (typically sites/all/modules).

Dependencies:
  The basic CAPTCHA module requires
  PHP Captcha library Gregwar/Captcha (https://github.com/Gregwar/Captcha).
  To install it add contains of captcha/composer.json to
  your composer.json file or run:
    composer require gregwar/captcha:1.0.11

Conflicts/known issues:
  CAPTCHA and page caching do not work together currently.
  However, the CAPTCHA module does support the Drupal core page
  caching mechanism: it just disables the caching of the pages
  where it has to put its challenges.
  If you use other caching mechanisms, it is possible that CAPTCHA's
  won't work, and you get error messages like 'CAPTCHA validation
  error: unknown CAPTCHA session ID'.

Configuration:
  The configuration page is at admin/config/people/captcha,
  where you can configure the CAPTCHA module
  and enable challenges for the desired forms.
  You can also tweak the image CAPTCHA to your liking.
