# vim-config
## vim配置文件


下载安装：

- git clone --recursive git@github.com:nani0119/vim-config.git .vim

- 在vim中执行EX命令：PluginInstall 安装插件

## 插件管理器

- 地址：https://github.com/VundleVim/Vundle.vim

## 所需插件
### 1) fzf 

- 地址：https://github.com/junegunn/fzf

- 快速查找


### 2) unimpaired.vim

- 地址：https://github.com/tpope/vim-unimpaired

- 创建快速遍历Vim列表的按键映射项

 [a / ]a   遍历参数列表

 [q / ]q   遍历quickfix列表

 [l / ]l   遍历位置列表

 [t / ]t   遍历标签列表

 [b / ]b   遍历缓冲区列表

 [B / ]B   first/last缓冲区列表



### 3) commentary.vim

- 地址：https://github.com/tpope/vim-commentary

- 快速注释

 gc{motion}           注释/反注释{motion}内容

 gcc                  注释/反注释当前行

 {Visual}gc           注释/反注释高亮

 gc                   注释/反注释文本对象(操作待觉模式)

 :[range]Commentary   注释/反注释范围

### 4) surround.vim

- 地址： https://github.com/tpope/vim-surround

- 为选中的文本加分割符

 "Hello world"      cs"'          'Hello world'

 'Hello world'      cs'<q>        <q>Hello worls<q>

 "Hello world"      ds"           Hello world

 Hello world        ysiw]         [Hello] world

 Hello world        yss)          (Hello world)

 ds： 删除

 ys： 添加

 yss：针对整行

 cs： 修改


### 5) visual-star-search.vim

- 地址：https://github.com/nelstrom/vim-visual-star-search

- 在visual模式下通过‘\*’或‘#’实现查找选中的整段文本而不是单词

### 6) qargs.vim

- 地址：vim实用技巧/substitution

- 通过Qargs命令将quickfix列表中的文件加载到参数列表中

: vimgrep     /\<c-r\>//    **/*.txt
 
: Qargs

### 7) vim-markdown

- 地址：https://github.com/tpope/vim-markdown

### 8) hruvasagar/vim-table-mode

- 地址：https://github.com/dhruvasagar/vim-table-mode
- 创建、格式化markdown表格

1. let g:table_mode_corner='|'  //markdown表格
2. \tm 打开或者关闭该功能
3. |输入两次生成表头分割线
4. \tt命令或者:[range]Tableize可以生成表格，数据间需要使用“,”分割
5. [range]Tableize/{pattern}生成表格时使用其他分割符，例如1,5Tableize/;  ,使用;分割数据，g:table_mode_delimiter定义默认分割符
6. [|, ]|, {|,|}在表格左右上下移动
7. \tdd 删除一行
8. \tdc 删除一列
9. i|、a| 表格文本对象
