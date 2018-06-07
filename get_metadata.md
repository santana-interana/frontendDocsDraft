```
{
	"boards": [],
	"currentUserId": "u3",
	"success": true,
	"panels": [],
	"requestedObjects": [
		{
			"queryRequestId": "q346",
			"debug_info": {
				"checkpoints": [
					{
						"perf_info": {
							"used_columns": [],
							"num_scans": 1
						},
						"event_name": "query start",
						"ast": {
							"allowSampling": true,
							"operation": "REQUEST",
							"outputTrees": [
								{
									"dataType": {
										"basic": "UNDEFINED",
										"isList": false
									},
									"orderBy": [
										{
											"dataType": {
												"basic": "UNDEFINED",
												"isList": false
											},
											"operand": {
												"dataType": {
													"basic": "UNDEFINED",
													"isList": false
												},
												"operation": "MEASURE_REFERENCE",
												"measureIndex": 0
											},
											"operation": "ORDER_ELEMENT"
										}
									],
									"operation": "OUTPUT_QUERY",
									"measures": [
										{
											"dataType": {
												"basic": "UNDEFINED",
												"isList": false
											},
											"operation": "COUNT"
										}
									],
									"timespec": {
										"end": {
											"origin": "NOW",
											"setCalendarHour": [
												0
											]
										},
										"trailingWindow": {
											"isAuto": true,
											"calendarDays": 1
										},
										"isTimeBucketed": true,
										"start": {
											"origin": "NOW",
											"setCalendarHour": [
												0
											],
											"calendarDays": -7
										},
										"resolution": {
											"isAuto": true,
											"calendarDays": 1
										}
									}
								}
							],
							"timezone": "UTC",
							"timespec": {
								"end": {
									"origin": "NOW",
									"setCalendarHour": [
										0
									]
								},
								"trailingWindow": {
									"isAuto": true,
									"calendarDays": 1
								},
								"isTimeBucketed": true,
								"start": {
									"origin": "NOW",
									"setCalendarHour": [
										0
									],
									"calendarDays": -7
								},
								"resolution": {
									"isAuto": true,
									"calendarDays": 1
								}
							},
							"tableId": "t1",
							"dataType": {
								"basic": "UNDEFINED",
								"isList": false
							},
							"queryId": "r346",
							"processingStartTime": 1528344512,
							"timeOffsets": [
								{
									"calendarWeeks": 0
								}
							]
						},
						"timestamp": 1528344513.0936766
					},
					{
						"event_name": "after expansion",
						"timestamp": 1528344513.1552114
					},
					{
						"event_name": "after strings",
						"timestamp": 1528344513.3294728
					},
					{
						"event_name": "after data servers",
						"timestamp": 1528344513.558051
					},
					{
						"event_name": "after result processing",
						"timestamp": 1528344513.6020112
					}
				],
				"thriftObjects": [
					"tQuery(multiscan=True, resource_limits=None, computed_columns={}, orderby_config=None, timeout_projection_ms=30000, top_groups={}, max_groups_per_shard=50000, compile_flows=True, timeout_ms=180000, priority=0, flow_scans={}, max_groups=100, flow_columns=None, selects={'select_11': tSelectColumns(columns=['v(0) 1 24 left_join(left_join_5) 0.0 + / * *'], table='reduce_10', filter=None, limit=None)}, readserver_oom_score_adj=500, time_merges={'time_merge_9': tTimeMerge(time_windows=[tTimeWindow(width=86400000, start=1527724800000), tTimeWindow(width=86400000, start=1527811200000), tTimeWindow(width=86400000, start=1527897600000), tTimeWindow(width=86400000, start=1527984000000), tTimeWindow(width=86400000, start=1528070400000), tTimeWindow(width=86400000, start=1528156800000), tTimeWindow(width=86400000, start=1528243200000)], table='shard_merge_8'), 'time_merge_4': tTimeMerge(time_windows=[tTimeWindow(width=1, start=0)], table='agg_scan_1')}, string_agg_host='10.1.55.146', scans=[], shards=[tLeaf(port=8500, host='10.1.55.146', shard_id=0), tLeaf(port=8500, host='10.1.55.146', shard_id=1), tLeaf(port=8500, host='10.1.55.146', shard_id=2), tLeaf(port=8500, host='10.1.55.146', shard_id=3), tLeaf(port=8500, host='10.1.55.146', shard_id=4), tLeaf(port=8500, host='10.1.55.146', shard_id=5)], joins={'left_join_5': tLeftJoin(left_keys=[], right_table='time_merge_4', right_value='v(0)')}, random_streams={'random_stream_2': tRandomStream(num_events=1, name='random_stream_2')}, aggregation_scans={'agg_scan_6': tAggregationScan(aggregators=[tAggInfo(sharded_by_unique_key=False, arg=None, filter=None, type=1, unique_key=None, arg2=None, arguments=None), tAggInfo(sharded_by_unique_key=False, arg=None, filter=None, type=1, unique_key=None, arg2=None, arguments=None)], group_by=[], table='event_table_7'), 'agg_scan_1': tAggregationScan(aggregators=[tAggInfo(sharded_by_unique_key=False, arg=None, filter=None, type=1, unique_key=None, arg2=None, arguments=None)], group_by=[], table='shard_merge_3')}, progress_update_period_ms=1000, table_model=True, deadline_ms=10000, id=346, lookup_columns={}, reduces={'reduce_10': tReduce(fields=[], table='time_merge_9')}, timeout_projection_window_ms=0, unions={}, min_number_of_shard_groups=16, funnels={}, shard_merges={'shard_merge_3': tShardMerge(table='random_stream_2'), 'shard_merge_8': tShardMerge(table='agg_scan_6')}, shards_in_shard_group=None, output_tables=['select_11'], rod_config=None, flows=None, funnel_columns={}, string_agg_port=8600, event_table_selects={'event_table_7': tEventTableSelect(columns=[], table=tEventTable(micro_shard_level=0, time_windows=[tTimeWindow(width=86400000, start=1527724800000), tTimeWindow(width=86400000, start=1527811200000), tTimeWindow(width=86400000, start=1527897600000), tTimeWindow(width=86400000, start=1527984000000), tTimeWindow(width=86400000, start=1528070400000), tTimeWindow(width=86400000, start=1528156800000), tTimeWindow(width=86400000, start=1528243200000)], time_column_id=1, shard_column_id=None, data_folders=['/var/lib/interana/data/datasets/f/1/1/ia-data-0', '/var/lib/interana/data/datasets/f/1/1/ia-data-1', '/var/lib/interana/data/datasets/f/1/1/ia-data-2', '/var/lib/interana/data/datasets/f/1/1/ia-data-3', '/var/lib/interana/data/datasets/f/1/1/ia-data-4', '/var/lib/interana/data/datasets/f/1/1/ia-data-5']))}, sorts={})"
				],
				"dataserverResults": {
					"full_query": {
						"leaves_used": 1,
						"perf.num.nodes": 1,
						"perf.cpu_ns.readserver": 73271415,
						"cores_used": 4,
						"error": "",
						"shards_used": 6,
						"rows_examined": 0,
						"perf.num.cores": 4,
						"perf.tag.flow": "",
						"cpu_u_ms": 80,
						"rows_filtered_to": 0,
						"perf.num.columns": 0,
						"perf.bytes.memory.data_leaf": 188702720,
						"perf.tag.cohort": "",
						"disk_bytes_mapped": 8928,
						"perf.wall_ns.data_leaf": 77652349,
						"perf.tag.funnel": "",
						"wall_ms": 77,
						"perf.tag.group_by": "",
						"cpu_sys_ms": 0
					},
					"leaf_info": [
						{
							"recv_ms": 44,
							"leaf": "10.1.55.146",
							"debug": {
								"cpu_sys_ms": 0,
								"wall_ms": 43,
								"disk_bytes_mapped": 8928,
								"cores_used": 4,
								"error": "",
								"shards_used": 6,
								"rows_examined": 0,
								"leaves_used": 1,
								"cpu_u_ms": 36,
								"rows_filtered_to": 0
							}
						}
					]
				}
			},
			"rows": [
				[
					1527724800000,
					1527811200000,
					0,
					0,
					0
				],
				[
					1527811200000,
					1527897600000,
					0,
					0,
					0
				],
				[
					1527897600000,
					1527984000000,
					0,
					0,
					0
				],
				[
					1527984000000,
					1528070400000,
					0,
					0,
					0
				],
				[
					1528070400000,
					1528156800000,
					0,
					0,
					0
				],
				[
					1528156800000,
					1528243200000,
					0,
					0,
					0
				],
				[
					1528243200000,
					1528329600000,
					0,
					0,
					0
				]
			],
			"timespec": {
				"start": 1527724800000,
				"end": 1528329600000
			},
			"success": true,
			"queryInfo": {
				"rowsFilteredTo": 0,
				"shardsRequested": 6,
				"coresUsed": 4,
				"error": "",
				"cpuSysMs": 0,
				"cpuUMs": 80,
				"rowsExamined": 0,
				"shardsUsed": 6,
				"wallMs": 77,
				"leavesUsed": 1,
				"shardsTotal": 24,
				"diskBytesMapped": 8928
			},
			"id": "r346",
			"objectType": "QUERY_RESPONSE",
			"table": {
				"id": "t1",
				"name": "fashion"
			},
			"columns": [
				{
					"dataType": {
						"basic": "INTEGER"
					},
					"timeOffsetIndex": 0,
					"label": "START_TIME"
				},
				{
					"dataType": {
						"basic": "INTEGER"
					},
					"timeOffsetIndex": 0,
					"label": "END_TIME"
				},
				{
					"dataType": {
						"basic": "FLOAT",
						"isList": false
					},
					"measureIndex": 0,
					"timeOffsetIndex": 0,
					"label": "MEASURE_VALUE"
				},
				{
					"dataType": {
						"basic": "INTEGER"
					},
					"measureIndex": 0,
					"timeOffsetIndex": 0,
					"label": "EVENT_COUNT"
				},
				{
					"dataType": {
						"basic": "INTEGER"
					},
					"measureIndex": 0,
					"timeOffsetIndex": 0,
					"label": "OBJECT_COUNT"
				}
			],
			"timestamp": 1528344512000
		},
		{
			"id": "q347",
			"allowSampling": true,
			"timezone": "UTC",
			"parentQueryResponseId": "r346",
			"timespec": {
				"start": {
					"origin": "NOW",
					"setCalendarHour": [
						0
					],
					"calendarDays": -7
				},
				"trailingWindow": {
					"isAuto": true,
					"calendarDays": 1
				},
				"isTimeBucketed": true,
				"end": {
					"origin": "NOW",
					"setCalendarHour": [
						0
					]
				},
				"resolution": {
					"isAuto": true,
					"calendarDays": 1
				}
			},
			"requestedIds": [],
			"objectType": "QUERY_REQUEST",
			"measures": [
				{
					"operation": "REFERENCE",
					"referenceId": "k3"
				},
				{
					"operation": "REFERENCE",
					"referenceId": "k4"
				}
			],
			"queryRole": "EXPLORE_EXAMPLE",
			"maxExampleRows": 100,
			"tableId": "t1",
			"chartOptions": {
				"chartType": "TABLE"
			},
			"queryType": "EXAMPLE_EVENTS"
		},
		{
			"id": "q346",
			"allowSampling": true,
			"timezone": "UTC",
			"timespec": {
				"start": {
					"origin": "NOW",
					"setCalendarHour": [
						0
					],
					"calendarDays": -7
				},
				"trailingWindow": {
					"isAuto": true,
					"calendarDays": 1
				},
				"isTimeBucketed": true,
				"end": {
					"origin": "NOW",
					"setCalendarHour": [
						0
					]
				},
				"resolution": {
					"isAuto": true,
					"calendarDays": 1
				}
			},
			"requestedIds": [],
			"objectType": "QUERY_REQUEST",
			"measures": [
				{
					"name": "set 1",
					"operation": "COUNT"
				}
			],
			"queryRole": "EXPLORE",
			"orderBy": [
				{
					"operation": "ORDER_ELEMENT",
					"operand": {
						"operation": "MEASURE_REFERENCE",
						"measureIndex": 0
					}
				}
			],
			"maxGroups": 10,
			"tableId": "t1",
			"chartOptions": {
				"multipleAxes": false,
				"tableSort": [],
				"stackBarsById": null,
				"chartType": "TIME"
			},
			"timeOffsets": [
				{
					"calendarWeeks": 0
				}
			]
		},
		{
			"queryRequestId": "q347",
			"debug_info": {
				"checkpoints": [
					{
						"perf_info": {
							"used_columns": [],
							"num_scans": 0
						},
						"event_name": "query start",
						"ast": {
							"allowSampling": true,
							"operation": "REQUEST",
							"dataType": {
								"basic": "UNDEFINED",
								"isList": false
							},
							"timespec": {
								"end": {
									"origin": "NOW",
									"setCalendarHour": [
										0
									]
								},
								"trailingWindow": {
									"isAuto": true,
									"calendarDays": 1
								},
								"isTimeBucketed": true,
								"start": {
									"origin": "NOW",
									"setCalendarHour": [
										0
									],
									"calendarDays": -7
								},
								"resolution": {
									"isAuto": true,
									"calendarDays": 1
								}
							},
							"parentQueryResponseId": "r346",
							"outputTrees": [
								{
									"dataType": {
										"basic": "UNDEFINED",
										"isList": false
									},
									"maxExampleRows": 100,
									"operation": "EXAMPLES_QUERY",
									"measures": [
										{
											"dataType": {
												"basic": "UNDEFINED",
												"isList": false
											},
											"operation": "REFERENCE",
											"referenceId": "k3"
										},
										{
											"dataType": {
												"basic": "UNDEFINED",
												"isList": false
											},
											"operation": "REFERENCE",
											"referenceId": "k4"
										}
									],
									"timespec": {
										"end": {
											"origin": "NOW",
											"setCalendarHour": [
												0
											]
										},
										"isTimeBucketed": false,
										"start": {
											"origin": "NOW",
											"setCalendarHour": [
												0
											],
											"calendarDays": -7
										}
									}
								}
							],
							"tableId": "t1",
							"queryId": "r347",
							"processingStartTime": 1528344513,
							"timezone": "UTC",
							"timeOffsets": [
								{
									"calendarHours": 0
								}
							]
						},
						"timestamp": 1528344513.6625059
					},
					{
						"event_name": "after expansion",
						"timestamp": 1528344513.699155
					},
					{
						"event_name": "after strings",
						"timestamp": 1528344513.7374117
					},
					{
						"event_name": "after data servers",
						"timestamp": 1528344513.8705602
					},
					{
						"event_name": "after result processing",
						"timestamp": 1528344513.9004035
					}
				],
				"thriftObjects": [
					"tQuery(multiscan=True, resource_limits=None, computed_columns={}, orderby_config=None, timeout_projection_ms=30000, top_groups={}, max_groups_per_shard=50000, compile_flows=True, timeout_ms=180000, priority=0, flow_scans={}, max_groups=100, flow_columns=None, selects={'select_2': tSelectColumns(columns=['v(0)', 'v(1)'], table='event_table_1', filter=None, limit=100)}, readserver_oom_score_adj=500, time_merges={}, string_agg_host='10.1.55.146', scans=[], shards=[tLeaf(port=8500, host='10.1.55.146', shard_id=0), tLeaf(port=8500, host='10.1.55.146', shard_id=1), tLeaf(port=8500, host='10.1.55.146', shard_id=2), tLeaf(port=8500, host='10.1.55.146', shard_id=3), tLeaf(port=8500, host='10.1.55.146', shard_id=4), tLeaf(port=8500, host='10.1.55.146', shard_id=5)], joins={}, random_streams={}, aggregation_scans={}, progress_update_period_ms=1000, table_model=True, deadline_ms=10000, id=347, lookup_columns={}, reduces={}, timeout_projection_window_ms=0, unions={}, min_number_of_shard_groups=16, funnels={}, shard_merges={'shard_merge_3': tShardMerge(table='select_2')}, shards_in_shard_group=None, output_tables=['shard_merge_3'], rod_config=None, flows=None, funnel_columns={}, string_agg_port=8600, event_table_selects={'event_table_1': tEventTableSelect(columns=['int_col(1)', 'int_col(2)'], table=tEventTable(micro_shard_level=0, time_windows=[tTimeWindow(width=604800000, start=1527724800000)], time_column_id=1, shard_column_id=None, data_folders=['/var/lib/interana/data/datasets/f/1/1/ia-data-0', '/var/lib/interana/data/datasets/f/1/1/ia-data-1', '/var/lib/interana/data/datasets/f/1/1/ia-data-2', '/var/lib/interana/data/datasets/f/1/1/ia-data-3', '/var/lib/interana/data/datasets/f/1/1/ia-data-4', '/var/lib/interana/data/datasets/f/1/1/ia-data-5']))}, sorts={})"
				],
				"dataserverResults": {
					"full_query": {
						"leaves_used": 1,
						"perf.num.nodes": 1,
						"perf.cpu_ns.readserver": 20675847,
						"cores_used": 4,
						"error": "",
						"shards_used": 6,
						"rows_examined": 0,
						"perf.num.cores": 4,
						"perf.tag.flow": "",
						"cpu_u_ms": 16,
						"rows_filtered_to": 0,
						"perf.num.columns": 1,
						"perf.bytes.memory.data_leaf": 185528320,
						"perf.tag.cohort": "",
						"disk_bytes_mapped": 8992,
						"perf.wall_ns.data_leaf": 51698740,
						"perf.tag.funnel": "",
						"wall_ms": 52,
						"perf.tag.group_by": "",
						"cpu_sys_ms": 8
					},
					"leaf_info": [
						{
							"recv_ms": 44,
							"leaf": "10.1.55.146",
							"debug": {
								"cpu_sys_ms": 4,
								"wall_ms": 44,
								"disk_bytes_mapped": 8992,
								"cores_used": 4,
								"error": "",
								"shards_used": 6,
								"rows_examined": 0,
								"leaves_used": 1,
								"cpu_u_ms": 20,
								"rows_filtered_to": 0
							}
						}
					]
				}
			},
			"rows": [],
			"timespec": {
				"start": 1527724800000,
				"end": 1528329600000
			},
			"success": true,
			"queryInfo": {
				"rowsFilteredTo": 0,
				"shardsRequested": 6,
				"coresUsed": 4,
				"error": "",
				"cpuSysMs": 8,
				"cpuUMs": 16,
				"rowsExamined": 0,
				"shardsUsed": 6,
				"wallMs": 52,
				"leavesUsed": 1,
				"shardsTotal": 24,
				"diskBytesMapped": 8992
			},
			"id": "r347",
			"objectType": "QUERY_RESPONSE",
			"table": {
				"contexts": [
					{
						"operation": "REFERENCE",
						"isRawContext": true,
						"referenceId": "k1",
						"id": "k3",
						"name": "time",
						"createdTime": 1528224185000,
						"lastUpdatedTime": 1528224185000
					},
					{
						"operation": "REFERENCE",
						"isRawContext": true,
						"referenceId": "k2",
						"id": "k4",
						"name": "user",
						"createdTime": 1528224185000,
						"lastUpdatedTime": 1528224185000
					}
				],
				"id": "t1",
				"name": "fashion",
				"columns": [
					{
						"operation": "COLUMN",
						"dataType": {
							"isAggregable": false,
							"basic": "INTEGER",
							"units": "EPOCH_MILLISECONDS",
							"isGroupable": false
						},
						"id": "k1",
						"name": "time",
						"createdTime": 1528224185000,
						"lastUpdatedTime": 1528224185000
					},
					{
						"operation": "COLUMN",
						"dataType": {
							"isAggregable": false,
							"basic": "STRING",
							"stringNamespaceId": 2,
							"isGroupable": true
						},
						"id": "k2",
						"name": "user",
						"createdTime": 1528224185000,
						"lastUpdatedTime": 1528224185000
					}
				]
			},
			"columns": [],
			"timestamp": 1528344513000
		}
	],
	"version": 399,
	"users": [
		{
			"id": "u2",
			"email": "root@localhost",
			"isAdmin": true
		},
		{
			"id": "u3",
			"email": "test@interana.com",
			"isAdmin": true
		}
	],
	"explorerQueryResponseIds": [
		"r1",
		"r5",
		"r11",
		"r15",
		"r19",
		"r21",
		"r23",
		"r25",
		"r27",
		"r29",
		"r31",
		"r57",
		"r59",
		"r61",
		"r73",
		"r298",
		"r302",
		"r326",
		"r328",
		"r346"
	],
	"config": {},
	"tables": [
		{
			"timeColumnId": "k1",
			"iaColumnSetContextId": "k6",
			"timeColumnRange": {
				"end": 1394737200000,
				"start": 1393369200000
			},
			"actionContextId": null,
			"name": "fashion",
			"actorIds": [
				"k4"
			],
			"description": "",
			"contexts": [
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k1",
					"popularity": 0.909464,
					"id": "k3",
					"name": "time",
					"createdTime": 1528224185000,
					"lastUpdatedTime": 1528224185000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k2",
					"popularity": 1,
					"id": "k4",
					"name": "user",
					"createdTime": 1528224185000,
					"lastUpdatedTime": 1528224185000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k5",
					"popularity": 0,
					"id": "k6",
					"name": "__ia_column_set__",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k7",
					"popularity": 0.362137,
					"id": "k8",
					"name": "action",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k9",
					"popularity": 0,
					"id": "k10",
					"name": "registration_time",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k11",
					"popularity": 0,
					"id": "k12",
					"name": "gender",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k13",
					"popularity": 0,
					"id": "k14",
					"name": "category",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k15",
					"popularity": 0,
					"id": "k16",
					"name": "user_last_action_time",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k17",
					"popularity": 0,
					"id": "k18",
					"name": "from_recommended",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k19",
					"popularity": 0,
					"id": "k20",
					"name": "product_total",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k21",
					"popularity": 0,
					"id": "k22",
					"name": "subcategory",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k23",
					"popularity": 0,
					"id": "k24",
					"name": "product_id",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k25",
					"popularity": 0,
					"id": "k26",
					"name": "user_birthdate",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k27",
					"popularity": 0,
					"id": "k28",
					"name": "store",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k29",
					"popularity": 0,
					"id": "k30",
					"name": "product_likes",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k31",
					"popularity": 0,
					"id": "k32",
					"name": "user_action_count",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k33",
					"popularity": 0,
					"id": "k34",
					"name": "product_loves",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k35",
					"popularity": 0,
					"id": "k36",
					"name": "product_hates",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k37",
					"popularity": 0,
					"id": "k38",
					"name": "user_age",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k39",
					"popularity": 0,
					"id": "k40",
					"name": "user_gender",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				}
			],
			"id": "t1",
			"objectType": "TABLE",
			"columns": [
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "INTEGER",
						"units": "EPOCH_MILLISECONDS",
						"isGroupable": false
					},
					"id": "k1",
					"name": "time",
					"createdTime": 1528224185000,
					"lastUpdatedTime": 1528224185000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 2,
						"isGroupable": true
					},
					"id": "k2",
					"name": "user",
					"createdTime": 1528224185000,
					"lastUpdatedTime": 1528224185000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 5,
						"isGroupable": false,
						"isList": true
					},
					"id": "k5",
					"name": "__ia_column_set__",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 7,
						"isGroupable": true
					},
					"id": "k7",
					"name": "action",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "INTEGER",
						"units": "EPOCH_MILLISECONDS",
						"isGroupable": false
					},
					"id": "k9",
					"name": "registration_time",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 11,
						"isGroupable": true
					},
					"id": "k11",
					"name": "gender",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 13,
						"isGroupable": true
					},
					"id": "k13",
					"name": "category",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "INTEGER",
						"units": "EPOCH_MILLISECONDS",
						"isGroupable": false
					},
					"id": "k15",
					"name": "user_last_action_time",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 17,
						"isGroupable": true
					},
					"id": "k17",
					"name": "from_recommended",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": true,
						"basic": "INTEGER",
						"isGroupable": false
					},
					"id": "k19",
					"name": "product_total",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 21,
						"isGroupable": true
					},
					"id": "k21",
					"name": "subcategory",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": true,
						"basic": "INTEGER",
						"isGroupable": false
					},
					"id": "k23",
					"name": "product_id",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": true,
						"basic": "INTEGER",
						"isGroupable": false
					},
					"id": "k25",
					"name": "user_birthdate",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 27,
						"isGroupable": true
					},
					"id": "k27",
					"name": "store",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": true,
						"basic": "INTEGER",
						"isGroupable": false
					},
					"id": "k29",
					"name": "product_likes",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": true,
						"basic": "INTEGER",
						"isGroupable": false
					},
					"id": "k31",
					"name": "user_action_count",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": true,
						"basic": "INTEGER",
						"isGroupable": false
					},
					"id": "k33",
					"name": "product_loves",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": true,
						"basic": "INTEGER",
						"isGroupable": false
					},
					"id": "k35",
					"name": "product_hates",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": true,
						"basic": "INTEGER",
						"isGroupable": false
					},
					"id": "k37",
					"name": "user_age",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 39,
						"isGroupable": true
					},
					"id": "k39",
					"name": "user_gender",
					"createdTime": 1528224189000,
					"lastUpdatedTime": 1528224189000
				}
			]
		},
		{
			"timeColumnId": "k41",
			"iaColumnSetContextId": "k48",
			"timeColumnRange": {
				"end": 1430467200000,
				"start": 1427871600000
			},
			"actionContextId": null,
			"name": "music",
			"actorIds": [
				"k45",
				"k46"
			],
			"description": "",
			"contexts": [
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k41",
					"popularity": 0,
					"id": "k44",
					"name": "ts",
					"createdTime": 1528224194000,
					"lastUpdatedTime": 1528224194000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k42",
					"popularity": 0,
					"id": "k45",
					"name": "userId",
					"createdTime": 1528224194000,
					"lastUpdatedTime": 1528224194000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k43",
					"popularity": 0,
					"id": "k46",
					"name": "artist",
					"createdTime": 1528224194000,
					"lastUpdatedTime": 1528224194000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k47",
					"popularity": 0,
					"id": "k48",
					"name": "__ia_column_set__",
					"createdTime": 1528224199000,
					"lastUpdatedTime": 1528224199000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k49",
					"popularity": 0,
					"id": "k50",
					"name": "sessionId",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k51",
					"popularity": 0,
					"id": "k52",
					"name": "page",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k53",
					"popularity": 0,
					"id": "k54",
					"name": "auth",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k55",
					"popularity": 0,
					"id": "k56",
					"name": "lastName",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k57",
					"popularity": 0,
					"id": "k58",
					"name": "method",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k59",
					"popularity": 0,
					"id": "k60",
					"name": "location",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k61",
					"popularity": 0,
					"id": "k62",
					"name": "location.platform",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k63",
					"popularity": 0,
					"id": "k64",
					"name": "location.browser",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k65",
					"popularity": 0,
					"id": "k66",
					"name": "location.browser_majorver",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k67",
					"popularity": 0,
					"id": "k68",
					"name": "location.browser_minorver",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k69",
					"popularity": 0,
					"id": "k70",
					"name": "location.browser_patchver",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k71",
					"popularity": 0,
					"id": "k72",
					"name": "location.device",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k73",
					"popularity": 0,
					"id": "k74",
					"name": "status",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k75",
					"popularity": 0,
					"id": "k76",
					"name": "level",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k77",
					"popularity": 0,
					"id": "k78",
					"name": "itemInSession",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k79",
					"popularity": 0,
					"id": "k80",
					"name": "firstName",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k81",
					"popularity": 0,
					"id": "k82",
					"name": "registration",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k83",
					"popularity": 0,
					"id": "k84",
					"name": "gender",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k85",
					"popularity": 0,
					"id": "k86",
					"name": "song",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "REFERENCE",
					"isRawContext": true,
					"referenceId": "k87",
					"popularity": 0,
					"id": "k88",
					"name": "length",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				}
			],
			"id": "t2",
			"objectType": "TABLE",
			"columns": [
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "INTEGER",
						"units": "EPOCH_MILLISECONDS",
						"isGroupable": false
					},
					"id": "k41",
					"name": "ts",
					"createdTime": 1528224194000,
					"lastUpdatedTime": 1528224194000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": true,
						"basic": "INTEGER",
						"isGroupable": true
					},
					"id": "k42",
					"name": "userId",
					"createdTime": 1528224194000,
					"lastUpdatedTime": 1528224194000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 43,
						"isGroupable": true
					},
					"id": "k43",
					"name": "artist",
					"createdTime": 1528224194000,
					"lastUpdatedTime": 1528224194000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 47,
						"isGroupable": false,
						"isList": true
					},
					"id": "k47",
					"name": "__ia_column_set__",
					"createdTime": 1528224199000,
					"lastUpdatedTime": 1528224199000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": true,
						"basic": "INTEGER",
						"isGroupable": false
					},
					"id": "k49",
					"name": "sessionId",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 51,
						"isGroupable": true
					},
					"id": "k51",
					"name": "page",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 53,
						"isGroupable": true
					},
					"id": "k53",
					"name": "auth",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 55,
						"isGroupable": true
					},
					"id": "k55",
					"name": "lastName",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 57,
						"isGroupable": true
					},
					"id": "k57",
					"name": "method",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 59,
						"isGroupable": true
					},
					"id": "k59",
					"name": "location",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 61,
						"isGroupable": true
					},
					"id": "k61",
					"name": "location.platform",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 63,
						"isGroupable": true
					},
					"id": "k63",
					"name": "location.browser",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 65,
						"isGroupable": true
					},
					"id": "k65",
					"name": "location.browser_majorver",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 67,
						"isGroupable": true
					},
					"id": "k67",
					"name": "location.browser_minorver",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 69,
						"isGroupable": true
					},
					"id": "k69",
					"name": "location.browser_patchver",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 71,
						"isGroupable": true
					},
					"id": "k71",
					"name": "location.device",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": true,
						"basic": "INTEGER",
						"isGroupable": false
					},
					"id": "k73",
					"name": "status",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 75,
						"isGroupable": true
					},
					"id": "k75",
					"name": "level",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": true,
						"basic": "INTEGER",
						"isGroupable": false
					},
					"id": "k77",
					"name": "itemInSession",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 79,
						"isGroupable": true
					},
					"id": "k79",
					"name": "firstName",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "INTEGER",
						"units": "EPOCH_MILLISECONDS",
						"isGroupable": false
					},
					"id": "k81",
					"name": "registration",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 83,
						"isGroupable": true
					},
					"id": "k83",
					"name": "gender",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "STRING",
						"stringNamespaceId": 85,
						"isGroupable": true
					},
					"id": "k85",
					"name": "song",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				},
				{
					"operation": "COLUMN",
					"dataType": {
						"isAggregable": false,
						"basic": "FLOAT",
						"isGroupable": false
					},
					"id": "k87",
					"name": "length",
					"createdTime": 1528224214000,
					"lastUpdatedTime": 1528224214000
				}
			]
		}
	]
}
```
