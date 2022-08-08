# Markup CKEditor (for Form Builder)

A module for ProcessWire CMS/CMF. An inputfield for displaying markup editable via CKEditor.

The module is intended for use with the Form Builder module. Allows blocks of static text to be included within a form, which can be edited in the form settings using CKEditor.

## Screenshots

![2017-07-07_163113](https://user-images.githubusercontent.com/1538852/27943285-e7bff30a-6331-11e7-8f87-d43f4b9eefb0.png)

![2017-07-07_163135](https://user-images.githubusercontent.com/1538852/27943286-e7c9f9e0-6331-11e7-8e5c-d2fbe58dc4b1.png)

## Usage

[Install](http://modules.processwire.com/install-uninstall/) the Markup CKEditor module.

In the Form Builder module settings, add "MarkupCKEditor" to "Inputfield types to use with FormBuilder".

In your form settings, add a new field of type "Markup CKEditor". Enter the text you want to show in this field using "Markup Text" on the "Details" tab.

## Configuration

In the module config you can set items for the CKEditor toolbar that will apply to all Markup CKEditor fields.

If you want to insert images in your markup field then add "Image" to the toolbar items to enable the standard CKEditor image plugin. The ProcessWire image plugin is not usable because in a FormBuilder form there is no page to store images in.

## Advanced

There is a `InputfieldMarkupCKEditor::ckeReady` hookable method for users who want to do advanced customisation of the CKEditor inputfield.

It receives three arguments:
* The InputfieldCKEditor object
* The form as a FormBuilderForm object
* The field as a FormBuilderField object

### Example

```php
$wire->addHookAfter('InputfieldMarkupCKEditor::ckeReady', function(HookEvent $event) {
    /** @var InputfieldCKEditor $cke */
    $cke = $event->arguments(0);
    /** @var FormBuilderForm */
    $form = $event->arguments(1);
    /** @var FormBuilderField $field */
    $field = $event->arguments(2);

    if($form->name === 'test_form' && $field->name === 'my_cke_markup_field') {
        $cke->contentsCss = '/site/templates/MarkupCKEditor/contents.css';
        $cke->stylesSet = 'ckstyles:/site/templates/MarkupCKEditor/ckstyles.js';
    }
});
```
