# Chart

支持的图表类型：

- 流程图 (Flowchart)
- 序列图 (Sequence Diagram)
- 类图 (Class Diagram)
- 状态图 (State Diagram)
- 甘特图 (Gantt Chart)
- 饼图 (Pie Chart)

## 流程图

```mermaid
graph TB
    A[开始] --> B{条件判断}
    B -.->|Yes| C[执行操作A]
    B ==>|No| D(执行操作B)
    C ---> E((结束))
    D --> E
```

方向：

- TD 或 TB：从上到下
- BT：从下到上
- RL：从右到左
- LR：从左到右

## 时序图与甘特图

```mermaid
sequenceDiagram
    participant A as 用户
    participant B as 系统
    participant C as 数据库
    
    A->>B: 登录请求
    B->>C: 验证用户信息
    C-->>B: 返回验证结果
    B-->>A: 登录成功/失败
```

```mermaid
gantt
    title 项目开发计划
    dateFormat  YYYY-MM-DD
    section 设计阶段
    需求分析      :done,    des1, 2024-01-01,2024-01-15
    UI设计       :active,  des2, 2024-01-10, 30d
    section 开发阶段
    前端开发      :         dev1, after des2, 45d
    后端开发      :         dev2, 2024-02-01, 60d
    section 测试阶段
    单元测试      :crit,    test1, after dev1, 15d
    集成测试      :         test2, after dev2, 10d
```

## 饼图

```mermaid
pie
    title 浏览器市场份额
    "Chrome" : 65
    "Safari" : 15
    "Firefox" : 10
    "其他" : 10
```

## 类图

```mermaid
classDiagram
    class 用户 {
        +用户名: string
        +密码: string
        +登录()
    }
    
    class 订单 {
        +订单号: int
        +创建日期: date
        +计算总价()
    }
    
    用户 "1" --> "n" 订单
```

## 高级技巧

### 主体定制

```mermaid
%%{init: {'theme': 'forest'}}%%
pie
    title 自定义主题
    "项目A" : 30
    "项目B" : 50
    "项目C" : 20
```

### 交互式图表

```mermaid
graph TD
    A[点击我] --> B[显示详细信息]
    click A "https://www.runoob.com" "这是提示文本"
```
