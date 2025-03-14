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
 </p>
</details>
<details>
 <summary>Part2</summary>
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
>>Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
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
 4)Проверьте, что ветка patch1 доступна в удалёный репозитории.
 
 [Ссылка на ветку](https://github.com/Ekaterina416b/MyRepository/commits/patch1/)
 5)Создайте pull-request patch1 -> master.
