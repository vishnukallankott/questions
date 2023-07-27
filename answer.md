
// For find the longest word in a string
const LongestString=(details)=>{
    const data=details.split(' ');
    let longest=""
    for(i=0;i<data.length;i++){
        if(data[i].length>longest.length){
            longest=data[i]
        }
    }
    return longest
}
const details="The quick brown fox jumped over the lazy dog"
console.log(LongestString(details))


// Repeat a string n number of times
const repeatString=(str,num)=>{
   let repeat=""
   for(i=0;i<num;i++){
        repeat=repeat+str
   }
   return repeat
}

const str = "abc"
const num=3;
const out=repeatString(str,num)
console.log(out)


// Remove duplicates from an array
// method 1 [using Set()]
const a =[1, 20, 3, 1, 3, 3]
const b=[...new Set(a)]
console.log(b)

//Remove duplicates in an array

const duplicate=[1, 20, 3, 1, 3, 3]
const removeDuplicates=(duplicate)=>{
   return duplicate.reduce((acc,cur)=>{
            if(!acc.includes(cur)){
                acc.push(cur)
            }
            return acc
    },[])
}

console.log(removeDuplicates(duplicate));

// Remove falsy values


const removefalsy=(array)=>{
    const outPut=[]
    for(i=0;i<array.length;i++){
        if(array[i]){
            outPut.push(array[i])
        }
    }
    return outPut
}

const details1=[42, "everything", "", 2, false, "everything"] 
const result=removefalsy(details1)
console.log(result)

//Truncate a string


const truncate=(str,maxsize)=>{
    if(str.length>maxsize){
       return str.slice(0,maxsize)+"..."


    }
    return str
}
const str1='Absolute victory'
const truncatedString=truncate(str1,3)
console.log(truncatedString)
