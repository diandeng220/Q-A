# Questions

### ["1", "2", "3"].map(parseInt) 答案是什么
    看来这个题的时候原本觉得非常简单的一道题，还是哉到了小心机上。
    在浏览器上直接console.log()的答案千差万别啊。 answer：[1,NAN,NAN]
    
    马上回头看了下两个方法，
    array.map((value,index,array)=>{
        
    })
    
    parseInt(value,radix);
    radix:可选。表示要解析的数字的基数。该值介于 2 ~ 36 之间。
        如果省略该参数或其值为 0，则数字将以 10 为基础来解析。如果它以 “0x” 或 “0X” 开头，将以 16 为基数。
        如果该参数小于 2 或者大于 36，则 parseInt() 将返回 NaN。
    
    可以看出来最后完整的代码应该是
    ["1", "2", "3"].map((value,index,array)=>{
        return parseInt(value,index);
    })
    
    所以最后的答案是 [1, NaN, NaN]
