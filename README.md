# FSW (font-spider-walker-strengthen)

## 遍历你的代码目录，借助于 font-spider 动态生成你所需要的字体
> 可支持定制化的字体抽离（中文|英文|数字|特殊字符）的一种或多种 默认全部类型



## 用法

```
$ yarn add font-spider-walker-strengthen -D

$ fsw --help 

Usage: fsw [options]

  Options:

    -V, --version                 output the version number
    -s, --src [source]            源码文件夹的路径 (default: ./src)
    -f, --fontName [font name]    字体名称 (default: MyFont)
    --fontPath [font path]        字体路径 (default: ./font/)
    -t, --filetypes [file types]  接受的文件后缀,用|连接 (default: js|jsx|ts|tsx)
    -h, --help                    output usage information
    --searchRange [search Range]  搜索类型，用|连接 (default: chinese|english|number|symbol)

推荐用法：我更推荐把这个命令写入项目中的package.json的命令里 这样就不需要每次集成都要输入一大堆的options了
```



比如在你项目的根目录下

```
----your project
|-------src
|-------build 
|-------fontDir
|-------------MyFont123.ttf               # 字体源文件


$ fsw --fontPath ./fontDir --fontName MyFont123 --filetypes js

----your project
|-------src
|-------build 
|-------fontDir
|-------------.font-spider/MyFont123.ttf   # 字体源文件
|-------------MyFont123.ttf
|-------------MyFont123.woff
|-------------MyFont123.svg
```



## Why 

[抽离工具 font-spider-walker](https://github.com/iplus26/font-spider-walker) 

> 该库可以遍历你的代码目录，借助于 font-spider 动态生成你所需要的字体，但是有个缺点只支持中文字体的抽离。 

 
