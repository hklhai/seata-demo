# 测试springcloud-jpa-seata

# 修改项目问题

缺少版本
```
    <build>
        <plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
                <version>2.2.0.RELEASE</version>
            </plugin>
        </plugins>
    </build>
```



## 1. 下载seata新版本
https://github.com/seata/seata/releases/tag/v0.9.0
### 启动命令
win
```
seata-server.bat -p 8091
```

Linux
```
./seata-server.sh -p 8091
```

## 2. springcloud-jpa-seata中mysql版本修改
执行all_in_one.sql建立order、storage、account数据库

## 3. 数据库配置
account-service、order-service、storage-service 

## 4. mysql版本
springcloud-jpa-seata项目pom.xml中MySQL版本\

## 5. 启动服务
account-service、order-service、storage-service、business-service

## 6. 测试
1. POST http://l1:8084/purchase/commit
2. POST http://l1:8084/purchase/rollback

## 7. 验证
account_tbl
order_tbl
storage_tbl



