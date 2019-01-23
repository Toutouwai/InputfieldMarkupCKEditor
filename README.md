# Markup CKEditor (for Form Builder)

A module for ProcessWire CMS/CMF. An inputfield for displaying markup editable via CKEditor.

The module is intended for use with the Form Builder module. Allows blocks of static text to be included within a form, which can be edited in the form settings using CKEditor.

## Usage

[Install](http://modules.processwire.com/install-uninstall/) the Markup CKEditor module.

In the Form Builder module settings, add "MarkupCKEditor" to "Inputfield types to use with FormBuilder".

In your form settings, add a new field of type "Markup CKEditor". Enter the text you want to show in this field using "Markup Text" on the "Details" tab.

There is an option to hide the inputfield label in the rendered form.
*Note: this option is not currently working in the "Basic" framework due to an [issue with FormBuilder v0.3.4](https://processwire.com/talk/topic/19728-checkbox-label-not-skipped-for-basic-output-framework/).*

## Screenshots

![2017-07-07_163113](https://user-images.githubusercontent.com/1538852/27943285-e7bff30a-6331-11e7-8f87-d43f4b9eefb0.png)

![2017-07-07_163135](https://user-images.githubusercontent.com/1538852/27943286-e7c9f9e0-6331-11e7-8e5c-d2fbe58dc4b1.png)

## License

Released under Mozilla Public License v2. See file LICENSE for details.
