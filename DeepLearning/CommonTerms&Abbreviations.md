# �������Ｐ�������� in Mess

+ pretext task����Ԥѵ������Ҳ��ǰ�����񡢴�������
+ downstream task����������ͨ��ָ�����������΢��������
+ end to end���˵��ˡ��ṩһ�����룬�͵õ�һ�������
+ backbone��ָ���������硣ͨ���Ǹ�����ȡ���������硣
+ head������㡣����֮ǰ��ȡ��������head ������Щ��������Ԥ�⡣
+ neck��ָ���� backbone �� head ֮��ģ�Ϊ�˸��õ����� backbone ��ȡ��������������ش�������硣
+ bottleneck��ƿ����ָ���������ά��>>���ά�ȡ�</br>
&emsp;&emsp;&emsp;&emsp;&emsp;&ensp;&thinsp;ͨ������ bottle_num=256 ,ָ��������ά��Ϊ256��
+ baseline����Ϊ��׼��ģ�ͣ������Ƚ�ģ��Ч���Ĳο��㡣</br>
&emsp;&emsp;&emsp;&emsp;&ensp;&thinsp;baseline������ģ�Ϳ���������ض������������Ԥ��Ч����
+ batch��ģ��ѵ��ʱ��һ�ε�������һ���ݶȸ��£���ʹ�õ���������
+ batch size��һ�� batch �е�����������
+ bias��ƫ�Ҳ��ƫ����������ԭ��Ľؾ��ƫ�ơ�</br>
&emsp;&emsp;&ensp;&thinsp;ƫ���ڻ���ѧϰģ����ͨ����b����w<sub>0</sub>��ʾ��
+ binary classification����Ԫ���ࡣ
+ class-imbalanced�����಻ƽ��ġ�
+ checkpoint�����㣬һ�����ݣ����ڲ���ģ�ͱ������ض�ʱ���״̬��</br>
&emsp;&emsp;&emsp;&emsp;&emsp;&ensp;&thinsp;���� checkpoint�����Ե���ģ��Ȩ�أ������Ựִ��ѵ����ʹģ���ڷ����������Լ�����������ҵ��ռ����</br>
&emsp;&emsp;&emsp;&emsp;&emsp;&ensp;&thinsp;ע�⣺checkpoint ��������ͼ������ṹ������
+ cost���ɱ��������ڡ���ʧ���ĺ��塣
+ clustering�����ࡣ
+ decision boundary�����߽߱硣�ڷ��������У�ģ��ѧ�������֮��ķֽ��ߡ�
+ dense feature���ܼ�������һ�ִ󲿷�ֵ�Ƿ���ֵ��������ͨ���Ǹ���ֵ������</br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;��ϡ��������ԡ�
+ discrete feature����ɢ�������������޸�����ֵ��</br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&ensp;&nbsp;������������ԡ�
+ badcase��ģ��Ԥ��Ч���ϲ������/�������͡�
+ query������ֱ��Ϊ����ѯ������ָ�����Ѱ��ϵͳ��ģ�͡����ݼ������ݿ���ض���Ϣ��Ԥ��������
  + ���������У�query ͨ����ָ����ģ���ṩ�����Խ���Ԥ���������ģ�ͻ��ڸ�������������Ϊ query result��
  + ��Attention�У��ڻ���Attention��ģ�ͣ�e.g. Transformer���У�query �����ڼ���ע����Ȩ��ʱʹ�õļ���ֵ��������ɲ���֮һ��</br>query ���ڸ��ݼ�ֵ����ע�����������Ա��ֵ�м�����Ϣ��
+ BND Box���� Bounding Box���߽��
+ GT��Ground Truth����ʾ�������ϣ�������ľ��ο���ʵ�򣩣��������ο���Ϣ�������Ϣ��
+ DT��Detection Truth����ʾģ�ͼ����ľ��ο�Ԥ��򣩣��������ο���Ϣ�������Ϣ��
+ Anchor��ê�򡣲�ͬ�ڱ߽��Anchor�����ѧϰģ���ڲ���ǰ�ٶ��Ŀ����Կ�ס��Ҫ�������壬��ʵ�ֶ�λ���ܡ�Anchor�������Խƥ�䣬ѵ��Ч��Խ�á�</br>ͨ����Ԥ���趨9���ߴ磬Ҳ���� Anchor-free ������Ҫ Anchor�������硣

# ����������д

+ SSLD���򵥵İ�ල��ǩ���󷨣�Simple Semi-supervised Label Distillation�� </br>
 &emsp;&emsp;&emsp;&thinsp;Paddlepaddle�ṩ��һ��֪ʶ���󷽰���
+ MSA����ͷע�������ƣ�Multi-head Self-Attention��
+ FC��ȫ���Ӳ㣨Fully connected layer��
+ OHEM: ���������ھ�Online hard example mining��
+ BN������һ����Batch Normalization��
+ GAP��ȫ��ƽ���ػ���Global Average Pooling��
+ BP�����򴫲���Back-propagation��