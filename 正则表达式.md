Word中（通配符+正则表达式）用法

https://www.jianshu.com/p/395fc18235f4

https://blog.csdn.net/qq_40741855/article/details/84833820

<table><tbody><tr><th><strong>用于查找</strong></th><th><strong>类型</strong></th><th><strong>示例</strong></th></tr><tr><td>任一字符</td><td><strong>?</strong></td><td>s?t 可找到“sat”和“set”。</td></tr><tr><td>任何字符串</td><td><strong>*</strong></td><td>s*d 可找到“sad”和“started”。</td></tr><tr><td>单词开头</td><td><strong>&lt;</strong></td><td>&lt;(inter) 可找到“interesting”和“intercept”，但找不到“splintered”。</td></tr><tr><td>单词结尾</td><td><strong>&gt;</strong></td><td>(in)&gt; 可找到“in”和“within”，但找不到“interesting”。</td></tr><tr><td>指定字符之一</td><td><strong>[ ]</strong></td><td>w[io]n 可找到“win”和“won”。</td></tr><tr><td>此范围内的任一字符</td><td><strong>[-]</strong></td><td>[r-t]ight 可找到“right”和“sight”。范围必须是升序。</td></tr><tr><td>除了括号内范围中的字符之外的任一字符</td><td><strong>[!x-z]</strong></td><td>t[!a-m]ck 可找到“tock”和“tuck”，但找不到“tack”或“tick”。</td></tr><tr><td>前一个字符或表达式的&nbsp;<em>n</em>&nbsp;个匹配项</td><td><strong>{n}</strong></td><td>fe{2}d 可找到“feed”，但找不到“fed”。</td></tr><tr><td>前一个字符或表达式的至少&nbsp;<em>n</em>&nbsp;个匹配项</td><td><strong>{n,}</strong></td><td>fe{1,}d 可找到“fed”和“feed”。</td></tr><tr><td>前一个字符或表达式的&nbsp;<em>n</em>&nbsp;到&nbsp;<em>m</em>&nbsp;个匹配项</td><td><strong>{n,m}</strong></td><td>10{1,3} 可找到“10”、“100”和“1000”。</td></tr><tr><td>前一个字符或表达式的一个或多个匹配项</td><td><strong>@</strong></td><td>lo@t 可找到“lot”和“loot”。</td></tr></tbody></table>

【答案】 @[^30-^127]{1,4}[一-龥]
