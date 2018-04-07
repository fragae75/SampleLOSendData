# SampleLOSendData

Sample application for Datavenue Live Objects : https://liveobjects.orange-business.com/#/liveobjects

It is a simple sample that sends a MQTT payload to Live Objects as a MQTT device ("json+device").
It generates a standard Live Objects MQTT payload as follow :<br>
 
	{
		"streamId":"StreamSampleLO001",
		"timestamp":"2018-04-07T15:52:31.150Z",
		"location":{"lat":45.759723,"lon":4.84223},
		"model":"demo",
		"value":
		{
			"hygrometry":xx,
			"revmin":xxxx,
			"temperature":xx
		},
		"tags":["SampleLO"],
		"metadata":{"source":"urn:lo:nsid:sensor:SampleLO001","connector":"mqtt"}
	}

This sample generates the same payload as the Android app available at : https://play.google.com/store/apps/details?id=com.orange.lo.assetdemo <br>


<h2> Installation notes </h2>

1) Create an account on Live Objects. You can get a free account (10 MQTT devices for 1 year) at : https://liveobjects.orange-business.com/#/request_account <br>
Don't check "Lora" otherwise the account will not be instantly created.

2) Generate your API key : menu Configuration/API Keys click on "Add"

3) Create a MyKey class : 

package com.test.SampleLOSendData; <br>

public final class MyKey { <br>
	static String key = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"; <br>
}<br>

4) You will find into the repository 4 jar files into the /lib. Add them as "external JARs" into you IDE (eg Eclipse).
