自部署文档已更新 https://docs.refly.ai/zh/guide/self-deploy

case

https://refly.ai/share/code/cod-eiuua6fou3aci24dn0ljxzme DeepLearning.AI web

https://refly.ai/canvas/c-vicwmalwwqok1mz9rqegfg0p

https://refly.ai/share/code/cod-fpvp6qm8v4faaj4nzx8lwwi8

https://refly.ai/share/code/cod-mndplsmkfqj0sumu9r8y7u8x

  

本地部署

接入deepseek 报错，直接执行本地文件：

docker exec -i refly_db psql -U refly -d refly < deploy/model-providers/deepseek.sql

接入Claude3.7

docker exec -i refly_db psql -U refly -d refly -c "INSERT INTO \"refly\".\"model_infos\" (\"name\", \"label\", \"provider\", \"tier\", \"enabled\", \"is_default\", \"context_limit\", \"max_output\", \"capabilities\") VALUES ('anthropic/claude-3.7-sonnet', 'Claude 3.7 Sonnet', 'anthropic', 't1', 't', 'f', 200000, 128000, '{\"vision\":true}');"

  

存储空间已满

docker exec -i refly_db psql 'postgresql://refly:test@localhost:5432/refly' << EOF

update refly.storage_usage_meters set file_count_quota = 10000

EOF

  

ERROR: Request: POST /v1/knowledge/document/create unknown err: NotFoundError: No SubscriptionPlan found

INSERT INTO "refly"."subscription_plans" ("plan_type", "lookup_key", "t1_token_quota", "t2_token_quota", "object_storage_quota", "vector_storage_quota", "interval", "t1_count_quota", "t2_count_quota", "file_count_quota") VALUES ('free', '', 0, -1, -1, -1, NULL, -1, -1, -1);