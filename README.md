# idl4-cc-node-red-rpi

## Your first circuit

	[
		{
			"id": "f1de87166743083b",
			"type": "rpi-gpio out",
			"z": "69c38f1beeb5c50b",
			"name": "",
			"pin": "21",
			"set": "",
			"level": "0",
			"freq": "",
			"out": "out",
			"bcm": true,
			"x": 460,
			"y": 340,
			"wires": []
		},
		{
			"id": "b4ea1ab78479bc24",
			"type": "inject",
			"z": "69c38f1beeb5c50b",
			"name": "",
			"props": [
				{
					"p": "payload"
				},
				{
					"p": "topic",
					"vt": "str"
				}
			],
			"repeat": "",
			"crontab": "",
			"once": false,
			"onceDelay": 0.1,
			"topic": "",
			"payload": "true",
			"payloadType": "bool",
			"x": 230,
			"y": 340,
			"wires": [
				[
					"f1de87166743083b"
				]
			]
		},
		{
			"id": "0920a95452acbd74",
			"type": "inject",
			"z": "69c38f1beeb5c50b",
			"name": "",
			"props": [
				{
			"p": "payload"
				},
				{
					"p": "topic",
					"vt": "str"
				}
			],
			"repeat": "",
			"crontab": "",
			"once": false,
			"onceDelay": 0.1,
			"topic": "",
			"payload": "false",
			"payloadType": "bool",
			"x": 230,
			"y": 400,
			"wires": [
				[
					"f1de87166743083b"
				]
			]
		}
	]

## 
