����:
        SC �������������ƹ������ͷ������ͨ�ŵ������г���
�÷�:
        sc <server> [command] [service name] <option1> <option2>...
 
 
        ѡ�� <server> �ĸ�ʽΪ "\\ServerName"
        ���� "sc [command]" ���Ի���й�����Ľ�һ������
        ����:
          query-----------��ѯ�����״̬��
                          ��ö�ٷ������͵�״̬��
          queryex---------��ѯ�������չ״̬��
                          ��ö�ٷ������͵�״̬��
          start-----------��������
          pause-----------������� PAUSE ��������
          interrogate-----������� INTERROGATE ��������
          continue--------������� CONTINUE ��������
          stop------------������� STOP ����
          config----------���ķ��������(����)��
          description-----���ķ����������
          failure---------���ķ���ʧ��ʱִ�еĲ�����
          failureflag-----���ķ����ʧ�ܲ�����־��
          sidtype---------���ķ���ķ��� SID ���͡�
          privs-----------���ķ��������Ȩ�ޡ�
          qc--------------��ѯ�����������Ϣ��
          qdescription----��ѯ�����������
          qfailure--------��ѯʧ��ʱ����ִ�еĲ�����
          qfailureflag----��ѯ�����ʧ�ܲ�����־��
          qsidtype--------��ѯ����ķ��� SID ���͡�
          qprivs----------��ѯ���������Ȩ�ޡ�
          qtriggerinfo----��ѯ����Ĵ�����������
          qpreferrednode--��ѯ��ѡ�ķ��� NUMA �ڵ㡣
          delete----------(��ע���)ɾ������
          create----------��������(������ӵ�ע���)��
          control---------������Ϳ��ơ�
          sdshow----------��ʾ����İ�ȫ��������
          sdset-----------���÷���İ�ȫ��������
          showsid---------��ʾ��Ӧ�ڼٶ����Ƶ� SID �ַ�����
          triggerinfo-----���÷���Ĵ�����������
          preferrednode---������ѡ�ķ��� NUMA �ڵ㡣
          GetDisplayName--��ȡ����� DisplayName
          GetKeyName------��ȡ����� ServiceKeyName��
          EnumDepend------ö�ٷ���������ϵ��
 
C:\Users\administrator>sc create testService binPath= "E:\C++\vs2015Test\testService\Debug\testService.exe" start= auto
[SC] CreateService �ɹ�
C:\Users\administrator>net start testService
 
 
ͨ��services.msc �鿴�´��µķ���
 
C:\Users\administrator>sc delete
����:
        ��ע���ɾ�������
        ��������������У�����һ�����Ѿ���
        ���˷���ľ�������񽫼򵥵ر��Ϊ
        ɾ����
�÷�:
        sc <server> delete [service name]
C:\Users\administrator>sc delete testService
[SC] DeleteService �ɹ�
C:\Users\administrator>
 
C:\Users\administrator>sc create
����:
        ��ע���ͷ������ݿ��д��������
�÷�:
        sc <server> create [service name] [binPath= ] <option1> <option2>...
 
ѡ��:
ע��: ѡ�����ư����Ⱥš�
      �Ⱥź�ֵ֮����Ҫһ���ո�
 type= <own|share|interact|kernel|filesys|rec>
       (Ĭ�� = own)
 start= <boot|system|auto|demand|disabled|delayed-auto>
       (Ĭ�� = demand)
 error= <normal|severe|critical|ignore>
       (Ĭ�� = normal)
 binPath= <BinaryPathName>
 group= <LoadOrderGroup>
 tag= <yes|no>
 depend= <�����ϵ(�� / (б��) �ָ�)>
 obj= <AccountName|ObjectName>
       (Ĭ�� = LocalSystem)
 DisplayName= <��ʾ����>
 password= <����>

