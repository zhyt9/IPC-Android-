# IPC-Android-
IPC 即Inter-Process Communication

1.进程和线程
  进程：一般指一个执行单元，在PC和移动设备上指一个程序或者一个应用，一个进程可以包含多个线程
  线程：CPU调度的最小单元
  
2.通过给四大组件指定android：process 属性来开启多进程模式
  以":"开头的进程，属于当前应用的私有进程
  不以":"开头的进程，属于全局进程，其他应用可以通过ShareUID方式和它跑在同一个进程中
  
3.Android为每一个应用分配了一个独立的虚拟机，即每一个进程都分配了一个独立的虚拟机
  同一个进程中的组件属于同一个虚拟机同一个Application
  不同进程中的组件属于两个不同的虚拟机和Application，所以不能通过内存来共享数据
