## SKILL DEMO 4 NOTES

**Step 1**

```
cd step1
mkdir source
mkdir data
mkdir lib
touch source/Main.java
touch lib/Library.java
mkdir data/2022
mkdir data/2023
touch data/2022/data.csv
touch data/2023/data.csv
```

**Step 2**

```
cd project
touch README.md
git add . 
git commit -m "skill demo"
```

**Step 3**

```
cd buggy
bash test.sh
bash test.sh >/home/student/test-fail-output.txt
vim ListExamples.java
```

***Step 4***

once in the file, change these lines:

in function filter:

```
result.add(s);
```

in funciton merge:

```
if (list1.get(index1).compareTo(list2.get(index2)) <= 0) 
index1++;
index2++;
```

```
:wq 
bash test.sh
bash test.sh >/home/student/test-success-output.txt
```

**Step 5**

```
git add .
git commit -m "fix bugs"
```

**Step 6**

```
javac -g BCrypt.java Main.java
jdb Main mypassword
> stop in BCrypt.hashpw
> run
echo byte[number] > hashed.txt
```

in skill demo i got 24 this is after the locals command

- use `step` until line 677
- use `next` until line 685
- locals
- exit