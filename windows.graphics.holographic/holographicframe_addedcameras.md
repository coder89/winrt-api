---
-api-id: P:Windows.Graphics.Holographic.HolographicFrame.AddedCameras
-api-type: winrt property
---

<!-- Property syntax
public Windows.Foundation.Collections.IVectorView<Windows.Graphics.Holographic.HolographicCamera> AddedCameras { get; }
-->

# Windows.Graphics.Holographic.HolographicFrame.AddedCameras

## -description
Gets the list of HolographicCamera objects that were added since last frame.

Cameras only show up in this list after they surface in the CameraAdded event to //! let apps initialize any per-camera buffers on a background thread.

## -property-value
A collection of HolographicCamera objects that were added.

## -remarks

## -examples

## -see-also
