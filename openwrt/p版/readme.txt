p��pythonʹ�ý̳̣�

1��
   �������ļ�������root�ļ����У�ʹ�� 'scp -r �ļ��� /' ��������ļ��и��ǽ�ȥ��
2��
   �޸��ļ�Ȩ��Ϊ777���Ҽ������޸ġ�
3��
   ���ţ���puttyֱ��ճ���⼸�����
   #!/bin/sh
   cp /lib/netifd/proto/ppp.sh /lib/netifd/proto/ppp.sh_bak
   sed -i '/proto_run_command/i username=`echo -e "$username"`' /lib/netifd/proto/ppp.sh
   sed -i '/proto_run_command/i password=`echo -e "$password"`' /lib/netifd/proto/ppp.sh
   �����˺�Ҫ����\r\n
4����װpython��
����ʣ���С����7.5M�������·�ʽ��װ

   opkg update

   opkg install python-light -d ram

   export PATH=$PATH:/tmp/usr/bin/

   export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/tmp/usr/lib/


   �����������ӵ�/etc/profile�У�����·��������һ��ִ��
   opkg update    
   opkg install python-lightd
   ���ú�֮�����drcom��������������ִ��  
   opkg update    
   opkg install python-lightd
5�� 
   ��������wiresharkץ����ȥhttps://drcoms.github.io/drcom-generic/������������Ȼ����luci������д���ɡ�
6��
   /etc/rc.d/S90drocm��һ�����ӣ�������Ҫ���½������Ҽ��½����ӣ����ӵ�../init.d/drcom���ɡ�