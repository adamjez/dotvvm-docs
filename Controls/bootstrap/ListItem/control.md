Represents a single item in Bootstrap lists and menus.

This control is used inside several Bootstrap controls - e.g. the [Breadcrumb](/docs/controls/bootstrap/Breadcrumb) and [NavigationBar](/docs/controls/bootstrap/NavigationBar) controls.

_In the `ListGroup` control, you have to use the [ListGroupItem](/docs/controls/bootstrap/ListGroupItem) control._

<br />

If you set the `NavigateUrl` property or you use the `RouteName` and `Param-*` properties,
the item behaves like a hyperlink. For more information abou `RouteName` properties see the
[RouteLink](../builtin/RouteLink) control - the usage is the same.

If you set the `Click` command, the specified method in the viewmodel will be 
triggered.

Remember that you cannot use those two features together.