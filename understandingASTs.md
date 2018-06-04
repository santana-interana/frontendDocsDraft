# What is an AST

In computer science, an abstract syntax tree (AST), or just syntax tree, is a tree representation of the abstract syntactic structure of source code written in a programming language. 

E.g.:

## run_query

### Request

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

### Response

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
## get_meatadata

### Request

```
{
	"waitSeconds": 60,
	"fromVersion": 96079,
	"requestedIds": []
}
```

### Response

```
{
	"requestedObjects": [
		{
			"columns": [
				{
					"measureIndex": 0,
					"dataType": {
						"isAggregable": false,
						"isList": false,
						"isGroupable": false,
						"basic": "INTEGER",
						"units": "EPOCH_MILLISECONDS"
					},
					"label": "MEASURE_VALUE",
					"timeOffsetIndex": 0
				},
				{
					"measureIndex": 1,
					"dataType": {
						"isAggregable": false,
						"stringNamespaceId": 2,
						"isGroupable": true,
						"basic": "STRING",
						"isList": false
					},
					"label": "MEASURE_VALUE",
					"timeOffsetIndex": 0
				},
				{
					"measureIndex": 2,
					"dataType": {
						"isAggregable": false,
						"stringNamespaceId": 49,
						"isGroupable": true,
						"basic": "STRING",
						"isList": false
					},
					"label": "MEASURE_VALUE",
					"timeOffsetIndex": 0
				}
			],
			"timespec": {
				"end": 1528070400000,
				"start": 1527465600000
			},
			"objectType": "QUERY_RESPONSE",
			"debug_info": {
				"checkpoints": [
					{
						"ast": {
							"timezone": "UTC",
							"processingStartTime": 1528140824,
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
							"dataType": {
								"basic": "UNDEFINED",
								"isList": false
							},
							"parentQueryResponseId": "r55359",
							"timeOffsets": [
								{
									"calendarHours": 0
								}
							],
							"allowSampling": true,
							"operation": "REQUEST",
							"queryId": "r55360",
							"outputTrees": [
								{
									"operation": "EXAMPLES_QUERY",
									"maxExampleRows": 100,
									"measures": [
										{
											"referenceId": "k4",
											"operation": "REFERENCE",
											"dataType": {
												"basic": "UNDEFINED",
												"isList": false
											}
										},
										{
											"referenceId": "k6",
											"operation": "REFERENCE",
											"dataType": {
												"basic": "UNDEFINED",
												"isList": false
											}
										},
										{
											"referenceId": "k50",
											"operation": "REFERENCE",
											"dataType": {
												"basic": "UNDEFINED",
												"isList": false
											}
										}
									],
									"timespec": {
										"end": {
											"setCalendarHour": [
												0
											],
											"origin": "NOW"
										},
										"isTimeBucketed": false,
										"start": {
											"setCalendarHour": [
												0
											],
											"origin": "NOW",
											"calendarDays": -7
										}
									},
									"dataType": {
										"basic": "UNDEFINED",
										"isList": false
									}
								}
							],
							"tableId": "t1"
						},
						"timestamp": 1528140824.0423317,
						"perf_info": {
							"num_scans": 0,
							"used_columns": []
						},
						"event_name": "query start"
					},
					{
						"timestamp": 1528140824.0937078,
						"event_name": "after expansion"
					},
					{
						"timestamp": 1528140824.1127825,
						"event_name": "after strings"
					},
					{
						"timestamp": 1528140824.2435899,
						"event_name": "after data servers"
					},
					{
						"timestamp": 1528140824.3377583,
						"event_name": "after result processing"
					}
				],
				"thriftObjects": [
					"tQuery(output_tables=['shard_merge_3'], event_table_selects={'event_table_1': tEventTableSelect(table=tEventTable(shard_column_id=None, time_windows=[tTimeWindow(start=1527465600000, width=604800000)], time_column_id=3, data_folders=['/var/lib/interana/data/datasets/f/1/2/ia-data-0', '/var/lib/interana/data/datasets/f/1/2/ia-data-1', '/var/lib/interana/data/datasets/f/1/2/ia-data-2', '/var/lib/interana/data/datasets/f/1/2/ia-data-3', '/var/lib/interana/data/datasets/f/1/2/ia-data-4', '/var/lib/interana/data/datasets/f/1/2/ia-data-5'], micro_shard_level=0), columns=['int_col(3)', 'int_col(2)', 'int_col(49)'])}, shard_merges={'shard_merge_3': tShardMerge(table='select_2')}, multiscan=True, readserver_oom_score_adj=500, scans=[], resource_limits=None, timeout_ms=180000, top_groups={}, string_agg_host='10.1.63.90', reduces={}, min_number_of_shard_groups=16, joins={}, shards_in_shard_group=None, flow_scans={}, progress_update_period_ms=1000, aggregation_scans={}, rod_config=None, unions={}, table_model=True, id=55360, priority=0, max_groups=100, timeout_projection_window_ms=0, string_agg_port=8600, funnels={}, lookup_columns={}, compile_flows=True, funnel_columns={}, flows=None, time_merges={}, random_streams={}, deadline_ms=10000, computed_columns={}, sorts={}, timeout_projection_ms=30000, max_groups_per_shard=50000, shards=[tLeaf(shard_id=0, port=8500, host='10.1.63.90'), tLeaf(shard_id=1, port=8500, host='10.1.63.90'), tLeaf(shard_id=2, port=8500, host='10.1.63.90'), tLeaf(shard_id=3, port=8500, host='10.1.63.90'), tLeaf(shard_id=4, port=8500, host='10.1.63.90'), tLeaf(shard_id=5, port=8500, host='10.1.63.90')], selects={'select_2': tSelectColumns(table='event_table_1', filter=None, limit=100, columns=['v(0)', 'v(1)', 'v(2)'])}, orderby_config=None, flow_columns=None)"
				],
				"dataserverResults": {
					"full_query": {
						"perf.tag.funnel": "",
						"leaves_used": 1,
						"rows_examined": 1236,
						"perf.wall_ns.data_leaf": 91066215,
						"perf.cpu_ns.readserver": 42313284,
						"error": "",
						"perf.bytes.memory.data_leaf": 185528320,
						"disk_bytes_mapped": 75794,
						"perf.tag.flow": "",
						"cores_used": 16,
						"perf.tag.group_by": "",
						"cpu_sys_ms": 12,
						"cpu_u_ms": 48,
						"wall_ms": 90,
						"rows_filtered_to": 0,
						"perf.num.cores": 16,
						"perf.tag.cohort": "",
						"perf.num.columns": 2,
						"shards_used": 6,
						"perf.num.nodes": 1
					},
					"leaf_info": [
						{
							"recv_ms": 88,
							"debug": {
								"leaves_used": 1,
								"rows_examined": 1236,
								"error": "",
								"wall_ms": 85,
								"rows_filtered_to": 0,
								"cpu_u_ms": 44,
								"shards_used": 6,
								"disk_bytes_mapped": 75794,
								"cpu_sys_ms": 36,
								"cores_used": 16
							},
							"leaf": "10.1.63.90"
						}
					]
				}
			},
			"rows": [
				[
					1527825876563,
					"maverick@interana.com",
					"select_dataspace"
				],
				[
					1527886770690,
					"maverick@interana.com",
					"select_for_filter_event"
				],
				[
					1527887394232,
					"maverick@interana.com",
					"run_query"
				],
				[
					1527887405336,
					"maverick@interana.com",
					"run_query"
				],
				[
					1527887455129,
					"maverick@interana.com",
					"click_boards_button"
				],
				[
					1527634228209,
					"robin@interana.com",
					"select_split_by"
				],
				[
					1527634231651,
					"robin@interana.com",
					"clear_split_by"
				],
				[
					1527634275380,
					"robin@interana.com",
					"remove_measure"
				],
				[
					1527644697092,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527644697362,
					"barykin@interana.com",
					"run_query"
				],
				[
					1527644736821,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527644759693,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527644773509,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527644785109,
					"barykin@interana.com",
					"select_aggregation_target"
				],
				[
					1527644786648,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527644797436,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527644817053,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527645893105,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527645899559,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527645920665,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527645931373,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527645953723,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527645966112,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527645973322,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527645976504,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527645976532,
					"barykin@interana.com",
					"run_query"
				],
				[
					1527645990526,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527645998361,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527646008292,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527646018474,
					"barykin@interana.com",
					"select_aggregation_target"
				],
				[
					1527646021050,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527646027298,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527646033824,
					"barykin@interana.com",
					"select_aggregation_step"
				],
				[
					1527646035214,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527646035470,
					"barykin@interana.com",
					"run_query"
				],
				[
					1527646058216,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527646058474,
					"barykin@interana.com",
					"run_query"
				],
				[
					1527646693822,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527646694100,
					"barykin@interana.com",
					"run_query"
				],
				[
					1527646723671,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527646723973,
					"barykin@interana.com",
					"run_query"
				],
				[
					1527710278650,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710278901,
					"barykin@interana.com",
					"run_query"
				],
				[
					1527710310439,
					"barykin@interana.com",
					"select_aggregation_target"
				],
				[
					1527710312109,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710325722,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710344588,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710345138,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710354215,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710372108,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710396875,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710554069,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710574302,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710631797,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710670584,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710681146,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710687507,
					"barykin@interana.com",
					"select_aggregation_step"
				],
				[
					1527710691900,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710692172,
					"barykin@interana.com",
					"run_query"
				],
				[
					1527710696639,
					"barykin@interana.com",
					"select_aggregation_target"
				],
				[
					1527710697984,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710698248,
					"barykin@interana.com",
					"run_query"
				],
				[
					1527710713231,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710762814,
					"barykin@interana.com",
					"select_aggregation_target"
				],
				[
					1527710764091,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710775249,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710781864,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527710796534,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527815735583,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527815740934,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527815741200,
					"barykin@interana.com",
					"run_query"
				],
				[
					1527815753788,
					"barykin@interana.com",
					"click_explorer_go_button"
				],
				[
					1527494337902,
					"test@interana.com",
					"click_help_button"
				],
				[
					1527494430507,
					"test@interana.com",
					"click_boards_button"
				],
				[
					1527494440659,
					"test@interana.com",
					"click_boards_button"
				],
				[
					1527494500285,
					"test@interana.com",
					"click_boards_button"
				],
				[
					1527494500574,
					"test@interana.com",
					"click_boards_button"
				],
				[
					1527494605915,
					"test@interana.com",
					"run_query"
				],
				[
					1527494607256,
					"test@interana.com",
					"run_query_sampled"
				],
				[
					1527496279272,
					"test@interana.com",
					"run_query_sampled"
				],
				[
					1527497049104,
					"test@interana.com",
					"run_query"
				],
				[
					1527497051855,
					"test@interana.com",
					"run_query_sampled"
				],
				[
					1527497063473,
					"test@interana.com",
					"run_query"
				],
				[
					1527497065234,
					"test@interana.com",
					"run_query_sampled"
				],
				[
					1527497076080,
					"test@interana.com",
					"run_query"
				],
				[
					1527497078261,
					"test@interana.com",
					"run_query_sampled"
				],
				[
					1527563296310,
					"test@interana.com",
					"run_query_sampled"
				],
				[
					1527563304684,
					"test@interana.com",
					"run_query"
				],
				[
					1527563308768,
					"test@interana.com",
					"run_query_sampled"
				],
				[
					1527563373064,
					"test@interana.com",
					"run_query_sampled"
				],
				[
					1527563373720,
					"test@interana.com",
					"run_query"
				],
				[
					1527563414227,
					"test@interana.com",
					"select_split_by"
				],
				[
					1527563416205,
					"test@interana.com",
					"run_query"
				],
				[
					1527563434192,
					"test@interana.com",
					"clear_split_by"
				],
				[
					1527563440327,
					"test@interana.com",
					"toggle_table_view"
				],
				[
					1527563450555,
					"test@interana.com",
					"select_split_by"
				],
				[
					1527563468692,
					"test@interana.com",
					"select_aggregation_step"
				],
				[
					1527563490693,
					"test@interana.com",
					"select_aggregation_step"
				],
				[
					1527602030724,
					"test@interana.com",
					"click_boards_button"
				],
				[
					1527602053166,
					"test@interana.com",
					"select_dataspace"
				]
			],
			"id": "r55360",
			"success": true,
			"queryInfo": {
				"rowsExamined": 1236,
				"cpuSysMs": 12,
				"shardsRequested": 6,
				"wallMs": 90,
				"error": "",
				"leavesUsed": 1,
				"diskBytesMapped": 75794,
				"shardsTotal": 24,
				"rowsFilteredTo": 0,
				"coresUsed": 16,
				"cpuUMs": 48,
				"shardsUsed": 6
			},
			"timestamp": 1528140824000,
			"table": {
				"columns": [
					{
						"id": "k49",
						"dataType": {
							"isAggregable": false,
							"stringNamespaceId": 49,
							"isGroupable": true,
							"basic": "STRING"
						},
						"lastUpdatedTime": 1523986536000,
						"operation": "COLUMN",
						"createdTime": 1523986536000,
						"name": "action"
					},
					{
						"id": "k3",
						"dataType": {
							"isAggregable": false,
							"isGroupable": false,
							"basic": "INTEGER",
							"units": "EPOCH_MILLISECONDS"
						},
						"lastUpdatedTime": 1523924066000,
						"operation": "COLUMN",
						"createdTime": 1523924066000,
						"name": "__time__"
					},
					{
						"id": "k2",
						"dataType": {
							"isAggregable": false,
							"stringNamespaceId": 2,
							"isGroupable": true,
							"basic": "STRING"
						},
						"lastUpdatedTime": 1523924066000,
						"operation": "COLUMN",
						"createdTime": 1523924066000,
						"name": "username"
					}
				],
				"id": "t1",
				"contexts": [
					{
						"referenceId": "k49",
						"lastUpdatedByUserId": "u4",
						"id": "k50",
						"lastUpdatedTime": 1524163961000,
						"operation": "REFERENCE",
						"createdTime": 1523986536000,
						"name": "action"
					},
					{
						"referenceId": "k3",
						"lastUpdatedByUserId": "u4",
						"id": "k4",
						"lastUpdatedTime": 1524163953000,
						"operation": "REFERENCE",
						"createdTime": 1523924066000,
						"name": "__time__"
					},
					{
						"referenceId": "k2",
						"lastUpdatedByUserId": "u4",
						"id": "k6",
						"lastUpdatedTime": 1526074272000,
						"operation": "REFERENCE",
						"createdTime": 1523924066000,
						"name": "username"
					}
				],
				"name": "3.x usage"
			},
			"queryRequestId": "q51430"
		},
		{
			"measures": [
				{
					"referenceId": "k4",
					"operation": "REFERENCE"
				},
				{
					"referenceId": "k6",
					"operation": "REFERENCE"
				},
				{
					"referenceId": "k50",
					"operation": "REFERENCE"
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
			"queryRole": "EXPLORE_EXAMPLE",
			"objectType": "QUERY_REQUEST",
			"maxExampleRows": 100,
			"queryType": "EXAMPLE_EVENTS",
			"requestedIds": [],
			"id": "q51430",
			"timezone": "UTC",
			"parentQueryResponseId": "r55359",
			"allowSampling": true,
			"chartOptions": {
				"chartType": "TABLE"
			},
			"tableId": "t1"
		}
	],
	"explorerQueryResponseIds": [],
	"version": 96081,
	"fromVersion": 96079,
	"currentUserId": "u4",
	"boards": [],
	"panels": [],
	"success": true,
	"tables": [],
	"users": [],
	"config": {
		"showMetricBuilder": true,
		"showAppVersion": true,
		"showBoards": true
	}
}
```
