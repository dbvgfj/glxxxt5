# 第五次作业
Begin
查询CF_User表中所有数据
IF LoginName=test1 则 查询该记录UserID数据记为A
查询CF_UserRole表中所有数据
IF UserID=A 则 查询该记录RoleID数据记为B
查询CF_Privilege表记为a中所有数据和查询Sys_Menu表记为b中所有数据
IF a.Privilege=B and a.PrivilegeAccess=Sys_Menu and a.PrivilegeOperation=Permit and a.PrivilegeAccess=b.Sys_Menu
查询Sys_Menu表中MenuName数据
Print MenuName
End 
