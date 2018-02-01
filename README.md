描述:
        SC 是用于与服务控制管理器和服务进行通信的命令行程序。
用法:
        sc <server> [command] [service name] <option1> <option2>...
 
 
        选项 <server> 的格式为 "\\ServerName"
        键入 "sc [command]" 可以获得有关命令的进一步帮助
        命令:
          query-----------查询服务的状态，
                          或枚举服务类型的状态。
          queryex---------查询服务的扩展状态，
                          或枚举服务类型的状态。
          start-----------启动服务。
          pause-----------向服务发送 PAUSE 控制请求。
          interrogate-----向服务发送 INTERROGATE 控制请求。
          continue--------向服务发送 CONTINUE 控制请求。
          stop------------向服务发送 STOP 请求。
          config----------更改服务的配置(永久)。
          description-----更改服务的描述。
          failure---------更改服务失败时执行的操作。
          failureflag-----更改服务的失败操作标志。
          sidtype---------更改服务的服务 SID 类型。
          privs-----------更改服务的所需权限。
          qc--------------查询服务的配置信息。
          qdescription----查询服务的描述。
          qfailure--------查询失败时服务执行的操作。
          qfailureflag----查询服务的失败操作标志。
          qsidtype--------查询服务的服务 SID 类型。
          qprivs----------查询服务的所需权限。
          qtriggerinfo----查询服务的触发器参数。
          qpreferrednode--查询首选的服务 NUMA 节点。
          delete----------(从注册表)删除服务。
          create----------创建服务(将其添加到注册表)。
          control---------向服务发送控制。
          sdshow----------显示服务的安全描述符。
          sdset-----------设置服务的安全描述符。
          showsid---------显示相应于假定名称的 SID 字符串。
          triggerinfo-----配置服务的触发器参数。
          preferrednode---设置首选的服务 NUMA 节点。
          GetDisplayName--获取服务的 DisplayName
          GetKeyName------获取服务的 ServiceKeyName。
          EnumDepend------枚举服务的依存关系。
 
C:\Users\administrator>sc create testService binPath= "E:\C++\vs2015Test\testService\Debug\testService.exe" start= auto
[SC] CreateService 成功
C:\Users\administrator>net start testService
 
 
通过services.msc 查看新创新的服务。
 
C:\Users\administrator>sc delete
描述:
        从注册表删除服务项。
        如果服务正在运行，或另一进程已经打开
        到此服务的句柄，服务将简单地标记为
        删除。
用法:
        sc <server> delete [service name]
C:\Users\administrator>sc delete testService
[SC] DeleteService 成功
C:\Users\administrator>
 
C:\Users\administrator>sc create
描述:
        在注册表和服务数据库中创建服务项。
用法:
        sc <server> create [service name] [binPath= ] <option1> <option2>...
 
选项:
注意: 选项名称包括等号。
      等号和值之间需要一个空格。
 type= <own|share|interact|kernel|filesys|rec>
       (默认 = own)
 start= <boot|system|auto|demand|disabled|delayed-auto>
       (默认 = demand)
 error= <normal|severe|critical|ignore>
       (默认 = normal)
 binPath= <BinaryPathName>
 group= <LoadOrderGroup>
 tag= <yes|no>
 depend= <依存关系(以 / (斜杠) 分隔)>
 obj= <AccountName|ObjectName>
       (默认 = LocalSystem)
 DisplayName= <显示名称>
 password= <密码>

