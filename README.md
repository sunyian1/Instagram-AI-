[Instagram智能获客系统_README.md](https://github.com/user-attachments/files/27064059/Instagram._README.md)
# Instagram Intelligent Lead Generation System

> 中文 / English / Русский

---

## 中文介绍

### 项目名称

**Instagram 智能获客系统**

### 项目简介

Instagram 智能获客系统是一套面向 Instagram 私域流量、海外客户开发和精准营销场景打造的自动化工具。系统集成账号管理、目标用户抓取、AI 智能筛选、用户分类、自动私信、账号状态检测和数据统计等功能，帮助运营人员更高效地发现潜在客户，并进行稳定、可控的私信触达。

本项目并不是简单的批量群发工具，而是一套完整的自动化获客流程系统。它可以从目标博主出发，持续抓取相关用户，自动识别潜在客户，并根据用户分类执行不同的后续任务。

### 核心功能

#### 1. 多账号管理

系统支持对不同用途的 Instagram 账号进行分类管理，包括：

- 抓粉账号
- 群发账号
- 正常账号
- 异常账号

系统会记录账号的使用次数、最后操作时间、当前状态和运行锁，避免多个任务同时使用同一个账号。

#### 2. 自动抓取用户

系统可以围绕指定的金融博主或目标账号，自动抓取其粉丝和关注列表，并将抓取到的用户保存到数据库中。

抓取过程支持断点续爬，即使程序中断，也可以从上一次进度继续执行。

#### 3. 用户自动分类

系统会根据用户资料信息将用户分类为：

- 群发用户
- 博主用户
- 金融博主

不同类型的用户会进入不同的后续处理流程。

#### 4. AI 智能判断

系统内置 AI 判断模块，可以分析 Instagram 用户的：

- 用户名
- 昵称
- 个人简介
- 近期帖子内容

AI 会判断该用户是否符合指定条件，例如是否为美国相关账号、是否与金融、投资、股票、财富、交易等领域相关。

只有同时满足条件的用户，才会被升级为高价值金融博主，并进入后续抓取流程。

#### 5. 自动私信触达

系统支持使用群发账号向目标用户自动发送私信。

私信模块支持：

- 多账号并发
- 单账号发送间隔控制
- 发送成功后记录状态
- 防止重复发送
- 失败重试
- 异常账号识别
- 封禁账号自动清理

#### 6. 账号异常检测

系统会自动检测账号是否异常或封禁。

当账号操作失败时，系统不会立即误判，而是会多次确认账号状态：

- 确认封禁：自动删除账号
- 未封但连续失败：标记异常
- 网络异常无法确认：保留账号，等待后续检查

同时系统支持后台定时巡检，定期检查数据库中的抓粉账号和群发账号。

#### 7. 后台自动运行

系统包含多个后台任务模块：

- 账号入库任务
- 抓粉任务
- AI 判断任务
- 私信发送任务
- 账号巡检任务
- 状态 API 服务

启动后无需人工持续干预，只要数据库中存在待处理数据，系统会自动执行对应任务。

#### 8. 状态 API

系统提供轻量级状态 API，可用于前端面板或监控系统展示核心数据，例如：

- 抓粉账号数量
- 群发账号数量
- 已私信用户数量
- 未私信用户数量
- 博主数量
- 金融博主数量

### 适用场景

本项目适用于以下场景：

- Instagram 私域获客
- 海外客户开发
- 金融投资类用户筛选
- 股票 / 加密货币 / 财富管理社群引流
- 多账号自动化运营
- Instagram 精准营销
- 潜在客户自动发现与触达

### 项目优势

- 自动化程度高
- 支持多账号并发
- 支持 AI 精准筛选
- 支持断点续爬
- 支持账号异常检测
- 支持发送频率控制
- 支持状态监控
- 架构轻量，适合长期运行

### 工作流程

```text
导入账号
  ↓
账号自动入库
  ↓
抓取目标博主用户
  ↓
用户自动分类
  ↓
AI 判断高价值用户
  ↓
金融博主继续扩展抓取
  ↓
群发用户进入私信队列
  ↓
自动私信触达
  ↓
记录发送状态与账号状态
```

### 免责声明

本项目仅用于技术研究、数据分析和自动化流程学习。使用者应遵守 Instagram 平台规则、当地法律法规以及相关服务条款。由于不当使用造成的任何风险或损失，由使用者自行承担。

---

## English Introduction

### Project Name

**Instagram Intelligent Lead Generation System**

### Overview

The Instagram Intelligent Lead Generation System is an automation tool designed for Instagram private traffic growth, overseas customer acquisition, and precision marketing. It integrates account management, target user crawling, AI-based user filtering, user classification, automated direct messaging, account health checking, and real-time data statistics.

This project is not just a simple bulk messaging tool. It is a complete automated lead generation workflow that can discover target users, classify them, identify high-value accounts, and perform controlled outreach through Instagram direct messages.

### Core Features

#### 1. Multi-account Management

The system supports managing different types of Instagram accounts, including:

- Crawling accounts
- Direct messaging accounts
- Normal accounts
- Abnormal accounts

It records account usage count, last operation time, current status, and locking state to prevent multiple workers from using the same account simultaneously.

#### 2. Automated User Crawling

The system can crawl followers and followings from selected target accounts, such as finance-related bloggers or influencers.

The crawling process supports resumable progress. If the program stops unexpectedly, it can continue from the last saved position.

#### 3. User Classification

Crawled users are automatically classified into different categories:

- Messaging users
- Blogger users
- Finance bloggers

Different categories are handled by different backend workflows.

#### 4. AI-powered User Evaluation

The system includes an AI evaluation module that analyzes Instagram user information such as:

- Username
- Full name
- Biography
- Recent post content

The AI module determines whether a user matches specific requirements, such as being US-related and related to finance, investing, stocks, wealth, or trading.

Only users that satisfy all required conditions are promoted as high-value finance bloggers and used for further crawling.

#### 5. Automated Direct Messaging

The system supports automated Instagram direct messaging through dedicated messaging accounts.

The DM module supports:

- Multi-account concurrency
- Per-account sending interval control
- Successful send tracking
- Duplicate prevention
- Failure retry
- Abnormal account detection
- Banned account cleanup

#### 6. Account Health Checking

The system automatically checks whether accounts are abnormal or banned.

When an operation fails, the system does not immediately remove the account. Instead, it verifies the account status multiple times:

- Confirmed banned: remove from database
- Not banned but repeatedly failed: mark as abnormal
- Network or uncertain error: keep the account for future checks

A background audit worker can periodically inspect all crawling and messaging accounts.

#### 7. Background Automation

The system contains multiple background workers:

- Account ingestion worker
- Crawling worker
- AI evaluation worker
- Direct messaging worker
- Account audit worker
- Status API server

Once started, the system can continue processing data automatically without constant manual intervention.

#### 8. Status API

A lightweight status API is provided for dashboards or monitoring systems. It can return key metrics such as:

- Crawling account count
- Messaging account count
- Sent DM count
- Pending DM count
- Blogger count
- Finance blogger count

### Use Cases

This project can be used for:

- Instagram lead generation
- Overseas customer development
- Finance-related audience discovery
- Stock, crypto, and wealth management community growth
- Multi-account Instagram automation
- Precision marketing
- Automated prospect discovery and outreach

### Advantages

- High level of automation
- Multi-account concurrency support
- AI-powered target filtering
- Resumable crawling
- Account health monitoring
- Sending frequency control
- Status monitoring API
- Lightweight architecture suitable for long-running tasks

### Workflow

```text
Import accounts
  ↓
Automatic account ingestion
  ↓
Crawl target blogger users
  ↓
Classify users automatically
  ↓
Evaluate high-value users with AI
  ↓
Expand finance blogger crawling
  ↓
Add messaging users to DM queue
  ↓
Send automated direct messages
  ↓
Record messaging and account status
```

### Disclaimer

This project is intended for technical research, data analysis, and automation workflow learning only. Users must comply with Instagram platform rules, local laws, and applicable terms of service. Any risk or loss caused by improper use is the sole responsibility of the user.

---

## Русское описание

### Название проекта

**Интеллектуальная система лидогенерации для Instagram**

### Обзор проекта

Интеллектуальная система лидогенерации для Instagram — это инструмент автоматизации, предназначенный для поиска потенциальных клиентов, развития частного трафика, международного маркетинга и точечного продвижения в Instagram.

Система объединяет управление аккаунтами, сбор целевых пользователей, AI-фильтрацию, классификацию пользователей, автоматическую отправку личных сообщений, проверку состояния аккаунтов и статистику в реальном времени.

Это не просто инструмент массовой рассылки. Это полноценная автоматизированная система, которая помогает находить целевую аудиторию, определять ценных пользователей и выполнять контролируемое взаимодействие через Instagram Direct.

### Основные функции

#### 1. Управление несколькими аккаунтами

Система поддерживает разные типы Instagram-аккаунтов:

- аккаунты для сбора пользователей;
- аккаунты для отправки сообщений;
- нормальные аккаунты;
- проблемные аккаунты.

Для каждого аккаунта сохраняются количество операций, время последнего использования, текущий статус и состояние блокировки, чтобы избежать одновременного использования одного аккаунта несколькими задачами.

#### 2. Автоматический сбор пользователей

Система может автоматически собирать подписчиков и подписки целевых аккаунтов, например финансовых блогеров или тематических лидеров мнений.

Процесс сбора поддерживает продолжение с последней сохранённой позиции. Если программа была остановлена, она может продолжить работу без потери прогресса.

#### 3. Автоматическая классификация пользователей

Собранные пользователи автоматически распределяются по категориям:

- пользователи для рассылки;
- блогеры;
- финансовые блогеры.

Каждая категория обрабатывается отдельным рабочим процессом.

#### 4. AI-анализ пользователей

Система использует AI-модуль для анализа информации Instagram-профиля:

- имени пользователя;
- полного имени;
- описания профиля;
- последних публикаций.

AI определяет, соответствует ли аккаунт заданным условиям, например связан ли он с США и относится ли к финансам, инвестициям, акциям, трейдингу, богатству или другим похожим темам.

Только пользователи, которые соответствуют всем условиям, переводятся в категорию ценных финансовых блогеров.

#### 5. Автоматическая отправка личных сообщений

Система поддерживает автоматическую отправку сообщений через отдельные аккаунты для рассылки.

Модуль сообщений поддерживает:

- параллельную работу нескольких аккаунтов;
- контроль интервала отправки для каждого аккаунта;
- запись успешных отправок;
- защиту от повторной отправки;
- повторные попытки при ошибках;
- обнаружение проблемных аккаунтов;
- удаление заблокированных аккаунтов.

#### 6. Проверка состояния аккаунтов

Система автоматически проверяет, не заблокирован ли аккаунт и не находится ли он в abnormal-состоянии.

При ошибке операции система не удаляет аккаунт сразу, а сначала несколько раз проверяет его состояние:

- подтверждённая блокировка: аккаунт удаляется из базы;
- аккаунт не заблокирован, но часто ошибается: помечается как проблемный;
- ошибка сети или неопределённый результат: аккаунт сохраняется для будущей проверки.

Также доступна фоновая проверка всех аккаунтов через заданные интервалы времени.

#### 7. Фоновая автоматизация

Система содержит несколько фоновых рабочих модулей:

- модуль загрузки аккаунтов;
- модуль сбора пользователей;
- модуль AI-оценки;
- модуль отправки личных сообщений;
- модуль проверки аккаунтов;
- API состояния системы.

После запуска система может работать автоматически без постоянного ручного контроля.

#### 8. API состояния

Система предоставляет лёгкий API для отображения статистики в панели мониторинга.

API может возвращать:

- количество аккаунтов для сбора;
- количество аккаунтов для рассылки;
- количество отправленных сообщений;
- количество ожидающих сообщений;
- количество блогеров;
- количество финансовых блогеров.

### Сценарии использования

Проект подходит для:

- лидогенерации в Instagram;
- поиска зарубежных клиентов;
- поиска аудитории в финансовой тематике;
- продвижения сообществ по акциям, криптовалюте и инвестициям;
- автоматизации работы с несколькими Instagram-аккаунтами;
- точечного маркетинга;
- автоматического поиска и первичного контакта с потенциальными клиентами.

### Преимущества

- высокий уровень автоматизации;
- поддержка нескольких аккаунтов;
- AI-фильтрация целевой аудитории;
- продолжение сбора после остановки;
- проверка состояния аккаунтов;
- контроль частоты отправки сообщений;
- API для мониторинга;
- лёгкая архитектура для длительной работы.

### Рабочий процесс

```text
Импорт аккаунтов
  ↓
Автоматическое добавление аккаунтов
  ↓
Сбор пользователей целевых блогеров
  ↓
Автоматическая классификация пользователей
  ↓
AI-оценка ценных пользователей
  ↓
Расширенный сбор финансовых блогеров
  ↓
Добавление пользователей в очередь сообщений
  ↓
Автоматическая отправка Direct-сообщений
  ↓
Запись статуса отправки и состояния аккаунтов
```

### Отказ от ответственности

Проект предназначен только для технических исследований, анализа данных и изучения автоматизации рабочих процессов. Пользователи обязаны соблюдать правила платформы Instagram, местное законодательство и соответствующие условия использования сервисов. Все риски и последствия неправильного использования несёт сам пользователь.
