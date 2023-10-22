[Полная версия задания](https://github.com/netology-code/ajs-homeworks/tree/ajs8/modules)

# Домашнее задание к лекции «Модули»

**Важно**: каждая задача выполняется в виде отдельного проекта с собственным GitHub репозиторием.

**Важно**: на данные задачи требование отсутствия ошибок в ESLint не распространяется (но вы можете его запустить и изучить ошибки, которые вам будут показаны).

**Важно**: решения должны быть построены на базе [шаблона Webpack](/ci-template) (для задач под номерами 1 и 2).

В личном кабинете на сайте [netology.ru](http://netology.ru/) в поле комментария к домашней работе вставьте ссылки на ваши GitHub-проекты.

---

## Webpack

### Легенда

Ваш проект разросся и необходимо его разделить на модули. Модули помогают обеспечить изолированность кода и внести порядок в проект. Но для работы с модулями необходимо настроить загрузчик модулей (удостоверьтесь с помощью сервиса [caniuse.com](http://caniuse.com/) что модули поддерживаются не везде).

### Описание

Используйте следующую структуру, чтобы настроить экспорт в бандл:
- каталог `src`:
  - каталог `css`
    - файл `style.css` (в качестве содержимого используйте `body { color: #999; }`)
  - каталог `js`
    - файл `app.js` (в качестве содержимого используйте `console.log('app worked')`)
  - файл `index.html` (шаблон для HTMLWebpackPlugin) (содержимое файла - произвольно, скрипты и стили должны подключаться автоматически, за счёт использования HTMLWebpackPlugin и MiniCssExtractPlugin)
  - файл `index.js` (Webpack entry point)
- файл `webpack.config.js`
- файл `package.json`
- другие файлы

Убедитесь, что после экспорта, бандл запускается и работает (создайте для этого скрипт в npm, который запускает HTTP-сервер для каталога `dist`). HTTP-сервер выберите сами.

---