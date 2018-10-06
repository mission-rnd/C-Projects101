# C-Projects101

## How to create projects 

1. Clone https://github.com/mission-rnd/C-DummyProject 
2. Change the folder name to the new lesson name. ie C-NewLessonName. Also delete the .git folder which will be present in the folder. 
3. Go into the new folder and Open the sln file in VS Studio 2013. (Open only in that , or VS 2013 community or express), As if you open in later versions projects will be upgraded/downgraded which we dont want.
3. Right click on project name and change the name (Rename). ie from C-DummyProject to C-NewLessonName. Also change the src->MainBasics.cpp name to MainNewLessonName.cpp

4. Save (Ctrl+S) and Close the project and VS Studio 2013. 
5. Create a new repo in github.com/mission-rnd/ with your new lesson naming. C-NewLessonName should be the repo name. Dont click on add gitignore or add readme. 
6. Open cmd into the C-NewLessonName folder and run below commands
```
git init
git add .
## Above should add only files which are required. src and spec folder , .sln and .gitignore, Check that by doing git status
git commit -m "Added new lesson"
git remote add origin https://github.com/mission-rnd/C-NewLessonName.git
## Replace origin url with your url
git push -u origin master
```



### Files naming rules
1. Main file should be named as Main<LessonName>.cpp
2. Every project should have a FunctionHeaders.h file which is included in above file. 
3. Question files should be QuestionName.cpp
4. Every question file should have a respective test file in spec folder. It should be named as QuestionNameSpec.cpp

### Some other important points

### How to create an exam.
