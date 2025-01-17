---
Description: Raised by the audio renderer when the audio session is disconnected from a Windows Terminal Services (WTS) session. The audio renderer is now invalid.
ms.assetid: 08f9844c-f3b1-4d60-990e-9131f3312f6b
title: MEAudioSessionDisconnected event
ms.topic: reference
ms.date: 05/31/2018
---

# MEAudioSessionDisconnected event

Raised by the audio renderer when the audio session is disconnected from a Windows Terminal Services (WTS) session. The audio renderer is now invalid.

The Media Session forwards this event to the application.

## Event values

Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.



| VARTYPE                | Description                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT\_EMPTY<br/>   | No event data.<br/> <br/>                                                     |
| VT\_UNKNOWN<br/> | Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.<br/> <br/> |



## Remarks

This event is sent by the audio renderer's stream sink. The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](https://msdn.microsoft.com/en-us/library/Dd370941(v=VS.85).aspx) event from the audio session with the disconnection reason equal to DisconnectReasonSessionDisconnected.

The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.

## Requirements



|                                     |                                                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                                           |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## See also

<dl> <dt>

[Media Foundation Events](media-foundation-events.md)
</dt> <dt>

[Streaming Audio Renderer](streaming-audio-renderer.md)
</dt> </dl>

 

 




