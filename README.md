# An
Практика
1. Создание нового проекта
npx create-expo-app MyApp --template expo-template-blank-typescript
cd MyApp
npm start


После запуска проект откроется в браузере или Expo Go.

2. Скачать и запустить проект с GitHub
git clone https://github.com/filin2009/rn_flexboxfroggy
cd rn_flexboxfroggy
npm install
npm start


Открой через веб-эмулятор (Expo Web).

3. Подключение @react-navigation/native
npm install @react-navigation/native
npx expo install react-native-screens react-native-safe-area-context


Добавь в код:

import { NavigationContainer } from '@react-navigation/native';

4. Удаление и пересоздание node_modules
rm -rf node_modules
npm install


(или на Windows — rmdir /s /q node_modules)

5. Приложение с чёрным квадратом
export default function App() {
  return (
    <View style={{flex:1, justifyContent:'center', alignItems:'center'}}>
      <View style={{width:100, height:100, backgroundColor:'black', justifyContent:'center', alignItems:'center'}}>
        <Text style={{color:'white'}}>Привет</Text>
      </View>
    </View>
  );
}

6. Квадрат с кнопками (смена цвета)
import { useState } from 'react';
import { View, Button } from 'react-native';

export default function App() {
  const [color, setColor] = useState('black');
  return (
    <View style={{alignItems:'center', marginTop:100}}>
      <View style={{width:100, height:100, backgroundColor:color}}/>
      <Button title="Красный" onPress={()=>setColor('red')}/>
      <Button title="Зеленый" onPress={()=>setColor('green')}/>
    </View>
  );
}

7. Три квадрата
<View style={{flexDirection:'row', justifyContent:'space-around', marginTop:100}}>
  <View style={{width:50, height:50, backgroundColor:'gold'}}/>
  <View style={{width:50, height:50, backgroundColor:'gray'}}/>
  <View style={{width:50, height:50, backgroundColor:'green'}}/>
</View>

8. Светофор
<View style={{alignItems:'center', marginTop:100}}>
  <View style={{width:100, height:100, borderRadius:50, backgroundColor:'red', margin:10}}/>
  <View style={{width:100, height:100, borderRadius:50, backgroundColor:'yellow', margin:10}}/>
  <View style={{width:100, height:100, borderRadius:50, backgroundColor:'green', margin:10}}/>
</View>

9. Флаг ПМР
<View>
  <View style={{height:90, backgroundColor:'red'}}/>
  <View style={{height:90, backgroundColor:'green'}}/>
  <View style={{height:90, backgroundColor:'red'}}/>
</View>

10. Компонент Dog

Dog.tsx

import { View, Text } from 'react-native';
export default function Dog({name}:{name:string}) {
  return (
    <View style={{backgroundColor:'green', height:100, justifyContent:'center', alignItems:'center', margin:5}}>
      <Text style={{color:'white'}}>{name}</Text>
    </View>
  );
}


App.tsx

import Dog from './Dog';
export default function App() {
  return (
    <>
      <Dog name="Шарик1"/>
      <Dog name="Шарик2"/>
      <Dog name="Шарик3"/>
    </>
  );
}

11. Переменная стейта
const [data, setData] = useState<string>('Пример');

12. Три кнопки с текстом
import { useState } from 'react';
import { View, Button, Text } from 'react-native';

export default function App() {
  const [text, setText] = useState('');
  return (
    <View style={{marginTop:100}}>
      <Button title="Кнопка1" onPress={()=>setText('Нажата кнопка1')}/>
      <Button title="Кнопка2" onPress={()=>setText('Нажата кнопка2')}/>
      <Button title="Кнопка3" onPress={()=>setText('Нажата кнопка3')}/>
      <Text>{text}</Text>
    </View>
  );
}

13. Компонент Header

Header.tsx

import { Text, View } from 'react-native';
export default function Header() {
  return (
    <View style={{padding:20, backgroundColor:'lightblue'}}>
      <Text style={{fontSize:20}}>Главная страница</Text>
    </View>
  );
}


App.tsx

import Header from './Header';
export default function App() {
  return <Header />;
}







Теория
. Мобильное устройство — портативное устройство с автономным питанием и доступом к сети. Примеры: ноутбук, планшет, телефон, Smart TV.

2. Операционная система — программа, управляющая устройством и его ресурсами. Бывает: Windows, Linux, macOS, Android, iOS и др.

3. Android — ОС от Google (2008), открытая, на базе Linux. Сейчас актуальны версии 13–15. Dalvik и ART — движки выполнения кода.

4. iOS — ОС от Apple (2007), закрытая, только для устройств Apple. Инструмент — XCode. Jailbreak — снятие ограничений.

5. Нативные языки Android: Java и Kotlin. Среда — Android Studio.

6. Нативные языки iOS: Objective-C и Swift. Среда — XCode.

7. Кроссплатформенные: Flutter (Dart), .NET MAUI (C#), Ionic, React Native (JS/TS). Позволяют писать одно приложение для разных ОС.

8. Магазины приложений — сервисы для загрузки и обновления ПО. Android: Google Play, Amazon, Xiaomi, F-Droid, 4PDA.

9. Магазины iOS — Apple Store (официальный), Cydia (неофициальный, через Jailbreak).

10. Git — система контроля версий. Репозитории хранят код. Github — облачный сервис. .gitignore исключает файлы из репозитория.

11. JavaScript — язык для веба (1995, Netscape). Движки: V8 (Chrome), Gecko (Firefox), Quantum.

12. TypeScript — надстройка над JS от Microsoft (2012), добавляет строгую типизацию.

13. React — библиотека JS. Основы: JSX (разметка), компоненты (функции/классы), пропсы (входные данные), стейт (внутренние данные).

14. React Native — фреймворк 2015 г. для мобильных приложений на JS. Плюсы — скорость и кроссплатформенность; минусы — производительность и зависимость от нативных модулей.

15. Expo — набор инструментов для RN, позволяет быстро создавать и тестировать проекты (в т.ч. через Snack).

16. Для RN+Expo под Windows нужны: Git, Github Desktop, NodeJS, VS Code, командная строка, браузер.

17. package.json — описание проекта и зависимостей; tsconfig.json — настройки TypeScript.

18. Новый проект: npx create-expo-app. Существующий — клонировать с Github (git clone) и запустить (npm start или через Snack).

19. Эмулятор — виртуальное устройство для теста. Android — Bluestacks, Nox, LDPlayer; iOS — XCode Simulator.

20. Компоненты RN — строительные блоки интерфейса. Бывают встроенные (View, Text, Image), свои и сторонние (через import).

21. JSX — синтаксис, похожий на HTML, используется в React. Вставка переменных — {переменная}.

22. State — внутреннее состояние компонента. Меняется через setState или useState, после чего компонент перерисовывается.

23. Props — входные параметры компонента. Передаются как атрибуты при вызове.

24. Стили — объект JS, подключается через style={styles.name}. Похожи на CSS.

25. Цвета — задают оформление. Можно использовать именованные цвета ('red') или HEX ('#ff0000').

26. Кнопки: Button (простая), Pressable (гибкая), TouchableOpacity (с эффектом прозрачности).

27. Обработчики событий (onPress, onChangeText) выполняют действия при взаимодействии пользователя.

28. Списки: FlatList, SectionList — выводят массивы данных. Главное — задать data и renderItem.

29. FlexBox — система позиционирования элементов. Помогает адаптировать интерфейс под экран и динамически менять структуру.

30. Несколько стилей можно объединять массивом: style={[styles.one, styles.two]}. Поздний стиль перекрывает ранний.

31. Шрифты — внешний вид текста. Подключение через Expo-Font, require('./font.ttf'), использование в style={{fontFamily:'...'}}.

32. Навигация — переход между экранами. Бывает стековая, табовая, дроверная и др.

33. Стековая навигация (@react-navigation/stack) — переход «вперёд/назад» между экранами (push/pop).

34. Консоль — инструмент отладки. console.log() выводит сообщения.

35. Работа с сервером — получение данных в формате JSON через fetch(), преобразование response.json() и использование в компоненте.

