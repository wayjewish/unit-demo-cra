# Привет
![1648222839_9-kartinkof-club-p-plokho-ochen-plokho-mem-9](https://github.com/wayjewish/unit-demo-cra/assets/52935522/0b1ab60a-e6f4-4873-b95c-fd4c29166386)
  
Телеграмм для связи @wayjewish  
По таске многое не понял - поэтому сделал что смог:  

- [x] Настройте линтер для соответствия сообщений о коммитах формату conventional commits
  
*локально в проекте настроен commitlint*  
![Снимок экрана 2023-07-17 103426](https://github.com/wayjewish/unit-demo-cra/assets/52935522/c204a3fc-6a59-472d-95a3-b959220a259b)
  
- [x] Настройте автоматический запуск проверок в CI для пулл реквестов  
  - [x] обязательно должны запускаться автотесты + опционально можете подключить линтер для кода  
  - [x] проверки должны запускаться автоматом на каждый коммит в PR  
  - [x] результат должен быть виден на странице PR в интерфейсе GitHub  
  - [x] нужно настроить ограничение на мерж изменений, если проверки не прошли
  
*этот пункт готов https://github.com/wayjewish/unit-demo-cra/pull/7*  
![Снимок экрана 2023-07-17 103744](https://github.com/wayjewish/unit-demo-cra/assets/52935522/98ce72f4-6e79-4c8d-b86d-f1901e304215)  
![Снимок экрана 2023-07-17 104535](https://github.com/wayjewish/unit-demo-cra/assets/52935522/c0cd1190-b5cb-4724-9bbf-f0485e069f68)  

- [ ] Настройте релизный процесс
  - [x] релиз должен запускаться автоматически при появлении в git нового релизного тега  
*тут вроде норм*  
  - [x] версия релиза должна соответствовать релизному тегу  
*создается релиз с той же версией что и тег, но пустой*  
  - [ ] должен формироваться changelog по истории коммитов от предыдущего релизного тэга  
  - [ ] должна создаваться запись в реестре релизов — считаем, что это issue на GitHub с пометкой RELEASE. Там должна сохраняться вся важная информация: автор и дата релиза (можно взять из тэга), номер версии, changelog  
*issue создается но без нужной инфы*  
  - [ ] предусмотрите корректную работу скрипта при многократном запуске с тем же тэгом (должна обновляться информация в существующей записи реестра релизов, а не создаваться новая)  
  - [ ] должны запускаться проверки, аналогичные PR, а ссылка на результат должна добавляться в реестр релизов  
*запускаю в начале перед релизом, не уверен что так правильно, и без записи результата*  
  - [x] если проверки прошли, приложение должно выкладываться на gh-pages  
*[PAGE](https://wayjewish.github.io/unit-demo-cra/)*  
  - [ ] после этого релизный issue можно автоматом закрывать  
  
- [x] Автоматизацию можно настроить через GitHub Actions или другой бесплатный аналог  
  - [x] секреты должны храниться защищенно  
  
*В общем полный фейл у меня с этой таской*  
*Сорян за такую сырую работу и спасибо)*  
  
--------------------------------------------------------------------------------  
  
В этом репозитории находится пример приложения с тестами:

- [e2e тесты](e2e/example.spec.ts)
- [unit тесты](src/example.test.tsx)

Для запуска примеров необходимо установить [NodeJS](https://nodejs.org/en/download/) 16 или выше.

Как запустить:

```sh
# установить зависимости
npm ci

# запустить приложение
npm start
```

Как запустить e2e тесты:

```sh
# скачать браузеры
npx playwright install

# запустить тесты
npm run e2e
```

Как запустить модульные тесты:

```sh
npm test
```
