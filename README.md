构建词库
==========

从原始文本中，自动构建词库，目前只适用于中文。参考：

http://www.matrix67.com/blog/archives/5044

###成词条件
1. 互信息
2. 左右熵
3. 位置成词概率
4. ngram 频率

###运行方法
见Main.java，输入参数为原始文本文件路径。
输出为words_sort.data，抽取出来的词，可根据阈值进行调整。


###TODO
1. 单机支持100G+数据集的抽取。
2. 整理代码
3. 指出中文语料

###示例

####《金瓶梅》抽取结果
```shell
西门庆  4754    6.727920454563199   2.0315193024276885  0.17472535684926388
月娘    1829    6.491853096329675   2.3714166640957095  0.22135096835144072
敬济    906 9.084808387804362   2.554594603718855   0.14485683987274656
春梅    799 8.134426320220927   2.7880175589451714  0.16484505593416485
玳安    796 8.228818690495881   2.865686193737731   0.11791820110723605
后边    617 6.6293566200796095  4.008365154080131   0.2160373686259245
玉楼    594 7.977279923499917   2.27346284978306    0.27518689925240297
明日    580 6.189824558880018   2.705423396095033   0.1774535638537181
两银子  458 6.129283016944967   2.351100547282295   0.3809078896437581
小厮    454 7.257387842692652   3.945653525477103   0.16666666666666666
打发    444 6.870364719583405   3.694604352707633   0.18409496065046307
如今    410 6.643856189774725   2.1460777430093394  0.1780766096169519
淫妇    382 7.768184324776926   3.277903508489837   0.2555205047318612
桂姐    371 7.584962500721156   2.5922046565140424  0.36255305256284687
老婆    331 6.266786540694902   3.5783015008688523  0.3758007117437722
衣服    309 8.90388184573618    2.786139685416002   0.13284518828451883
丫头    297 7.383704292474053   4.291010086795063   0.21875
潘金莲  288 8.276124405274238   2.4955186567189194  0.35333669524289796
昨日    285 6.857980995127572   2.6387249970833997  0.1774535638537181
王婆    284 7.1799090900149345  2.3129267619188907  0.3758007117437722
```

####《西游记》抽取结果
```shell
八戒    1807    7.88874324889826    2.00952580557629    0.36441586280814575
师父    1632    7.507794640198696   3.745294449785798   0.1371395690812608
大圣    1270    6.599912842187128   2.7790919785432147  0.13128460061010055
唐僧    1003    7.076815597050832   4.350465172292435   0.43277723258096173
菩萨    765 9.471675214392045   3.6013747138664756  0.15910495734948696
妖精    634 7.199672344836364   3.1817261900583627  0.13134411600669268
徒弟    439 8.060695931687555   2.498555429145656   0.15553809897879026
兄弟    284 7.845490050944376   2.93037668783551    0.16085578446909668
宝贝    283 9.319672120946995   2.616164396748633   0.15108220492589827
今日    282 6.714245517666122   2.1303069812971214  0.1774535638537181
取经    263 7.539158811108032   2.663944888382171   0.10181178023912565
如今    259 6.189824558880018   2.056188859866133   0.1780766096169519
认得    223 6.357552004618085   2.9543379335926954  0.2326782564877803
东土    212 8.422064766172811   3.326253983395916   0.14745277618775043
孙大圣  202 6.022367813028454   2.4886576514017107  0.13128460061010055
变作    189 7.554588851677638   3.0713596792578635  0.23452975920036348
玉帝    189 8.912889336229961   2.973106046717708   0.27518689925240297
土地    179 7.499845887083206   3.1206506190132566  0.2819944064037033
欢喜    173 8.861086905995393   2.184918471204895   0.31727272727272726
贫僧    170 7.400879436282184   2.0731236036504477  0.43277723258096173
```
