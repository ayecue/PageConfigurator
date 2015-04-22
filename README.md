# PageConfigurator

> Compatible with Pimcore 3.x.x

## Description

This plugin allows you to create so called "PageConfiguration" objects and also save all properties of your view in one object.

To create a "PageConfiguration" object you just create a normal class in the classes panel. There you need to write this in the "parent" field: "Object_PageConfiguration". Add as much fields as you want to your created class. Now create a new object from this class. Add this object to the page properties of a page of your choice. Now add this code in the code of your page:
```
$config = new PageConfigurator_Config($this);
```

Now you got all informations in this variable. All PageConfiguration objects get automaticly merged to the config object. This means that you can access directly the properties of the different objects. Just remember that same field names can get overwritten.

You can use the "PageConfigurator" even without the "PageConfiguration" objects. It will automaticly get all properties from you view.

This plugin is useful if you want to write less page properties.

## How to install

* Create folder and drop files in "/plugins/PageConfigurator"
* Go to extension menu and click enable