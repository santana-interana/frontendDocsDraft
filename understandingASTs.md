# What is an AST

In computer science, an abstract syntax tree (AST), or just syntax tree, is a tree representation of the abstract syntactic structure of source code written in a programming language. 

E.g.:

## Request

```
{
	"requestedIds": [],
	"fromVersion": 96077,
	"tableId": "t1",
	"timezone": "UTC",
	"timespec": {
		"start": {
			"origin": "NOW",
			"calendarDays": -7,
			"setCalendarHour": [
				0
			]
		},
		"end": {
			"origin": "NOW",
			"setCalendarHour": [
				0
			]
		},
		"isTimeBucketed": true,
		"resolution": {
			"calendarDays": 1,
			"isAuto": true
		},
		"trailingWindow": {
			"calendarDays": 1,
			"isAuto": true
		}
	},
	"timeOffsets": [
		{
			"calendarWeeks": 0
		}
	],
	"measures": [
		{
			"name": "set 1",
			"operation": "COUNT"
		}
	],
	"chartOptions": {
		"chartType": "TIME",
		"multipleAxes": false,
		"tableSort": [],
		"stackBarsById": null
	},
	"allowSampling": true,
	"queryRole": "EXPLORE",
	"maxGroups": 10,
	"orderBy": [
		{
			"operation": "ORDER_ELEMENT",
			"operand": {
				"operation": "MEASURE_REFERENCE",
				"measureIndex": 0
			}
		}
	]
}
```

## Response

```
{
	"requestedObjects": [
		{
			"timestamp": 1528140823000,
			"objectType": "QUERY_RESPONSE",
			"id": "r55359",
			"queryRequestId": "q51429"
		},
		{
			"measures": [
				{
					"operation": "COUNT",
					"name": "set 1"
				}
			],
			"timespec": {
				"resolution": {
					"isAuto": true,
					"calendarDays": 1
				},
				"end": {
					"setCalendarHour": [
						0
					],
					"origin": "NOW"
				},
				"isTimeBucketed": true,
				"start": {
					"setCalendarHour": [
						0
					],
					"origin": "NOW",
					"calendarDays": -7
				},
				"trailingWindow": {
					"isAuto": true,
					"calendarDays": 1
				}
			},
			"maxGroups": 10,
			"queryRole": "EXPLORE",
			"objectType": "QUERY_REQUEST",
			"requestedIds": [],
			"id": "q51429",
			"timezone": "UTC",
			"orderBy": [
				{
					"operation": "ORDER_ELEMENT",
					"operand": {
						"operation": "MEASURE_REFERENCE",
						"measureIndex": 0
					}
				}
			],
			"timeOffsets": [
				{
					"calendarWeeks": 0
				}
			],
			"allowSampling": true,
			"chartOptions": {
				"stackBarsById": null,
				"multipleAxes": false,
				"chartType": "TIME",
				"tableSort": []
			},
			"tableId": "t1"
		}
	],
	"explorerQueryResponseIds": [],
	"version": 96078,
	"fromVersion": 96077,
	"currentUserId": "u4",
	"boards": [],
	"panels": [],
	"queryResponseId": "r55359",
	"success": true,
	"tables": [],
	"users": [],
	"config": {
		"showMetricBuilder": true,
		"showAppVersion": true,
		"showBoards": true
	},
	"queryRequestId": "q51429"
}
```
