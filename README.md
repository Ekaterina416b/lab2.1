# lab2.1
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
cd ~/Documents/hello_world_repo
touch hello_world.cpp
nano hello_world.cpp
```
