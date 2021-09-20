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

                 const getUsersWithFriend = (users, friendName) => users.filter(user => user.friends.includes(friendName));



5. Задача. Пользователи с другом
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
Дополни функцию getFriends(users) так, чтобы она возвращала массив друзей всех пользователей (свойство friends). У нескольких пользователей могут быть одинаковые друзья, сделай так чтобы возвращаемый массив не содержал повторений.

                
                 const getFriends = (users) =>
                  users.flatMap(user => user.friends).filter((friend, index, allFriends) => allFriends.indexOf(friend) === index);


6. Задача. Активные пользователи
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
  {
  Задание
Дополни функцию getActiveUsers(users) так, чтобы она возвращала массив активных пользователей, значение свойства isActive которых true.


                const getActiveUsers = (users) => users.filter(user => user.isActive === true); 
                
                
                
   7. Задача. Общее количество друзей
Этот массив объектов мы будем передавать в параметр users при вызове функции из задания.

[
  {
    name: 'Moore Hensley',
    email: 'moorehensley@indexia.com',
    eyeColor: 'blue',
    friends: ['Sharron Pace'],
    isActive: false,
    balance: 2811,
    gender: 'male'
  },
  { 
  Задание
Дополни функцию getTotalFriendCount(users) так, чтобы она считала и возвращала общее количество друзей (свойство friends) всех пользователей из массива users.


               const getTotalFriendCount = users => { return users.reduce((total, user) => {return total + user.friends.length}, 0);};



 8. Задача. Сортировка по балансу
Этот массив объектов мы будем передавать в параметр users при вызове функции из задания.

[
  {
    name: 'Moore Hensley',
    email: 'moorehensley@indexia.com',
    eyeColor: 'blue',
    friends: ['Sharron Pace'],
    isActive: false,
    balance: 2811,
    gender: 'male'
  },
  {Задание
Дополни функцию sortByAscendingBalance(users) так, чтобы она возвращала массив пользователей отсортированный по возрастанию их баланса (свойство balance).


                const sortByAscendingBalance = users => {
                  const newBalance = (a, b) => a.balance - b.balance;
                  return users.sort(newBalance);


9. Задача. Сортировка по количеству друзей
Этот массив объектов мы будем передавать в параметр users при вызове функции из задания.
Задание
Дополни функцию sortByDescendingFriendCount(users) так, чтобы она возвращала массив пользователей отсортированный по убыванию количества их друзей (свойство friends).


                const sortByDescendingFriendCount = users => [...users].sort((a, b) => b.friends.length - a.friends.length);



10. Задача. Имена друзей
Этот массив объектов мы будем передавать в параметр users при вызове функции из задания.

[
  {
    name: 'Moore Hensley',
    email: 'moorehensley@indexia.com',
    eyeColor: 'blue',
    friends: ['Sharron Pace'],
    isActive: false,
    balance: 2811,
    gender: 'male'
  },
  {
  Задание
Дополни функцию getSortedFriends(users) так, чтобы она возвращала массив уникальных имён друзей (свойство friends) отсортированный по алфавиту .


                const getSortedFriends = users =>
                  users
                  .flatMap(user => user.friends)
                  .filter((friend, index, allFriends) => allFriends.indexOf(friend) === index)
                  .sort((a, b) => a.localeCompare(b));



11. Задача. Общий баланс
Этот массив объектов мы будем передавать в параметр users при вызове функции из задания.
Задание
Дополни функцию getTotalBalanceByGender(users, gender) так, чтобы она возвращала общий баланс пользователей (свойство balance), пол которых (свойство gender) совпадает со значением параметра gender.

                const getTotalBalanceByGender = (users, gender) =>
                   [...users]
                   .filter(user => user.gender === gender)
                   .map(user => user.balance)
                   .reduce((total, value) => total + value, 0);
