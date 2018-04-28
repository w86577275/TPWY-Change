# TPWY-说明： 
+ added  
- fixed   
* improved

Current version 2018.4.8-2018.4.14
----------------------------------
[Web]
+ 未新增
- 修复添加教室时教学楼可能为空的情况（SYJ）
* 优化任选课公选页面（SYJ）
[Client]

Current version 2018.4.15-2018.4.21
-----------------------------------
[Web]
+ 新增院系送审审核页面（哈工程版），设置到的数据库更改，无。权限改动无，新菜单已经报备爽爽进行配置。（WZS）
  新增导师查询抽签页面（张东旭写），目前配置给哈工程，会需要给其他高校也进行页面配置，涉及权限，无。（WZS）
  
- 送审BUG修复和功能修改，不一一列举（WZS）
  20180409	public List<ResultEntity> GetRoomID(string Buildingid) 方法存在错误，已修正。	王兆松
  20180409	开题，中期，预答辩，答辩，学位论文，几个页面论文题目字段加长为400字节，涉及对应数据库表，BLL，和前端页面。已修改	王兆松 
* 成绩打印优化（WZS）
  涉及到相关的数据库表、视图和存储过程为 dbo.pp_ScoreReportPrint（全修改），dbo.VB_SelectCourse_SimpleRSEx（修改，添加字段，重修重考缓考申请状态字   段），dbo.VB_SelectCourse_StuDetailWithSnoEx（修改，添加字段，重修重考缓考申请状态字段），dbo.VB_SelectCourse_NewEx（修改，添加字段，重修重考缓   考申请状态字段）， dbo.计算用学生选课采集表（新增表），dbo.计算用成绩与学分结果表（新增表），dbo.nTB_StuScoreStatic（修改，新增字段），             dbo.nTB_StuSelCourseCredit（修改，新增字段）。以上改动皆可以通过数据库对比工具更新，不需要额外手动。
  各家更新时注意暂时将“平均成绩与学分计算.sql”一并拿过去进行执行，直到这个方法被WZS做成触发器和页面为止，更新时候找WZS要“平均成绩与学分计算.sql”。（WZS）
  
[Client]

Current version 2018.4.21-2018.4.28
-----------------------------------
