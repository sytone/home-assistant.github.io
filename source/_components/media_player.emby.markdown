
---
layout: page
title: "Emby"
description: "Instructions how to integrate Emby into Home Assistant."
date: 2016-10-13 22:00
sidebar: true
comments: false
sharing: true
footer: true
logo: emby.png
ha_category: Media Player
ha_release: "0.32"
ha_iot_class: "Local Polling"
---


The `emby` platform allows you to control a [Emby](http://emby.media/) multimedia system from Home Assistant.

To add Emby to your installation, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
media_player:
  - platform: emby
    host: 192.168.11.5
    api_key: "emby_api_key"
```

Configuration variables:

- **host** (*Required*): The host name or address of the device that is running Emby.
- **api_key** (*Requred*): The api-key you would like home-assistant to use to authenticate.
- **ssl** (*Optional*): True if you want to connect with https. Be sure to set the port also.
- **port** (*Optional*): The port number. Defaults to 8096.

## Getting the API Key

To get a API key you need to log into the Admin area of Emby under Manage Server. Scroll down to the Expert sections and Click on Advanced. At the top of the page select the Security tab. You will be presented with a list of existing keys or none if this is your first one. Click on the Add button and given the application an distincitve name. I went with Home Assistant as it seemed like a good idea at the time. 

Once you have the Api Key you can copy it to your configuration. 

To go stright to the security page use the following link, ensure you update the IP address and port if different. 

    http://192.168.0.1:8096/web/serversecurity.html
