---
layout: post
title: Migrate from Xamarin SfDataGrid to .NET MAUI SfDataGrid | Syncfusion 
description: Learn here all about Migrating from Syncfusion Xamarin SfDataGrid to Syncfusion .NET MAUI SfDataGrid control and more.
platform: MAUI
control: SfDataGrid
documentation: ug
--- 

# Migrate from Xamarin.Forms SfDataGrid to .NET MAUI SfDataGrid

To make migration from [Xamarin SfDataGrid](https://www.syncfusion.com/xamarin-ui-controls/xamarin-datagrid) to [.NET MAUI SfDataGrid](https://www.syncfusion.com/maui-controls/maui-datagrid) easier, we kept most of the APIs from Xamarin SfDataGrid in MAUI SfDataGrid. However, to maintain the consistency of API naming in MAUI SfDataGrid, we renamed some of the APIs. The APIs that have been changed in MAUI SfDataGrid from Xamarin SfDataGrid are detailed as follows.

## Namespaces 

<table>
<tr>
<th>Xamarin SfDataGrid</th>
<th>.NET MAUI SfDataGrid</th></tr>
<tr>
<td>Syncfusion.SfDataGrid.XForms</td>
<td>Syncfusion.Maui.DataGrid</td></tr>
<tr>
<td>Syncfusion.Data</td>
<td>Syncfusion.Maui.Data</td></tr>
</table>

## Enums

<table>
<tr>
<th>Xamarin SfDataGrid</th>
<th>.NET MAUI SfDataGrid</th>
<th>Description</th></tr>
<tr>
<td>{{'[ColumnSizer](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.ColumnSizer.html)'| markdownify }}</td>
<td>{{'[ColumnWidthMode](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.ColumnWidthMode.html)'| markdownify }}</td>
<td>Defines constants that specify how the columns in a {{'[SfDataGrid](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html)'| markdownify }} are sized.</td></tr>
<tr>
<td>{{'[SortTapAction](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.SortTapAction.html)'| markdownify }}</td>
<td>{{'[DataGridSortingGestureType](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridSortingGestureType.html)'| markdownify }}</td>
<td>Defines the constants that specifies how the sorting is applied.</td>
</tr>
</table>

## Properties

<table>
<tr>
<th>Xamarin SfDataGrid</th>
<th>.NET MAUI SfDataGrid</th>
<th>Description</th></tr>
<tr>
<td>{{'[AutoGenerateColumns](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.SfDataGrid.html#Syncfusion_SfDataGrid_XForms_SfDataGrid_AutoGenerateColumns)'| markdownify }}</td>
<td>{{'[AutoGenerateColumnsMode.None](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.ColumnWidthMode.html)'| markdownify }}</td>
<td>Defines constants that specify how the columns in a {{'[SfDataGrid](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html)'| markdownify }} are sized.</td></tr>
<tr>
<td>{{'[AllowSorting](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.SfDataGrid.html#Syncfusion_SfDataGrid_XForms_SfDataGrid_AllowSorting)'| markdownify }}</td>
<td>{{'[SortingMode.Single](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridSortingMode.html#Syncfusion_Maui_DataGrid_DataGridSortingMode_Single)'| markdownify }}</td>
<td>Specifies that the single column alone can be sorted at a time.</td>
</tr>
<tr>
<td>{{'[AllowMultiSorting](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.SfDataGrid.html#Syncfusion_SfDataGrid_XForms_SfDataGrid_AllowMultiSorting)'| markdownify }}</td>
<td>{{'[SortingMode.Multiple](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridSortingMode.html#Syncfusion_Maui_DataGrid_DataGridSortingMode_Multiple)'| markdownify }}</td>
<td>Specifies that the multiple columns can be sorted.</td>
</tr>
<tr>
<td>{{'[SortTapAction](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.SortTapAction.html)'| markdownify }}</td>
<td>{{'[SortingGestureType](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html#Syncfusion_Maui_DataGrid_SfDataGrid_SortingGestureType)'| markdownify }}</td>
<td>Defines the constants that specifies how the sorting is applied.</td>
</tr>
<tr>
<td>{{'[IsHidden](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridColumn.html#Syncfusion_SfDataGrid_XForms_GridColumn_IsHidden)'| markdownify }}</td>
<td>{{'[Visible](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridColumn.html#Syncfusion_Maui_DataGrid_DataGridColumn_Visible)'| markdownify }}</td>
<td>Gets or sets a value indicating whether a column should be visible.</td>
</tr>
<tr>
<td>{{'[SelectedItem](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.SfDataGrid.html#Syncfusion_SfDataGrid_XForms_SfDataGrid_SelectedItem)'| markdownify }}</td>
<td>{{'[SelectedRow](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html#Syncfusion_Maui_DataGrid_SfDataGrid_SelectedRow)'| markdownify }}</td>
<td>Gets or sets a row which is currently selected.</td>
</tr>
<tr>
<td>{{'[SelectedItems](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.SfDataGrid.html#Syncfusion_SfDataGrid_XForms_SfDataGrid_SelectedItems)'| markdownify }}</td>
<td>{{'[SelectedRows](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html#Syncfusion_Maui_DataGrid_SfDataGrid_SelectedRows)'| markdownify }}</td>
<td>Gets or sets the collection of rows which are all selected.</td>
</tr>
<tr>
<td>{{'[CurrentItem](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.SfDataGrid.html#Syncfusion_SfDataGrid_XForms_SfDataGrid_CurrentItem)'| markdownify }}</td>
<td>{{'[CurrentRow](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html#Syncfusion_Maui_DataGrid_SfDataGrid_CurrentRow)'| markdownify }}</td>
<td>Gets or sets a row which is currently navigated.</td>
</tr>
<tr>
<td>{{'[HeaderBackgroundColor](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.DataGridStyle.html#Syncfusion_SfDataGrid_XForms_DataGridStyle_HeaderBackgroundColor)'| markdownify }}</td>
<td>{{'[HeaderRowBackground](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStyle.html#Syncfusion_Maui_DataGrid_DataGridStyle_HeaderRowBackground)'| markdownify }}</td>
<td>Gets or sets the background for the header row.</td>
</tr>
<tr>
<td>{{'[RowBackgroundColor](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.DataGridStyle.html#Syncfusion_SfDataGrid_XForms_DataGridStyle_RowBackgroundColor)'| markdownify }}</td>
<td>{{'[RowBackground](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStyle.html#Syncfusion_Maui_DataGrid_DataGridStyle_RowBackground)'| markdownify }}</td>
<td>Gets or sets the background of the data rows.</td>
</tr>
<tr>
<td>{{'[RowForegroundColor](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.DataGridStyle.html#Syncfusion_SfDataGrid_XForms_DataGridStyle_RowForegroundColor)'| markdownify }}</td>
<td>{{'[RowTextColor](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStyle.html#Syncfusion_Maui_DataGrid_DataGridStyle_RowTextColor)'| markdownify }}</td>
<td>Gets or sets the text color of the data row.</td>
</tr>
<tr>
<td>{{'[HeaderForegroundColor](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.DataGridStyle.html#Syncfusion_SfDataGrid_XForms_DataGridStyle_HeaderForegroundColor)'| markdownify }}</td>
<td>{{'[HeaderRowTextColor](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStyle.html#Syncfusion_Maui_DataGrid_DataGridStyle_HeaderRowTextColor)'| markdownify }}</td>
<td>Gets or sets the text color of the header row.</td>
</tr>
<tr>
<td>{{'[GridCellBorderColor](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.DataGridStyle.html#Syncfusion_SfDataGrid_XForms_DataGridStyle_GridCellBorderColor)'| markdownify }}</td>
<td>{{'[GridLineColor](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStyle.html#Syncfusion_Maui_DataGrid_DataGridStyle_GridLineColor)'| markdownify }}</td>
<td>Gets or sets the color for the grid lines.</td>
</tr>
<tr>
<td>{{'[GridCellBorderWidth](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.DataGridStyle.html#Syncfusion_SfDataGrid_XForms_DataGridStyle_GridCellBorderWidth)'| markdownify }}</td>
<td>{{'[GridLineStrokeThickness](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStyle.html#Syncfusion_Maui_DataGrid_DataGridStyle_GridLineStrokeThickness)'| markdownify }}</td>
<td>Gets or sets the stroke thickness of the grid lines.</td>
</tr>
<tr>
<td>{{'[SelectionBackgroundColor](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.DataGridStyle.html#Syncfusion_SfDataGrid_XForms_DataGridStyle_SelectionBackgroundColor)'| markdownify }}</td>
<td>{{'[SelectionBackground](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStyle.html#Syncfusion_Maui_DataGrid_DataGridStyle_SelectionBackground)'| markdownify }}</td>
<td>Gets or sets the background of the selected rows.</td>
</tr>
<tr>
<td>{{'[SelectionForegroundColor](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.DataGridStyle.html#Syncfusion_SfDataGrid_XForms_DataGridStyle_SelectionForegroundColor)'| markdownify }}</td>
<td>{{'[SelectedRowTextColor](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStyle.html#Syncfusion_Maui_DataGrid_DataGridStyle_SelectedRowTextColor)'| markdownify }}</td>
<td>Gets or sets the text color of the selected rows.</td>
</tr>
<tr>
<td>{{'[ColumnSizer](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html#Syncfusion_Maui_DataGrid_SfDataGrid_ColumnSizer)'| markdownify }}</td>
<td>{{'[ColumnWidthMode](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html#Syncfusion_Maui_DataGrid_SfDataGrid_ColumnWidthMode)'| markdownify }}</td>
<td>Gets or sets the value that indicates how all the columns widths are determined.</td>
</tr>
<tr>
<td>{{'[FontAttribute](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridColumn.html#Syncfusion_SfDataGrid_XForms_GridColumn_FontAttribute)'| markdownify }}</td>
<td>{{'[DataGridCell.FontAttributes](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridCell.html#Syncfusion_Maui_DataGrid_DataGridCell_FontAttributes)'| markdownify }}</td>
<td>Gets or sets the font attributes.</td>
</tr>
<tr>
<td>{{'[HeaderFont](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridColumn.html#Syncfusion_SfDataGrid_XForms_GridColumn_HeaderFont)'| markdownify }}</td>
<td>{{'[DataGridHeaderCell.FontFamily](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridCell.html#Syncfusion_Maui_DataGrid_DataGridCell_FontFamily)'| markdownify }}</td>
<td>Gets or sets the font family.</td>
</tr>
<tr>
<td>{{'[HeaderFontAttribute](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridColumn.html#Syncfusion_SfDataGrid_XForms_GridColumn_HeaderFontAttribute)'| markdownify }}</td>
<td>{{'[DataGridHeaderCell.FontAttributes](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridCell.html#Syncfusion_Maui_DataGrid_DataGridCell_FontAttributes)'| markdownify }}</td>
<td>Gets or sets the font attributes.</td>
</tr>
<tr>
<td>{{'[RecordFont](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridColumn.html#Syncfusion_SfDataGrid_XForms_GridColumn_RecordFont)'| markdownify }}</td>
<td>{{'[DataGridCell.FontFamily](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridCell.html#Syncfusion_Maui_DataGrid_DataGridCell_FontFamily)'| markdownify }}</td>
<td>Gets or sets the font family.</td>
</tr>
<tr>
<td>{{'[FrozenRowsCount](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.SfDataGrid.html#Syncfusion_SfDataGrid_XForms_SfDataGrid_FrozenRowsCount)'| markdownify }}</td>
<td>{{'[FrozenRowCount(https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html#Syncfusion_Maui_DataGrid_SfDataGrid_FrozenRowCount)'| markdownify }}</td>
<td>The number of non-scrolling rows at the top of SfDataGrid.</td>
</tr>
<tr>
<td>{{'[FrozenColumnsCount](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.SfDataGrid.html#Syncfusion_SfDataGrid_XForms_SfDataGrid_FrozenColumnsCount)'| markdownify }}</td>
<td>{{'[FrozenColumnCount(https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html#Syncfusion_Maui_DataGrid_SfDataGrid_FrozenColumnCount)'| markdownify }}</td>
<td>The number of non-scrolling columns at the left side of SfDataGrid.</td>
</tr>
</table>

## Events

<table>
<tr>
<th>Xamarin SfDataGrid</th>
<th>.NET MAUI SfDataGrid</th>
<th>Description</th></tr>
<tr>
<td>{{'[GridTapped](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.SfDataGrid.html#Syncfusion_SfDataGrid_XForms_SfDataGrid_GridTapped)'| markdownify }}</td>
<td>{{'[CellTapped](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html#Syncfusion_Maui_DataGrid_SfDataGrid_CellTapped)'| markdownify }}</td>
<td>Occurs when the cell is tapped.</td>
</tr>
<tr>
<td>{{'[GridDoubleTapped](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.SfDataGrid.html#Syncfusion_SfDataGrid_XForms_SfDataGrid_GridDoubleTapped)'| markdownify }}</td>
<td>{{'[CellDoubleTapped](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html#Syncfusion_Maui_DataGrid_SfDataGrid_CellDoubleTapped)'| markdownify }}</td>
<td>Occurs when the cell is tapped twice.</td>
</tr>
<tr>
<td>{{'[GridLongPressed](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.SfDataGrid.html#Syncfusion_SfDataGrid_XForms_SfDataGrid_GridLongPressed)'| markdownify }}</td>
<td>{{'[CellLongPress](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html#Syncfusion_Maui_DataGrid_SfDataGrid_CellLongPress)'| markdownify }}</td>
<td>Occurs when the cell is long pressed for particular period.</td>
</tr>
<tr>
<td>{{'[QueryRowStyle](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.SfDataGrid.html#Syncfusion_SfDataGrid_XForms_SfDataGrid_QueryRowStyle)'| markdownify }}</td>
<td>-</td>
<td>This event is not available in MAUI DataGrid. You can write the custom style for {{'[DataGridRow](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridRow.html)'| markdownify }} TargetType.<br>
By writing the converter, you can achieve the requirement conditionally. Refer {{'[Conditional Styling](https://help.syncfusion.com/maui/datagrid/conditional-styling)'| markdownify }} UG documentation for more information.
</td>
</tr>
<tr>
<td>{{'[QueryCellStyle](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.SfDataGrid.html#Syncfusion_SfDataGrid_XForms_SfDataGrid_QueryCellStyle)'| markdownify }}</td>
<td>-</td>
<td>This event is not available in MAUI DataGrid. You can write the custom style for {{'[DataGridCell](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridCell.html)'| markdownify }} TargetType.<br> By writing the converter, you can achieve the requirement conditionally. Refer {{'[Conditional Styling](https://help.syncfusion.com/maui/datagrid/conditional-styling)'| markdownify }} UG documentation for more information.
</td>
</tr>
</table>

## Methods

<table>
<tr>
<th>Xamarin SfDataGrid</th>
<th>.NET MAUI SfDataGrid</th>
<th>Description</th></tr>
<tr>
<td>{{'[GetRowHeight](https://help.syncfusion.com/xamarin/datagrid/row-height-customization#auto-fit-the-grid-rows-based-on-content)'| markdownify }}</td>
<td>{{'[GetIntrinsicRowHeight](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridQueryRowHeightEventArgs.html#Syncfusion_Maui_DataGrid_DataGridQueryRowHeightEventArgs_GetIntrinsicRowHeight_System_Int32_System_Boolean_System_Collections_Generic_List_System_String__)'| markdownify }}</td>
<td>Gets the row height to fit that row based on the content.<br>
We have passed the optional parameters such as {{'[canIncludeHiddenColumns](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridRowSizingOptions.html#Syncfusion_SfDataGrid_XForms_GridRowSizingOptions_CanIncludeHiddenColumns)'| markdownify }} and {{'[excludedColumns](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridRowSizingOptions.html#Syncfusion_SfDataGrid_XForms_GridRowSizingOptions_ExcludeColumns)'| markdownify }} where as we have not provided the {{'[GridRowSizingOptions](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridRowSizingOptions.html)'| markdownify }} class as parameters.
</td>
</tr>
</table>

## Classes

<table>
<tr>
<th>Xamarin SfDataGrid</th>
<th>.NET MAUI SfDataGrid</th>
<th>Description</th></tr>
<tr>
<td>{{'[GridColumn](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridColumn.html)'| markdownify }}</td>
<td>{{'[DataGridColumn](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridColumn.html)'| markdownify }}</td>
<td>Represents the base class for the different column types of the {{'[SfDataGrid](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html)'| markdownify }} control.</td>
</tr>
<tr>
<td>{{'[GridNumericColumn](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridNumericColumn.html)'| markdownify }}</td>
<td>{{'[DataGridNumericColumn](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridNumericColumn.html)'| markdownify }}</td>
<td>A column which is used to handle the numeric values.</td>
</tr>
<tr>
<td>{{'[GridDateTimeColumn](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridDateTimeColumn.html)'| markdownify }}</td>
<td>{{'[DataGridDateColumn](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridDateColumn.html)'| markdownify }}</td>
<td>A column which is used to show any type of System.DateTime.</td>
</tr>
<tr>
<td>{{'[GridImageColumn](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridImageColumn.html)'| markdownify }}</td>
<td>{{'[DataGridImageColumn](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridImageColumn.html)'| markdownify }}</td>
<td>A column which is used to show any type of ImageSource.</td>
</tr>
<tr>
<td>{{'[GridTemplateColumn](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridTemplateColumn.html)'| markdownify }}</td>
<td>{{'[DataGridTemplateColumn](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridTemplateColumn.html)'| markdownify }}</td>
<td>A column which is used to show any type of template.</td>
</tr>
<tr>
<td>{{'[GridTextColumn](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridTextColumn.html)'| markdownify }}</td>
<td>{{'[DataGridTextColumn](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridTextColumn.html)'| markdownify }}</td>
<td>Represents a {{'[SfDataGrid](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html)'| markdownify }} column that hosts textual Content in its cells.</td>
</tr>
<tr>
<td>{{'[GridCell](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridCell.html)'| markdownify }}</td>
<td>{{'[DataGridCell](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridCell.html)'| markdownify }}</td>
<td>Represents a record cell in a {{'[SfDataGrid](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html)'| markdownify }} control.</td>
</tr>
<tr>
<td>{{'[VirtualizingCellsControl](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.VirtualizingCellsControl.html)'| markdownify }}</td>
<td>{{'[DataGridRow](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridRow.html)'| markdownify }}</td>
<td>Represents a record row in a {{'[SfDataGrid](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html)'| markdownify }} control.</td>
</tr>

<tr>
<td>{{'[GridHeaderCellControl](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridHeaderCellControl.html)'| markdownify }}</td>
<td>{{'[DataGridHeaderCell](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridHeaderCell.html)'| markdownify }}</td>
<td>Represents a header cell in a {{'[SfDataGrid](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html)'| markdownify }} control</td>
</tr>

<tr>
<td>{{'[GridColumnSizer](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridColumnSizer.html)'| markdownify }}</td>
<td>{{'[DataGridColumnSizer](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridColumnSizer.html)'| markdownify }}</td>
<td>Represents a class that handles the sizing for all the {{'[columns](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html#Syncfusion_Maui_DataGrid_SfDataGrid_Columns)'| markdownify }} in the Columns collection in a {{'[SfDataGrid](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html)'| markdownify }} control.</td>
</tr>

<tr>
<td>{{'[GridSummaryRow](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridSummaryRow.html)'| markdownify }}</td>
<td>{{'[DataGridSummaryRow](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridSummaryRow.html)'| markdownify }}</td>
<td> Represents a class that defines the summary information of summary row.</td>
</tr>

<tr>
<td>{{'[GridTableSummaryRow](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridTableSummaryRow.html)'| markdownify }}</td>
<td>{{'[DataGridTableSummaryRow](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridTableSummaryRow.html)'| markdownify }}</td>
<td> Represents a class that defines summary information of table summary row in {{'[SfDataGrid](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html)'| markdownify }}.</td>
</tr>

<tr>
<td>{{'[Position](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.Position.html)'| markdownify }}</td>
<td>{{'[SummaryRowPosition](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SummaryRowPosition.html)'| markdownify }}</td>
<td> Defines the constants that specify whether the table summary row is positioned at the top or bottom of the {{'[SfDataGrid](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html)'| markdownify }} control.</td>
</tr>

<tr>
<td>{{'[TableSummaryRowControl](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.TableSummaryRowControl.html)'| markdownify }}</td>
<td>{{'[DataGridTableSummaryRowView](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridTableSummaryRowView.html)'| markdownify }}</td>
<td> Represents a table summary row in a {{'[SfDataGrid](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html)'| markdownify }} control.</td>
</tr>

<tr>
<td>{{'[StackedColumn](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.StackedColumn.html)'| markdownify }}</td>
<td>{{'[DataGridStackedColumn](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStackedColumn.html)'| markdownify }}</td>
<td>Represents a column that is stacked across the specified child columns in it.</td>
</tr>

<tr>
<td>{{'[StackedHeaderCellControl](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.StackedHeaderCellControl.html)'| markdownify }}</td>
<td>{{'[DataGridStackedHeaderCell](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStackedHeaderCell.html)'| markdownify }}</td>
<td>Represents a {{'[DataGridStackedCell](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStackedHeaderCell.html)'| markdownify }} in a {{'[SfDataGrid](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html)'| markdownify }} control.</td>
</tr>

<tr>
<td>{{'[GridStackedHeaderCellRenderer](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridStackedHeaderCellRenderer.html)'| markdownify }}</td>
<td>{{'[DataGridStackedHeaderCellRenderer](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStackedHeaderCellRenderer.html)'| markdownify }}</td>
<td>A class for cell renderer that displays{{'[DataGridStackedHeaderRow](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStackedHeaderRow.html)'| markdownify }} in a {{'[DataGridStackedCell](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStackedHeaderCell.html)'| markdownify }}.</td>
</tr>

<tr>
<td>{{'[StackedHeaderRow](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.StackedHeaderRow.html)'| markdownify }}</td>
<td>{{'[DataGridStackedHeaderRow](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStackedHeaderRow.html)'| markdownify }}</td>
<td>The {{'[DataGridStackedHeaderRow](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStackedHeaderRow.html)'| markdownify }} contains the collection of {{'[DataGridStackedColumn](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStackedColumn.html)'| markdownify }} to be grouped under a particular category.}}.</td>
</tr>

<tr>
<td>{{'[GridStackedHeaderCellControl](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfDataGrid.XForms.GridStackedHeaderCellControl.html)'| markdownify }}</td>
<td>{{'[DataGridStackedHeaderRowView](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStackedHeaderRowView.html)'| markdownify }}</td>
<td>Represents a {{'[DataGridStackedHeaderRow](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.DataGridStackedHeaderRow.html)'| markdownify }} as a control in a {{'[SfDataGrid](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.DataGrid.SfDataGrid.html)'| markdownify }} control.</td>
</tr>

</table>

## Known issues 

* [Android] Horizontal scrolling performance is not smooth in the Debug solution configuration when compared to Xamarin.Forms SfDataGrid. However, the scrolling performance is smooth when the solution configuration is Release.

## Upcoming Features   

*   Paging
*	Right to left
*	Accessibility
*	Custom selection
*	Grouping
*	Summaries (Group and Caption)
*	Editing
*	ComboBox column
*	Load more
*	Swiping
*	Exporting to Excel and Pdf
*	Unbound row
*	Unbound column
*	Pull To Refresh
*	Column drag and drop
*	Row drag and drop
