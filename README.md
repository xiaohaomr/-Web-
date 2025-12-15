# 校园社团管理系统

一个基于Web的校园社团管理系统，提供社团信息管理、活动发布、成员管理等功能，助力校园社团高效运作。

## 项目简介

本系统旨在为校园社团提供一个便捷的管理平台，实现社团信息、成员、活动的数字化管理。系统采用前后端分离的设计思路，前端使用HTML、CSS、JavaScript实现用户界面，后端使用PHP处理业务逻辑，MySQL存储数据。

## 功能特性

### 学生功能
- **用户登录/注册**：支持学号登录和账号注册
- **社团浏览**：查看校园内所有社团信息
- **活动参与**：浏览和报名参与社团活动
- **个人中心**：查看个人信息和参与的活动记录

### 管理员功能
- **社团管理**：创建、编辑和管理社团信息
- **成员管理**：审核成员申请，管理成员信息
- **活动管理**：发布、编辑和管理社团活动
- **数据统计**：查看社团和活动的数据统计信息

## 技术栈

### 前端技术
- **HTML5**：页面结构搭建
- **CSS3**：页面样式设计，包括响应式布局
- **JavaScript**：交互逻辑实现，表单验证等

### 后端技术
- **PHP**：服务器端脚本语言，处理业务逻辑
- **MySQL**：关系型数据库，存储系统数据

### 开发工具
- 文本编辑器（如VS Code、Sublime Text等）
- XAMPP/WAMP：本地服务器环境
- MySQL Workbench/Navicat：数据库管理工具

## 项目结构

```
web校园社团管理系统/
├── css/               # 样式文件目录
│   ├── active.css     # 活动页面样式
│   ├── active2.css    # 活动详情页面样式
│   ├── index.css      # 登录页面样式
│   ├── indexTwo.css   # 首页样式
│   ├── information.css # 信息页面样式
│   ├── systemb.css    # 系统页面样式
│   └── systemc.css    # 系统管理页面样式
├── image/             # 图片资源目录
│   ├── iamgestyle1.jpg
│   ├── iamgestyle2.jpg
│   ├── iamgestyle3.jpg
│   ├── indexBackground.mp4
│   ├── indexClub1.jpg
│   ├── indexClub2.jpg
│   ├── indexClub3.jpg
│   ├── indexClub4.jpg
│   └── stylebackground.jpg
├── js/                # JavaScript文件目录
│   ├── active.js      # 活动页面交互逻辑
│   ├── active2.js     # 活动详情页面交互逻辑
│   ├── index.js       # 登录页面交互逻辑
│   ├── indexTwo.js    # 首页交互逻辑
│   ├── information.js # 信息页面交互逻辑
│   ├── systemb.js     # 系统页面交互逻辑
│   └── systemc.js     # 系统管理页面交互逻辑
├── mysql/             # 数据库文件目录
│   └── database.sql   # 数据库初始化脚本
├── php/               # PHP文件目录
│   ├── login.php      # 登录处理逻辑
│   └── system.php     # 系统业务处理逻辑
├── Register.html      # 注册页面
├── active.html        # 活动页面
├── active2.html       # 活动详情页面
├── index.html         # 登录页面
├── indexTwo.html      # 首页
├── information.html   # 信息页面
├── systemb.html       # 系统页面
├── systemc.html       # 系统管理页面
├── start_server.bat   # 服务器启动脚本
└── start_server_simple.bat # 简易服务器启动脚本
```

## 安装与部署

### 环境要求
- PHP 5.6+ 或 PHP 7.x
- MySQL 5.6+ 或 MySQL 8.x
- Apache Web Server

### 本地安装

1. **安装本地服务器环境**
   - 推荐使用 XAMPP（Windows）或 MAMP（Mac）
   - 下载地址：https://www.apachefriends.org/

2. **导入数据库**
   - 启动 XAMPP，开启 Apache 和 MySQL 服务
   - 打开浏览器访问 http://localhost/phpmyadmin
   - 创建名为 `club_student_info` 的数据库
   - 导入 `mysql/database.sql` 文件

3. **部署项目文件**
   - 将项目文件复制到 XAMPP 的 `htdocs` 目录下
   - 目录结构：`C:\xampp\htdocs\web校园社团管理系统\`

4. **访问系统**
   - 打开浏览器访问 http://localhost/web校园社团管理系统/index.html

### 服务器部署

1. **配置服务器环境**
   - 安装 Apache、PHP、MySQL
   - 确保 PHP 扩展 `mysqli` 已启用

2. **导入数据库**
   - 使用数据库管理工具导入 `mysql/database.sql` 文件

3. **部署项目文件**
   - 将项目文件上传到服务器的网站根目录

4. **配置数据库连接**
   - 修改 PHP 文件中的数据库连接信息（如果需要）

## 使用说明

### 学生登录
1. 打开系统登录页面（http://localhost/web校园社团管理系统/index.html）
2. 输入学号和密码
3. 点击登录按钮

### 管理员登录
1. 打开系统登录页面
2. 点击"管理者登录"按钮
3. 使用管理员账号登录

### 社团管理
1. 登录管理员账号
2. 进入系统管理页面
3. 点击"社团管理"模块
4. 进行社团的创建、编辑和管理操作

### 活动发布
1. 登录管理员账号
2. 进入系统管理页面
3. 点击"活动管理"模块
4. 发布新活动或管理已有活动

## 数据库设计

### 主要数据表

#### students（学生表）
| 字段名 | 数据类型 | 说明 |
|--------|----------|------|
| id | INT | 主键，自增 |
| student_id | VARCHAR(20) | 学号，唯一 |
| name | VARCHAR(50) | 姓名 |
| password | VARCHAR(255) | 密码 |
| club | VARCHAR(50) | 所属社团 |
| role | VARCHAR(20) | 角色（member/admin） |

#### clubs（社团表）
| 字段名 | 数据类型 | 说明 |
|--------|----------|------|
| id | INT | 主键，自增 |
| name | VARCHAR(50) | 社团名称，唯一 |
| president | VARCHAR(50) | 社长 |
| member_count | INT | 成员数 |
| status | VARCHAR(20) | 状态（active/inactive） |
| description | TEXT | 社团描述 |

#### events（活动表）
| 字段名 | 数据类型 | 说明 |
|--------|----------|------|
| id | INT | 主键，自增 |
| title | VARCHAR(100) | 活动标题 |
| club | VARCHAR(50) | 举办社团 |
| date_time | DATETIME | 活动时间 |
| status | VARCHAR(20) | 状态（planning/registering/published） |
| description | TEXT | 活动描述 |

#### applications（申请记录表）
| 字段名 | 数据类型 | 说明 |
|--------|----------|------|
| id | INT | 主键，自增 |
| student_id | VARCHAR(20) | 学号 |
| student_name | VARCHAR(50) | 姓名 |
| club | VARCHAR(50) | 申请社团 |
| status | VARCHAR(20) | 状态（pending/approved/rejected） |

## 默认账号

### 学生账号
- 学号：2021001
- 密码：123456

### 管理员账号
- 用户名：admin001
- 密码：admin123

## 浏览器支持

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## 开发与维护

### 开发环境配置
1. 安装Node.js（可选，用于前端开发工具）
2. 安装代码编辑器（如VS Code）
3. 安装浏览器开发者工具

### 项目维护
- 定期备份数据库
- 更新系统代码时注意兼容性
- 定期检查系统安全性

## 注意事项

1. 系统默认使用UTF-8编码，请确保数据库和服务器环境也使用UTF-8编码
2. 首次使用系统请先导入数据库
3. 生产环境部署时请修改默认密码，确保系统安全
4. 系统使用了视频背景，请确保服务器环境支持视频文件的访问

## 许可证

本项目采用MIT许可证，详见LICENSE文件。

## 联系方式

如有问题或建议，请联系：
- 邮箱：contact@club.example.com
- 电话：010-12345678

## 更新日志

### v1.0.0（2025-12-15）
- 系统初始版本发布
- 实现用户登录/注册功能
- 实现社团管理功能
- 实现活动管理功能
- 实现成员管理功能

---

**© 2025 校园社团管理系统 版权所有**
