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
