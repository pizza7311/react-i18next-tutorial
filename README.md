# react-i18next-tutorial

### 설치

아래의 패키지를 설치한다

* react-i18next
* i18next

```
npm i i18next react-i18next
```

### 시작하기

src 폴더안에 i18n 폴더를 생성한다.  


그리고 i18n의 설정파일을 작성한다

```js
import i18n from 'i18next';
import { initReactI18next } from 'react-i18next';
import en from './en.json'
import ko from './ko.json'


i18n
    .use(initReactI18next)
    .init({
        debug: true,
        resources: {
            en: {
                translation: en
            },
            ko: {
                translation: ko
            }
        },
        fallbackLng: 'en'
    })
```

i18n 의 use() 메소드로 여러가지 플러그인을 적용할수있다.  
기본적으로 [사용자의 브라우저 언어를 감지하는 플러그인](https://github.com/i18next/i18next-browser-languageDetector)을 자주 사용하는것 같지만 이 예제에서는 
다른 플러그인은 사용하지 않았다.  
