# Remove Characteres 

## String

- To remove multiple characters present in a string. Example, to remove the '%' character:
```
echo "73%73%77%6F%72%64%3D%66%69%" | sed 's/%//g'
```


## File
- To remove multiple characters present in a file:
```
sed 's/[aoe]//g' file
```

- To remove 1st character in every line:
```
sed 's/^.//' file
```

 - To remove the last character in every line
 ```
 sed 's/.$//' file
 ```

- To remove the 1st occurence of "b" in file
```
 sed 's/b//' file
 ```
 
