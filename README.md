# cs-magic-log

一个基于 loguru 的自定义日志工具，提供了简单的配置和使用方式。

- pypi: [cs-magic-log](https://pypi.org/project/cs-magic-log/)

## 安装

```bash
poetry add cs-magic-log
# 或
pip install cs-magic-log
```

## 使用方法

### 基础用法

```python
from cs_magic_log import logger

logger.info("这是一条信息")
logger.debug("这是一条调试信息")
logger.error("这是一条错误信息")
```

### 自定义配置

```python
from cs_magic_log import LogConfig, setup_logger

config = LogConfig(
    console_level="DEBUG",
    file_level="INFO",
    log_file="my_app.log",
    rotation="1 day"
)

logger = setup_logger(config)
logger.info("使用自定义配置的日志")
```

## 特性

- 同时支持控制台和文件输出
- 彩色控制台输出
- 可配置的日志等级
- 自动日志文件轮转
- 支持自定义日志格式