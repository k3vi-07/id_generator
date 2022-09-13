### 身份组成方式

[中华人民共和国国家标准](https://zh.wikipedia.org/wiki/%E4%B8%AD%E5%8D%8E%E4%BA%BA%E6%B0%91%E5%85%B1%E5%92%8C%E5%9B%BD%E5%9B%BD%E5%AE%B6%E6%A0%87%E5%87%86)[GB 11643-1999《公民身份号码》](https://zh.wikisource.org/wiki/GB_11643-1999_%E5%85%AC%E6%B0%91%E8%BA%AB%E4%BB%BD%E5%8F%B7%E7%A0%81)中规定：公民身份号码是特征组合码，由十七位数字本体码和一位校验码组成。

18位数字组合的方式是：

| 1 1 0 1 0	2 | Y Y	Y Y	M M D D | 8 8 | 8 | X |
| :---------: | :---------------: | :----: | :--: | :----: |
|    区域码(6位)    |  出生日期码(8位)     | 顺序码(2位) | 性别码(1位) | 校验码(1位) |


- **区域码** 指的是公民常住户口所在县（市、镇、区）的[行政区划代码](https://zh.wikipedia.org/wiki/%E4%B8%AD%E5%8D%8E%E4%BA%BA%E6%B0%91%E5%85%B1%E5%92%8C%E5%9B%BD%E8%A1%8C%E6%94%BF%E5%8C%BA%E5%88%92%E4%BB%A3%E7%A0%81)，如110102是北京市-西城区。但港澳台地区居民的身份号码只精确到省级。
- **出生日期码** 表示公民出生的公历年（4位）、月（2位）、日（2位）。
- **顺序码** 表示在同一区域码所标识的区域范围内，对同年、同月、同日出生的人编定的顺序号。
- **性别码** 奇数表示男性，偶数表示女性。
- 最后一位是**校验码**，这里采用的是**ISO 7064:1983,MOD 11-2**校验码系统。校验码为一位数，但如果最后采用校验码系统计算的校验码是“10”，碍于身份证号码为18位的规定，则以“X”代替校验码“10”。

### 校验码计算方法
-  **1.** 将身份证号码从右至左标记为![](https://wikimedia.org/api/rest_v1/media/math/render/svg/779a0c3f011a79efb854f48c9a7398cc17b04305)，![](https://wikimedia.org/api/rest_v1/media/math/render/svg/bbf42ecda092975c9c69dae84e16182ba5fe2e07)
即为校验码；
-  **2.** 计算权重系数 ![](https://wikimedia.org/api/rest_v1/media/math/render/svg/5f817855c5ad3b88b412e60f83f2201fd386ea2a)

所以:


|**i**|18|17|16|15|14|13|12|11|10|9|8|7|6|5|4|3|2|1|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:| :-:| :-:|
| **W<sub>i</sub>** |7|9|10|5|8|4|2|1|6|3|7|9|10|5|8|4|2|1|

- **3.**  计算![](https://wikimedia.org/api/rest_v1/media/math/render/svg/dad8e73b5a78c0c3d0ca9097d64adad4daacbf31)
- **4.**  ![](https://wikimedia.org/api/rest_v1/media/math/render/svg/81eb5f69ce9a438d004f0fb85b6b14dfa4c3b27a)





### 工具类主要功能
1、随机生成符合标准规则的身份证号
2、根据区域代码生成
3、生成指定数量



[√]: 参考代码地址: https://github.com/jayknoxqu/id-number-util
