---
-api-id: M:Windows.UI.Notifications.TileUpdater.StartPeriodicUpdate(Windows.Foundation.Uri,Windows.Foundation.DateTime,Windows.UI.Notifications.PeriodicUpdateRecurrence)
-api-type: winrt method
---

<!-- Method syntax
public void StartPeriodicUpdate(Windows.Foundation.Uri tileContent, Windows.Foundation.DateTime startTime, Windows.UI.Notifications.PeriodicUpdateRecurrence requestedInterval)
-->

# Windows.UI.Notifications.TileUpdater.StartPeriodicUpdate

## -description
Begins a series of timed updates for the tile that the updater is bound to. Update content is retrieved from a specified Uniform Resource Identifier (URI). Updates begin at a specified time.

## -parameters
### -param tileContent
The Uniform Resource Identifier (URI) from which the XML content of the tile update will be retrieved.

### -param startTime
The time at which the Uniform Resource Identifier (URI) should first be polled for new tile content.

### -param requestedInterval
The frequency with which the Uniform Resource Identifier (URI) is polled for new tile content, following the initial update at *startTime*.

## -remarks

## -examples

## -see-also
[StartPeriodicUpdate(Uri, PeriodicUpdateRecurrence)](tileupdater_startperiodicupdate_1967457783.md), [How to set up periodic notifications for tiles](XREF:TODO:m_ui_tiles.howto_setup_tile_polling), [Guidelines and checklist for periodic notifications](XREF:TODO:m_ui_tiles.guidelines_for_polling), [App tiles and badges sample](http://go.microsoft.com/fwlink/p/?linkid=231469), [Quickstart: Sending a tile update](http://msdn.microsoft.com/library/d4b2cebf-9dec-4c8f-bc6d-23edca7aaf83), [Tile and tile notification overview](http://msdn.microsoft.com/library/10a05b52-42c4-4f85-9310-57663e378b9e), [The tile template catalog](http://msdn.microsoft.com/library/2d3dd627-9a34-493c-bda4-ff7b80817e4f), [Guidelines and checklist for tiles](http://msdn.microsoft.com/library/e825f754-97dd-41c2-aff4-4dfb60eda677), [How to schedule a tile notification](http://msdn.microsoft.com/library/56b0c3e3-be90-4461-a8b1-79e88072b37c), [How to set up periodic notifications for tiles](XREF:TODO:m_ui_tiles.howto_setup_tile_polling), [Tiles XML schema](XREF:TODO:tile.Schema_Root)