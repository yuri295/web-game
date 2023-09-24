# 컨트롤드 인풋 vs 언컨트롤드 인풋
## 언컨트롤드 인풋
    - value가 onSubmit 안에서만 사용하는 경우 언컨트롤드 인풋 사용 가능
    (컨트롤드 인풋을 e.target.children.word로 대체할 수 있기 때문)
    - input 안에 있는 value를 지우고 언컨트롤드 인풋으로 전환
    - 간단한 경우만 사용
    - defaultValue 사용
'''
const onSubmitForm = (e) => {
    e.preventDefault();
    if (word[word.length - 1] === e.target.children.word.value[0]) {
        setResult('딩동댕');
        setWord(e.target.children.word.value);
        e.target.children.word.value = '';
        inputRef.current.focus();
    }else {
        setResult('땡');
        e.target.children.word.value = '';
        inputRef.current.focus();
    }
};

'''