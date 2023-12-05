<!-- default badges list -->
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T830455)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->

# WPF Tree List - Control Visibility of Expand Buttons when Sub-level Children are not Fetched

This example demonstrates how to specify whether a child node has children (and should display the expand button) when the [TreeListView](https://docs.devexpress.com/WPF/9566/controls-and-libraries/data-grid/views/treelist-view) does not fetch sub-level nodes.

The `TreeListView` in hierarchical binding mode fetches child nodes of sub-level nodes when you expand their parent node. Such behavior is designed to determine whether to display expand buttons. You can set the [TreeListView.FetchSublevelChildrenOnExpand](https://docs.devexpress.com/WPF/DevExpress.Xpf.Grid.TreeListView.FetchSublevelChildrenOnExpand) property to `false` to keep sub-level children unfetched. In this case, all child nodes display expand buttons (even if they do not have children). The expand button hides when you expand a node that does not contain child nodes:

![image](https://docs.devexpress.com/WPF/images/fetch-sub-level-children.gif)

Follow the steps below to prevent this behavior:

1. Your data source objects should contain a field that specifies whether an item has children.
2. Assign the field name to the [TreeListView.HasChildNodesPath](https://docs.devexpress.com/WPF/DevExpress.Xpf.Grid.TreeListView.HasChildNodesPath) property to display expand buttons only when required.

As a result, the `TreeListView` does not fetch sub-level children to determine whether to display expand buttons:

![image](https://docs.devexpress.com/WPF/images/has-child-nodes-path.gif)

## Files to Review

* [MainWindow.xaml](./CS/HasChildNodes/MainWindow.xaml)
* [ViewModel.cs](./CS/HasChildNodes/ViewModel.cs) (VB: [ViewModel.vb](./VB/HasChildNodes/ViewModel.vb))

## Documentation

* [Expand and Collapse Nodes](https://docs.devexpress.com/WPF/9569/controls-and-libraries/data-grid/grid-view-data-layout/nodes/expand-and-collapse-nodes)
* [TreeListView.HasChildNodesPath](https://docs.devexpress.com/WPF/DevExpress.Xpf.Grid.TreeListView.HasChildNodesPath)
* [TreeListView.FetchSublevelChildrenOnExpand](https://docs.devexpress.com/WPF/DevExpress.Xpf.Grid.TreeListView.FetchSublevelChildrenOnExpand)
* [Bind to Hierarchical Data Structure](https://docs.devexpress.com/WPF/10366/controls-and-libraries/data-grid/display-hierarchical-data/bind-to-hierarchical-data-structure)

## More Examples

* [WPF Tree List - Control Whether to Create Child Nodes](https://github.com/DevExpress-Examples/how-to-control-whether-to-create-child-nodes)
* [WPF Tree List - Implement the Child Nodes Path](https://github.com/DevExpress-Examples/wpf-treelist-implement-childnodespath)
