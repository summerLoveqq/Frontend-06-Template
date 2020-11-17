学习笔记
1 AST 抽象语法树
    汇编语言先做分词，分成层层嵌套的语法树结构；
    构建语法树叫语法分析：LL算法（从左到右扫描，从左到右规约）、LR算法；
2 四则运算
    TokenNumber: 0 - 9 的组合
    Operator: + - * / 之一
    Whitespace: <SP>
    LineTerminator: <LF> <CR>
3 正则表达式
    每个正则表达式包含5个属性：source、global、ignoreCase、multiline、lastIndex;
    ## const regExp = /([0-9\.]+)|([ \t]+)|([\r\n]+)|([\+]+)|([\-]+)|([\*]+)|([\/]+)/g;
    souce: 一个只读字符串，表示正则表达式文本 - ([0-9\.]+)|([ \t]+)|([\r\n]+)|([\+]+)|([\-]+)|([\*]+)|([\/]+);
    global: 一个只读的布尔值，表示正则表达式是否有修饰符g - true;
    ignoreCase: 一个只读的布尔值，表示正则表达式是否有修饰符i - false;
    multiline: 一个只读的布尔值，表示正则表达式是否有修饰符m - false;
    lastIndex: 一个可读/写的整数，如果匹配模式中带有g修饰符，这个属性存储在整个字符串下一次检索的开始位置，这个属性会被exec和test方法用到;
        let regExp = /javascript/g;
        let str = 'javascript';
        console.log(regExp.test(str)); // true
        console.log(regExp.test(str)); // false
