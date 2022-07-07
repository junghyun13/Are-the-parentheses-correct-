# Are-the-parentheses-correct-
# python
# Correct pairing of parentheses means that if it is opened with a '(' character, it must be paired and closed with a ')' character. True if true, False if incorrect. 괄호가 바르게 짝지어졌다는 것은 '(' 문자로 열렸으면 반드시 짝지어서 ')' 문자로 닫혀야 한다 맞으면 True를 틀리면 False를 출력한다.
def solution(s):
    answer=True
    SS=[]
    for S in s:
        if S=='(':
            SS.append(S) #여기서는 SS에 (을 추가한다.
        else: #s가 )라면
            if SS==[]:
                answer=False
                break
            else:
                SS.pop() #SS에 있는 맨 끝쪽의 (를 뺀다.
    if SS!=[]:
        answer=False
    return answer
s=')()(()'
a=solution(s)
print(a)
#result--> False
