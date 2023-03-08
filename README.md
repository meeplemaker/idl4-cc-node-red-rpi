# idl4-cc-node-red-rpi

## Node-RED (basics)

### Your first circuit

#### Circuit

![First circuit (circuit)](/img/firstCircuit_circuit.png)

#### Flow

![First circuit (flow)](/img/firstCircuit_flow.png)


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

## Digital switch

	[
		{
			"id": "d9a9b9aa83caae0b",
			"type": "rpi-gpio out",
			"z": "e08c0da476decd5e",
			"name": "",
			"pin": "21",
			"set": true,
			"level": "0",
			"freq": "",
			"out": "out",
			"bcm": true,
			"x": 520,
			"y": 220,
			"wires": []
		},
		{
			"id": "253cb9021c914b37",
			"type": "toggle",
			"z": "e08c0da476decd5e",
			"name": "",
			"onOffTopic": "X",
			"onValue": "true",
			"onType": "bool",
			"offValue": "false",
			"offType": "bool",
			"toggleTopic": "",
			"toggleValue": "",
			"toggleType": "any",
			"passOnOff": "ifChanged",
			"x": 350,
			"y": 220,
			"wires": [
				[
					"d9a9b9aa83caae0b"
				]
			]
		},
		{
			"id": "758893a3c947886c",
			"type": "inject",
			"z": "e08c0da476decd5e",
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
			"payload": "",
			"payloadType": "date",
			"x": 180,
			"y": 220,
			"wires": [
				[
					"253cb9021c914b37"
				]
			]
		}
	]
	
## Physical switch

	[
		{
			"id": "244cd0a2c293fd68",
			"type": "rpi-gpio in",
			"z": "10a5f914b7088318",
			"name": "",
			"pin": "26",
			"intype": "up",
			"debounce": "25",
			"read": true,
			"bcm": true,
			"x": 160,
			"y": 180,
			"wires": [
				[
					"8ae6161202666574"
				]
			]
		},
		{
			"id": "1b5302e8e3c83357",
			"type": "rpi-gpio out",
			"z": "10a5f914b7088318",
			"name": "",
			"pin": "21",
			"set": true,
			"level": "0",
			"freq": "",
			"out": "out",
			"bcm": true,
			"x": 540,
			"y": 180,
			"wires": []
		},
		{
			"id": "8ae6161202666574",
			"type": "toggle",
			"z": "10a5f914b7088318",
			"name": "",
			"onOffTopic": "X",
			"onValue": "true",
			"onType": "bool",
			"offValue": "false",
			"offType": "bool",
			"toggleTopic": "",
			"toggleValue": "false",
			"toggleType": "bool",
			"passOnOff": "",
			"x": 350,
			"y": 180,
			"wires": [
				[
					"1b5302e8e3c83357"
				]
			]
		}
	]
	
## RGB-led (basic)

	[
		{
			"id": "e19f66f0e913b410",
			"type": "rpi-gpio out",
			"z": "524949a46aa74ae0",
			"name": "R",
			"pin": "21",
			"set": "",
			"level": "0",
			"freq": "",
			"out": "pwm",
			"bcm": true,
			"x": 550,
			"y": 320,
			"wires": []
		},
		{
			"id": "325d1f5a448c2207",
			"type": "rpi-gpio out",
			"z": "524949a46aa74ae0",
			"name": "G",
			"pin": "20",
			"set": "",
			"level": "0",
			"freq": "",
			"out": "pwm",
			"bcm": true,
			"x": 550,
			"y": 260,
			"wires": []
		},
		{
			"id": "31946b9e42c6f185",
			"type": "rpi-gpio out",
			"z": "524949a46aa74ae0",
			"name": "B",
			"pin": "16",
			"set": "",
			"level": "0",
			"freq": "",
			"out": "pwm",
			"bcm": true,
			"x": 550,
			"y": 200,
			"wires": []
		},
		{
			"id": "779477ab50e4a9c5",
			"type": "inject",
			"z": "524949a46aa74ae0",
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
			"payload": "0",
			"payloadType": "num",
			"x": 330,
			"y": 140,
			"wires": [
				[
					"31946b9e42c6f185"
				]
			]
		},
		{
			"id": "4b74ef8ea60a934e",
			"type": "inject",
			"z": "524949a46aa74ae0",
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
			"payload": "100",
			"payloadType": "num",
			"x": 330,
			"y": 180,
			"wires": [
				[
					"31946b9e42c6f185"
				]
			]
		},
		{
			"id": "b3fc44abe82d8d59",
			"type": "inject",
			"z": "524949a46aa74ae0",
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
			"payload": "0",
			"payloadType": "num",
			"x": 330,
			"y": 240,
			"wires": [
				[
					"325d1f5a448c2207"
				]
			]
		},
		{
			"id": "57357c1fdd522855",
			"type": "inject",
			"z": "524949a46aa74ae0",
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
			"payload": "100",
			"payloadType": "num",
			"x": 330,
			"y": 280,
			"wires": [
				[
					"325d1f5a448c2207"
				]
			]
		},
		{
			"id": "c8ed0c208a5c4861",
			"type": "inject",
			"z": "524949a46aa74ae0",
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
			"payload": "0",
			"payloadType": "num",
			"x": 330,
			"y": 340,
			"wires": [
				[
					"e19f66f0e913b410"
				]
			]
		},
		{
			"id": "090cb18ecaeb5165",
			"type": "inject",
			"z": "524949a46aa74ae0",
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
			"payload": "100",
			"payloadType": "num",
			"x": 330,
			"y": 380,
			"wires": [
				[
					"e19f66f0e913b410"
				]
			]
		}
	]
	
## RGB-led (advanced)

	[
		{
			"id": "ffa1b2fae0e89a3e",
			"type": "rpi-gpio out",
			"z": "d16962be0f87af64",
			"name": "R",
			"pin": "21",
			"set": "",
			"level": "0",
			"freq": "",
			"out": "pwm",
			"bcm": true,
			"x": 570,
			"y": 580,
			"wires": []
		},
		{
			"id": "554870b4ea8527f3",
			"type": "rpi-gpio out",
			"z": "d16962be0f87af64",
			"name": "G",
			"pin": "20",
			"set": "",
			"level": "0",
			"freq": "",
			"out": "pwm",
			"bcm": true,
			"x": 570,
			"y": 520,
			"wires": []
		},
		{
			"id": "f80ac0247cd6a333",
			"type": "rpi-gpio out",
			"z": "d16962be0f87af64",
			"name": "B",
			"pin": "16",
			"set": "",
			"level": "0",
			"freq": "",
			"out": "pwm",
			"bcm": true,
			"x": 570,
			"y": 460,
			"wires": []
		},
		{
			"id": "1c800be5dfd3d8e1",
			"type": "function",
			"z": "d16962be0f87af64",
			"name": "HEX to RGB",
			"func": "var hex = msg.payload\n\n// Parse hex value into three separate 2-digit hex values for red, green, and blue\n// Omit the #-character\nvar r = parseInt(hex.substring(1, 3), 16);\nvar g = parseInt(hex.substring(3, 5), 16);\nvar b = parseInt(hex.substring(5, 7), 16);\n\n// Map the values to percentage\nconst values = [r,g,b]\nconst valuesPercentage = values.map(x => x/255*100);\n\n// Prepare 3 messages with seperate percentages\nvar msg0 = {\"payload\":valuesPercentage[2]}\nvar msg1 = {\"payload\":valuesPercentage[1]}\nvar msg2 = {\"payload\":valuesPercentage[0]}\n\n// Return the messages to each output\nreturn [msg0, msg1, msg2];",
			"outputs": 3,
			"noerr": 0,
			"initialize": "",
			"finalize": "",
			"libs": [],
			"x": 370,
			"y": 520,
			"wires": [
				[
					"f80ac0247cd6a333"
				],
				[
					"554870b4ea8527f3"
				],
				[
					"ffa1b2fae0e89a3e"
				]
			]
		},
		{
			"id": "551bdaf8ff3e477d",
			"type": "inject",
			"z": "d16962be0f87af64",
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
			"payload": "#FF00FF",
			"payloadType": "str",
			"x": 160,
			"y": 480,
			"wires": [
				[
					"1c800be5dfd3d8e1"
				]
			]
		},
		{
			"id": "3c1dbcf68ccad300",
			"type": "inject",
			"z": "d16962be0f87af64",
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
			"payload": "#66CDAA",
			"payloadType": "str",
			"x": 160,
			"y": 520,
			"wires": [
				[
					"1c800be5dfd3d8e1"
				]
			]
		},
		{
			"id": "4d41f6ea15b6ef12",
			"type": "inject",
			"z": "d16962be0f87af64",
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
			"payload": "#00FF00",
			"payloadType": "str",
			"x": 160,
			"y": 440,
			"wires": [
				[
					"1c800be5dfd3d8e1"
				]
			]
		},
		{
			"id": "45842211584ed4cb",
			"type": "inject",
			"z": "d16962be0f87af64",
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
			"payload": "#FF0000",
			"payloadType": "str",
			"x": 160,
			"y": 560,
			"wires": [
				[
					"1c800be5dfd3d8e1"
				]
			]
		},
		{
			"id": "c6ce401359f09074",
			"type": "inject",
			"z": "d16962be0f87af64",
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
			"payload": "#FF69B4",
			"payloadType": "str",
			"x": 160,
			"y": 600,
			"wires": [
				[
					"1c800be5dfd3d8e1"
				]
			]
		}
	]




