# 数据库

## **table**

1. user（no,name,sex,grade`入学（职）年份`,dept,major`学生的专业`,title`老师的职称`）
2. course(no,name,credit`学分`,class_hour`学时`,teacher)
3. sc(Sno,Cno,grade)

# 前端

用bootstrap框架

https://blog.csdn.net/newlw/article/details/123017533

## 首页（登录页面）

## 学生界面

1. 信息查询：学生个人信息（可修改密码）、专业信息、学院信息
2. 查询已选课程信息，退课
3. 查询所有开设课程的信息
4. 查询已选课程的成绩

## 教师界面

1. 信息查询：教师个人信息（可修改密码）
2. 查看学生选此教师开设课程的详情，包括各个学生的个人信息，以及已选学生人数等
3. 为此教师开设课程中的学生，录入此门课程的成绩

## 管理员界面

- 学生管理：
  - 录入学生：先检测学生表中是否存在学号冲突的学生，若无则插入此学生信息。
  - 删除学生：先查询出此学生所有已选课程，系统将其全部退选后，再删除此学生。
- 教师管理：
  - 录入教师：同"录入学生"。
- 课程管理：
  - 创建课程
  - 更新课程
  - 删除课程
- 选课管理：
  - 删除选课记录



# 后端接口

## user

1. login，实现登录
2. add，增加用户
3. delete，删除用户
4. update，更新用户信息

## course

1. all，获取所有课程信息
2. search_by_no，根据教师工号查看课程信息
3. add，增加课程
4. delete，删除课程
5. update，更新课程

## sc

1. delete，删除选课信息（对应管理员和学生退选）
2. update，更新选课信息（对应老师登成绩）
3. search_by_Sno，根据学号得到选课信息
4. search_by_Cno，根据课程得到选课信息（对应教师查看课程选课情况）

