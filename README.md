------------------------------ BINBIN GENERATOR IN JS ------------------------------

1. You can Copy the code Below to use it anywhere:
2. The functions has two parameters:
   1. num - The amount of words you want the code to generate.
   2. sufix - The amount of suffixes you want each word to have.

3. Or you can use my website to generate the words! <a href="https://bingenerator.surge.sh/" target="_blank">Binbin Generator</a>

```bash
function binbCreator(num=5,sufix=3){
    const consonants = ['b','c','d','f','g','h','j','k','l','m','n','p','q','r','s','t','v','w','x','y','z'];
    const vowels = ['a','e','i','o','u'];
    let binResult = [];
    for(let cont=1;cont<=num;cont++){
        let binWord='binb'+vowels[Math.floor(Math.random()*vowels.length)];
        while(binWord.length<=parseInt(sufix)+3){
            binWord+=(Math.random()<0.5 ? consonants[Math.floor(Math.random()*consonants.length)] : vowels[Math.floor(Math.random()*vowels.length)]);
        }
        binResult.push(binWord);
    }
    return binResult;
}
```
