# **Работа с .gitignore**

Очевидно, что мы хотим хранить только исходный код и ничего другого в репозитории. А что может быть еще? Как минимум, скомпилированные классы и/или файлы, которые создают среды разработки. 

Чтобы гит их игнорировал, есть специальный файл, который нужно самостоятльно создать. Делаем это так: создаем файл в корне проекта с названием .gitignore, и в этом файле каждая строка будет шаблоном для игнорирования.

В этом примере гит игнор будет выглядеть так:

```bash=
*.class
target/
*.asm
.idea/
```

Рассмотрим содержимое файла:
* первая строка — это игнорирование всех файлов с расширением .class;
* вторая строка — это игнорирование папки target и всего, что она содержит;
* третья строка — это игнорирование всех файлов с расширением .asm;
* четвертая строка — это игнорирование папки .idea.

Добавляем наш файл:

```bash=
git add .gitignore
git commit -m “added .gitignore file”
```

Теперь при использовании команды

```bash=
git add -A
```
в репозиторий попадут только нужные нам файлы.

---

 [**назад**](/base.md) | 
[**дальше**](/branch.md) | 
 [**на главную страницу**](/readme.md)