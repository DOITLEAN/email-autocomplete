jquery.email-autocomplete.js
=========

[![Build Status](https://travis-ci.org/10w042/email-autocomplete.svg?branch=0.1.0)](https://travis-ci.org/10w042/email-autocomplete)

A jQuery plugin that suggests and autocompletes the domain whenever your users type in an email address field.

What does it do?
----------------

When your user types in "user@gm", the plugin will suggest for e.g. "user@gmail.com", based on the first result from a list of predefined email domains.

![diagram](https://raw.github.com/yzlow/email-autocomplete/master/doc_assets/example.png)

Press the tab-key, or simply click on the suggestion to automatically fill in the rest of the domain. (or tap on the suggestion for mobile users.)

You can also use the right arrow key. (new in 0.1.0)

See a live demo [here](http://yzlow.github.io/email-autocomplete/demo/).

Installation
------------

To use, download the minified library into your javascripts directory. jquery.email-autocomplete.js is also available unminimized.

Usage (jQuery)
-----------------

Include jQuery and Email Autocomplete into your HTML.

```html
<script src="jquery.min.js"></script>
<script src="jquery.email-autocomplete.min.js"></script>
```

You should have a text field.

```html
<input id="email" name="email" type="email" />
```

Now, attach the plugin to the text field.

```html
<script>
$("#email").emailautocomplete({
  suggClass: "custom-classname", //default: "eac-sugg". your custom classname (optional)
  domains: ["example.com"] //additional domains (optional)
});
</script>
```

Styling
-----------------

Use the following CSS to style the suggestion text color

```css
.eac-sugg{
  color:#ccc;
}
```

Domains
-------

Email Autocomplete has its own default domains if the `domains` option isn't provided.

* gmail.com
* googlemail.com
* yahoo.com
* yahoo.co.uk
* hotmail.com
* hotmail.co.uk
* live.com
* msn.com
* comcast.net
* sbcglobal.net
* verizon.net
* facebook.com
* outlook.com
* att.net
* gmx.com
* icloud.com
* me.com
* mac.com
* aol.com

Author
-------

- Low Yong Zhen, [@lowyongzhen](https://twitter.com/lowyongzhen).

License
-------

Copyright (c) 2014

Licensed under the MIT License.


Known Issues:
----------------

- On android stock browser, if "Settings > Accessibility > Scale text up and down" value is not at 100%, text width is unabled to be retrieved correctly.