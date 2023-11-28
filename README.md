# WAR2.0
# 日本版本(1.02)
RA＝｛（0.297×uBB＋0.327×HBP-0.108×奪三振＋1.401×被HR＋0.036×滾地球-0.124×内野飛球＋0.132×外野飛球＋0.289×平飛球）÷（奪三振＋0.745×滾地球＋0.304×平飛球＋0.994×内野飛球＋0.675×外野飛球）×27｝+定数

*定数=全體[聯盟 ERA｛（0.297×uBB＋0.327×HBP-0.108×奪三振＋1.401×被HR＋0.036×滾地球-0.124×内野飛球＋0.132×外野飛球＋0.289×平飛球）÷（奪三振＋0.745×滾地球＋0.304×平飛球＋0.994×内野飛球＋0.675×外野飛球）×27｝]

PF補正値（tRA から減算）＝（本拠地球場での対戦打席数÷総対戦打席数）×（本拠地試合での両軍合わせた tRA －それ以外の試合での両軍合わせた tRA）

SPRAR＝（1.39×聯盟平均tRA－PF補正後tRA）÷9×（獲得出局數÷3）
RPRAR＝（1.34×聯盟平均tRA－PF補正後tRA）÷9×（獲得出局數÷3）
WAR（投手）＝（SPRAR＋RPRAR）÷RPW

# CPBL 2023版本
分子係數:該狀態下RE24平均
分母係數:該狀態下的出局比例
| 狀態 | RE24 | 出局比例 |
| ------------- | ------------- |
| uBB  | Content Cell  |
| HBP  | Content Cell  |
| SO  | Content Cell  |
| HR  | Content Cell  |
| 滾地球  | Content Cell  | Content Cell |
| 內野飛球  | Content Cell  | Content Cell |
| 外野飛球  | Content Cell  | Content Cell |
| 平飛球  | Content Cell  | Content Cell |

1.定数=全體 [ 聯盟ERA-｛（ 0.321082×uBB＋0.335785×HBP -0.271232×奪三振＋1.702948×被HR -0.051968×滾地球+0.084087×内野飛球-0.265915×外野飛球＋0.297010×平飛球）÷（奪三振+0.710088×滾地球+0.286522×平飛球+0.702312×内野飛球+0.987735×外野飛球）×27｝]

2.RA=｛（0.321082×uBB＋0.335785×HBP -0.271232×奪三振＋1.702948×被HR -0.051968×滾地球+0.084087×内野飛球-0.265915×外野飛球＋0.297010×平飛球）÷（奪三振+0.710088×滾地球+0.286522×平飛球+0.702312×内野飛球+0.987735×外野飛球）×27｝+定数

3.球場因素修正值（从tRA中减去）=（球隊主场對到的BF ÷ 整季投手群對到的BF） × （本隊主场比赛的两队tRA總和 - 其他比赛的两對tRA總和）
*原打席數改為Batter Face(BF) 

4. RAR＝（1.356×聯盟平均tRA－PF補正後tRA）÷9×（獲得出局數÷3）
取SPRAR(1.39)和RPRAR(1.34) 平均數1.365

# CPBL 2022版本
分子係數:該狀態下RE24平均
分母係數:該狀態下的出局比例

1.定数=全體 [ 聯盟ERA-｛（ 0.311522×uBB＋0.328145×HBP -0.27208×奪三振＋1.657671×被HR -0.0554×滾地球+0.065453×内野飛球-0.26825×外野飛球＋0.327159×平飛球）÷（奪三振+0.712091×滾地球+0.261841×平飛球+0.710578×内野飛球+0.982011×外野飛球）×27｝]

2.RA=｛（ 0.311522×uBB＋0.328145×HBP -0.27208×奪三振＋1.657671×被HR -0.0554×滾地球+0.065453×内野飛球-0.26825×外野飛球＋0.327159×平飛球）÷（奪三振+0.712091×滾地球+0.261841×平飛球+0.710578×内野飛球+0.982011×外野飛球）×27｝+定数

3.球場因素修正值（从tRA中减去）=（球隊主场對到的BF ÷ 整季投手群對到的BF） × （本隊主场比赛的两队tRA總和 - 其他比赛的两對tRA總和）
*原打席數改為Batter Face(BF) 

4. RAR＝（1.356×聯盟平均tRA－PF補正後tRA）÷9×（獲得出局數÷3）
取SPRAR(1.39)和RPRAR(1.34) 平均數1.365




5.計算Run per Win
是指增加一場勝利所需的得分數量。通常來說，總得分增加10分（或總失分減少10分）會使球隊的勝場增加一場。RPW通常等於10。
原日本公式: RPW = 10 × SQRT（兩隊每局平均得分）
日本公式下 CPBL_2022_RPW  = 6.723292499

FG公式: RPW = 9*(MLB Runs Scored / MLB Innings Pitched)*1.5 + 3
FG公式下 CPBL_2022_RPW  = 9.102359373

6.計算WAR
WAR = RAR/RPW
