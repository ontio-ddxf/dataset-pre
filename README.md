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
			"name": "公共标签",
			"value": [{
				"tag2Id": "tag2",
				"name": "个人信息",
				"value": [{
						"tag3Id": "tag3",
						"name": "ABO血型",
						"value": "O型"
					},
					{
						"tag3Id": "tag3",
						"name": "性别",
						"value": "男"
					}
				]
			}, {
				"tag2Id": "tag2",
				"name": "个人健康标签",
				"value": [{
						"tag3Id": "tag3",
						"name": "您吸烟吗？",
						"value": "吸烟"
					},
					{
						"tag3Id": "tag3",
						"name": "药物过敏史",
						"value": "无"
					}
				]
			}]
		},
		{
			"tag1Id": "tag1",
			"name": "诊断标签",
			"value": [{
				"tag2Id": "tag2",
				"name": "手术",
				"value": [{
					"tag3Id": "tag3",
					"name": "是否做过手术",
					"value": "否"
				}]
			}, {
				"tag2Id": "tag2",
				"name": "残疾情况",
				"value": [{
					"tag3Id": "tag3",
					"name": "残疾情况",
					"value": "无"
				}]
			}]
		}
	],
	"createtime": "20190402",
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
		"tag1": "公共标签",
		"tag2": "个人信息",
		"tag3": "性别",
		"answerType": "", //数据存在但敏感(SENSITIVE)，数据不存在(EMPTY)以及数据存在且在value字段
		"value": "男"
	}]
}


```
