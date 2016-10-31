# 第五次作业
##查询用户test1可以查看的页面
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
</br>
select * from Sys_Menu where MenuID=(    </br>
select PrivilegeAccessKey from CF_Privilege where PrivilegeAccess=Sys_Menu and PrivilegeOperation=Permit and PrivilegeMasterKey=(   </br>
select RoleID from CF_UserRole where UserID=(    </br>
select UserID from CF_User where LoginName=test1)))    
</br>
![1](https://cloud.githubusercontent.com/assets/16076941/19847496/42cbb0fa-9f82-11e6-8994-2377c792492b.png)


</br>
</br></br></br>
##对订单(order)页面中的操作权限
Begin   </br>
查询CF_User表中所有数据    </br>
IF LoginName=test1 则 查询该记录UserID数据记为A    </br>
查询CF_UserRole表中所有数据    </br>
IF UserID=A 则 查询该记录RoleID数据记为B    </br>
查询CF_Privilege表记为a中所有数据和查询Sys_Button表记为b中所有数据    </br>
IF a.Privilege=B and a.PrivilegeAccess=Sys_Button and a.PrivilegeOperation=Permit and a.PrivilegeAccess=b.Sys_Button   </br>
Print BtnName    </br>
End   </br>
</br>

select a.ManuName from Sys_Menu as a,CF_Privilege as b where a.MenuID=b.PrivilegeAccessKey and  </br>
b.PrivilegeAccess=Sys_Menu and b.PrivilegeOperation=Permit and b.PrivilegeMasterKey=(   </br>
select RoleID from CF_UserRole where UserID=(    </br>
select UserID from CF_User where LoginName=test1)))    </br>
</br>
![2](https://cloud.githubusercontent.com/assets/16076941/19847570/d7a513b0-9f82-11e6-9584-2d8e7285e373.png)
