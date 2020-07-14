### 命令行和配置

| 库名                                                  | 说明                                                         |
| ----------------------------------------------------- | ------------------------------------------------------------ |
| [spf13/viper](https://github.com/spf13/viper)         | 应用程序的完整配置解决方案 【不适合动态修改配置和高并发情况下动态获取配置】 |
| [spf13/cobra](https://github.com/spf13/cobra)         | 提供了简单的接口来创建命令行程序，Docker 和 Kubernetes 类型风格 |
| [BurntSushi/toml](https://github.com/BurntSushi/toml) | toml 配置文件库                                              |
| [yaml.v2](https://gopkg.in/yaml.v2)                   | yaml 配置文件库                                              |

### Web 开发框架

| 库名                                          | 说明                                                         |
| --------------------------------------------- | ------------------------------------------------------------ |
| [gin](https://github.com/gin-gonic/gin)       | 简单易用功能强大的主流 Web 框架                              |

### 日志类

| 库名                                                  | 说明                                                       |
| ----------------------------------------------------- | ---------------------------------------------------------- |
| [sirupsen/logrus](https://github.com/sirupsen/logrus) | 完全兼容 Golang 标准库日志模块，提供扩展性，日志格式可定制 |
| [go.uber.org/zap](https://go.uber.org/zap)            | 高性能日志库                                               |

### 数据存储类

| 库名                                                         | 说明                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [jinzhu/gorm](https://github.com/jinzhu/gorm)                | MySQL  ORM， 提供了灵活的扩展性和完整的用户文档，推荐优先使用 |
| [jmoiron/sqlx](https://github.com/jmoiron/sqlx)              | MySQL 驱动，优先推荐使用 ORM                                 |
| [gocraft/dbr](github.com/gocraft/dbr)                        | MySQL 驱动，优先推荐使用 ORM                                 |
| [mongodb/mongo-go-driver](https://github.com/mongodb/mongo-go-driver) | MongoDB  官方驱动                                            |
| [globalsign/mgo](https://github.com/globalsign/mgo)          | MongoDB mgo 库的 fork 版本，被社区验证                       |
| [go-redis/redis](https://github.com/go-redis/redis)          | Redis 完善的可配置项和丰富的 API 封装                        |

### 消息队列

| 库名                                                        | 说明                                     |
| ----------------------------------------------------------- | ---------------------------------------- |
| [segmentio/kafka-go](https://github.com/segmentio/kafka-go) | Kafka Shopify 项目验证                   |
| [Shopify/sarama](https://github.com/Shopify/sarama)         | Kafka Segmentio 项目验证，API 封装更友好 |
| [nsqio/go-nsq](https://github.com/nsqio/go-nsq)             | NSQ 官方                                 |

### 搜索库

| 库名                                                         | 说明                                           |
| ------------------------------------------------------------ | ---------------------------------------------- |
| [elastic/go-elasticsearch](https://github.com/elastic/go-elasticsearch) | ElasticSearch 官方                             |
| [olivere/elastic](https://github.com/olivere/elastic)        | ElasticSearch 社区版，早期采用的版本，经过验证 |

### JSON 处理工具

| 库名                                                     | 说明                                |
| -------------------------------------------------------- | ----------------------------------- |
| [json-iterator/go ](https://github.com/json-iterator/go) | 100% 兼容标准库，特定场景下更加优秀 |

### 进程管理

| 库名                                                      | 说明                                     |
| --------------------------------------------------------- | ---------------------------------------- |
| [jpillora/overseer](https://github.com/jpillora/overseer) | 可监控的、支持程序平滑重启、程序平滑升级 |

### 错误处理

| 库名                                                         | 说明                                               |
| ------------------------------------------------------------ | -------------------------------------------------- |
| [pkg/errors](https://github.com/pkg/errors)                  | 提供丰富的错误处理 API                             |
| [sync/errgroup](https://godoc.org/golang.org/x/sync/errgroup) | 并发场景下错误处理，方便使用，waitgroup 的简化版本 |

### 工具类

| 库名                                                         | 说明                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [ory/fosite](https://github.com/ory/fosite)                  | Authentication，标准的 OAuth 2.0 实现与 OpenID 支持          |
| [dgrijalva/jwt-go](https://github.com/dgrijalva/jwt-go)      | Authentication jwt 库                                        |
| [casbin/casbin](https://github.com/casbin/casbin)            | Authorization，完善的 ACL 和 RBAC 支持                       |
| [go-playground/validator](https://github.com/go-playground/validator) | 验证库，提供丰富特性与灵活可扩展性，并支持 i18               |
| [asaskevich/govalidator](https://github.com/asaskevich/govalidator) | 验证库，社区活跃版本                                         |
| [fsnotify/fsnotify](https://github.com/fsnotify/fsnotify)    | 文件更新通知 ，提供灵活的扩展性支持                          |
| [robfig/cron](https://github.com/robfig/cron)                | 定时任务                                                     |
| [satori/go.uuid](https://github.com/satori/go.uuid)          | uuid 库，支持 RFC 4122 & DCE 1.1 标准                        |
| [google/uuid](https://github.com/google/uuid)                | uuid 库，Google 出品，支持 RFC 4122 & DCE 1.1 标准           |

### Metrics

| 库名                                                         | 说明                                                     |
| ------------------------------------------------------------ | -------------------------------------------------------- |
| [prometheus/client_golang](https://github.com/prometheus/client_golang) | 鼎鼎有名的 Prometheus 监控的客户端库，Metrics 的唯一选择 |

### 测试库

| 库名                                                    | 说明                                                         |
| ------------------------------------------------------- | ------------------------------------------------------------ |
| [stretchr/testify](https://github.com/stretchr/testify) | 提供功能强大的 assert 包，可以更方便的测试组织、初始化测试等功能 |
| [h2non/gock](https://github.com/h2non/gock)             | 提供链式 API 方式                                            |

### 工具库

| 库名                                                         | 说明                              |
| ------------------------------------------------------------ | --------------------------------- |
| [spaolacci/murmur3](https://github.com/spaolacci/murmur3)    | MurmurHash3 实现                  |
| [wangbin/jiebago](https://github.com/wangbin/jiebago)        | jiaba 分词，性能优秀              |
| [hashicorp/golang-lru](https://github.com/hashicorp/golang-lru) | lru 算法                          |
| [mitchellh/mapstructure](https://github.com/mitchellh/mapstructure) | 支持复杂的 map 与 struct 相互转化 |

### 外部优选库

| 库名                                                         | 说明                                                     |
| ------------------------------------------------------------ | -------------------------------------------------------- |
| [grpc](https://google.golang.org/grpc)                       | Google 出品                                              |
| [grpc-ecosystem/grpc-gateway](https://github.com/grpc-ecosystem/grpc-gateway) | gRPC Gateway                                             |
| [grpc-ecosystem/go-grpc-middleware](https://github.com/grpc-ecosystem/go-grpc-middleware) | gRPC 相关插件，日志、Trace、认证等常用插件               |
| [gogo/protobuf](https://github.com/gogo/protobuf)            | 第三方对 gRPC protobuf 扩展，提供灵活的可定制特性        |
| [golang](https://github.com/golang)                          | Golang 官方维护了大量基础库，有着优秀的实现              |
| [kubernetes/kubernetes](https://github.com/kubernetes/kubernetes) | k8s  生态滋生了诸多优秀的封装                            |
| [aws/aws-sdk-go](https://github.com/aws/aws-sdk-go)          | AWS 官方 SDK 中独立封装了大量的优秀库                    |
| [segmentio](https://github.com/segmentio)                    | Segmentio 维护的库，优秀的设计与优雅的实现和封装动机说明 |