# 大数据开发SQL面试题50题（含答案）
本文整理了互联网大厂数据开发、数据分析、数仓等数据相关岗位面试过程中经常出现的SQL面试题，并给出了参考答案。涉及了炸裂函数、开窗函数、聚合函数开窗、在线直播人数等 以及这两年各大厂面疯了各种连续问题。

| 公司   | 面试题目                                     | 题目简介                                     | 详细内容及参考答案                                |
| ---- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| 字节跳动 | [最高峰同时直播人数](https://www.dwsql.com/interview/zijie/01) | 有如下数据记录直播平台主播上播及下播时间，根据该数据计算出平台最高峰同时直播人数。 | https://www.dwsql.com/interview/zijie/01 |
| 字节跳动 | [每分钟最大直播人数](https://www.dwsql.com/interview/zijie/02) | 有如下数据记录直播平台主播上播及下播时间，根据该数据计算出平台每分钟最大直播人数。 | https://www.dwsql.com/interview/zijie/02 |
| 字节跳动 | [股票波峰波谷](https://www.dwsql.com/interview/zijie/03) | 有如下数据，记录每天每只股票的收盘价格，请查出每只股票的波峰和波谷的日期和价格； **波峰**：股票价格高于前一天和后一天价格时为波峰 **波谷**：股票价格低于前一天和后一天价格是为波谷 | https://www.dwsql.com/interview/zijie/03 |
| 字节跳动 | [合并日期重叠的活动](https://www.dwsql.com/interview/zijie/04) | 已知有表记录了每个大厅的活动开始日期和结束日期，每个大厅可以有多个活动。请编写一个SQL查询合并在同一个大厅举行的所有重叠的活动，如果两个活动至少有一天相同，那他们就是重叠的 | https://www.dwsql.com/interview/zijie/04 |
| 字节跳动 | [查询最近一笔有效订单](https://www.dwsql.com/interview/zijie/05) | 现有订单表t_order，包含订单ID，订单时间,下单用户，当前订单是否有效   | https://www.dwsql.com/interview/zijie/05 |
| 字节跳动 | [共同使用ip用户检测问题](https://www.dwsql.com/interview/zijie/06) | 现有用户登录日志表，记录了每个用户登录的IP地址，请查询共同使用过3个及以上IP的用户对； | https://www.dwsql.com/interview/zijie/06 |
| 美团   | [每分钟最大直播人数](https://www.dwsql.com/interview/meituan/01) | 有如下数据记录直播平台主播上播及下播时间，根据该数据计算出平台每分钟最大直播人数。 | https://www.dwsql.com/interview/meituan/01 |
| 拼多多  | [累加刚好超过各省GDP40%的地市名称](https://www.dwsql.com/interview/pdd/01) | 现有各省地级市的gdp数据,求从高到底累加刚好超过各省GDP40%的地市名称，临界地市也需要。 例如:浙江省的杭州24% 宁波 20% ,杭州+宁波=44% 大于40% 取出杭州、宁波。江苏省的苏州19% 南京 14% 无锡 12%，苏州+南京=33% ，苏州+南京+无锡=45%，取出 苏州、南京、无锡 | https://www.dwsql.com/interview/pdd/01   |
| 拼多多  | [求连续段的起始位置和结束位置](https://www.dwsql.com/interview/pdd/02) | 有一张表t_id记录了id，id不重复，但是会存在间断，求出连续段的起始位置和结束位置。 | https://www.dwsql.com/interview/pdd/02   |
| 拼多多  | [求连续段的最后一个数及每个连续段的个数](https://www.dwsql.com/interview/pdd/03) | 有一张表t_id记录了id，id不重复，但是会存在间断，求出连续段的最后一个数及每个连续段的个数 | https://www.dwsql.com/interview/pdd/03   |
| 小红书  | [品牌营销活动天数](https://www.dwsql.com/interview/xhs/01) | 有营销活动记录表，记录了每个品牌每次营销活动的开始日期和营销活动的结束日期，现需要统计出每个品牌的总营销天数。 注意： 1:苹果第一行数据的营销结束日期比第二行数据的营销开始日期要晚，这部分有重叠的日期的要去重计算。 2:苹果第二行数据的营销结束日期和第三行的开始日期不连续，2019-09-07以及2019-09-08不统计到营销天数中。 | https://www.dwsql.com/interview/xhs/01   |
| 小红书  | [用户商品购买收藏行为特征加工](https://www.dwsql.com/interview/xhs/02) | 已知有:购买记录表t_order,包含自增id:id,用户ID:user_id，商品ID:goods_id,订单时间：order_time,商品类别：goods_type;用户收藏记录表t_collect_log,包含自增id，用户ID:user_id，商品ID：goods_id，收藏时间 collect_time;请用一句sql语句得出以下查询结果，得到所有用户的商品行为特征，其中用户行为分类为4种：是否已购买、购买未收藏、收藏未购买、收藏且购买。 | https://www.dwsql.com/interview/xhs/02   |
| 小红书  | [查询每个用户的第一条和最后一条记录](https://www.dwsql.com/interview/xhs/03) | 现有一张订单表 t_order 有订单ID、用户ID、商品ID、购买商品数量、购买时间，请查询出每个用户的第一条记录和最后一条记录。 | https://www.dwsql.com/interview/xhs/03   |
| 快手   | [最高峰同时直播人数](https://www.dwsql.com/interview/kuaishou/01) | 有如下数据记录直播平台主播上播及下播时间，根据该数据计算出平台最高峰同时直播人数。 | https://www.dwsql.com/interview/kuaishou/01 |
| 快手   | [用户中两人一定认识的组合数](https://www.dwsql.com/interview/kuaishou/02) | 有某城市网吧上网记录表，包含字段：网吧id，访客id（身份证号），上线时间，下线时间。规则1：如果两个用户在同一个网吧上线时间或者下线时间间隔在10分钟以内，则两个用户可能认识；规则2：如果两个用户在三家以上的网吧出现过【规则1】可能认识的情况，则两人一定认识；请计算该市中两人一定认识的组合数 | https://www.dwsql.com/interview/kuaishou/02 |
| 腾讯   | [向用户推荐好友喜欢的音乐](https://www.dwsql.com/interview/tencent/01) | 现有三张表分别为：用户关注表t_follow(user_id,follower_id)记录用户ID及其关注的人ID，请给用户1推荐他关注的用户喜欢的音乐名称 | https://www.dwsql.com/interview/tencent/01 |
| 腾讯   | [占据好友封面个数](https://www.dwsql.com/interview/tencent/02) | 有两个表，朋友关系表user_friend，用户步数表user_steps。朋友关系表包含两个字段，用户id，用户好友的id；用户步数表包含两个字段，用户id，用户的步数.查询： 占据多少个好友的封面（在好友的列表中排行第一，且必须超过好友的步数） | https://www.dwsql.com/interview/tencent/02 |
| 腾讯   | [合并连续支付订单](https://www.dwsql.com/interview/tencent/03) | 现有一张用户支付表：t_user_pay包含字段订单ID,用户ID,商户ID,支付时间,支付金额。如果同一用户在同一商户存在多笔订单，且中间该用户没有其他商户的支付记录，则认为是连续订单，请把连续订单进行合并，时间取最早支付时间，金额求和 | https://www.dwsql.com/interview/tencent/03 |
| 腾讯   | [连续5天涨幅超过5%的股票](https://www.dwsql.com/interview/tencent/04) | 现有一张股票价格表stock_data有3个字段分别是股票代码(stock_code),日期(trade_date)，收盘价格(closing_price) ，请找出满足连续5天以上（含）每天上涨超过5%的股票,并给出连续满足天数及开始和结束日期。 备注：不考虑停牌或其他情况，仅仅关注每天连续5天上涨超过5%的股票 | https://www.dwsql.com/interview/tencent/04 |
| 腾讯   | [连续登陆超过N天的用户](https://www.dwsql.com/interview/tencent/05) | 现有用户登录日志表 t_login_log,包含用户ID(user_id),登录日期(login_date)。数据已经按照用户日期去重，请查出连续登录超过4天的用户ID | https://www.dwsql.com/interview/tencent/05 |
| 腾讯   | [微信运动步数在好友中的排名](https://www.dwsql.com/interview/tencent/06) | 有两个表，朋友关系表user_friend，用户步数表user_steps。朋友关系表包含两个字段，用户id，用户好友的id；用户步数表包含两个字段，用户id，用户的步数.用户在好友中的排名 | https://www.dwsql.com/interview/tencent/06 |
| 百度   | [股票波峰波谷](https://www.dwsql.com/interview/baidu/01) | 有如下数据，记录每天每只股票的收盘价格，请查出每只股票的波峰和波谷的日期和价格； **波峰**：股票价格高于前一天和后一天价格时为波峰 **波谷**：股票价格低于前一天和后一天价格是为波谷 | https://www.dwsql.com/interview/baidu/01 |
| 百度   | [合并用户浏览行为](https://www.dwsql.com/interview/baidu/02) | 有一份用户访问记录表，记录用户id和访问时间，如果用户访问时间间隔小于60s则认为时一次浏览，请合并用户的浏览行为。 | https://www.dwsql.com/interview/baidu/02 |
| 百度   | [无效搜索](https://www.dwsql.com/interview/baidu/03) | 现有一份用户搜索日志，包含用户ID，时间，用户搜索内容。定义 无效搜索：如果用户下一次搜索内容中包含本次搜索内容，则认为本次搜索为无效搜索。请查询用户无效搜索记录 | https://www.dwsql.com/interview/baidu/03 |
| 京东   | [合并数据](https://www.dwsql.com/interview/jingdong/01) | 已知有数据A如下，请分别根据A生成B和C。                    | https://www.dwsql.com/interview/jingdong/01 |
| 滴滴   | [取出累计值与1000差值最小的记录](https://www.dwsql.com/interview/didi/01) | 已知有表t_cost_detail包含id和money两列，id为自增，请累加计算money值，并求出累加值与1000差值最小的记录。 | https://www.dwsql.com/interview/didi/01  |
| 三一重工 | [部门人员数据分析](https://www.dwsql.com/interview/sanyi/01) | 现有一张员工在职所在部门信息表，包含员工ID、所属部门、开始日期、结束日期，请查询出如下内容1.2024年1月31日A部门在职员工数；2.2024年1月份A部门员工最多时有多少员工；3.2024年1月份A部门平均有多少员工； | https://www.dwsql.com/interview/sanyi/01 |
| 华为   | [合并日期重叠的活动](https://www.dwsql.com/interview/huawei/01) | 已知有表记录了每个大厅的活动开始日期和结束日期，每个大厅可以有多个活动。请编写一个SQL查询合并在同一个大厅举行的所有重叠的活动，如果两个活动至少有一天相同，那他们就是重叠的 | https://www.dwsql.com/interview/huawei/01 |
| meta | [计算每个用户的受欢迎程度](https://www.dwsql.com/interview/meta/1) | 有好友关系表t_friend，记录了user1_id,user2_id的好友关系对。现定义用户受欢迎程度=用户拥有的朋友总数/平台上的用户总数,请计算出每个用户的受欢迎程度。 | https://www.dwsql.com/interview/meta/1   |
| 其他常见 | [每年成绩都有所提升的学生](https://www.dwsql.com/interview/cj/1) | 一张学生成绩表(student_scores)，有year-学年，subject-课程，student-学生，score-分数这四个字段，请完成如下问题：问题1：每年每门学科排名第一的学生.问题2：每年总成绩都有所提升的学生 | https://www.dwsql.com/interview/cj/1     |
| 其他常见 | [连续点击三次用户](https://www.dwsql.com/interview/cj/2) | 有用户点击日志记录表 t_click_log，包含user_id(用户ID),click_time(点击时间)，请查询出连续点击三次的用户数，连续点击三次：指点击记录中同一用户连续点击，中间无其他用户点击； | https://www.dwsql.com/interview/cj/2     |
| 其他常见 | [去掉最大最小值的部门平均薪水](https://www.dwsql.com/interview/cj/3) | 有员工薪资表t_salary,包含员工ID(emp_id)，部门ID(depart_id)，薪水(salary),请计算去除最高最低薪资后的平均薪水；（每个部门员工数不少于3人） | https://www.dwsql.com/interview/cj/3     |
| 其他常见 | [当前活跃用户连续活跃天数](https://www.dwsql.com/interview/cj/4) | 有用户登录日志表，包含日期、用户ID，当天是否登录，请查询出当天活跃的用户当前连续活跃天数 | https://www.dwsql.com/interview/cj/4     |
| 其他常见 | [销售额连续3天增长的商户](https://www.dwsql.com/interview/cj/5) | 有一张订单记录表 t_order 包含 订单ID(order_id),商户ID(shop_id),订单时间(order_time)和订单金额(order_amt),请查询出过去至少存在3天销售额连续增长的商户 | https://www.dwsql.com/interview/cj/5     |
| 其他常见 | [不及格课程数大于2的学生的平均成绩及其排名](https://www.dwsql.com/interview/cj/6) | 有学生每科科目成绩，求不及格课程数大于2的学生的平均成绩及其成绩平均值后所在的排名。 | https://www.dwsql.com/interview/cj/6     |
| 其他常见 | [计算次日留存率](https://www.dwsql.com/interview/cj/7) | 现有用户登录记录表，已经按照用户日期进行去重处理。以用户登录的最早日期作为新增日期，请计算次日留存率是多少 | https://www.dwsql.com/interview/cj/7     |
| 其他常见 | [按照顺序进行行转列拼接](https://www.dwsql.com/interview/cj/8) | 已知有表中含有两列数据id，val,数据内容如下，请按照id的大小将val进行拼接。 | https://www.dwsql.com/interview/cj/8     |
| 其他常见 | [所有考试科目的成绩都大于对应学科平均成绩的学生](https://www.dwsql.com/interview/cj/9) | 有学生每科科目成绩，找出所有科目成绩都大于对应学科的平均成绩的学生        | https://www.dwsql.com/interview/cj/9     |
| 其他常见 | [用户行为路径分析](https://www.dwsql.com/interview/cj/10) | 有一张用户操作行为记录表 t_act_log 包含用户ID(user_id),操作编号(op_id),操作时间(op_time)要求:统计每天符合以下条件的用户数：A操作之后是B操作，AB操作必须相邻;统计每天用户行为序列为A-B-D的用户数;其中:A-B之间可以有任何其他浏览记录(如C,E等),B-D之间除了C记录可以有任何其他浏览记录(如A,E等) | https://www.dwsql.com/interview/cj/10    |

