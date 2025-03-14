---
{
    "title": "检查连接缓存",
    "language": "zh-CN"
}
---

<!-- 
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.
-->

# 检查连接缓存

## 请求路径

`GET /api/check_rpc_channel/{host_to_check}/{remot_brpc_port}/{payload_size}`

## 描述

该功能用于检查 brpc 的连接缓存。

## Path parameters

* `host_to_check`

    需要查检的 IP。

* `remot_brpc_port`

    需要查检的端口。

* `payload_size`

    负载大小，单位 B，取值范围 1~1024000。

## 请求体

无

## 响应

    ```
    {
        "msg":"success",
        "code":0,
        "data": "open brpc connection to {host_to_check}:{remot_brpc_port} success.",
        "count":0
    }
    ```
## 示例


    ```
    curl http://127.0.0.1:8040/api/check_rpc_channel/127.0.0.1/8060/1024000
    ```

