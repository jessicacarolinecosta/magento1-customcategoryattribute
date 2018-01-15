# magento1-customcategoryattribute
Custom category attribute for Magento 1

## Installation
Put the ```app``` directory into your Magento root folder

## Change the attribute name/type
Go to ```app/code/community/Tek/CustomCatAttribute/sql/add_category_attribute/mysql4-upgrade-0.0.1-0.0.2.php``` and change the information about the new attribute.

```custom_attribute``` is the ID of attribute 

```type``` is the type for input (text, textarea, etc)

```label``` is the title of input in frontend

## Get the attribute value in front-end
Mage::getResourceModel('catalog/category')->getAttributeRawValue($categoryObject->getId(), "custom_attribute", Mage::app()->getStore()->getId());
