[![license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/itstep-vrn/GhostHouse/blob/master/LICENSE) [![CodeFactor](https://www.codefactor.io/repository/github/itstep-vrn/ghosthouse/badge)](https://www.codefactor.io/repository/github/itstep-vrn/ghosthouse) [![https://avatars1.githubusercontent.com/u/9919?s=200&v=4](https://github.com/AndreyDolzhenko)
# Ghost House (Дом с Привидениями)
Консольная игра-угадайка.

***
- **Игра, в которой нужно пройти 3 этажа и не встретиться с привидением**
- **© Dolzhenko Andrey, 2019**
- **© Компьютерная академия ШАГ. Воронеж, 2019**
- **Версия: 0.1 (Июль 2019)**
- **adol2000@rambler.ru**
***

## Что делает?

Предлагает выбор одной из 3-х дверей на 3-х уровнях (этажах).  
Компьютер выбирает дверь случайным образом, пользователь вводит цифры от 1 до 3.  
:dizzy_face:  Если выбор пользователя совпал с выбором компьютера, в двери появляется привидение – ***пользователь проиграл***.   
:sunglasses: Если выбор пользователя не совпал с выбором компьютера, то открывается пустая дверь – ***пользователь выиграл***.  
С каждым выигрышем пользователь проходит на следующий этаж (всего нужно пройти 3 этажа).  
С каждым проигрышем у пользователя уменьшается жизнь на 1 единицу (всего 3 жизни). При этом пользователь остается на том же этаже, на котором встретил привидение.  
Если пользователь выиграл 3 раза, то он проходит на следующий уровень, на котором его встречает Принцесса.  
Если пользователь проиграл 3 раза, то он встречается со Злым колдуном и Привидением, которые ему говорят, что у него кончились жизни и он проиграл.  

## Воспроизведение:

•	Консоль  
•	В игре не встроен синтаксический анализатор. Все команды необходимо вводить ЦИФРАМИ, следуя инструкциям в игре.  

## Getting Started

Скопируйте файл .exe в любое месте на вашем компьютере. Если у вас установлены библиотеки Visual Studio или сама программа Visual Studio, игра запустится.  


## Описание кода программы:

### Подключение библиотек и пространства имен:
```cpp
#include<iostream> //Библиотека ввода и вывода информации
#include<stdlib.h> //Стандартная библиотека для контроля выполнения программы
#include<time.h> //Библиотека для работы с системной датой и временем. Используется при расчете случайного значения
using namespace std; //Использование стандартного пространства имен
```
  
### Основные функции:
- `void Name()`  - Выводит название игры как часть игрового поля. Выводится при любой коммуникации с пользователем
- `void Start()` - Заставка. Выводится вначале один раз. Является визитной карточкой игры
- `void Description()` - Описание. Выводится один раз, описывает сценарий игры
- `void Choise()` - Выбор двери. Выводится на каждом уровне, когда игрок должен угадать дверь
- `void Win()` - Выводится в конце игры при удачном прохождении всех уровней
- `void Loss()` - Выводится в конце игры при потере всех жизней

_Геймплей игры основан на совпадении или несовпадении случайного выбора "двери" копьютером и выбора, сделанного игроком._
_Визуализация привидения в выбранной двери или отсутствие привидения в открытой двери описана в функциях:_

```cpp
void LeftDoorGhost(); // Привидение в левой двери, остальные закрыты  
void MiddleDoorGhost(); // Привидение в средней двери, остальные закрыты  
void RightDoorGhost(); // Привидение в правой двери, остальные закрыты  

void LeftDoorUser(); // Открытая пустая левая дверь, остальные закрыты  
void MiddleDoorUser(); // Открытая пустая средняя дверь, остальные закрыты  
void RightDoorUser(); // Открытая пустая правая дверь, остальные закрыты  
```
