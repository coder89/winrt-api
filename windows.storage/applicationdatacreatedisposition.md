---
-api-id: T:Windows.Storage.ApplicationDataCreateDisposition
-api-type: winrt enum
---

<!-- Enumeration syntax
public enum Windows.Storage.ApplicationDataCreateDisposition : int
-->

# ApplicationDataCreateDisposition

## -description
Specifies options for creating application data containers or returning existing containers. This enumeration is used by the [ApplicationDataContainer.CreateContainer](applicationdatacontainer_createcontainer.md) method.

## -enum-fields
### -field Always:0
Always returns the specified container. Creates the container if it does not exist.

### -field Existing:1
Returns the specified container only if it already exists. Raises an exception of type **System.Exception** if the specified container does not exist.


## -remarks

## -examples
Call the [ApplicationDataContainer.CreateContainer | createContainer](applicationdatacontainer_createcontainer.md) method to create a settings container or to return an existing container.

This example creates a settings container named `exampleContainer` and adds a setting named `exampleSetting`. The **Always | always** value from the [ApplicationDataCreateDisposition](applicationdatacreatedisposition.md) enumeration indicates that the container should be created if it does not already exist.

Use the [ApplicationDataContainer.Values | values](applicationdatacontainer_values.md) property to access the `exampleSetting` setting in the `exampleContainer` container.

Call the [ApplicationDataContainer.DeleteContainer | deleteContainer](applicationdatacontainer_deletecontainer.md) method to delete the `exampleContainer` settings container when you have finished with it.

```javascript
var applicationData = Windows.Storage.ApplicationData.current;

var localSettings = applicationData.localSettings;

// Create a setting in a container

var container = localSettings.createContainer("exampleContainer", 
    Windows.Storage.ApplicationDataCreateDisposition.Always);

if (localSettings.containers.hasKey("exampleContainer"))
{
    localSettings.containers.lookup("exampleContainer").values["exampleSetting"] = "Hello Windows";
}

// Read data from a setting in a container

var hasContainer = localSettings.containers.hasKey("exampleContainer");

if (hasContainer)
{
    // Access data in: 
    //   localSettings.containers.lookup("exampleContainer").values.hasKey("exampleSetting");
}

// Delete a container

localSettings.deleteContainer("exampleContainer");
```

```csharp
Windows.Storage.ApplicationDataContainer localSettings = Windows.Storage.ApplicationData.Current.LocalSettings;

// Create a setting in a container

Windows.Storage.ApplicationDataContainer container = 
   localSettings.CreateContainer("exampleContainer", Windows.Storage.ApplicationDataCreateDisposition.Always);

if (localSettings.Containers.ContainsKey("exampleContainer"))
{
   localSettings.Containers["exampleContainer"].Values["exampleSetting"] = "Hello Windows";
}

// Read data from a setting in a container

bool hasContainer = localSettings.Containers.ContainsKey("exampleContainer");
bool hasSetting = false;

if (hasContainer)
{
   hasSetting = localSettings.Containers["exampleContainer"].Values.ContainsKey("exampleSetting");
}

// Delete a container

localSettings.DeleteContainer("exampleContainer");
```

```vb
Dim localSettings As Windows.Storage.ApplicationDataContainer = Windows.Storage.ApplicationData.Current.LocalSettings

' Create a setting in a container

Dim container As Windows.Storage.ApplicationDataContainer = 
   localSettings.CreateContainer("exampleContainer", Windows.Storage.ApplicationDataCreateDisposition.Always)

If localSettings.Containers.ContainsKey("exampleContainer") Then
    localSettings.Containers("exampleContainer").Values("exampleSetting") = "Hello Windows"
End If

' Read data from a setting in a container

Dim hasContainer As Boolean = localSettings.Containers.ContainsKey("exampleContainer")
Dim hasSetting As Boolean = False

If hasContainer Then
    hasSetting = localSettings.Containers("exampleContainer").Values.ContainsKey("exampleSetting")
End If

' Delete a container

localSettings.DeleteContainer("exampleContainer")
```

```cpp
ApplicationDataContainer^ localSettings = ApplicationData::Current->LocalSettings;

// Create a setting in a container

ApplicationDataContainer^ container = 
   localSettings->CreateContainer("exampleContainer", ApplicationDataCreateDisposition::Always);

if (localSettings->Containers->HasKey("exampleContainer"))
{
   auto values = localSettings->Containers->Lookup("exampleContainer")->Values;
   values->Insert("exampleSetting", "Hello Windows");
}

// Read data from a setting in a container

bool hasContainer = localSettings->Containers->HasKey("exampleContainer");
bool hasSetting = false;

if (hasContainer)
{
   auto values = localSettings->Containers->Lookup("exampleContainer")->Values;
   hasSetting = values->HasKey("exampleSetting");
}

// Delete a container

localSettings->DeleteContainer("exampleContainer");
```



## -see-also
[Quickstart: Local application data (JavaScript)](http://msdn.microsoft.com/library/87dfe8e5-2d01-45cf-bcb1-25f54219a439), [Store and retrieve settings and other app data](http://msdn.microsoft.com/library/41676a02-325a-455e-8565-c9ec0bc3a8fe), [Quickstart: Roaming application data (JavaScript)](http://msdn.microsoft.com/library/60f40214-c201-4afe-a2f5-0ef3a7de0076), [Store and retrieve settings and other app data](http://msdn.microsoft.com/library/41676a02-325a-455e-8565-c9ec0bc3a8fe), [Store and retrieve settings and other app data](http://msdn.microsoft.com/library/41676a02-325a-455e-8565-c9ec0bc3a8fe), [ApplicationDataContainer.CreateContainer](applicationdatacontainer_createcontainer.md)