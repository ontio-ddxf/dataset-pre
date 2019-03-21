# dataset-pre


* [上传 dataset](#上传-dataset)
* [查询 dataset](#查询-dataset)


### 上传 dataset



```

/api/v1/datadealer/dataset/submit
method: POST

{
	"id": "0000000001",
	"data": [{
			"tag1Id": "tag1",
			"value": [{
				"tag2Id": "tag2",
				"value": [{
						"tag3Id": "tag3",
						"value": "O型"
					},
					{
						"tag3Id": "tag3",
						"value": "男"
					}
				]
			}, {
				"tag2Id": "tag2",
				"value": [{
						"tag3Id": "tag3",
						"value": "吸烟"
					},
					{
						"tag3Id": "tag3",
						"value": "无"
					}
				]
			}]
		},
		{
			"tag1Id": "tag1",
			"value": [{
				"tag2Id": "tag2",
				"value": [{
					"tag3Id": "tag3",
					"value": "否"
				}]
			}, {
				"tag2Id": "tag2",
				"value": [{
					"tag3Id": "tag3",
					"value": "无"
				}]
			}]
		}
	],
	"createtime": "20190402",
	"metadata": {
	
	},
	"price": "0.1",
	"coin": "ong"
}

```

### 查询 dataset



```
/api/v1/datadealer/dataset/query
method: POST

{
	"answers": [{
		"tag3id": "34546546757",
		"answerType": "", //数据存在但敏感(SENSITIVE)，数据不存在(EMPTY)以及数据存在且在value字段
		"value": "男"
	}]
}


```
