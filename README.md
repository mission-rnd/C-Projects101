# C-Projects101

## How to create projects 

1. Clone https://github.com/mission-rnd/C-DummyProject
2. Change the folder name to the new lesson name. ie C-NewLessonName. Also delete the .git folder which will be present in the folder. 
3. Go into the new folder and Open the sln file in VS Studio 2013. (Open only in that , or VS 2013 community or express), As if you open in later versions projects will be upgraded/downgraded which we dont want.
3. Right click on project name and change the name (Rename). ie from C-DummyProject to C-NewLessonName. Also change the src->MainBasics.cpp name to MainNewLessonName.cpp
![Alt text](images/cproject2.png?raw=true "Renaming project in Vs 2013")
4. Save (Ctrl+S) and Close the project and VS Studio 2013. 
5. Create a new repo in github.com/mission-rnd/ with your new lesson naming. C-NewLessonName should be the repo name. Dont click on add gitignore or add readme. 
6. Open cmd into the C-NewLessonName folder and run below commands
```
git init
## This will add all files
git add .
## Above should add only files which are required. src and spec folder , .sln and .gitignore, Check that by doing git status
## Make sure you dont commit the sdf file, if its present your gitignore is not configured properly,manually remove that file and do 
## git add .
git commit -m "Added new lesson"
git remote add origin https://github.com/mission-rnd/C-NewLessonName.git
## Replace origin url with your url
git push -u origin master
```
7. For first question you can rename Sum.cpp to YourQuestion.cpp. Edit current question with your question.
8. Add the function signature which you expect student needs to test from main, into FunctionHeaders.h
9. Similary rename spec->SumSpec.cpp to YourQuestionSpec.cpp . And make sure you also rename the test class name present in the test file from SumSpec to YourQuestionSpec. Also rename test cases whatever you write.
10. Add sample code for your question in Main.cpp (Or whatever file has main method). 
11. You can add new questions by right clicking on src->SourceFiles. Add New Item-> Visual C++ -> Cpp file.
12. You can add new test case file by right clicking on spec->Source files. Add New Item -> VisualC++ -> Cpp file. Copy any existing test file contents into the new file. Edit #include at top and class name appropirately. 
13. Every question + test case file you add. Commit them to git and push them to master. If you are the only one working on the project commit direclty to master, if you are working on a project with 2-3 others contributing, follow github newbranch-> raise PR model. 

Final new lesson should be something like this https://github.com/mission-rnd/C-NewLessonName

### Files naming rules
1. Main file should be named as Main<LessonName>.cpp
2. Every project should have a FunctionHeaders.h file which is included in above file. 
3. Question files should be QuestionName.cpp (Start with Capital letter)
4. Every question file should have a respective test file in spec folder. It should be named as QuestionNameSpec.cpp
5. Test case naming format is question_testCase1 or question_testingparticularconcept. ie Sum_Test1 or Sum_TestIntegerOverflow

### Some other important points
1. Make sure you test your new project from tool before releasing by following these steps.

### How to create an exam.
