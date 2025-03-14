# lab2.1
<details>
 <summary>Part1</summary>
 <p>
1)Создайте пустой репозиторий на сервисе github.com (или gitlab.com, или bitbucket.com). 

2)Выполните инструкцию по созданию первого коммита на странице репозитория, созданного на предыдещем шаге. 
``` 
echo "# MyRepository" >> README.md
git init
>>Reinitialized existing Git repository in /Users/makbuk/Documents/.git/
Documents % git config user.name "Ekaterina Karpina"
Documents % git config user.email "karpina.katia@gmail.com"
git add README.md
git commit -m "first commit"
>>[main (root-commit) 3c5a746] first commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md
git branch -M master
git remote add origin https://github.com/Ekaterina416b/MyRepository.git
git push -u origin master
Username for 'https://github.com': Ekaterina416b
Password for 'https://Ekaterina416b@github.com': 
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 234 bytes | 234.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Ekaterina416b/MyRepository.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.
makbuk@MacBook-Air-makbuk Documents % 
```
3)Создайте файл hello_world.cpp в локальной копии репозитория (который должен был появиться на шаге 2). Реализуйте программу Hello world на языке C++ используя плохой стиль кода. Например, после заголовочных файлов вставьте строку using namespace std;.
```
cd ~/Documents/MyRepository
touch hello_world.cpp
nano hello_world.cpp
```
[hello_world.cpp](hello_world.cpp)
4)Добавьте этот файл в локальную копию репозитория.
```
git add hello_world.cpp
```
5)Закоммитьте изменения с осмысленным сообщением.
```
git commit -m "Add hello_world.cpp with bad code style"
>>[master acc580f] Add hello_world.cpp with bad code style
 1 file changed, 7 insertions(+)
 create mode 100644 MyRepository/hello_world.cpp
```
6,7)Изменитьте исходный код так, чтобы программа через стандартный поток ввода запрашивалось имя пользователя. А в стандартный поток вывода печаталось сообщение Hello world from @name, где @name имя пользователя.Закоммитьте новую версию программы. Почему не надо добавлять файл повторно git add?
```
git commit -am "Update hello_world.cpp to ask for user's name"
>>[master 5aa4647] Update hello_world.cpp to ask for user's name
 1 file changed, 5 insertions(+), 1 deletion(-)
```
Флаг -a автоматически добавляет изменения в уже отслеживаемых файлах, поэтому git add не требуется.
8)Запуште изменения в удалёный репозиторий.
```
git push origin master
>>Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (8/8), 948 bytes | 948.00 KiB/s, done.
Total 8 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Ekaterina416b/MyRepository.git
   3c5a746..5aa4647  master -> master
```
9)Проверьте, что история коммитов доступна в удалёный репозитории.
<img width="1280" alt="1 9  scrin" src="https://github.com/user-attachments/assets/0394ce4c-5018-43c7-ad67-85f5178bffaf" />
[Ссылка на коммиты](https://github.com/Ekaterina416b/MyRepository/commits/master/)
 </p>
</details>
 
 1)В локальной копии репозитория создайте локальную ветку patch1.
 ```
 MyRepository % git checkout -b patch1
 >>Switched to a new branch 'patch1'
 ```
 2)Внесите изменения в ветке patch1 по исправлению кода и избавления от using namespace std;.
 ```
 MyRepository % nano hello_world.cpp
 ```
 3)commit, push локальную ветку в удалённый репозиторий.
 ```
 git add hello_world.cpp
 git commit -m "Remove using namespace std; and improve code style"
>>[patch1 84e9612] Remove using namespace std; and improve code style
 1 file changed, 10 insertions(+)
 create mode 100644 MyRepository/hello_world.cpp
git push origin patch1
>>Enumerating objects: 5, done.Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 539 bytes | 539.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'patch1' on GitHub by visiting:
remote:      https://github.com/Ekaterina416b/MyRepository/pull/new/patch1
remote: 
To https://github.com/Ekaterina416b/MyRepository.git
 * [new branch]      patch1 -> patch1
```
 4)Проверьте, что ветка patch1 доступна в удалёный репозитории. 
 
 [Ссылка на ветку](https://github.com/Ekaterina416b/MyRepository/commits/patch1/) 
 
 5)Создайте pull-request patch1 -> master.
 <img width="1012" alt="2 5 scrin" src="https://github.com/user-attachments/assets/e40974c2-52f5-46eb-bccf-3cef1fb97909" />
6)В локальной копии в ветке patch1 добавьте в исходный код комментарии.
```
git checkout patch1
nano hello_world.cpp
```
7)commit, push.
```
git add hello_world.cpp
git commit -m "Add comments to the code"
>>[patch1 21df999] Add comments to the code
 1 file changed, 1 insertion(+), 1 deletion(-)
git push origin patch1
>>Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 441 bytes | 441.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Ekaterina416b/MyRepository.git
   84e9612..21df999  patch1 -> patch1
```
8)Проверьте, что новые изменения есть в созданном на шаге 5 pull-request
<img width="925" alt="2 8 scrin" src="https://github.com/user-attachments/assets/9af0a760-ff02-419f-88be-52abc9a6bbf7" />
9) В удалённый репозитории выполните слияние PR patch1 -> master и удалите ветку patch1 в удаленном репозитории.
<img width="937" alt="2 9 scrin" src="https://github.com/user-attachments/assets/ee395c45-4480-466a-ad53-552a0cae6edf" />
После удаления ветки
<img width="927" alt=" 2 12 scrin" src="https://github.com/user-attachments/assets/f4f8d618-9d9b-485d-a3db-5f2791daecdf" />
10) Локально выполните pull.
```
git checkout master
>>D	hello_world_repo/hello_world.cpp
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
git pull origin master              
>>remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 922 bytes | 461.00 KiB/s, done.
From https://github.com/Ekaterina416b/MyRepository
 * branch            master     -> FETCH_HEAD
   5aa4647..5634f13  master     -> origin/master
Updating 5aa4647..5634f13
Fast-forward
 MyRepository/hello_world.cpp | 10 ++++++++++
 1 file changed, 10 insertions(+)
 create mode 100644 MyRepository/hello_world.cpp
```
11)С помощью команды git log просмотрите историю в локальной версии ветки master.
```
git log
```
[task2.11.txt](https://github.com/Ekaterina416b/lab2.1/blob/master/task2.11.txt)


