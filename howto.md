git clone git@github.com:sql3/KotlinAsFirst2020.git сохраняем репозиторий на компьютер  
cd KotlinAsFirst2020 переходим в этот репозиторий  
git remote add upstream-my https://github.com/sql3/KotlinAsFirst2021.git добавляем мой репозиторий в KotlinAsFirst2020  
git fetch upstream-my подгружаем KotlinAsFirst2021  
git branch backport создаем новую ветку backport  
git checkout backport переходим в нее  
git cherry-pick d535f359...FETCH_HEAD загружаем историю commit'ов  
git remote add upstream-theirs https://github.com/xXX-feddy-XXx/KotlinAsFirst2021.git добовляем репозиторий напарника  
git fetch upstream-theirs подгружаем его  
git add . добавляем измененные файлы, в которых возникли ошибки merge  
git commit -m "merge" коммитим  
git checkout master переходим в master  
git merge backport upstream-theirs/master объединяем  
Исправляем конфликты в vs code и там же делаем commit'ы  
git remote -v > remotes создаем файл remotes  
Создаем файл howto.md в vs code, описываем действия, делаем commit и push.  
