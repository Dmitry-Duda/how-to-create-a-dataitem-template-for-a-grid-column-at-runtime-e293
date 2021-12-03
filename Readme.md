<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/128538626/13.1.5%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/E293)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->
# ASP.NET - Create a DataItemTemplate for an ASPxGridView column at Runtime

This example demonstrates how to create a [DataItemTemplate](https://docs.devexpress.com/AspNet/DevExpress.Web.GridViewDataColumn.DataItemTemplate) at runtime.

![ASPxGridView-DataItemTemplate](ASPxGridView-DataItemTemplate.png)

<!-- default file list -->
## Files to look at:

* [Default.aspx](./CS/HyperlinkColumn/Default.aspx) (VB: [Default.aspx](./VB/HyperlinkColumn/Default.aspx))
* [Default.aspx.cs](./CS/HyperlinkColumn/Default.aspx.cs) (VB: [Default.aspx.vb](./VB/HyperlinkColumn/Default.aspx.vb))
* [details.aspx](./CS/HyperlinkColumn/details.aspx) (VB: [details.aspx](./VB/HyperlinkColumn/details.aspx))
* [details.aspx.cs](./CS/HyperlinkColumn/details.aspx.cs) (VB: [details.aspx.vb](./VB/HyperlinkColumn/details.aspx.vb))
<!-- default file list end -->

## Implementation Details

Use a column's [DataItemTemplate](https://docs.devexpress.com/AspNet/DevExpress.Web.GridViewDataColumn.DataItemTemplate) property to specify a template for the column's cells. This property gets an object with an [ITemplate](https://docs.microsoft.com/en-us/dotnet/api/system.web.ui.itemplate) standard interface. To create this object, declare a custom class and implement the [ITemplate](https://docs.microsoft.com/en-us/dotnet/api/system.web.ui.itemplate) interface in it.

In the class's [InstantiateIn](https://docs.microsoft.com/ru-ru/dotnet/api/system.web.ui.itemplate.instantiatein) method, create controls and add them to the [control collection](https://docs.microsoft.com/ru-ru/dotnet/api/system.windows.forms.control.controls) of the container passed to this method as the **Control** parameter. A container type is different for each template type. For the [DataItemTemplate](https://docs.devexpress.com/AspNet/DevExpress.Web.GridViewDataColumn.DataItemTemplate), the parent container is the [GridViewDataItemTemplateContainer](https://docs.devexpress.com/AspNet/DevExpress.Web.GridViewDataItemTemplateContainer). Use the container's properties to obtain a row's information. For example, use the **KeyValue** property to get a row key (`container.KeyValue`).

To specify a template for a column's cells, create an instance of a template class and assign it to the column's [DataItemTemplate](https://docs.devexpress.com/AspNet/DevExpress.Web.GridViewDataColumn.DataItemTemplate) property.

## Documentation

[How to: Create Edit Form Template at Runtime](https://docs.devexpress.com/AspNet/4341/components/grid-view/examples/how-to-create-edit-form-template-at-runtime)

## More Examples

* [How to: Create Edit Form Templates Dynamically](https://github.com/DevExpress-Examples/how-to-create-edit-form-templates-dynamically-e986)

* [How to: Implement a Dynamical DataItem Template for Several Same-type Columns](https://github.com/DevExpress-Examples/how-to-implement-a-dynamical-dataitem-template-for-several-same-type-columns-e4020)