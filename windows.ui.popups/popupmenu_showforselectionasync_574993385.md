---
-api-id: M:Windows.UI.Popups.PopupMenu.ShowForSelectionAsync(Windows.Foundation.Rect)
-api-type: winrt method
---

<!-- Method syntax
public Windows.Foundation.IAsyncOperation<Windows.UI.Popups.IUICommand> ShowForSelectionAsync(Windows.Foundation.Rect selection)
-->

# Windows.UI.Popups.PopupMenu.ShowForSelectionAsync

## -description
Shows the context menu above the specified selection.

## -parameters
### -param selection
The coordinates (in DIPs) of the selected rectangle, relative to the window. The context menu is placed directly above and centered on this rectangle such that selection is not covered.

> [!NOTE]
> For VB, C#, and C++, this window is the [CoreWindow](../windows.ui.core/corewindow.md) associated with the thread that is calling the context menu.

## -returns
A [IUICommand](iuicommand.md) object that represents the context menu command invoked by the user, after the [ShowForSelectionAsync](popupmenu_showforselectionasync.md) call completes.

If no command is invoked, [ShowForSelectionAsync](popupmenu_showforselectionasync.md) returns **null**.

## -remarks
You can see complete code examples that demonstrate how to create and customize context menu in the [Context menu sample](http://go.microsoft.com/fwlink/p/?linkid=234891) on the [ sample home page](http://go.microsoft.com/fwlink/p/?linkid=226952).

## -examples
Before you can show a context menu, you must add an event listener for the [oncontextmenu](XREF:TODO:wwa.oncontextmenu_Event) event. For example, the [Context menu sample](http://go.microsoft.com/fwlink/p/?linkid=234891) listens for the event on specific HTML elements, and then calls the `scenario1AttachmentHandler` function.



[!code-js[addcontextmenueventlistener_js](../windows.ui.popups/code/ContextMenu/js/js/scenario1.js#Snippetaddcontextmenueventlistener_js)]



[!code-js[showforselection_commandshaveids_js](../windows.ui.popups/code/ContextMenu/js/js/scenario2.js#Snippetshowforselection_commandshaveids_js)]

Additionally, the [Context menu sample](http://go.microsoft.com/fwlink/p/?linkid=234891) uses two helper functions (`getSelectionRect` and `getclientCoordinates`) to set the coordinates for the selection rectangle.



[!code-js[selectionrect_js](../windows.ui.popups/code/ContextMenu/js/js/scenario2.js#Snippetselectionrect_js)]

## -see-also
[Adding context menus](XREF:TODO:m_ui_contextmenu.adding_context_menus_portal), [Context menu sample](http://go.microsoft.com/fwlink/p/?linkid=234891), [Guidelines and checklist for ](XREF:TODO:m_ui_contextmenu.guidelines_and_checklist_for_context_menus), [IUICommand](iuicommand.md), [oncontextmenu](XREF:TODO:wwa.oncontextmenu_Event), [Rect](../windows.foundation/rect.md), [ShowForSelectionAsync(Rect, Placement)](popupmenu_showforselectionasync_655080999.md), [UICommand](uicommand.md)
tes, and those coordinates are used as the *selection*[Rect](../windows.foundation/rect.md).

## -see-also
[Adding context menus](XREF:TODO:m_ui_contextmenu.adding_context_menus_portal), [Context menu sample](http://go.microsoft.com/fwlink/p/?linkid=234891), [Guidelines and checklist for ](XREF:TODO:m_ui_contextmenu.guidelines_and_checklist_for_context_menus), [IUICommand](iuicommand.md), [oncontextmenu](XREF:TODO:wwa.oncontextmenu_Event), [Rect](../windows.foundation/rect.md), [ShowForSelectionAsync(Rect, Placement)](popupmenu_showforselectionasync_655080999.md), [UICommand](uicommand.md)