# msearch
本机文件内容快速检索工具

# 使用方式
msearch -dir [要搜索的目录，使用/进入] -k [要搜索的内容关键词] -o [输出结果]

如 msearch -dir c:/ -k 密码,账户 -o result.txt 表示在c:/盘下检索包含密码,账户的文件，结果放在result.txt内

如 msearch -dir c:/ -k 密码,账户 -bea .ppt   -o result.txt 表示在c:/盘下检索包含密码,账户的文件,不检索ppt格式后缀的文件，结果放在result.txt内

如 msearch -dir c:/ -k 密码,账户 -we .txt   -o result.txt 表示在c:/盘下检索包含密码,账户的文件,只检索txt格式后缀的文件，结果放在result.txt内

# 参数说明
-dir [string] 文件路径，检索的文件路径，默认./

-sm [string] 搜索模式 str:内容检索 ,file:文件名检索，all:全部检索

-rm [string] 检索规则 w:目录白名单过滤（需配合-w 设置白名单），默认b:黑名单模式

-ms [int] 检索文件大学，单位位M，默认100M 超过100M的文件不会进行检索

-k [string] 检索的关键词，使用逗号分隔 默认：密码,password=,姓名

-ka [string] 增加关键词，在默认基础上新增关键词

-b [string] 路径黑名单(默认存在部分windows黑名单)，逗号分隔

-ba [string] 在默认基础上增加路径黑名单，逗号分隔

-w [string] 路径白名单，默认位空，在-rm w 模式下，匹配白名单

-be [string] 后缀黑名单，默认情况下，不检索.exe,.dll格式文件

-bea [string] 默认基础上新增的后缀黑名单，逗号分隔

-we [string] 后缀白名单，默认为空，逗号分隔，使用后，只匹配该类型的文件  如：-we .txt,.docx  就只检索 .txt,.docx文件内的内容

-o 输入的文件，默认fileSearchResult.txt


