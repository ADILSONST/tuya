![logo](https://github.com/rospogrigio/localtuya-homeassistant/blob/master/img/logo-small.png)


A Home Assistant custom Integration for local handling of Tuya-based devices.

### Usage and setup [Documentation](https://xzetsubou.github.io/hass-localtuya/)

<br>

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?category=integration&repository=hass-localtuya&owner=xZetsubou)

## Features
- [Cloud API](/cloud_api) 
- Supported protocols: `3.1`, `3.2`, `3.3`, `3.4`, and `3.5`
- Supported Sub-devices: `Devices that function through gateways`
- Auto-configure devices - *`Requires a cloud API setup`*
- Automatic insertion - *`Requires a cloud API setup`*
- Devices discovery - *`Discovers Tuya devices on your network`* 


<br>

<details><summary>Reporting an issue</summary>
<p>

Whenever you write a bug report, it helps tremendously if you include debug logs directly (otherwise we will just ask for them and it will take longer). So please enable debug logs like this and include them in your issue:

```yaml
logger:
  default: warning
  logs:
    custom_components.localtuya: debug
    custom_components.localtuya.pytuya: debug
```
Then, edit the device that is showing problems and check the "Enable debugging for this device" button.

</p>
</details> 

<!-- ### Notes

* Do not declare anything as "tuya", such as by initiating a "switch.tuya". Using "tuya" launches Home Assistant's built-in, cloud-based Tuya integration in lieu of localtuya.

* This custom integration updates device status via pushing updates instead of polling, so status updates are fast (even when manually operated).

* The integration also supports the Tuya IoT Cloud APIs, for the retrieval of info and of the local_keys of the devices. 
The Cloud API account configuration is not mandatory (LocalTuya can work also without it) but is strongly suggested for easy retrieval (and auto-update after re-pairing a device) of local_keys. Cloud API calls are performed only at startup, and when a local_key update is needed. -->

<details><summary> Cʀᴇᴅɪᴛs </summary>
<p>
    
[Rospogrigio](https://github.com/rospogrigio), originally maintained LocalTuya. This fork was created when the upstream version was at `v5.2.1`.

[NameLessJedi](https://github.com/NameLessJedi/localtuya-homeassistant) and [mileperhour](https://github.com/mileperhour/localtuya-homeassistant) being the major sources of inspiration, and whose code for switches is substantially unchanged.

[TradeFace](https://github.com/TradeFace/tuya/), for being the only one to provide the correct code for communication with the cover (in particular, the 0x0d command for the status instead of the 0x0a, and related needs such as double reply to be received): 

sean6541, for the working (standard) Python Handler for Tuya devices.

[jasonacox](https://github.com/jasonacox), for the TinyTuya project from where I big help and refrences to upgrade integration.

[uzlonewolf](https://github.com/uzlonewolf), for maintaining in TinyTuya who improved the tool so much and introduce new features like new protocols etc..

postlund, for the ideas, for coding 95% of the refactoring and boosting the quality of this repo to levels hard to imagine (by me, at least) and teaching me A LOT of how things work in Home Assistant.

</p>
</details> 
