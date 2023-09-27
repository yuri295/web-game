# 리액트 반복문
```html
<ul>
    {[
        ['사과','맛있다'],
        ['바나나','달다'],
        ['포도','말랑말랑하다'],
        ['귤','시다'],
        ['감','떫다'],
        ['배','시원하다'],

    ].map((v) => {
        return (
            <li><b>{v[0]}</b> - {v[1]}</li>
        );
    })}
    
```
## key
```html
<ul>
    {[
        [fruit: '사과', taste: '맛있다'],
        [fruit: '바나나', taste:'달다'],
        [fruit: '포도',taste: '말랑말랑하다'],
        [fruit: '귤',taste: '시다'],
        [fruit: '감',taste: '떫다'],
        [fruit: '배',taste: '시원하다'],

    ].map((v) => {
        return (
            <li key={v.fruit + v.taste}><b>{v.fruit}</b> - {v.taste}</li>
        );
    })}
    

```