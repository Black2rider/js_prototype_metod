1. Задача. Общие элементы
Задание
Функция getCommonElements(firstArray, secondArray) принимает два массива произвольной длины в параметры firstArray и secondArray, и возвращает новый массив их общих элементов, то есть тех которые есть в обоих массивах.
Выполни рефакторинг функции так, чтобы вместо цикла for она использовала метод forEach.

        function getCommonElements(firstArray, secondArray) {
            const commonElements = [];
            // Пиши код ниже этой строки

           // for (let i = 0; i < firstArray.length; i += 1) {
            //  if (secondArray.includes(firstArray[i])) {
            //    commonElements.push(firstArray[i]);
            //  }
            //}

            firstArray.forEach(function(element){
             if(secondArray.includes(element)) {
               commonElements.push(element);
                };
            })

            return commonElements;
            // Пиши код выше этой строки
          }
  
  
  
 2. Задание
Функция changeEven(numbers, value) принимает массив чисел numbers и обновляет каждый элемент, значение которого это чётное число, добавляя к нему значение параметра value.

Выполни рефакторинг функции так, чтобы она стала чистой - не изменяла массив чисел numbers, а создавала, наполняла и возвращала новый массив с обновлёнными значениями.

        function changeEven(numbers, value) {
            // Пиши код ниже этой строки
          const arrow = [];
            numbers.forEach(el => {
              if (el % 2 === 0) {
                arrow.push(el + value);
              } else { arrow.push(el)
              };
            });
             return arrow;
            // Пиши код выше этой строки
          }
          
 3. Задача. Пользователи в возрастной категории
Этот массив объектов мы будем передавать в параметр users при вызове функции из задания.

[
  {
    name: 'Moore Hensley',
    email: 'moorehensley@indexia.com',
    eyeColor: 'blue',
    friends: ['Sharron Pace'],
    isActive: false,
    balance: 2811,
    gender: 'male',
    age: 37
  },
  Задание
Дополни функцию getUsersWithAge(users, minAge, maxAge) так, чтобы она возвращала массив пользователей, возраст которых (свойство age) попадает в промежуток от minAge до maxAge.

            const getUsersWithAge = (users, minAge, maxAge) => 
            users.filter(user => user.age >= minAge && user.age < maxAge);


4. Задача. Пользователи с другом
Этот массив объектов мы будем передавать в параметр users при вызове функции из задания.
[
  {
    name: 'Moore Hensley',
    email: 'moorehensley@indexia.com',
    eyeColor: 'blue',
    friends: ['Sharron Pace'],
    isActive: false,
    balance: 2811,
    gender: 'male',
    age: 37
  },
  Задание
Дополни функцию getUsersWithFriend(users, friendName) так, чтобы она возвращала массив пользователей у которых есть друг с именем в параметре friendName. Массив друзей пользователя хранится в свойстве friends.

5. адача. Пользователи с другом
Этот массив объектов мы будем передавать в параметр users при вызове функции из задания.

[
  {
    name: 'Moore Hensley',
    email: 'moorehensley@indexia.com',
    eyeColor: 'blue',
    friends: ['Sharron Pace'],
    isActive: false,
    balance: 2811,
    gender: 'male',
    age: 37
  },
  Задание
Дополни функцию getUsersWithFriend(users, friendName) так, чтобы она возвращала массив пользователей у которых есть друг с именем в параметре friendName. Массив друзей пользователя хранится в свойстве friends.

                const getUsersWithFriend = (users, friendName) => users.filter(user => user.friends.includes(friendName));
