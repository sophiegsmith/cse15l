**Skill Demo 3 commands**
`find submissions/ name "*.java" -exec wc -l {} + | sort | tail -n 1 | awk '{print $2}' > ../biggest.txt`
- biggest.txt: submissions/student5/Sorter.java
`grep -r "Collections.sort" submissions/ > ../sorts.txt`
- sorts.txt
```
submissions/student1/Sorter.java:    Collections.sort(a); // sort using a library function to save time
submissions/student6/Sorter.java:    Collections.sort(a);
submissions/student4/pa3-code/Sorter.java:    Collections.sort(nums);
```

-run grade.sh
`bash grade.sh`

-also add in grade.sh
`find submissions/ -name "results.txt" -exec grep -L "Compile error" {} \; xargs cat > run-results.txt`

-for the last step of the `grade.sh`
```
all_results=`find submissions -name "result.txt"`
cat $all_results | grep "Compile error"  > compile-errors.txt

# Here, add code to put all of the results for files that successfully ran into
# run-results.txt
cat $all_results | grep "Test results" > run-results.txt

```
