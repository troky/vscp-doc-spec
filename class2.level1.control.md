# Class=542 (0x021E) - Class2 Level I Control

    CLASS2.LEVEL1.CONTROL

## Description

This class mirrors the [CLASS1.CONTROL](./class1.control.md) class but use a different data format with a GUID stored in the first 16 bytes of the data followed by the standard data thus offset with 16-bytes.

See [CLASS2.PROTOCOL1](./class2.protocol1.md) for more information on the data format.
## <a name="type0"></a>Type=0 (0x00) - General event
    VSCP_TYPE_CONTROL_GENERALGeneral Event.
----

## <a name="type1"></a>Type=1 (0x01) - Mute on/off
    VSCP_TYPE_CONTROL_MUTEMute/Un-mute all sound generating nodes in a zone 

 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | If equal to zero no mute else mute.                                | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 

----

## <a name="type2"></a>Type=2 (0x02) - (All) Lamp(s) on/off
    VSCP_TYPE_CONTROL_ALL_LAMPSTurn on/off lamps on nodes in zone.

 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | If equal to zero off else on.                                      | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 

See also [CLASS1.CONTROL, Type=40](./class1.control.md#type40) and [CLASS1.CONTROL, Type=42](./class1.control.md#type41) which don't use byte 0 but instead are separated in two distinct events.

----

## <a name="type3"></a>Type=3 (0x03) - Open
    VSCP_TYPE_CONTROL_OPENPerform open on all nodes in zone. 

 | Data byte | Description                                                         | 
 | :---------: | -----------                                                         | 
 | 0         | Optional byte that have a meaning given by the issuer of the event. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.          | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.  | 


----

## <a name="type4"></a>Type=4 (0x04) - Close
    VSCP_TYPE_CONTROL_CLOSEPerform close on all nodes in zone. 

 | Data byte | Description                                                         | 
 | :---------: | -----------                                                         | 
 | 0         | Optional byte that have a meaning given by the issuer of the event. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.          | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.  | 


----

## <a name="type5"></a>Type=5 (0x05) - TurnOn
    VSCP_TYPE_CONTROL_TURNONTurn On a nodes in a zone/subzone. 

 | Data byte | Description                                                         | 
 | :---------: | -----------                                                         | 
 | 0         | Optional byte that have a meaning given by the issuer of the event. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.          | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.  | 


----

## <a name="type6"></a>Type=6 (0x06) - TurnOff
    VSCP_TYPE_CONTROL_TURNOFFTurn Off a nodes in a zone/subzone. 

 | Data byte | Description                                                         | 
 | :---------: | -----------                                                         | 
 | 0         | Optional byte that have a meaning given by the issuer of the event. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.          | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.  | 


----

## <a name="type7"></a>Type=7 (0x07) - Start
    VSCP_TYPE_CONTROL_STARTStart all nodes in a zone.

 | Data byte | Description                                                         | 
 | :---------: | -----------                                                         | 
 | 0         | Optional byte that have a meaning given by the issuer of the event. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.          | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.  | 

----

## <a name="type8"></a>Type=8 (0x08) - Stop
    VSCP_TYPE_CONTROL_STOPStop all nodes in zone. 

 | Data byte | Description                                                         | 
 | :---------: | -----------                                                         | 
 | 0         | Optional byte that have a meaning given by the issuer of the event. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.          | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.  | 


----

## <a name="type9"></a>Type=9 (0x09) - Reset
    VSCP_TYPE_CONTROL_RESETPerform Reset on all nodes in zone. 

 | Data byte | Description                                                         | 
 | :---------: | -----------                                                         | 
 | 0         | Optional byte that have a meaning given by the issuer of the event. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.          | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.  | 


----

## <a name="type10"></a>Type=10 (0x0A) - Interrupt
    VSCP_TYPE_CONTROL_INTERRUPTPerform Interrupt on all nodes in zone. 

 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | Interrupt level. (0 – 255 , zero is lowest interrupt level. ).   | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 


----

## <a name="type11"></a>Type=11 (0x0B) - Sleep
    VSCP_TYPE_CONTROL_SLEEPPerform Sleep on all nodes in zone. 

 | Data byte | Description                                                         | 
 | :---------: | -----------                                                         | 
 | 0         | Optional byte that have a meaning given by the issuer of the event. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.          | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.  | 


----

## <a name="type12"></a>Type=12 (0x0C) - Wakeup
    VSCP_TYPE_CONTROL_WAKEUPWakeup all nodes in zone. 

 | Data byte | Description                                                         | 
 | :---------: | -----------                                                         | 
 | 0         | Optional byte that have a meaning given by the issuer of the event. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.          | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.  | 


----

## <a name="type13"></a>Type=13 (0x0D) - Resume
    VSCP_TYPE_CONTROL_RESUMEResume all nodes in zone. 

 | Data byte | Description                                                         | 
 | :---------: | -----------                                                         | 
 | 0         | Optional byte that have a meaning given by the issuer of the event. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.          | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.  | 


----

## <a name="type14"></a>Type=14 (0x0E) - Pause
    VSCP_TYPE_CONTROL_PAUSEPause all nodes in zone. 

 | Data byte | Description                                                         | 
 | :---------: | -----------                                                         | 
 | 0         | Optional byte that have a meaning given by the issuer of the event. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.          | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.  | 


----

## <a name="type15"></a>Type=15 (0x0F) - Activate
    VSCP_TYPE_CONTROL_ACTIVATEActivate all nodes in zone. 

 | Data byte | Description                                                         | 
 | :---------: | -----------                                                         | 
 | 0         | Optional byte that have a meaning given by the issuer of the event. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.          | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.  | 


----

## <a name="type16"></a>Type=16 (0x10) - Deactivate
    VSCP_TYPE_CONTROL_DEACTIVATEDeactivate all nodes in zone. 

 | Data byte | Description                                                         | 
 | :---------: | -----------                                                         | 
 | 0         | Optional byte that have a meaning given by the issuer of the event. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.          | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.  | 


----

## <a name="type17"></a>Type=17 (0x11) - Reserved for future use
    VSCP_TYPE_CONTROL_RESERVED17Reserved. 
----

## <a name="type18"></a>Type=18 (0x12) - Reserved for future use
    VSCP_TYPE_CONTROL_RESERVED18Reserved. 
----

## <a name="type19"></a>Type=19 (0x13) - Reserved for future use
    VSCP_TYPE_CONTROL_RESERVED19Reserved.
----

## <a name="type20"></a>Type=20 (0x14) - Dim lamp(s)
    VSCP_TYPE_CONTROL_DIM_LAMPSDim all dimmer devices on a segment to a specified dim value. 

 | Data byte | Description                                                                             | 
 | :---------: | -----------                                                                             | 
 | 0         | Value (0 – 100) . 0 = off, 100 = full on. 254 dim down one step. 255 dim up one step. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.                              | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.                      | 

----

## <a name="type21"></a>Type=21 (0x15) - Change Channel
    VSCP_TYPE_CONTROL_CHANGE_CHANNELThis is typical for changing TV channels or for changing AV amp input source etc. 

 | Data byte | Description                                                                                                                                                                                                                                                                                                                                               | 
 | :---------: | -----------                                                                                                                                                                                                                                                                                                                                               | 
 | 0         | A value between 0 and 127 indicates the channel number. A value between 128 to 157 is change down by the specified number of channels. A value between 160 to 191 is change up by the specified number of channels. A value of 255 means that this is an extended change channel event and that the channel number is sent in byte 3 and after if needed. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.                                                                                                                                                                                                                                                                                                | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.                                                                                                                                                                                                                                                                                        | 

----

## <a name="type22"></a>Type=22 (0x16) - Change Level
    VSCP_TYPE_CONTROL_CHANGE_LEVELChange an absolute level. 

 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | Absolute level.                                                    | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 

----

## <a name="type23"></a>Type=23 (0x17) - Relative Change Level
    VSCP_TYPE_CONTROL_RELATIVE_CHANGE_LEVEL
 Relative Change Level request
 
 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | Relative level.                                                    | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 

----

## <a name="type24"></a>Type=24 (0x18) - Measurement Request
    VSCP_TYPE_CONTROL_MEASUREMENT_REQUESTMeasurement Request

| Data byte | Description                                                                                                                                                           | 
 | :---------: | -----------                                                                                                                                                           | 
 | 0         | Zero indicates all measurements supported by node should be sent (as separate events). Non-zero indicates a node specific index specifying which measurement to send. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.                                                                                                            | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.                                                                                                    | 

----

## <a name="type25"></a>Type=25 (0x19) - Stream Data
    VSCP_TYPE_CONTROL_STREAM_DATARequest to stream data

 | Data byte | Description                                                               | 
 | :---------: | -----------                                                               | 
 | 0         | Sequence number which is increase by one for each stream data event sent. | 
 | 1-7       | Stream data.                                                              | 

Use this event for streamed data out from a node. The source is then given by the nickname. If a specific received is needed use Zoned Stream. 

----

## <a name="type26"></a>Type=26 (0x1A) - Sync
    VSCP_TYPE_CONTROL_SYNCSynchronize events on a segment. 

 | Data byte | Description                                                                                                                                  | 
 | :---------: | -----------                                                                                                                                  | 
 | 0         | Sensor index for a sensor within a module (see [data coding](./data_coding.md). 255 is all sensors. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.                                                                                   | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.                                                                           | 

The sensor index can be used to index units within a module also or used as some other indexing schema. 

----

## <a name="type27"></a>Type=27 (0x1B) - Zoned Stream Data
    VSCP_TYPE_CONTROL_ZONED_STREAM_DATARequest streamed data from nodes identified by zone/subzone.

 | Data byte | Description                                                               | 
 | :---------: | -----------                                                               | 
 | 0         | Sequence number which is increase by one for each stream data event sent. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.                | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.        | 
 | 3-7       | Stream data.                                                              | 

----

## <a name="type28"></a>Type=28 (0x1C) - Set Pre-set
    VSCP_TYPE_CONTROL_SET_PRESETSome nodes may have pre-set configurations to choose from. With this event a pre-set can be set for a zone/sub-zone.

A node that receive and act on this event send CLASS1.INFORMATION, 

Type=48 as a response event. 

 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | Code for pre-set to set.                                           | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 

----

## <a name="type29"></a>Type=29 (0x1D) - Toggle state
    VSCP_TYPE_CONTROL_TOGGLE_STATEToggle the state of a node.

Note: This may be a bad design option as it often demands that the state should be known for the node on beforehand.

 | Data byte | Description                                                         | 
 | :---------: | -----------                                                         | 
 | 0         | Optional byte that have a meaning given by the issuer of the event. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.          | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.  | 

----

## <a name="type30"></a>Type=30 (0x1E) - Timed pulse on
    VSCP_TYPE_CONTROL_TIMED_PULSE_ONWith this event it is possible to generate a timed pulse that is on for a specified time.

 | Data byte | Description                                                         | 
 | :---------: | -----------                                                         | 
 | 0         | Optional byte that have a meaning given by the issuer of the event. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.          | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.  | 
 | 3         | Control byte.                                                       | 
 | 4-7       | Set time as a long with MSB in the first byte.                      | 

##### Control Byte

The control byte have the following bits defined

 | Bit | Description                                                          | 
 | :---: | -----------                                                          | 
 | 0-3 | Time code (see table below)                                          | 
 | 4   | Reserved                                                             | 
 | 5   | Reserved                                                             | 
 | 6   | Send on event ( Class=20 Type = 3 (0x03) On ) when pulse goes on.    | 
 | 7   | Send off event ( Class=20 Type = 4 (0x04) Off ) when pulse goes off. | 

##### Time code

 | Code | Description                     | 
 | :----: | -----------                     | 
 | 0    | Time specified in microseconds. | 
 | 1    | Time specified in milliseconds. | 
 | 2    | Time specified in seconds.      | 
 | 3    | Time specified in minutes.      | 
 | 4    | Time specified in hours.        | 
 | 5    | Time specified in days.         | 


----

## <a name="type31"></a>Type=31 (0x1F) - Timed pulse off
    VSCP_TYPE_CONTROL_TIMED_PULSE_OFFWith this event it is possible to generate a timed pulse that is off for a specified time.

 | Data byte | Description                                                         | 
 | :---------: | -----------                                                         | 
 | 0         | Optional byte that have a meaning given by the issuer of the event. | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.          | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.  | 
 | 3         | Control byte.                                                       | 
 | 4-7       | Set time as a long with MSB in the first byte.                      | 

##### Control Byte

The control byte have the following bits defined

 | Bit | Description                                                          | 
 | :---: | -----------                                                          | 
 | 0-3 | Time code (see table below)                                          | 
 | 4   | Reserved                                                             | 
 | 5   | Reserved                                                             | 
 | 6   | Send on event ( Class=20 Type = 3 (0x03) On ) when pulse goes on.    | 
 | 7   | Send off event ( Class=20 Type = 4 (0x04) Off ) when pulse goes off. | 

##### Time code

 | Code | Description                     | 
 | :----: | -----------                     | 
 | 0    | Time specified in microseconds. | 
 | 1    | Time specified in milliseconds. | 
 | 2    | Time specified in seconds.      | 
 | 3    | Time specified in minutes.      | 
 | 4    | Time specified in hours.        | 
 | 5    | Time specified in days.         | 


----

## <a name="type32"></a>Type=32 (0x20) - Set country/language
    VSCP_TYPE_CONTROL_SET_COUNTRY_LANGUAGESet country and language.

 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | Country/Language code.                                             | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 
 | 3-7       | Country/Language code specific                                     | 

 | Language code | Description          | Example                                           | 
 | :---------: | -----------          | -------                                           | 
 | 0             | Custom coded system  | Byte 3 = 0 English, Byte 3 = 1 German or similar. | 
 | 1             | ISO 639-1            | nl for Dutch, en for English.                     | 
 | 2             | ISO 639-2/T          | nid for Dutch, eng for English.                   | 
 | 3             | ISO 639-2/B          | dut for Dutch, eng for English.                   | 
 | 4             | ISO 639-3            | nid for Dutch, eng for English.                   | 
 | 5             | IETF (RFC-5646/4647) | en-US for American English. en-GB British.        | 


ISO codes can be found [here](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)

----

## <a name="type33"></a>Type=33 (0x21) - Big Change level
    VSCP_TYPE_CONTROL_BIG_CHANGE_LEVELBig Change level can be used in situations when the one byte level of CLASS1.CONTROL, Type=22 is not enough.

 | Data byte | Description                                                                                               | 
 | :---------: | -----------                                                                                               | 
 | 0         | Index                                                                                                     | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.                                                | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones.                                        | 
 | 3-7       | Level as signed Integer. The range can be adjusted by the user by sending the needed number of bytes 1-5. | 

----

## <a name="type34"></a>Type=34 (0x22) - Move shutter up
    VSCP_TYPE_CONTROL_SHUTTER_UPMove shutter up.

 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | Index.                                                             | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 

----

## <a name="type35"></a>Type=35 (0x23) - Move shutter down
    VSCP_TYPE_CONTROL_SHUTTER_DOWNMove shutter down.

 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | Index.                                                             | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 

----

## <a name="type36"></a>Type=36 (0x24) - Move shutter left
    VSCP_TYPE_CONTROL_SHUTTER_LEFTMove shutter left.

 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | Index.                                                             | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 


----

## <a name="type37"></a>Type=37 (0x25) - Move shutter right
    VSCP_TYPE_CONTROL_SHUTTER_RIGHTMove shutter right.

 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | Index.                                                             | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 

----

## <a name="type38"></a>Type=38 (0x26) - Move shutter to middle position
    VSCP_TYPE_CONTROL_SHUTTER_MIDDLEMove shutter to middle position.

 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | Index.                                                             | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 

----

## <a name="type39"></a>Type=39 (0x27) - Move shutter to preset position
    VSCP_TYPE_CONTROL_SHUTTER_PRESETMove shutter to preset position.

 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | Index.                                                             | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 
 | 3         | Position 0-100.                                                    | 

----

## <a name="type40"></a>Type=40 (0x28) - (All) Lamp(s) on
    VSCP_TYPE_CONTROL_ALL_LAMPS_ONTurn on all lamps in a zone.

 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | Not used.                                                          | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 

See also [CLASS1.CONTROL, Type=2](./class1.control.md#type2)

----

## <a name="type41"></a>Type=41 (0x29) - (All) Lamp(s) off
    VSCP_TYPE_CONTROL_ALL_LAMPS_OFFTurn off all lamps in a zone.

 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | Not used.                                                          | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 

See also [CLASS1.CONTROL, Type=2](./class1.control.md#type2)

----

## <a name="type42"></a>Type=42 (0x2A) - Lock
    VSCP_TYPE_CONTROL_LOCKLock devices in a zone.

 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | Not used.                                                          | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 


----

## <a name="type43"></a>Type=43 (0x2B) - Unlock
    VSCP_TYPE_CONTROL_UNLOCKUnock devices in a zone.

 | Data byte | Description                                                        | 
 | :---------: | -----------                                                        | 
 | 0         | Not used.                                                          | 
 | 1         | Zone for which event applies to (0-255). 255 is all zones.         | 
 | 2         | Sub-zone for which event applies to (0-255). 255 is all sub-zones. | 


----

{% include "./bottom_copyright.md" %}