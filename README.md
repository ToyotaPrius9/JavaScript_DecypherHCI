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


In this function which takes two arguements "eMessage" and "key", i first created an array for all the letters with "dummychar" at the starting since this 
function won't quite read the first element in the array. After that, are two empty lists "ans" and "word". Afterwards i made the conversion of the second
arguement "key" and stored it into a variable called "keyString". Then for pre-measures for an incoming loop i've decalred j as a variable containing 0.
The loop created as the next step has "I" (which is 0) where in I will keep increasing as long as it is lower than the length of the first arguement of 
the function. And in that loop of I is J where in if J is strictly equals to the length of the keyString variable created recently, J will be 0 and the
empty list "ans" will be equaled to the first arguement's specific content location of I minused by the keyString variable's specific content of location "J".
After that, the recently created empty list of "word" will have it's contents added by the "letters" array's specific element
of the location of the "ans" which was worked on before this. After all of that, J will add itself. Lastly comes the creation of a new variable called "final"
where in final will contain the the main product of the variable "word" but makes them an actual readable formatted string. This function sure takes arguements
BUT i did not really taake the user input route.. I just ran the functions by putting in the examples from the forum which supposedly outputs scout mubashir and 
adabit.

