# String-Obfuscator
Modify characters to prevent social platforms from detecting duplication of content. 用于伪原创，防止社交平台检测内容重复性。

# 效果预览
https://dev-coco.github.io/post/String-Obfuscator/

# 使用方法
## 字符混淆
使用 `stringObfuscation` 函数，第一个参数放入需要混淆的内容，第二个参数放入混淆的类型，运行后会输出混淆后的字符。
```JavaScript
/**
 * @description 字符混淆
 * @param {string} content - 内容
 * @param {string} option - 类型
 * @returns {string} - 混淆后的内容
 */
stringObfuscator(content, option)
```
如果有部分内容不想被混淆，需要保留原来的样式，需要使用 `{}`，在大括号里的内容会被跳过，字符不会被混淆。

## 字符还原
使用 `stringDeobfuscator` 函数，放入混淆后的内容，运行后会输出还原后的内容。
```JavaScript
/**
 * @description 字符还原
 * @param {string} str - 混淆后的内容
 * @returns {string} - 还原后的内容
 */
stringDeobfuscator(str)
```

## 例子
```JavaScript
stringObfuscator('Hello, World!', 'style1')
>> 𝐇𝐞𝐥𝐥𝐨, 𝐖𝐨𝐫𝐥𝐝!

stringObfuscator('Hello, {World}!', 'style2')
>> 𝗛𝗲𝗹𝗹𝗼, World!

stringDeobfuscato('𝐇𝐞𝐥𝐥𝐨, 𝐖𝐨𝐫𝐥𝐝!')
>> Hello, World!
```
