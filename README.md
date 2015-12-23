- This 任务目前仅邮件有效,缺少时间、监听微博
- that 任务发送邮件和发送微博均有效
- 任务管理页面目前可以查看、开始、暂停任务，缺少修改、删除任务。


## 数据库格式

+ User表

```sql
CREATE TABLE `IFTTT`.`User` (
  `Email` VARCHAR(45) NOT NULL,
  `Password` VARCHAR(45) NOT NULL,
  `Rank` INT NOT NULL,
  `Consumption` INT NULL,
  `Balance` INT NULL,
  `isAdmin` BIT(1) NULL,
  PRIMARY KEY (`Email`));
```

+ PostMessage表

```sql
CREATE TABLE `IFTTT`.`PostMessage` (
  `ID` INT NOT NULL,
  `Email` VARCHAR(45) NOT NULL,
  `Subject` VARCHAR(21845) NOT NULL,
  `Content` VARCHAR(21845) NULL,
  `Time` DATETIME NULL,
  `Read` BIT(1) NULL,
  `Important` BIT(1) NULL,
  PRIMARY KEY (`ID`));
```