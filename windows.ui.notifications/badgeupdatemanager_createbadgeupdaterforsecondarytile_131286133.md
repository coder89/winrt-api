---
-api-id: M:Windows.UI.Notifications.BadgeUpdateManager.CreateBadgeUpdaterForSecondaryTile(System.String)
-api-type: winrt method
---

<!-- Method syntax
public Windows.UI.Notifications.BadgeUpdater CreateBadgeUpdaterForSecondaryTile(System.String tileId)
-->

# Windows.UI.Notifications.BadgeUpdateManager.CreateBadgeUpdaterForSecondaryTile

## -description
Creates and initializes a new instance of the [BadgeUpdater](badgeupdater.md), which enables you to change the appearance or content of a badge on a [secondary tile](../windows.ui.startscreen/secondarytile.md). The tile can belong to the calling app or any other app in the same package.

## -parameters
### -param tileId
The unique ID of the tile.

## -returns
The object you will use to send badge updates to the tile identified by *tileID*.

## -remarks

## -examples
The following example demonstrates how to send a numeric badge notification to a secondary tile with an ID of "SecondaryTile.Dynamic".

```javascript

var Notifications = Windows.UI.Notifications;

// Define the badge content
var badgeNotification = Notifications.BadgeUpdateManager.getTemplateContent(Notifications.BadgeTemplateType.badgeNumber);
var badgeAttributes = badgeNotification.getElementsByTagName("badge");
badgeAttributes[0].setAttribute("value", "6");

// Create the notification based on the XML content.
var badge = new Notifications.BadgeNotification(badgeNotification);

// Create a secondary tile updater, passing it the ID of the tile.
Notifications.BadgeUpdateManager.createBadgeUpdaterForSecondaryTile("SecondaryTile.Dynamic");

// Send the notification to the secondary tile.
tileUpdater.update(tileNotification);
```



## -see-also
[App tiles and badges sample](http://go.microsoft.com/fwlink/p/?linkid=231469), [Guidelines and checklist for tiles and badges](http://msdn.microsoft.com/library/e825f754-97dd-41c2-aff4-4dfb60eda677), [How to clear a badge](XREF:TODO:m_ui_tiles.howto_clear_a_badge), [How to send a glyph or numeric badge in a local notification](XREF:TODO:m_ui_tiles.howto_send_local_badge_notifications), [How to set up periodic notifications for badges](XREF:TODO:m_ui_tiles.howto_setup_badge_polling), [How to update a badge through push notifications](XREF:TODO:m_ui_tiles.howto_update_badges_push), [Badge XML schema](XREF:TODO:badge.Schema_Root), [Badge overview](http://msdn.microsoft.com/library/a64c58bb-d9c9-4c09-a685-4df94fa7dfdd)