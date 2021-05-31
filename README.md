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
