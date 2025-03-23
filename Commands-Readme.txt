* to execute and run test cases

  mvn clean install exec:java -Dexec.mainClass="mainapp.MyApp" -DskipTests=true

git config --global user.email ""
git config --global user.name ""
================================================================================

touch index.html
"add some code in index.html file"
git add index.html
git commit -m "adding index.html file"

git checkout -b blog-feature
"update index.html file with a code for blog section"
git add index.html
git commit -m "added blog feature"

git checkout main
git merge blog-feature --ff

git checkout -b comment-feature
"update index.html file with a code for comment section"
git add index.html
git commit -m "added comment section"

git checkout main
"update index.html file with a code for about us section"
git add index.html
git commit -m "added about us"

git merge comment-feature