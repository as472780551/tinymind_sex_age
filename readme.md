# 每个大类的数量, 小类的数量, 每个设备APP的数量, 
# 早中晚, 深夜, 以及时长, 周末, 周一,工作日,运行时间, 


# 绝对值,相对值

# 一天24小时,分割为4个段, 一周7天(), 28个维度.

# 以周为单位的趋势

# 删除无效APP的属性

# 所有APP最大周/月的APP百分比

# 单个APP的最大周/月的APP百分比

# 可视化,每一个的Device, APP数量, 百分比, 峰值

# 去除Test数据没有的维度

# 获取APP采样最多的那一周的数据, 使用APP最多的个数是几个, 每个时间段百分比
# 获取所有时间段的数据, 使用APP最多的个数是几个, 每个时间段百分比

# 安装的APP是多少个

# 每小时的分布, 最多的那一周和所有的数据,2个维度
# LDA 安装,和使用分别计算

# 一款应用超过2天算一次,有多少个应用属于这种情况

# 去除长Session后,时间分别分布如何
# 性别和年纪分开预测是否更合适
# 每个分组,app的个数以及各个时间段的时长
# 模型融合
# 每个字段对应的TFIDF
# 平均Package Duration
# 安装却不使用,反向指标
# 平均每天使用时间
# 按照周末和工作日百分比对比
# 删除长Session数据
# Top APP_Type
# 年龄是category还是value

# 删除低频APP, uselessAPP

# LDA 参数调整
# 最常用APP TOP#N 的归属label,以及时长
# DNN
# Drop usless in usage, not only lda
# Long Session的个数
# 统一只取最后N天的数据 ❎
# 去公共时间的数据
# 数据倾斜(年龄上面)


Ref: https://github.com/neuronblack/yiguan/blob/master/Untitled1.ipynb



nohup python -u tiny/gen_sub.py > gen_sub.log 2>&1 &

nohup python -u tiny/util.py > util.log 2>&1 &


nohup python -u tiny/test.py > test.log 2>&1 &

nohup python -u tiny/test2.py > test22.log 2>&1 &


nohup python -u tiny/usage.py > usage.log 2>&1 &


nohup python -u model/rf.py > rf.log 2>&1 &

nohup /apps/dslab/anaconda/python36new/bin/python -u model/dnn.py > dnn.log 2>&1 &
