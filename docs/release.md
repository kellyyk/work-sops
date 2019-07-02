# Release

## 3.1.32
- 新功能
    - 开放基础功能
    
# 3.1.33
- 新功能
    - 添加标准插件开发 APP 一键生成命令
- 优化项
    - 数据统计中任务统计下任务详情及执行耗时页面支持列表排序
    - 数据统计中任务统计下任务详情及执行耗时页面支持跳转到流程执行详情页面
    - 优化执行任务时在 redis, celery worker 及 rabbitmq 不可用时的错误提示
    - 失败节点在重试时，对应节点增加高亮提示
    - 任务克隆前增加确认弹窗
    - 优化流程被撤销后进行节点操作的错误提示
    - 小屏宽度下头部宽度样式调整
- bug fix
    - 修复子流程删除或更新后，全局变量区没有刷新的问题
    - 修复子流程输出字段未根据子流程版本进行获取的问题
    - 修复子流程版本更新后子流程表单值未更新的问题
    - 修复在忽略错误的状态下节点在内部返回错误时还会进入调度状态的问题
    - 修复流程编辑中删除打开参数填写框的标准插件报错的问题

# 3.1.34
- 新功能
    - 业务配置中执行者配置新增强制使用功能，可以让运维人员都以同一个运维身份执行任务
- 优化项
    - 优化管理员视图在小屏中的导航栏展示
- bug fix
    - 修复不合法的变量引用语法导致参数渲染报错的问题

# 3.1.35
- bug fix
    - 修复流程导入时包含子流程的全局变量引用 ID 获取不正确的问题，数据异常后台不再返回 500 状态码
    
# 3.1.37
- bug fix
    - 修复全新部署时数据库初始化失败的问题

# 3.1.38
- 新功能
    - 流程编排连线终点放到节点上自动吸附，优化编排体验
    
# 3.1.39
- bug fix
    - 修复分支/并行网关直连汇聚网关时，删除汇聚网关产生脏数据的问题
    
# 3.1.40
- 新功能
    - 任务执行中的节点点击可查看详情
    - 顺序流连线由双击任一点删除改为单击"x"删除
    - 自定义变量新增分组，区分普通变量和元变量
    - 导航重构，首页跳转放入 logo，新增管理员入口，帮助文档改为图标方式，业务下拉框优化
    - 画布编辑强制控制开始、结束节点个数为1，达到个数限制后无法再增加新的开始结束节点
    - 编辑流程时，可以在全局变量的列表快速复制变量 KEY
- 优化项
    - 页面最小宽度统一为 1320px
    - BK-发送通知标准插件，通知分组和附加人员组合校验
    - JOB-执行作业全局变量参数展示参数描述，支持JOB平台数组类型的云参
    - 全局变量说明、标准插件说明、任务参数提示统一样式
    - 全局变量名称、流程名称、任务名称、任务执行者等需要填写名称的表单校验前自动去掉前后空格
    - 修改文本框的内部边框间距，和输入框的输入起始位置对齐
    - 代码架构优化，标准插件集和变量集移动到项目根目录下的 pipeline_plugins 中
    - 流程编辑的子流程节点配置中版本更新按钮 tooltip icon 颜色修改
    - 全局变量为空时新增提示
    - 任务执行查看/修改参数面板，收起按钮不明显，样式优化
    - 页面弹框样式统一
    - 模板导入导出表单校验提示统一
    - 优化查询流程模板的速度
- bug fix
    - 修复新建任务选择职能化任务后，后续新建的任务阶段导航都多了职能化任务的问题
    - 修复节点名称长度少于 50 个字符后台报错的问题
    - 轻应用编辑弹窗打开时，名称字段为空的问题修复
    - 变量引用解析失败时返回用户输入参数，而不是 Variable 对象
    - 子流程切换，状态未更新，dataset 获取报错兼容处理
    - BK-定时，因时区问题导致的不执行问题，执行时间修改为与业务时区相对应
    - 修复业务非运维人员可以删除流程模板的问题

# 3.1.41
- bug fix
    - 修复多次点击节点重试按钮时后导致节点卡住无法完成的问题
    - 修复任务执行时，查看子流程任务节点详情接口调用，subprocess_stack字段传值错误导致接口报错的问题修复

# 3.1.42
- bug fix
    - 修复运维人员不能查看业务中所有流程的问题

# 3.1.43
- 优化项
    - 前端页面国际化
    - celery 任务中返回的数据国际化

# 3.1.44
- 优化项
    - 前端页面国际化
- bug fix
    - 修复通知分组消失的问题
   
# 3.1.45
- bug fix
    - 修复通知分组作为变量勾选后无法保存的问题
    
# 3.1.46
- bug fix
    - 修复业务运维无权限使用未授权的流程新建任务的问题，业务运维有业务的所有权限
    
# 3.1.47
- bug fix
    - 修复全新安装时可能出现数据库初始化失败的问题
    
# 3.2.1
- 新功能
    - 流程编辑支持一键自动编排，免除手动排版对齐的枯燥工作
    - 新增本地缓存功能，可以随时还原，再也不担心前端编排数据意外丢失了
    - 流程模板、任务记录页面新增查询筛选条件
    - 新建任务节点选择后，删除多余分支或并行与配对的汇聚网关
    - 新建任务、职能化认领预览流程的画布弹窗支持子流程跳转
    - JOB-快速执行脚本标准插件增加拉取业务脚本和公共脚本功能
    - JOB标准插件执行完成可以查看执行 IP 和 LOG 详情
    - 流程模板的标准插件节点可以设置失败后是否允许手动跳过和手动重试
    - 新增周期任务功能，可以使用流程模板在新建任务时选择周期执行策略，新建周期任务
    - 新增公共流程功能，管理员用户可以在管理员入口新建全业务可见的流程
- 优化项
    - 新建全局变量、新建缓存按钮尺寸调小
    - 文本框 textarea 内容超出宽度强制断行
    - JOB标准插件执行完成后，可以在输出参数中点击任务链接跳转到作业平台
    - 删除流程模板时，提示信息添加引用该流程的流程模板详情
    - 全局变量 KEY 不能以数字开头，提示优化
    - 保存编辑中的流程模板时，增加校验并保存编辑状态的全局变量的步骤，避免数据丢失
- bug fix
    - 修复删除流程模板时提示被引用的流程中包含了已删除的流程的问题
    - 修复删除汇聚网关产生脏数据的问题
    - 修复轻应用 logo 图片超过 100k 时提示信息不展示的问题
- note
    - 依赖版本：job_ce-5.0.1、job_ee-1.4.4（JOB-快速执行脚本标准插件增加拉取业务脚本和公共脚本功能）
    - 依赖版本：open_paas_ee-2.6.22、open_paas_ce-3.0.94（增加拉取业务脚本和公共脚本、SOPS周期任务API）

# 3.2.2
- 新功能
    - JOB-执行作业支持把云参作为输出参数引用到后续的任务节点参数中
- 优化项
    - 周期任务新建后默认启动
    - 周期任务列表页面版权信息贴底
    - 部分翻译优化
- bug fix
    - 修复流程编辑时，任务节点可以连接自身的问题
    - 修复公共流程模板新建任务跳转问题
    - 修复数据统计页面时间选择器样式和时间范围提示不统一的问题
    - 修复JOB-快速执行脚本使用公共脚本时传参错误问题
    - 修复IP选择器点击后自动收缩的问题
    - 修复自动编排标准插件参数丢失的问题
- note
    - 依赖版本：job_ce-5.0.1、job_ee-1.4.4（新增 job get_job_instance_global_var_value API）
    - 依赖版本：open_paas_ee-2.6.25（新增 job get_job_instance_global_var_value API）

# 3.2.3
- 优化项
    - 业务中查看的公共流程列表去掉子流程更新字段
    - 周期任务在运行时禁止修改流程的参数
- bug fix
    - 修复职能化人员使用公共流程新建任务报404的问题
    - 修复审计中心查看任务状态链接错误问题
    - 业务首页禁止在轻应用、职能化、审计中心页面触发
    - 修复数据统计外链跳转时业务切换问题
    
# 3.2.4
- 新功能
    - 新增导入流程模板替换JOB相关ID的接口
    - JOB-执行作业标准插件展示输出云参
- 优化项
    - 编辑流程模板时，公共属性中类型校验提示在选择类型后隐藏
    - 日期时间变量图标重叠的样式优化
    - 进入管理员入口导航后禁用业务切换
- bug fix
    - 修复标准插件表格参数未保存时，失去焦点后无法再次编辑的问题
    - 修复数据统计部分数据不准确的问题
    - 修复标准插件组合参数校验的问题
    - 修复CMDB系列标准插件拓扑树选择时ID重复导致多个节点被选中的问题
    - 修复同时唤醒并行分支的多个分支时部分子进程卡住的问题

# 3.2.5
- 新功能
- bug fix
    - 轻应用和职能化入口新建任务去掉周期执行选项
    - 修复日期时间变量图标重叠的样式问题
    - 修复流程编辑中标准插件配置的失败处理tooltip垂直方向错位问题
    
# 3.3.1
- 新功能
    - 代码架构调整，适配最新版开发框架
    - 流程编辑新增框选功能，可以多选节点并移动、删除、复制粘贴（包含开始、结束节点时不可复制）
    - 业务流程、公共流程新增子流程是否更新的筛选条件
    - 新建任务节点选择阶段新增预览模式，如果流程包含可选节点，用户可以预览调整节点后的流程（不包含网关的流程会自动编排）
    - 数据统计-任务统计新增按时间维度的任务数量趋势图
    - 社区版开放轻应用、职能化、数据统计功能
- 优化项
    - 标准运维SaaS部署时默认容器分配内存大小改为 2G
    - 流程编辑、任务执行页面样式重构
    - 职能化中心、审计中心、流程列表、任务列表等表格样式重构，新增高级搜索
    - JOB-执行作业区分云参和上下文参数，只有云参可以作为输出变量
    - JOB-执行作业的全局变量参数由通过 id 改为 通过 name 传参，多个JOB-执行作业的全局变量参数名一致可以复用参数
- bug fix
    - 新建职能化类型任务去掉周期执行选项
    
# 3.3.2
- bug fix
    - 修复社区版判断用户角色异常问题

# 3.3.3
- 新功能
    - 流程编辑画布添加标准插件个数提示
    - 添加【CC-转移主机至空闲机】插件
    - JOB 执行作业插件允许用户引用 JOB 云参
- 优化项
    - 国际化样式优化
    - 首页收藏流程弹框样式优化
    - 数据统计图表中筛选条件的时间选择宽度优化
    - 职能化中心、审计中心、轻应用任务表格样式优化，添加搜索条件
    - JOB 相关插件更改为 JOB 回调方式
- bug fix
    - 修复引用多选下拉框报错的问题
    - 流程编辑请求标准插件配置项 404 导致页面白屏问题
    - 修复新建任务节点调整后无标准插件节点的分支被误删除的问题
    - 修复 IP 选择器根据拓扑选择不生效的问题
    - 修复公共流程下查看业务相关插件后台返回 500 的问题
    - 修复插件参数中带中文时流程执行错误的问题
    - 修复社区版 JOB 跳转链接不正确的问题
    - 修复在前端数据结构不正确时，创建流程后台返回 500 的问题

# 3.3.4
- bug fix
    - 修复轻应用 LOGO 获取不到的问题
    - 修复流程统计 - 流程引擎 - 创建任务数不正确的问题
    - 修复用户能够通过轻应用进入标准运维业务首页的问题
    - 修复职能化中心不能正常认领任务的问题
- 优化项
    - JOB 相关插件拉取 CC 信息时不再使用缓存

# 3.3.5
- bug fix
    - 修复流程模板高级搜索栏中无法清空子流程状态的问题
    - 修复打开标准插件时表单可能会不渲染的问题
    - 修复职能化任务记录下任务状态信息样式错误的问题

# 3.3.6
- 优化项
    - 国际化完善
- bug fix
    - 修复运维在任务列表删除任务后，职能化列表还能看到任务的问题
    - 修复数据统计按标准插件统计分页异常的问题

# 3.3.7
- bug fix
    - 修复自动排版在流程存在换行的情况下错位的问题

# 3.3.8
- bug fix
    - 修复用户在没登录过标准运维的情况下无法调用 API 接口的问题
    
# 3.3.9
- bug fix
    - 修复周期任务在固定月份和日期时 beat 进程退出的问题
    - 修复任务节点失败后重试时如果参数填写出错，会导致无法通过修改参数再次重试的问题
    - 修复职能化认领页面点击认领按钮页面会重新刷新的问题
    - 修复任务节点执行时间超过一天后耗时计算不正确的问题

# 3.3.10
- bug fix
    - 修复获取任务流程状态接口 API 返回的节点名与实际节点名不符的问题

# 3.3.11
- bug fix
    - 修复在 API 中调用 ESB 获取用户信息异常的问题

# 3.3.12
- bug fix
    - 修复在 get_task_status API 返回的 elapsed_time 为 Float 的问题
    
# 3.3.13
- 新功能
    - 新增进阶版IP选择器类型的全局变量，支持多种选择IP方式，如通过勾选配置平台多级拓扑树动态获取，或者直接选择静态服务器，获取通过任一拓扑实例名字组合筛选/排除；之前的IP选择器改为IP选择器(简单版)
    - 新增节点回调 API，可以通过该接口继续执行中等待回调的标准插件节点，如BK-暂停、JOB系列插件
    - 在父流程中更新引用的子流程时，保留用户当前编辑输入参数表单的值
    - 轻应用、职能化中心、审计中心页面增加高级搜索功能
    - 任务执行节点树查看按照广度优先排序
    - 数据统计页面拉取所有未下线业务
- 优化项
    - 自定义全局变量改为从后台接口获取，去掉前端的 vue 硬编码
    - 流程编辑中本地缓存表格实现方式改为 table 元素实现，优化页面
    - 查看任务执行参数，需要等待所有参数加载完毕再取消 loading 状态
    - 新建或编辑全局变量时，配置项没有加载完成，禁用保存按钮
    - 获取节点详情及创建任务 API 返回数据新增任务树及任务链接
    - JOB-执行作业失败后查看 IP 日志详情未展示所有状态的 IP
    - 流程模板导出弹窗页面优化
    - 优化CMDB-故障机替换插件错误信息
    - 不允许用户在已停运业务下进行任何操作
    - 优化流程导入弹窗按钮的文案
    - 禁止业务流程和公共流程交叉导入时保留ID
    - 职能化中心列表所属业务置于第一列，ID改为任务ID并和运维视角保持一样的值
    - 优化执行任务修改参数禁用态中下拉框和文本框的 padding 边距
- bug fix
    - 修复JOB-快速执行脚本中先选择"公共脚本"或"业务脚本"并勾选到全局变量后，再选择"手工录入"时勾选的全局变量不消失的问题
    - 公共流程模版列表和普通流程模版列表数据源做区分，修复选择业务流程等待表格刷新时切换到公共流程，表格数据是业务流程的问题
    - 修复BK-发送通知插件中邮件通知内容不换行的问题
    - 修复任务执行页面查看任务参数节点树样式错位的问题
    - 修复节点重试取消按钮点击无效问题
    - 修复自定义全局变量为弹窗编辑时，不点开编辑直接保存导致value丢失的问题
    - 修复上传轻应用 LOGO 链接拼接错误的问题[企业版]
    - 修复用户在只有一个已归档业务时访问业务首页返回 500 的问题
    - 修复非运维角色执行任务时无法正确获取业务下拥有运维角色用户的问题
    - 修复获取公共流程列表接口中返回的数据缺少子流程是否更新的问题
    - 修复新建周期任务点击下一步后不跳转的问题
    - 修复下拉框Tag设置多选后default属性不生效的问题
- note
    - 依赖版本：open_paas_ce-3.2.507/open_paas_ee-2.7.20（新增节点回调 API，获取节点详情及创建任务 API 返回数据新增任务树及任务链接）
    
# 3.3.14
- 新功能
    - 添加公共流程模板导入 API，支持其他应用通过 API 新建公共流程
- 优化项
    - 轻应用页面重构，展示更新人、更新时间、使用权限等更多信息
    - redis 环境变量配置支持在部署时注入作为默认值，用户在数据库中配置项可以覆盖默认值
    - 新建任务的参数填写、职能化认领页面表格内 textarea 宽度自适应
    - 去掉流程模版本地缓存为空时 hover 底色
    - 执行任务时操作按钮状态切换优化
    - 导出流程弹窗 loading 时，禁用筛选条件下拉框
    - 不允许用户删除已经开始执行且未进入归档状态的任务
    - 页面头部导航左右间距统一
    - 优化 IP 选择器加载样式
    - 日志配置优化，支持本地开发时在 console 中展示请求日志
    - 优化本地开发配置，支持不使用全局变量，直接修改本地代码运行工程
- bug fix
    - 修复无编辑权限的用户可以更新流程模板数据的问题
    - 修复单元测试在使用 sqllite 时第一次 migrate 无法完成的问题
    - 修复任务执行前，修改参数保存后，查看参数节点参数信息不展示问题
    - 修复新建缓存控制台报校验相关错误的问题
    - 修复下拉框表单项搜索结果为空时，选择项被清空问题
    - 修复编辑表格类型参数导致插件参数面板收起的问题
    - 统一管理员入口页面的URL前缀，修复管理员入口页面刷新后默认业务被置空的问题
    - 修复任务执行页面，查看参数中汇聚节点后的插件节点未显示的问题
    - 修复页面中表格翻页后，通过高级搜索查询数据为空的问题
    - 修复职能化页面新建任务弹窗中，清空选择的业务后，流程模板选择项未清空的问题
    - 修复JOB-执行作业输出参数偶现显示其他插件节点已勾选输出参数的问题