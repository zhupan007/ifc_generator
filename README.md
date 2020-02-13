直接看house.txt

墙、门、窗、地板、洞口统一表示为：  
(n ox oy oz x_size y_size z_size x_yaw)  
元素编号，底部中心坐标， 宽，厚，高，偏角（弧度）
n=1,2,3,4,5 分别代表墙，门，窗，地板，洞口

如果窗户和门在墙上，则洞口需紧跟在墙的后面。举例：

1 ox oy oz x_size y_size z_size x_yaw  //第一堵墙    
2 ox oy oz x_size y_size z_size x_yaw   //在第一堵墙上的门  
3 ox oy oz x_size y_size z_size x_yaw  //在第一堵墙上的窗  
2 ox oy oz x_size y_size z_size x_yaw   //在第一堵墙上的第二个门  
5 ox oy oz x_size y_size z_size x_yaw   //在第一堵墙上的门的洞口  
5 ox oy oz x_size y_size z_size x_yaw  //在第一堵墙上的窗的洞口  
5 ox oy oz x_size y_size z_size x_yaw   //在第一堵墙上的第二个门的洞口  
1 ox oy oz x_size y_size z_size x_yaw  //第二堵墙    

使用方法：
下载ifc_generator这个文件夹  
在cmd中先进入ifc_generator文件夹里，然后输入
  
ifcdemo.exe house.txt house.ifc  
  
即可  
比如C:\Users\pan\PycharmProjects\gen_bim\ifc_generator>ifcdemo.exe house.txt house.ifc  
[Done]Generated ifc file: house.ifc

ifc打开软件推荐使用BIM Vision
