

#### 1. 如何处理单元测试产生的数据，下列哪些说法是正确的？

- A . 测试数据入库时加特殊前缀标识。
- B . 测试数据使用独立的测试库。
- C . 自动回滚单元测试产生的脏数据。
- D . 无须区别，统一在业务代码中进行判断和识别。

<details> <summary>答案（点击展开）</summary>  - ABC  </details>

#### 2. 关于并发处理，下列哪些说法符合《阿里巴巴 Java 开发手册》？

- A . 线程资源必须通过线程池提供，不允许在应用中自行显式创建线程。
- B . 同步处理时，能锁部分代码区块的情况下不要锁整个方法；高并发时，同步调用应该考虑到性能损耗。
- C . 创建线程或线程池时，推荐给线程指定一个有意义的名称，方便出错时回溯。
- D . 推荐使用 `Executors.newFixedThreadPool(int x)` 生成指定大小的线程池。( 线程池不允许使用 `Executors` 去创建，而是通过 `ThreadPoolExecutor` 的方式 )

<details> <summary>答案（点击展开）</summary>  - ABC  </details>

#### 3. 下列哪些说法符合《阿里巴巴 Java 开发手册》?`

- A . 对于“明确停止使用的代码和配置”，如方法、变量、类、配置文件、动态配置属性等要坚决从程序中清理出去，避免造成过多垃圾。
- B . 永久弃用的代码段注释掉即可，即不用加任何注释。
- C . 对于暂时被注释掉，后续可能恢复使用的代码片断，在注释代码上方，统一规定使用三个斜杠(///) 来说明注释掉代码的理由。
- D . 不要在视图模板中加入任何复杂的逻辑。

<details> <summary>答案（点击展开）</summary>  - ACD  </details>

#### 4. 关于分页查询，下列哪些说法符合《阿里巴巴 Java 开发手册》?

- A . 分页查询，当统计的 `count` 为 0 时，应该直接返回，不要再执行分页查询语句。
- B .`iBATIS` 自带的 `queryForList(String statementName,int start,int size)`分页接口有性能隐患，不允许使用。
- C . 定义明确的 `sql` 查询语句，通过传入参数 `start` 和 `size` 来实现分页逻辑。
- D . 可使用存储过程写分页逻辑，提高效率。

<details> <summary>答案（点击展开）</summary>  - ABC  </details>

#### 5. 关于接口使用抛异常还是返回错误码，下列哪些说法符合《阿里巴巴Java 开发手册》?

- A . 向公司外部提供的 `http/api` 接口，推荐使用“错误码”方式返回异常或者错误信息。
- B . 对于应用内部的方法调用，推荐使用“抛出异常”的方式处理异常或者错误信息。
- C . 跨应用的 `RPC`调用，推荐使用将“错误码”和“错误简短信息”封装成`Result`的方式进行返回。
- D . 对外提供的接口，一定要保证逻辑健壮性： 尽量避免空指针等技术类异常；对于业务类异常要做好错误码或者异常信息的封装。

<details> <summary>答案（点击展开）</summary>  - ABCD  </details>

#### 6. 关于类的序列化，下列说法哪些是正确的？

- A . 类的序列化与 `serialVersionUID` 毫无关系。
- B . 如果完全不兼容升级，不需要修改 `serialVersionUID` 值。
- C .POJO类的`serialVersionUID` 不一致会编译出错。
- D .POJO类的`serialVersionUID`不一致会抛出序列化运行时异常。

<details> <summary>答案（点击展开）</summary>  - D  </details>

#### 7. 关于 Java 的接口描述，下列哪些说法符合 《阿里巴巴 Java 开发手册》?

- A . 在接口类中的方法和属性使用 `public` 修饰符。
- B . 对于 `Service` 类，内部的实现类加 `Impl`的后缀与接口区别。例如：`ProductServiceImpl` 实现 `ProductService` 接口。
- C . 对于 `Service` 类，基于 `SOA` 的理念，是以接口方式暴露服务。
- D . 尽量不在接口里定义变量， 如果一定要定义变量，肯定是与接口方法相关，而且是整个应用的基础常量。

<details> <summary>答案（点击展开）</summary>  - BCD  </details>

#### 8. 集合在遍历过程中， 有时需要对符合一定条件的元素进行删除， 下列哪些说法是正确的？

- A . 在 `foreach` 循环里进行元素的 `remove` 操作。
- B . 使用 `Iterator` 方式，如果有并发，需要对` Iterator` 对象加锁。
- C .`Iterator` 进行元素的删除操作，绝对是线程安全的。
- D .`Java` 无法实现在遍历时，进行删除元素操作。

<details> <summary>答案（点击展开）</summary>  - B  </details>

#### 9.  关于基本数据类型与包装数据类型的使用标准， 下列哪些说法符合 《阿里巴巴 Java 开发手册》?

- A . 所有的 `POJO` 类属性必须使用包装数据类型。
- B . `RPC` 方法的返回值和参数必须使用包装数据类型。
- C . 因为`JAVA` 的自动装箱与拆箱机制，不需要根据场景来区分数据类型。
- D . 所有的局部变量推荐使用基本数据类型。

<details> <summary>答案（点击展开）</summary>  - ABD  </details>

#### 10. 关于索引的设计，下列哪些说法符合《阿里巴巴 Java 开发手册》？

- A. 对`varchar` 类型的字段建立索引，必须指定索引长度。
- B. 对 `varchar` 类型的字段建立索引，不需要指定索引长度，这样索引区分度最好。
- C. 业务上具有唯一特性的字段（含组合字段） ，必须指定唯一索引。
- D. 建复合索引时，一般选择区分度高的字段放在最左列。

<details> <summary>答案（点击展开）</summary>  - ACD  </details>


#### 11. 关于二方库版本号的命名方式，下列哪些说法符合《阿里巴巴 Java 开发手册》?

- A . 版本号命名格式：主版本号 . 次版本号 . 修订号。
- B . 主版本号 : 产品方向改变， 或者大规模 API 不兼容，或者架构不兼容升级。
- C . 次版本号 : 保持相对兼容性，增加主要功能特性，影响范围极小的 API 不兼容修改。
- D . 修订号 : 保持完全兼容性，修复 BUG 、新增次要功能特性等。

<details> <summary>答案（点击展开）</summary>  - ABCD  </details>

#### 12. 关于索引的使用，下列哪些说法是正确的？

- A . 查询语句 `WHERE a+1 = 5` 可以利用 `a` 索引。
- B . 查询语句 `WHERE date_format(gmt_create, '%Y-%m-%d') = '2016-11-11'` 无法利用 `gmt_create`索引。
- C . 当 `c` 列类型为` char` 时，查询语句 `WHERE c = 5` 无法利用` c `关于索引的设计和使用，下列哪些说法是正确的？

索引。
- D . 索引字段使用时不能进行函数运算。

<details> <summary>答案（点击展开）</summary>  - BCD  </details>

#### 13. 关于生产环境的日志文件，下列哪些说法符合《阿里巴巴 Java 开发手册》？

- A . 异常信息应该包括两类信息：案发现场信息和异常堆栈信息。
- B . 日志文件推荐至少保存 15 天，因为有些异常具备以“周”为频次发生的
特点。
- C . 避 免重 复 打 印 日志 ， 浪 费磁 盘 空 间 ，务 必在 `log4j.xml` 中 设 置
`additivity=false` 。
- D . 错误日志和业务日志尽量分开存放。

<details> <summary>答案（点击展开）</summary>  - ABCD  </details>

#### 14. 关于代码注释，下列哪些说法符合《阿里巴巴 Java 开发手册》?

- A . 特殊注释标记，请注明标记人与标记时间。
- B . 待办事宜（ TODO ） : （ [ 标记人，标记时间， [ 预计处理时间 ] ）
- C . 在注释中用 `FIXME` 标记某代码虽然实现了功能， 但是实现的方法有待商榷，希望将来能改进
- D . 在注释中用 `FIXME` 标记某代码是错误的，而且不能工作，需要及时纠正的情况

<details> <summary>答案（点击展开）</summary>  - ABD  </details>

#### 15. 关于 MySQL 性能优化的描述，下列哪些说法是正确的？

- A . 主键查询优先于二级索引查询。
- B . 表连接有一定的代价，故表连接数量越少越好。
- C . 一般情况下，二级索引扫描优先于全表扫描。
- D . 可以使用通过索引避免排序代价。

<details> <summary>答案（点击展开）</summary>  - ABCD  </details>

#### 16. 关于索引的设计和使用，下列哪些说法是正确的？

- A . 若查询条件中不包含索引的最左列，则无法使用索引。
- B . 对于范围查询，只能利用索引的最左列。
- C . 对于 `order by A` 或 `group by A` 语句，在 `A` 上建立索引，可以避免排序。
- D . 对于多列排序，需要所有所有列排序方向一致，才能利用索引。

<details> <summary>答案（点击展开）</summary>  - AD  </details>

#### 17. 关于类命名，下列哪些说法符合《阿里巴巴 Java 开发手册》?

- A . 抽象类命名使用 `Abstract` 或 `Base` 开头。
- B . 异常类命名使用 `Exception` 结尾。
- C . 测试类命名以它要测试的类的名称开始，以 `Test` 结尾。
- D . 如果使用到了设计模式，建议在类名中体现出具体模式。例如代理模式的类命名： `LoginProxy` ；观察者模式命名： `ResourceObserver` 。

<details> <summary>答案（点击展开）</summary>  - ABCD  </details>

#### 18. 关于代码注释，下列哪些说法符合《阿里巴巴 Java 开发手册》?

- A . 所有的抽象方法（包括接口中的方法）必须要用 `javadoc` 注释。
- B . 所有的方法，包括私有方法，最好都增加注释，有总比没有强。
- C . 过多过滥的注释，代码的逻辑一旦修改，修改注释是相当大的负担。
- D . 我的命名和代码结构非常好，可以减少注释的内容。

<details> <summary>答案（点击展开）</summary>  - ACD  </details>


#### 19. 关于 checked/unchecked exception ，下列哪些说法是正确的 ?

- A . 继承 `java.lang.Error` 的类属于`checked exception` 。
- B .`checked` 异常继承 `java.lang.Exception` 类。
- C .`unchecked` 异常继承 `java.lang.RuntimeException` 类。
- D .`NullPointerException` , `IllegalArgumentException` 属于 `unchecked exception` 。

<details> <summary>答案（点击展开）</summary>  - BCD  </details>


#### 20. 关于 Map 类型集合的遍历方式，下列哪些说法是正确的？

- A .`Map` 类型的实现类都同时实现了 `Iterator` 接口。
- B . 使用 `foreach` 进行遍历。
- C . 推荐使用 `keySet` 进行遍历。
- D . 推荐使用 `entrySet` 进行遍历。

<details> <summary>答案（点击展开）</summary>  - D  </details>

#### 21. 关于变量、方法名、包的命名，下列哪些说法符合《阿里巴巴 Java 开发手册》？

- A .`POJO` 类中的任何布尔类型的变量，都不要加 `is` ，因为部分框架解析时有可能会出现序列化错误。
- B . 包名统一使用单数形式，如： `com.alibaba.mpp.util` 。
- C . 中括号是数组类型的一部分，数组定义如下： `String[] args;` 不要误写为 `String args[]`；
- D .`Service/DAO` 层方法命名可以参考规约， 例如：删除的方法推荐使用 `remove`或 `delete` 做前缀。

<details> <summary>答案（点击展开）</summary>  - ABCD  </details>

#### 22. 关于常量定义，下列哪些说法符合《阿里巴巴 Java 开发手册》？

- A . 不允许出现任何魔法值（即未经预先定义的常量）直接出现在代码中。
- B . 魔法值是指程序中随意定义并赋值的变量值，如果代码编写者明白变量值意义是可以任意使用的，例如在代码中写 `if(status == 3) return error;`规范。
- C . 如果变量值仅在一个范围内变化推荐用 `Enum` 类。
- D . 在程序中，一律禁止使用枚举类型。

<details> <summary>答案（点击展开）</summary>  - AC  </details>

#### 23.  关于 maven 依赖、仲裁、规则，下列哪些说法是正确的？

- A .`<dependencies>` 的依赖会默认传递给子项目。
- B .`<dependencies>` 的依赖绝对不会传递给子项目。
- C . 在`<dependencyManagement>` 中指定版本号。
- D . 避免在不同的子项目，声明同一个二方库的不同版本号。

<details> <summary>答案（点击展开）</summary>  - ACD  </details>

#### 24. 关于二方库升级，下列哪些说法是正确的？

- A . 升级二方库只是改个版本号，不需要关联功能的回归。
- B . 升级二方库需要比对仲裁结果的差异，谨慎评估。
- C . 升级二方库，绝对不会影响到其它二方库的版本号。
- D . 只要此二方库负责人保证说不会有任何影响，即可大胆升级，直接发布上线。

<details> <summary>答案（点击展开）</summary>  - B  </details>


#### 25. 关于表字段和索引，下列哪些说法符合《阿里巴巴 Java 开发手册》?

- A . 表字段注释，如果修改字段含义或对字段表示的状态追加时，需要及时更新。
- B . 合适的字符存储长度，不但节约数据库表空间、节约索引存储，更重要的是提升检索速度。
- C . 针对表的每个字段都增加索引，加快查询速度。
- D . 字段的区分度越高，索引的查找速度越快。

<details> <summary>答案（点击展开）</summary>  - ABD  </details>

#### 26. 关于测试代码的覆盖率，下列哪些说法是正确的？

- A . 路径覆盖是最强覆盖， 符合路径覆盖且测试全部通过， 程序绝对没有问题。
- B . 语句覆盖度是最弱的覆盖度量方式。
- C . 分支覆盖与条件覆盖其实是一回事。
- D . 判定条件覆盖与路径覆盖其实是一回事。

<details> <summary>答案（点击展开）</summary>  - B  </details>

#### 27. Hashtable ，HashMap, ConcurrentHashMap 都是 Map 的实现类， 它们在处理 null 值的存储上有细微的区别，下列哪些说法是正确的？

- A .`Hashtable` 的 `KV` 都不可以为`null` 。
- B .`HashMap` 的 `KV` 都可以为`null` 。
- C .`HashMap` 的 `K` 不可以为 `null` ，`V` 可以为 `null` 。
- D .`ConcurrentHashMap` 的 `KV` 都不可以为 `null` 。

<details> <summary>答案（点击展开）</summary>  - ABD  </details>

#### 28. 关于数据库命名规则， 下列哪些说法符合 《阿里巴巴 Java 开发手册》?

- A . 数据库库名和表名没有规定，可任意取名，只要方便记忆即可。
- B . 库名应该尽量与应用名称保持一致，表的命名最好是业务名称`_`表名的方式。
- C . 无论是库名还是表名都禁用保留字，如 `desc`、`match`、`range` 等。
- D . 表名、字段名必须使用小写字母或数字。

<details> <summary>答案（点击展开）</summary>  - BCD  </details>

#### 29. 关于异常的处理方式，下列哪些说法是正确的？

- A . 为防止 `obj` 对象本身空指针异常，书写代码时应该注意加异常捕获处理，例如： `try { obj.method() } catch(NullPointerException e){ ??} `。
- B . 方法签名中，抛给调用者的关键字为 `throws`
- C . 方法内部，抛出异常实例对象为 `throws`
- D . 自定义异常要做到“认知对等”，即：抛出者和接收者要保持对自定义异常的认知统一，接收方需要知道这种异常的含义和对应的处理方案。

<details> <summary>答案（点击展开）</summary>  - BD  </details>


#### 30.  数组使用 Arrays.asList 转化为集合，下列说法哪些正确的？

- A . 数组元素的修改，会影响到转化过来的集合。
- B . 数组元素的修改，不会影响到转化过来的集合。
- C . 对 于 转 换 过 来 的 集 合 ，它 的 `add/remove/clear` 方 法 会 抛 出 :`UnsupportedOperationException` 。
- D .`Arrays.asList` 体现的是适配器模式，只是转换接口，后台的数据仍是数
组。

<details> <summary>答案（点击展开）</summary>  - ACD  </details>

#### 31. 关于文件编码和格式的设定，下列哪些说法符合《阿里巴巴 Java 开发手册》？

- A .IDE 的`text file encoding` 设置为`GBK` 格式。
- B .IDE 的`text file encoding`设置为`UTF-8` 格式。
- C .IDE 中文件的换行符使用 `unix` 格式。
- D .IDE 中文件的换行符使用 `windows` 格式。

<details> <summary>答案（点击展开）</summary>  - BC  </details>

#### 32. 关于数据库是与否概念的列的命名方式， 下列哪些说法符合 《阿里巴巴Java 开发手册》?

- A . 对于是与否概念的列名，必须使用 `can_abc` 来表示。
- B . 对于是与否概念的列名，必须使用 `is_abc` 来表示。
- C . 数据类型是 `varchar(1) `（ Y 表示是， N 表示否）。
- D . 数据类型是`unsigned tiny int`. （ 1 表示是， 0 表示否）。

<details> <summary>答案（点击展开）</summary>  - BD  </details>

#### 33. 以下关于格式规约的说法，正确的有哪些？

- A . 代码块缩进 `4` 个空格，如果使用`tab` 缩进，请设置成 `1` 个 `tab` 为 `4` 个空格；
- B . 代码块缩进 `5` 个空格，如果使用 `tab` 缩进，请设置成 `1` 个 `tab` 为 `5` 个空格。
- C . 为了保持代码美观，《手册》强烈推荐增加若干空格， 使某一行的变量与相邻对应位置的变量对齐。
- D . 方法体内的执行语句组、变量的定义语句组、不同的业务逻辑之间或者不同的语义之间推荐插入一个空行；相同业务逻辑和语义之间不需要插入空行。

<details> <summary>答案（点击展开）</summary>  - AD  </details>

#### 34. 通过集合 A.subList() 获取子集合 B，下列说法哪些是正确的？

- A . 返回的集合 B 没有实现 `Serializable` 接口，不能被序列化，所以不能应用于`RPC` 场景。
- B . 在 B 集合中添加某个元素，那么 A 集合也会添加进去此元素。
- C . 集合 A 中元素的修改不会影响到集合 B 的任何操作。
- D .对 A 元素个数的修改，会导致集合 B 的遍历产生`ConcurrentModificationException` 异常。

<details> <summary>答案（点击展开）</summary>  - ABD  </details>

#### 35. 关于捕获异常和抛异常， 下列哪些说法符合《阿里巴巴 Java 开发手册》？

- A . 如果需要捕获不同类型异常，为了方便处理，可以使用 `catch(Exceptione){...}` 。
- B . 不要捕获异常后不处理，丢弃异常信息。
- C . 捕获异常与抛异常，必须是完全匹配，或者捕获异常是抛异常的父类。
- D . 异 常 定 义 时 区 分 `unchecked / checked` 异 常 ， 避 免 直 接 使 用`RuntimeException` 抛出。

<details> <summary>答案（点击展开）</summary>  - BCD  </details>

#### 36. 关于线程安全，下列哪些说法是正确的？

- A .`SimpleDateFormat` 是线程不安全的类。
- B .`SimpleDateFormat` 是线程安全的类。
- C . 一般不要定义 `SimpleDateFormat` 的` static` 变量，如果定义为` static` ，必须保证线程安全。
- D . 推荐使用 `Apache` 封装好的 `DateUtils` 和 `DateFormatUtils` 工具类，来处理时- 间日期转换问题。

<details> <summary>答案（点击展开）</summary>  - ACD  </details>

#### 37. 为了更方便地进行单元测试，被测试的业务代码应避免以下哪些情况？

- A . 构造方法中做的事情过多。
- B . 存在过多的全局变量和静态方法。
- C . 存在过多的外部依赖。
- D . 存在过多的条件语句。

<details> <summary>答案（点击展开）</summary>  - ABCD  </details>

#### 38. 关于控制语句，下列哪些说法符合《阿里巴巴 Java 开发手册》？

- A . 推荐 `if-else` 的方式可以改写成卫语句的形式。
- B . 尽量减少 `try-catch` 块内的逻辑，定义对象、变量、获取数据库连接等操作可以移到 `try-catch `块外处理
- C .`if (condition) statements;` 单行语句不需要使用大括号。
- D . 在一个 `switch` 块内，都必须包含一个 `default` 语句并且放在最后，即使它什么代码也没有。

<details> <summary>答案（点击展开）</summary>  - ABD  </details>

#### 39. 关于参数有效性验证， 下列哪些说法符合 《阿里巴巴 Java 开发手册》？

- A . 防止 `page size` 过大导致内存溢出。
- B . 防止正则输入源串拒绝服务`ReDOS` 。
- C . 防止任意重定向。
- D . 预防 `SQL` 注入。

<details> <summary>答案（点击展开）</summary>  - ABCD  </details>

#### 40. 关于变量和常量定义，下列哪些符合《阿里巴巴 Java 开发手册》？

- A .Long a=2L；// 大写的 L
- B .Long a=2l; // 小写的 l
- C . 常量只定义一次，不再赋值，所以不需要命名规范。
- D . 不要使用一个常量类维护所有常量， 应该按常量功能进行归类， 分开维护。

<details> <summary>答案（点击展开）</summary>  - AD  </details>

#### 41. 在定义 DO/DTO/VO/ 等 POJO 类时，对属性默认值的设定， 下列哪些说法符合《阿里巴巴 Java 开发手册》？

- A . `String` 类型的默认值设定为空字符串。
- B . `Date` 类型的默认值设定为 `new Date()` 。
- C . 集合类型的默认值设定为 `Collections.EMPTY_LIST` 。
- D . 不要设定任何属性默认值。

<details> <summary>答案（点击展开）</summary>  - D  </details>

#### 42. 关于二方库依赖的解析命令，下列哪些说法是正确的？

- A .`mvn dependency:resolve` 打印出已仲裁依赖的列表。
- B .`mvn dependency:tree` 打印工程整个的依赖树结构。
- C .`mvn dependency:tree -Dverbose -Dincludes=commons-lang` 打印出与`commons-lang` 相关的详细依赖。
- D .`mvn clean install` 打印工程整个的依赖树结构，并部署到本地仓库中。

<details> <summary>答案（点击展开）</summary>  - ABC  </details>

#### 43. KV 结构的集合， 在处理 null 值的存储上有细微的区别， 下列哪些说法是正确的？

- A .`TreeMap` 的 `key` 不可以为 `null`
- B .`TreeMap` 的 `key` 可以为 `null`
- C .`ConcurrentHashMap` 的 `key` 可以为 `null`
- D .`ConcurrentHashMap` 的 `value` 可以为 `null`

<details> <summary>答案（点击展开）</summary>  - A  </details>


#### 44. 关于数据库中表相关的命名，下列哪些说法符合《阿里巴巴 Java 开发手册》?

- A . 表名、字段名禁止出现数字开头，禁止两个下划线中间只出现数字。
- B . 表名不使用复数名词。
- C . 表必备三字段命名： `id, gmt_create, gmt_modify`。
- D . 表必备三字段命名：`id, gmt_create, gmt_modified` 。

<details> <summary>答案（点击展开）</summary>  - ABD  </details>

#### 45. 关于多线程并行处理定时任务的情况，下列哪些说法符合《阿里巴巴Java 开发手册》?

- A . 推荐使用 `Timer` 方式处理。
- B . 推荐使用 `ScheduledExecutorService` 方式处理。
- C . `Timer` 运行多个 `TimeTask` 时，只要其中之一没有捕获抛出的异常，其它任务便会自动终止运行。
- D . `ScheduledExecutorService` 并发运行多个定时任务时， 其中某线程抛出异常，不会影响到其它线程的继续运行。

<details> <summary>答案（点击展开）</summary>  - BCD  </details>

#### 46. Java 代码的设计和开发注意事项，下列哪些说法符合《集合开发规约》?

- A . 禁止将 `URL` 、文件名、系统参数、数据库连接地址、 业务规则的可变参数，硬编码在工程中。
- B .`long` 或者 `Long` 初始赋值时，必须是大写的 L，不能小写。
- C . 当一个类有多个构造方法，或是多个同名方法，这些方法应该按顺序放置在一起，便于阅读。
- D . 相同参数类型， 同等业务含义， 才可以使用 `Java` 的可变参数， 参数的类型尽量避免使用 `Object` 。

<details> <summary>答案（点击展开）</summary>  - ABCD  </details>
`

#### 47. 关于数据库索引的命名， 下列哪些说法符合《阿里巴巴 Java 开发手册》？

- A . 主键索引 (`primary key`) ，字段类型为 `unsigned bigint` 、单表时推荐自增、步长为 1。
- B . 主键索引 (`primary key`) ，字段类型为 `unsigned bigint` 、单表时推荐自增、步长为 2。 
- C .  唯一索引（`unique key` ），命名规则为 `uk_` 字段名（如果多个字段继续下划线）。
- D . 普通索引 (`normal index`) ，标记成 `idx_`字段名（如果多个继续下划线） 。

<details> <summary>答案（点击展开）</summary>  - ACD  </details>

#### 48. 根据《阿里巴巴 Java开发手册》，以下功能必须进行水平权限控制校验的有？

- A .订单详情页面。
- B .类目管理后台。
- C .店铺装修后台。
- D .订单付款页面。

<details> <summary>答案（点击展开）</summary>  - ABCD  </details>

#### 49. 在多线程并发读写的情况下，下列哪些处理方式能保证对象的线程安全？

- A . 使用 `volatile` 关键字。
- B . 使用 `synchronized` 关键字给对象的读写操作加锁。
- C . 如果是基本类型，推荐使用 `java.util.concurrent.atomic` 包下面提供的线程安全的基本类型包装类，例如 `AtomicInteger` 。
- D . 如果是集合，推荐使用 `java.util.concurrent` 提供的并发集合类，例如：`ConcurrentHashMap` 。

<details> <summary>答案（点击展开）</summary>  - BCD  </details>

#### 50. 关于线程池管理线程的好处，下列哪些说法是正确的？

- A . 能够减少在创建和销毁线程上所花的时间以及系统资源的开销。
- B . 使用线程池一定能避免 `OOM` 问题。
- C . 线程资源必须通过线程池提供，不允许在应用中自行显式创建线程。
- D . 线程池能够根据资源等待情况，自动调整线程优先级并解决死锁问题。

<details> <summary>答案（点击展开）</summary>  - AC  </details>

#### 51. 关于加锁，下列哪些说法符合《阿里巴巴 Java 开发手册》？

- A . 可以只锁代码区块的情况下，就不要锁整个方法体。
- B . 高并发的业务场景下，要考虑加锁及同步处理带来的性能损耗，能用无锁数据结构，就不要用锁。
- C . 能用对象锁的情况下，就不要用类锁。
- D . 加锁时需要保持一致的加锁顺序，否则可能会造成死锁。

<details> <summary>答案（点击展开）</summary>  - ABCD  </details>

#### 52. 关于使用 explain 对数据库性能进行优化分析， 下列哪些说法符合 《阿里巴巴 Java开发手册》？

- A `SQL` 性能优化的目标：至少要达到`rang`级别，要求`ref` 级别，如果可以是`const`最好。
- B `index` 级别走的是扫描索引，所以速度会`ref` 快。
- C `range` 级别是指对表进行范围索引。
- D `ref`级别是指使用主键或者唯一索引。

<details> <summary>答案（点击展开）</summary>  - A  </details>


#### 53. 关于索引效率，下列哪些说法符合《阿里巴巴 Java 开发手册》？

- A . 使用索引的效率一定高于全表扫描的效率。
- B . 关于 `explain` 的结果， `type=index` 的索引效率好于 `type=ref` 。
- C . `sql` 查询条件 `where a like  ‘% 阿里 %’` ，不会走索引。
- D . `sql` 查询条件` where a like  ‘ 阿里 %’` ,`a`列创建了索引，一般会使用索引进行检索。

<details> <summary>答案（点击展开）</summary>  - C  </details>

#### 54. 关于枚举类型，以下描述符合规范的是？

- A . 只要是常量，就使用枚举值。
- B . 如果变量值在一个范围内变化,而且还带有名称之外的延伸属性，必须使用Enum类，如: `public enum MonthEnum{JANUARY(1),FEBRUARY(2),MARCH(3),APRIL(4),....,DECEMEBER(12);}`
- C . 枚举命名名建议带上Enum,枚举成员名称需要全大写，单词用`'_'`分割。
- D . 定义星期一至星期日这种范围固定的信息，不推荐使用枚举类型。
