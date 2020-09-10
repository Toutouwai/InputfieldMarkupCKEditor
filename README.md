# Markup CKEditor (for Form Builder)

A module for ProcessWire CMS/CMF. An inputfield for displaying markup editable via CKEditor.

The module is intended for use with the Form Builder module. Allows blocks of static text to be included within a form, which can be edited in the form settings using CKEditor.

## Usage

[Install](http://modules.processwire.com/install-uninstall/) the Markup CKEditor module.

In the Form Builder module settings, add "MarkupCKEditor" to "Inputfield types to use with FormBuilder".

In your form settings, add a new field of type "Markup CKEditor". Enter the text you want to show in this field using "Markup Text" on the "Details" tab.

## Configuration

In the module config you can set items for the CKEditor toolbar that will apply to all Markup CKEditor fields.

If you want to insert images in your markup field then add "Image" to the toolbar items to enable the standard CKEditor image plugin. The ProcessWire image plugin is not usable because in a FormBuilder form there is no page to store images in. Don't double-click on images in CKEditor or else PW will throw an exception because it expects CKEditor to be associated with a page.

## Screenshots

![2017-07-07_163113](https://user-images.githubusercontent.com/1538852/27943285-e7bff30a-6331-11e7-8f87-d43f4b9eefb0.png)

![2017-07-07_163135](https://user-images.githubusercontent.com/1538852/27943286-e7c9f9e0-6331-11e7-8e5c-d2fbe58dc4b1.png)

## License

Released under Mozilla Public License v2. See file LICENSE for details.
