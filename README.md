Password Strength Meter
=======================

Give feedback to users when are typing a password

![Strength Meter](https://f.cloud.github.com/assets/49499/2447754/9d3cc38c-ae9c-11e3-947e-dce7c32da441.png)

## Dependencies
1. [jQuery](http://jquery.com/)

## Instalation
Download `password-strength-meter.js` file and put on your HTML after `jQuery`
``` html
<script src="javascript/password-strength-meter.js"></script>
```
## Use
Initialize the plugin in the field(s) you want to check password streng
``` javascript
  // This is the markup for password strength meter (Visual feedback)
  var $strength_meter = $('.js-strength-meter');

  // Plugin initialization
  $('.js-password-input').passwordStrengthMeter({
    strength_meter: $strength_meter
  , options: {
    app_requirements: app_requirements
  }
  });

  // Check password strength
   $('.js-password-input').passwordStrengthMeter('check');

  // Check password is Valid
   $('.js-password-input').passwordStrengthMeter('checkIsValid');
   $('.js-password-input').data('is_valid');
```

## Default Strength Meter HTLM markup
You can use yours. And your custom CSS
``` html
  <div class="js-strength-meter strength-meter">
    <div class="strength-meter-message">
      <span class="js-strength-meter-label strength-meter-label">Strength </span>
      <span class="js-strength-meter-copy strength-meter-copy"></span>
    </div>
    <div class="strength-meter-bar">
      <div class="strength-meter-progress"></div>
    </div>
  </div>
```

## Options
This are the options you can configure

#### strength_meter_label_element
Type: `String`
Default: `.js-strength-meter-label`

This is a DIV that must be inside Strength meter HTML

#### strength_meter_copy_element
Type: `String`
Default: `.js-strength-meter-copy`

This is a DIV that must be inside Strength meter HTML. This is were the plugin put strength messages.

#### min_length
Type: `Integer`
Default: 8

This is the min length password must have.

#### ideal_length
Type: `Integer`
Default: 12

#### copy_too_short
Type: `String`
Default: `Too short`

Message when password is too short

#### copy_must_not_contain_spaces
Type: `String`
Default: `Can't contain spaces`

#### copy_must_contain_number_and_letters
Type: `String`
Default: `Must contain numbers and letters`

Message when password doesn't have numbers && letters

#### copy_app_requirements
Type: `String`
Default: `This password doesn\'t pass app requirements`

Message when password doesn't pass your requirements

#### copy_weak
Type: `String`
Default: `Weak`

#### copy_fair
Type: `String`
Default: `Fair`

#### copy_good
Type: `String`
Default: `Good`

#### copy_strong
Type: `String`
Default: `Strong`


*****

## The MIT License (MIT)

Copyright (c) 2014 Andrés Gutiérrez

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
