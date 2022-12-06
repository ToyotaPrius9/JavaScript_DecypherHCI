# JavaScript_DecypherHCI



function digitalDecipher(eMessage, key){
    const letters = ['dummychar','a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']
    let ans = [], word = []
    var keyString = key.toString();
    
    j = 0;
   
    for(let i = 0; i < eMessage.length; i++){
        if(j === keyString.length){
            j = 0
        }
            ans[i] = eMessage[i] - keyString[j]
            word[i] = letters[ans[i]];
            j++
    }
    
    let txt = word.join("")
    console.log(txt);
}




digitalDecipher([20, 12, 18, 30, 21], 1939);
digitalDecipher([14, 30, 11, 1, 20, 17, 18, 18], 1990);
digitalDecipher([6, 4, 1, 3, 9, 20], 100);


