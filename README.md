# Електроклікер (ElectroClicker)

## Опис

Електроклікер — це проста клікер-гра, реалізована на C++ з використанням бібліотеки SFML. Гравець натискає на кнопку, щоб накопичувати «енергію», яку можна витрачати на апгрейди, що підвищують потужність кліку.

## Функціональність

* Клік по головній кнопці для отримання енергії
* Система апгрейдів з трьома типами:

  * Батарейка (до 10 рівнів)
  * Сонячна панель (до 20 рівнів)
  * Вітрова електростанція (до 30 рівнів)
* Автозбереження прогресу у файл `Save/save.txt` кожну секунду
* Завантаження збережень при старті
* Динамічний інтерфейс із можливістю прокрутки списку апгрейдів
* Підтримка кастомних текстур (папка `TexturePack`)

## Залежності

* C++17 (або новіша версія)
* SFML 2.5 (Graphics, Window, System)
* Файл шрифту `OpenSans.ttf` у корені проєкту
* Опціонально: власні текстури у папці `TexturePack`

## Збірка та запуск

1. **Налаштування SFML**

   * Переконайтесь, що SFML встановлена в системі або вкажіть шлях до неї під час збірки.

2. **Компіляція (GCC/Clang)**

   ```bash
   g++ -std=c++17 main.cpp -o ElectroClicker -lsfml-graphics -lsfml-window -lsfml-system
   ```

3. **Запуск**

   ```bash
   ./ElectroClicker
   ```

> Якщо виникають проблеми з пошуком бібліотек SFML, вкажіть шлях за допомогою ключів `-I` та `-L`.

## Використання

* Натискайте кнопку **Нажать** для отримання енергії.
* Відкрийте список апгрейдів у нижній частині екрану та придбайте доступні покращення.
* Прогрес зберігається автоматично в `Save/save.txt` кожну секунду.

## Налаштування текстур

1. Створіть папку `TexturePack` у корені проєкту.
2. Додайте файли:

   * `battery.png`
   * `solar.png`
   * `wind.png`
   * `button.png`
   * `energy.png`
3. Якщо цих файлів немає, гра відобразить прості фігури замість текстур.

---

*Приємної гри та вдалої розробки!*
