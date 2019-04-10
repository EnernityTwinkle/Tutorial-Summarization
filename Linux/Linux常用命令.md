1、查看历史命令：

`
history
`
2、查找出现次数

`
grep -o 'str1\|str2' filename | wc -l
`
3、查看一个文本文件的数据行数

`
wc -l filename
`
4、查找一个文件中含有某个字符串的行号和内容

`
grep -n '献陵' filename
`
5、查看一个文件中指定行的内容

`
sed -n '12424998,12425010p' filename
`
