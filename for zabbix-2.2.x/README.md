Zatree���
==================================

��zabbix�߽�ǧ���򻧵�ʱ������Ҳ����Ҫ����ʲô��

zatree�Ǽ�����zabbix��һ���������Ҫ�������ṩhost group������չʾ����item��ָ���ؼ��ֲ�ѯ����������

���Թ�2.0.6��2.0.7�汾��������2.0.X�Ķ�Ӧ��֧�֣������֧����Ҳû�취���Լ����ָĸİɡ�

Zatree��װ
==================================

1�������ļ�

git clone https://github.com/spide4k/zatree.git zatree

2����������ļ�

����zabbix webĿ¼λ����/var/www/zabbix,����zabbixĿ¼

ZABBIX_PATH=/var/www/zabbix

��������ļ���Ŀ¼

cp -rf zatree $ZABBIX_PATH/

cd $ZABBIX_PATH/zatree/addfile

cp -f CLineGraphDraw_Zabbix.php CGraphDraw_Zabbix.php CImageTextTable_Zabbix.php $ZABBIX_PATH/include/classes/graphdraw/
cp -f zabbix.php zabbix_chart.php $ZABBIX_PATH/
cp -f CItemValue.php $ZABBIX_PATH/api/classes/
cp -f menu.inc.php $ZABBIX_PATH/include/
cp -f main.js $ZABBIX_PATH/js/
cp -f API.php $ZABBIX_PATH/include/classes/api/

3��֧��web interface,�޸������ļ�

vi $ZABBIX_PATH/zatree/zabbix_config.php

'user'=>'xxx', //web��½���û���

'passowrd'=>'xxx', //web��½������


��Ļ��ͼ
==================================

zatree��ҳ

![image](https://github.com/spide4k/zatree/raw/master/screenshots/1.jpg)

����ͼ��Ŵ�

![image](https://github.com/spide4k/zatree/raw/master/screenshots/2.jpg)

����
==================================

QQ����Ⱥ��216490997

��������
==================================

1������Ŵ�

���Դ�php����ʾ���󣬿���ʲôԭ��

vi /etc/php.ini

display_errors = On

����web server,Ȼ����web��־

2��Fatal error: Call to undefined function json_encode() in /var/www/html/zabbix/zatree/ZabbixApiAbstract.class.php on line 220

��Ҫphp encode֧��

yum install php-pecl-json

�����������������У��Ҳ���php-pecl-json�����������������

yum install php-pear

pecl install json

echo "extension=json.so" > /etc/php.d/json.ini

3������Ҳ���ʾһ��2��ͼ��˵����ֱ��ʲ��������ϰ���㻻�������������޸�graph.php�ļ����е�widthֵ

    181 <img  src="<?php echo $small_graph; ?>" width="357" height="211" style="float:left;padding-top:4px;padding-left:4px;"  /> </a>

4���������Сͼ����ʾʱ��Σ��༭�ļ�include/classes/class.cchart_zabbix.php����2363��

     2363                 //      $this->drawDate();

5:�����´���

Warning: array_key_exists() expects parameter 2 to be array, null given in zatree/ZabbixApiAbstract.class.php on line 255

Notice: Trying to get property of non-object in zatree/ZabbixApiAbstract.class.php on line 262

Warning: Invalid argument supplied for foreach() in zatree/graph.php online 130

�ڴ�������޸�php.ini������СΪXXX
memory_limit = XXXM

6:�Ƿ�֧����������ؼ��֣�
֧�֣��ؼ����ö��ŷָ�

7:����ѡ��Ĳ�ֵ��ʲô��˼��
��һ��ʱ������ֵ��ȥ��Сֵ�õ�һ�������Ȼ�����������������ѡ���һ��ʱ���ڵ�ͻ�������鿴�ǳ�����

����֧��
==================================

http://weibo.com/spider4k

http://weibo.com/chinahanna

http://weibo.com/678236656


С����
==================================

��������zatree��������а���, <a href="http://me.alipay.com/spider4k">�������</a>���Զ����߽���С����

ף������
