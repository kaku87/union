union
=====
###目标

本任务为高级别任务，并不打算直接开始。遵循小迭代的思路，先完成一些准备项目，积累相关开发经验和技术储备再开始。

###演示地址

heroku: http://gunion.herokuapp.com<br/>

vps: http://198.199.86.44:8080 <br/>

###项目进展

7/14/2013 Alpha 版本release<br/>

7/8/2013 强行发布pre alpha 

7/4/2013 核心开发团队，进行小迭代
  1. 部署vps
  2. 寻找突破口，制作可以运行的工会系统

从bay6出发，统计bay6的所有项目 ＝> 可以给项目分级（此步骤可省略，默认都是一级就好）＝>扫瞄bay6项目的commit，分到人头上，按时间一分，就是commit

可以按项目加权，按时间分组，就是每天的成长，求和就是总经验值，这样考虑因素少，算是简化。因为我们只关心，成员对bay6的贡献

能简化的话，就先按这个思路，出个用户成长值，有了这个值，就能排行，就能出历史变化报告了。而且，以后再改也容易，就是从新按其他规则取用户成长值就行

###职业工会升级系统

任务等级： 高级<br/>
前提任务： 完成三个中级任务<br/>

工会维护系统，提供工会成员成长系统维护，深度集成githubapi。通过github commit和不同认证项目commit，得到项目经验和等级和勋章。

遵循磨级，刷怪，组团打BOSS的模式。工会系统，需要有track成员commit的功能，需要能够track成员完成项目的功能。同时生成成员成长报告。有定的经验可以做高级别的任务。任务（项目做的越多）越得到信任。

###可操作拆分

union将划分为不同等级小任务，反复练习重构后会重写到主union任务中来。<br/>
初步划分<br/>
  1. github登录
  2. 团队成员github commit，收集
  3. 根据commit数量和认证项目等级加权，得到经验等级
  4. 生成成员成长报告，
  5. 生成成员，总经验值排名
  6. 生成成员，成长值排名，月份，周，迭代周期排名

### 说明

如何给成员手动跑分

[见这里](doc/score.markdown)

whenever<br/>
  1.生成定时处理 whenever -w<br/>
  2.更新定时处理 whenever -i<br/>
  3.清理定时处理 whenever -c<br/>

deplayed_job<br/>
```ruby
RAILS_ENV=production script/delayed_job start
RAILS_ENV=production script/delayed_job stop
```

