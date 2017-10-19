# RemoveDuplicateCharacters
Using an Object instance to remove duplicate characters from an array, here is the whole code.
```
<script>
	// Test arry
	var arry = [1,2,2,3,4,5,5,10];
	var obj= {};
	
	// Using object property uniqueness to remove the duplicate characther
	for (var i=0; i<arry.length; i++) {
		obj[arry[i]] = true;
		for(var j=i+1; j<arry.length;j++){
			if(obj.hasOwnProperty(arry[j])){
				arry.splice(j,1);
				j = j-1;
			}
		}
	}

	// Print arry in browser console
	console.log(arry);
</script>
```
