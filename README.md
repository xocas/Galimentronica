# Galimentronica
Proxecto PIT Galimentronica
codigo json para node red
[
    {
        "id": "cd8981348ee847cd",
        "type": "tab",
        "label": "Galinheiro v_1",
        "disabled": false,
        "info": "",
        "env": []
    },
    {
        "id": "20fd55bcea130118",
        "type": "ui_gauge",
        "z": "cd8981348ee847cd",
        "name": "",
        "group": "254328a200fa1097",
        "order": 2,
        "width": "4",
        "height": "4",
        "gtype": "gage",
        "title": "Luz",
        "label": "units",
        "format": "{{value}}",
        "min": 0,
        "max": "4000",
        "colors": [
            "#111100",
            "#2f9f9c",
            "#c2f2fc"
        ],
        "seg1": "",
        "seg2": "",
        "diff": false,
        "className": "",
        "x": 490,
        "y": 160,
        "wires": []
    },
    {
        "id": "b28a4b65f9a1469c",
        "type": "mqtt in",
        "z": "cd8981348ee847cd",
        "name": "Alarma",
        "topic": "Galinheiro_alarma",
        "qos": "1",
        "datatype": "auto-detect",
        "broker": "a8eacf02c1d45c1c",
        "nl": false,
        "rap": true,
        "rh": 0,
        "inputs": 0,
        "x": 110,
        "y": 220,
        "wires": [
            [
                "ead096d8907f3fd3"
            ]
        ]
    },
    {
        "id": "989a6a17869db46c",
        "type": "mqtt in",
        "z": "cd8981348ee847cd",
        "name": "",
        "topic": "Galinheiro_luz",
        "qos": "2",
        "datatype": "auto-detect",
        "broker": "be320fbad88613a9",
        "nl": false,
        "rap": true,
        "rh": 0,
        "inputs": 0,
        "x": 130,
        "y": 160,
        "wires": [
            [
                "20fd55bcea130118"
            ]
        ]
    },
    {
        "id": "f5eebf0f86482b20",
        "type": "mqtt in",
        "z": "cd8981348ee847cd",
        "name": "Dia Alarma",
        "topic": "Galinheiro_dia_alarma",
        "qos": "1",
        "datatype": "auto-detect",
        "broker": "a8eacf02c1d45c1c",
        "nl": false,
        "rap": true,
        "rh": 0,
        "inputs": 0,
        "x": 120,
        "y": 260,
        "wires": [
            [
                "99e080d3e8dee556"
            ]
        ]
    },
    {
        "id": "7b403a1f43055a34",
        "type": "mqtt in",
        "z": "cd8981348ee847cd",
        "name": "Hora Alarma",
        "topic": "Galinheiro_hora_alarma",
        "qos": "1",
        "datatype": "auto-detect",
        "broker": "a8eacf02c1d45c1c",
        "nl": false,
        "rap": true,
        "rh": 0,
        "inputs": 0,
        "x": 130,
        "y": 320,
        "wires": [
            [
                "2dafb46756d42d34"
            ]
        ]
    },
    {
        "id": "ac1b82f8b195156a",
        "type": "mqtt in",
        "z": "cd8981348ee847cd",
        "name": "Bateria",
        "topic": "Galinheiro_bat",
        "qos": "1",
        "datatype": "auto-detect",
        "broker": "a8eacf02c1d45c1c",
        "nl": false,
        "rap": true,
        "rh": 0,
        "inputs": 0,
        "x": 110,
        "y": 380,
        "wires": [
            [
                "fadc04896c1b5129"
            ]
        ]
    },
    {
        "id": "7d5e559bc52d0982",
        "type": "mqtt in",
        "z": "cd8981348ee847cd",
        "name": "Auga",
        "topic": "Galinheiro_auga",
        "qos": "1",
        "datatype": "auto-detect",
        "broker": "a8eacf02c1d45c1c",
        "nl": false,
        "rap": true,
        "rh": 0,
        "inputs": 0,
        "x": 110,
        "y": 520,
        "wires": [
            [
                "3ba2f1c894c11846"
            ]
        ]
    },
    {
        "id": "99e080d3e8dee556",
        "type": "ui_text",
        "z": "cd8981348ee847cd",
        "group": "4fe8d0fa457467f4",
        "order": 5,
        "width": 0,
        "height": 0,
        "name": "",
        "label": "Dia Alarma:",
        "format": "{{msg.payload}}",
        "layout": "row-left",
        "className": "",
        "x": 510,
        "y": 280,
        "wires": []
    },
    {
        "id": "2dafb46756d42d34",
        "type": "ui_text",
        "z": "cd8981348ee847cd",
        "group": "4fe8d0fa457467f4",
        "order": 6,
        "width": 0,
        "height": 0,
        "name": "",
        "label": "Hora Alarma:",
        "format": "{{msg.payload}}",
        "layout": "row-left",
        "className": "",
        "x": 510,
        "y": 340,
        "wires": []
    },
    {
        "id": "fadc04896c1b5129",
        "type": "ui_gauge",
        "z": "cd8981348ee847cd",
        "name": "",
        "group": "254328a200fa1097",
        "order": 3,
        "width": "4",
        "height": "4",
        "gtype": "gage",
        "title": "Bateria",
        "label": "% de batería",
        "format": "{{value}}",
        "min": 0,
        "max": "100",
        "colors": [
            "#ff0f09",
            "#ffff00",
            "#00ff00"
        ],
        "seg1": "",
        "seg2": "",
        "diff": false,
        "className": "",
        "x": 520,
        "y": 400,
        "wires": []
    },
    {
        "id": "3ba2f1c894c11846",
        "type": "ui_led",
        "z": "cd8981348ee847cd",
        "order": 1,
        "group": "4fe8d0fa457467f4",
        "width": 0,
        "height": 0,
        "label": "Auga Galiñeiro",
        "labelPlacement": "left",
        "labelAlignment": "center",
        "colorForValue": [
            {
                "color": "#ff0000",
                "value": "0",
                "valueType": "num"
            },
            {
                "color": "#008000",
                "value": "1",
                "valueType": "num"
            }
        ],
        "allowColorForValueInMessage": false,
        "shape": "circle",
        "showGlow": true,
        "name": "Auga Galiñeiro",
        "x": 560,
        "y": 520,
        "wires": []
    },
    {
        "id": "ead096d8907f3fd3",
        "type": "ui_led",
        "z": "cd8981348ee847cd",
        "order": 2,
        "group": "4fe8d0fa457467f4",
        "width": 0,
        "height": 0,
        "label": "Alarma intrusion",
        "labelPlacement": "left",
        "labelAlignment": "left",
        "colorForValue": [
            {
                "color": "#ff0000",
                "value": "1",
                "valueType": "num"
            },
            {
                "color": "#008000",
                "value": "0",
                "valueType": "num"
            }
        ],
        "allowColorForValueInMessage": false,
        "shape": "circle",
        "showGlow": true,
        "name": "Alarma",
        "x": 500,
        "y": 220,
        "wires": []
    },
    {
        "id": "8f5e988d54e94a13",
        "type": "mqtt in",
        "z": "cd8981348ee847cd",
        "name": "Hora do Galiñeiro",
        "topic": "Galinheiro_hora_actual",
        "qos": "1",
        "datatype": "auto-detect",
        "broker": "a8eacf02c1d45c1c",
        "nl": false,
        "rap": true,
        "rh": 0,
        "inputs": 0,
        "x": 150,
        "y": 580,
        "wires": [
            [
                "4568d3129e61e754"
            ]
        ]
    },
    {
        "id": "76f482f1a9749849",
        "type": "mqtt in",
        "z": "cd8981348ee847cd",
        "name": "Data do galiñeiro",
        "topic": "Galinheiro_data_actual",
        "qos": "1",
        "datatype": "auto-detect",
        "broker": "a8eacf02c1d45c1c",
        "nl": false,
        "rap": true,
        "rh": 0,
        "inputs": 0,
        "x": 140,
        "y": 640,
        "wires": [
            [
                "4a302becb669a9fd"
            ]
        ]
    },
    {
        "id": "4568d3129e61e754",
        "type": "ui_text",
        "z": "cd8981348ee847cd",
        "group": "4fe8d0fa457467f4",
        "order": 4,
        "width": 0,
        "height": 0,
        "name": "Hora do galiñeiro",
        "label": "Hora do galiñeiro:",
        "format": "{{msg.payload}}",
        "layout": "row-left",
        "className": "",
        "x": 530,
        "y": 580,
        "wires": []
    },
    {
        "id": "4a302becb669a9fd",
        "type": "ui_text",
        "z": "cd8981348ee847cd",
        "group": "4fe8d0fa457467f4",
        "order": 3,
        "width": 0,
        "height": 0,
        "name": "Día do galiñeiro",
        "label": "Dia do Galiñeiro",
        "format": "{{msg.payload}}",
        "layout": "row-left",
        "className": "",
        "x": 520,
        "y": 640,
        "wires": []
    },
    {
        "id": "74ba80115bd8d0f3",
        "type": "mqtt in",
        "z": "cd8981348ee847cd",
        "name": "Alimento",
        "topic": "Galinheiro_alimento",
        "qos": "1",
        "datatype": "auto-detect",
        "broker": "a8eacf02c1d45c1c",
        "nl": false,
        "rap": true,
        "rh": 0,
        "inputs": 0,
        "x": 140,
        "y": 440,
        "wires": [
            [
                "94edbd95f2218b74"
            ]
        ]
    },
    {
        "id": "94edbd95f2218b74",
        "type": "ui_gauge",
        "z": "cd8981348ee847cd",
        "name": "Alimento",
        "group": "254328a200fa1097",
        "order": 1,
        "width": "4",
        "height": "4",
        "gtype": "gage",
        "title": "Alimento",
        "label": "% de Grao",
        "format": "{{value}}",
        "min": 0,
        "max": "100",
        "colors": [
            "#ff0f09",
            "#ffff00",
            "#00ff00"
        ],
        "seg1": "",
        "seg2": "",
        "diff": false,
        "className": "",
        "x": 520,
        "y": 460,
        "wires": []
    },
    {
        "id": "2d1139b8c4c1a1f2",
        "type": "mqtt in",
        "z": "cd8981348ee847cd",
        "name": "",
        "topic": "Incubadora_temperatura",
        "qos": "2",
        "datatype": "auto-detect",
        "broker": "be320fbad88613a9",
        "nl": false,
        "rap": true,
        "rh": 0,
        "inputs": 0,
        "x": 150,
        "y": 720,
        "wires": [
            [
                "30a74c9795a4c075",
                "836a10c575cb0eac"
            ]
        ]
    },
    {
        "id": "1f8f92f7e5fb026e",
        "type": "mqtt in",
        "z": "cd8981348ee847cd",
        "name": "",
        "topic": "Incubadora_humedad",
        "qos": "2",
        "datatype": "auto-detect",
        "broker": "be320fbad88613a9",
        "nl": false,
        "rap": true,
        "rh": 0,
        "inputs": 0,
        "x": 140,
        "y": 800,
        "wires": [
            [
                "1be7e840291dc09c",
                "4abe3d19cacdc2fa"
            ]
        ]
    },
    {
        "id": "30a74c9795a4c075",
        "type": "ui_gauge",
        "z": "cd8981348ee847cd",
        "name": "",
        "group": "6490c83f1c89f49b",
        "order": 1,
        "width": "3",
        "height": "3",
        "gtype": "gage",
        "title": "Temperatura",
        "label": "Grados",
        "format": "{{value}}",
        "min": 0,
        "max": "50",
        "colors": [
            "#ff0f09",
            "#ffff00",
            "#00ff00"
        ],
        "seg1": "",
        "seg2": "",
        "diff": false,
        "className": "",
        "x": 510,
        "y": 720,
        "wires": []
    },
    {
        "id": "1be7e840291dc09c",
        "type": "ui_gauge",
        "z": "cd8981348ee847cd",
        "name": "",
        "group": "6490c83f1c89f49b",
        "order": 2,
        "width": "3",
        "height": "3",
        "gtype": "gage",
        "title": "Humedade",
        "label": "% Humedad relativa",
        "format": "{{value}}",
        "min": 0,
        "max": "100",
        "colors": [
            "#ff0f09",
            "#ffff00",
            "#00ff00"
        ],
        "seg1": "",
        "seg2": "",
        "diff": false,
        "className": "",
        "x": 510,
        "y": 840,
        "wires": []
    },
    {
        "id": "23276a4e833da19a",
        "type": "mqtt in",
        "z": "cd8981348ee847cd",
        "name": "",
        "topic": "Criadora_temperatura",
        "qos": "2",
        "datatype": "auto-detect",
        "broker": "be320fbad88613a9",
        "nl": false,
        "rap": true,
        "rh": 0,
        "inputs": 0,
        "x": 140,
        "y": 960,
        "wires": [
            [
                "5056baa0925de5fc",
                "1198f9b6b6be48da"
            ]
        ]
    },
    {
        "id": "5056baa0925de5fc",
        "type": "ui_gauge",
        "z": "cd8981348ee847cd",
        "name": "",
        "group": "46ca8bda11589e74",
        "order": 2,
        "width": 0,
        "height": 0,
        "gtype": "gage",
        "title": "Temperatura criadora",
        "label": "units",
        "format": "{{value}}",
        "min": "10",
        "max": "50",
        "colors": [
            "#00b500",
            "#e6e600",
            "#ca3838"
        ],
        "seg1": "",
        "seg2": "",
        "diff": false,
        "className": "",
        "x": 540,
        "y": 980,
        "wires": []
    },
    {
        "id": "1198f9b6b6be48da",
        "type": "ui_chart",
        "z": "cd8981348ee847cd",
        "name": "",
        "group": "46ca8bda11589e74",
        "order": 3,
        "width": 0,
        "height": 0,
        "label": "Historico Criadora",
        "chartType": "line",
        "legend": "false",
        "xformat": "HH:mm:ss",
        "interpolate": "linear",
        "nodata": "",
        "dot": false,
        "ymin": "10",
        "ymax": "50",
        "removeOlder": 1,
        "removeOlderPoints": "",
        "removeOlderUnit": "3600",
        "cutout": 0,
        "useOneColor": false,
        "useUTC": false,
        "colors": [
            "#1f77b4",
            "#aec7e8",
            "#ff7f0e",
            "#2ca02c",
            "#98df8a",
            "#d62728",
            "#ff9896",
            "#9467bd",
            "#c5b0d5"
        ],
        "outputs": 1,
        "useDifferentColor": false,
        "className": "",
        "x": 550,
        "y": 1040,
        "wires": [
            []
        ]
    },
    {
        "id": "836a10c575cb0eac",
        "type": "ui_chart",
        "z": "cd8981348ee847cd",
        "name": "",
        "group": "6490c83f1c89f49b",
        "order": 3,
        "width": 0,
        "height": 0,
        "label": "Rexistro de temperatura",
        "chartType": "line",
        "legend": "false",
        "xformat": "HH:mm:ss",
        "interpolate": "linear",
        "nodata": "",
        "dot": false,
        "ymin": "10",
        "ymax": "50",
        "removeOlder": 1,
        "removeOlderPoints": "",
        "removeOlderUnit": "3600",
        "cutout": 0,
        "useOneColor": false,
        "useUTC": false,
        "colors": [
            "#1f77b4",
            "#aec7e8",
            "#ff7f0e",
            "#2ca02c",
            "#98df8a",
            "#d62728",
            "#ff9896",
            "#9467bd",
            "#c5b0d5"
        ],
        "outputs": 1,
        "useDifferentColor": false,
        "className": "",
        "x": 570,
        "y": 760,
        "wires": [
            []
        ]
    },
    {
        "id": "4abe3d19cacdc2fa",
        "type": "ui_chart",
        "z": "cd8981348ee847cd",
        "name": "",
        "group": "6490c83f1c89f49b",
        "order": 4,
        "width": 0,
        "height": 0,
        "label": "Rexistro de humedade",
        "chartType": "line",
        "legend": "false",
        "xformat": "HH:mm:ss",
        "interpolate": "linear",
        "nodata": "",
        "dot": false,
        "ymin": "30",
        "ymax": "100",
        "removeOlder": 1,
        "removeOlderPoints": "",
        "removeOlderUnit": "3600",
        "cutout": 0,
        "useOneColor": false,
        "useUTC": false,
        "colors": [
            "#1f77b4",
            "#aec7e8",
            "#ff7f0e",
            "#2ca02c",
            "#98df8a",
            "#d62728",
            "#ff9896",
            "#9467bd",
            "#c5b0d5"
        ],
        "outputs": 1,
        "useDifferentColor": false,
        "className": "",
        "x": 540,
        "y": 880,
        "wires": [
            []
        ]
    },
    {
        "id": "2776fb0d05c00595",
        "type": "mqtt in",
        "z": "cd8981348ee847cd",
        "name": "",
        "topic": "Criadora_auga",
        "qos": "2",
        "datatype": "auto-detect",
        "broker": "be320fbad88613a9",
        "nl": false,
        "rap": true,
        "rh": 0,
        "inputs": 0,
        "x": 120,
        "y": 1100,
        "wires": [
            [
                "6e6e51adfe8dbe2a"
            ]
        ]
    },
    {
        "id": "6e6e51adfe8dbe2a",
        "type": "ui_led",
        "z": "cd8981348ee847cd",
        "order": 1,
        "group": "46ca8bda11589e74",
        "width": 0,
        "height": 0,
        "label": "Auga Criadora",
        "labelPlacement": "left",
        "labelAlignment": "center",
        "colorForValue": [
            {
                "color": "#ff0000",
                "value": "0",
                "valueType": "num"
            },
            {
                "color": "#008000",
                "value": "1",
                "valueType": "num"
            }
        ],
        "allowColorForValueInMessage": false,
        "shape": "circle",
        "showGlow": true,
        "name": "Auga Criadora",
        "x": 540,
        "y": 1140,
        "wires": []
    },
    {
        "id": "254328a200fa1097",
        "type": "ui_group",
        "name": "Galiñeiro",
        "tab": "38bf9be2a25a6c9a",
        "order": 3,
        "disp": true,
        "width": "6",
        "collapse": false,
        "className": ""
    },
    {
        "id": "a8eacf02c1d45c1c",
        "type": "mqtt-broker",
        "name": "test.mosquitto.org:1884",
        "broker": "test.mosquitto.org:1884",
        "port": "1884",
        "clientid": "",
        "autoConnect": true,
        "usetls": false,
        "protocolVersion": "4",
        "keepalive": "60",
        "cleansession": true,
        "birthTopic": "",
        "birthQos": "0",
        "birthPayload": "",
        "birthMsg": {},
        "closeTopic": "",
        "closeQos": "0",
        "closePayload": "",
        "closeMsg": {},
        "willTopic": "",
        "willQos": "0",
        "willPayload": "",
        "willMsg": {},
        "userProps": "",
        "sessionExpiry": ""
    },
    {
        "id": "be320fbad88613a9",
        "type": "mqtt-broker",
        "name": "test.mosquitto.org:1884",
        "broker": "test.mosquitto.org:1884",
        "port": "1884",
        "clientid": "",
        "autoConnect": true,
        "usetls": false,
        "protocolVersion": "4",
        "keepalive": "60",
        "cleansession": true,
        "birthTopic": "",
        "birthQos": "0",
        "birthPayload": "",
        "birthMsg": {},
        "closeTopic": "",
        "closeQos": "0",
        "closePayload": "",
        "closeMsg": {},
        "willTopic": "",
        "willQos": "0",
        "willPayload": "",
        "willMsg": {},
        "userProps": "",
        "sessionExpiry": ""
    },
    {
        "id": "4fe8d0fa457467f4",
        "type": "ui_group",
        "name": "Estado das alarmas",
        "tab": "38bf9be2a25a6c9a",
        "order": 4,
        "disp": true,
        "width": "6",
        "collapse": false,
        "className": ""
    },
    {
        "id": "6490c83f1c89f49b",
        "type": "ui_group",
        "name": "Incubadora",
        "tab": "38bf9be2a25a6c9a",
        "order": 1,
        "disp": true,
        "width": "6",
        "collapse": false,
        "className": ""
    },
    {
        "id": "46ca8bda11589e74",
        "type": "ui_group",
        "name": "Criadora",
        "tab": "38bf9be2a25a6c9a",
        "order": 2,
        "disp": true,
        "width": "6",
        "collapse": false,
        "className": ""
    },
    {
        "id": "38bf9be2a25a6c9a",
        "type": "ui_tab",
        "name": "Proxecto Galimentrónica. Incubadora e Galiñeiro Automatizado",
        "icon": "dashboard",
        "disabled": false,
        "hidden": false
    }
]
