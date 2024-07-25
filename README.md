
# Work-flow of our project Repo:
## main branch:
- this is gonna be our main branch.
you should not push any changes or deploy your working stright forward to this branch, and you also 
can't because i have disabled this option.

> **what you should do instead:**
every time you want to work on some 'issue' or add some changes:
you should go localy to your git directory, and do the following:

### updating local changes from the main repo & branching
> update the changes in your local git directory
```bash 
git pull origin main
```

*now you can start working on your issue, but first open new branch that indicates you are working on this specific issue*

```bash
git branch branch_name
```

### commits: 
> **after each change you want to "save" you should commmit it:**


quick note: (commits should be atomic-logic)

כלומר אם אתם עושים קומיט למספר קבצים מסויימים, הם צריכים להיות כולם קשורים אחד לשני לשינוי אותו אתם שומרים בקומיט הנ״ל

דוגמא: נניח אני עובד על משימה שקשורה בצד-שרת, אז נניח שביצעתי שינויים בקבצים הבאים:
```python
ServerUI.java , ServerFrameFXML1.fxml, ServerFrameFXML2.fxml
AnotherJavaClass.java, etc...
```
עבור כל אחד מהם אעשה את הפקודה הבאה, על מנת לכלול את כולם בקומיט הקרוב שאבצע:
```bash
git add filename.java
```
בנוסף ניתן לראות אילו קבצים אני כולל בקומיט הבא ע״י הפקודה:
מה שיופיע בירוק יכלל בקומיט, ומה שבאדום לא יכלל בקומיט
```bash
git status
```
כעת לאחר שהוספתי את כל הקבצים, על מנת לבצע קומיט אעשה את הפקודה הבאה:
```bash
git commit -m "text message that tells information about what i have changed in this commit"
```

## integration branch

> now that you have finished working on the issue, done all your commits on the specific branch, 

the next step is to push the changes to "integration" branch.

to this branch you push all the changes from the branch you have been working on.

the following action will create in git-hub "pull request", and only i as the repo manager can decide if to "merge" your work to the integration (and after that to the main branch - but this is my job).

**notice that after pushing you maybe will have "conflicts" so make sure you are dealing with them correctly!**

- pushing to the integration branch:
once you have decided you've done working on your issue branch and you want to push the changes to the integration:

```bash
git fetch origin
get switch your_branch
git merge origin/integration
```

**now you probobly will have conflicts, you should solve them:**

>to check if there is conflicts do:
```bash
git status
```
> if there is something in **RED** then open the file and you will see the following:

