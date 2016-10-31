# 第五次作业
Begin   </br>
查询CF_User表中所有数据   </br>
IF LoginName=test1 则 查询该记录UserID数据记为A   </br>
查询CF_UserRole表中所有数据    </br>
IF UserID=A 则 查询该记录RoleID数据记为B    </br>
查询CF_Privilege表记为a中所有数据和查询Sys_Menu表记为b中所有数据   </br>
IF a.Privilege=B and a.PrivilegeAccess=Sys_Menu and a.PrivilegeOperation=Permit and a.PrivilegeAccess=b.Sys_Menu    </br>
查询Sys_Menu表中MenuName数据   </br>
Print MenuName    </br>
End   </br>
