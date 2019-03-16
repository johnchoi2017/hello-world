# hello-world
just another description
print("몇번째 소수를 알고싶습니까")
nth = input()
i_nth = int(nth)
# print(nth)
found = 0 

for i in range (2,100001):
    if i == 2:
        found = found + 1
        found_num = 1
        print("found", i)
        continue
    for j in range (2, i):
        print(i, j)
        if i % j == 0:  
            break
        if i == (j+1):
            found = found + 1
            found_num = i
            print("found", i)
    if (found == i_nth):
        break

if found < i_nth:
    print("2부터 100000까지에는 소수가", found, "개만 있습니다")
else:
    print(nth,"현재 소수는", found_num, "입니다")
