# 01_Rix

by 周子揚 Rix

## Q1. 

### Questions 

Write python codes to illustrate Propositions C and D (suppose $X\sim exp(1)$)  
![image](https://github.com/user-attachments/assets/440f0b19-087a-45b3-bf30-691e555c702b)  
![image](https://github.com/user-attachments/assets/d240d996-dfe8-4d20-ab16-ee3740f9ea93)

### Answers

![image](https://github.com/user-attachments/assets/f66a033b-dc03-4f0f-ad3a-3a792ced9c49)
![Figure_1](https://github.com/user-attachments/assets/67e9cafc-812d-41d1-952d-b5fbb1423511)
![image](https://github.com/user-attachments/assets/de146f54-2a45-4c0b-b86d-9c506b4ac9ce)
![1](https://github.com/user-attachments/assets/c31e8827-1f09-4553-ad11-6037514ebd6c)
![2](https://github.com/user-attachments/assets/2aa22dd8-e407-4cfa-8c71-875f78b6ec91)
![3](https://github.com/user-attachments/assets/1575a3b4-1ccf-474b-ac2b-d6386e681733)

## Q2. 

### Questions 

Write python codes to illustration Ch02.65 for α = 2.  
![image](https://github.com/user-attachments/assets/be8180d5-c5d3-434e-a10e-0efbd4742f79)

### Answers

![image](https://github.com/user-attachments/assets/4232ae70-5280-4daa-b409-2da68e0cbfde)
![4](https://github.com/user-attachments/assets/ae534b72-6fbd-4b22-895b-b54b3ad41136)

## Q3. 

### Questions 

![image](https://github.com/user-attachments/assets/b5e632ab-3048-4c58-aeaa-2e314b5d143d)

### Answers

![image](https://github.com/user-attachments/assets/f4fcc95e-2384-41b3-a2d6-e1fb7713971f)

## Q4. 

### Questions 

![image](https://github.com/user-attachments/assets/e29f142f-200a-4222-9451-29dcc4cd04de)

### Answers

![image](https://github.com/user-attachments/assets/6651b348-a17d-4e38-95b2-270c240afc59)

## Q5. 

### Questions 

![image](https://github.com/user-attachments/assets/ff45c0f7-5594-43c3-a4f1-aa21149cf166)

### Answers

a.  
We need to find some coprime numbers to ensure that the generated numbers won't fall into a loop.  
so we choose a = 5, c = 3, m = 16, and seed number $x_0 = 7$.  
and the generated numbers are 7, 6, 1, 8, 11, 10, 5, 12, 15, 14, 9, 0, 3, 2, 13, 4, 7...  
looks 'random'  
b.  
RANDU  
```
def linear_congruential_generator(a, c, m, x0, n):
    sequence = [x0]
    for _ in range(n):
        x_next = (a * sequence[-1] + c) % m
        sequence.append(x_next)
    return sequence

a = 69069
c = 0
m = 2 ** 31
x0 = 1
n = 10

sequence = linear_congruential_generator(a, c, m, x0, n)

for i, x in enumerate(sequence):
    print(f"x{i} = {x}")
```
![image](https://github.com/user-attachments/assets/e3907781-91ab-4297-83e3-2d1d61b2d3b6)
```
def linear_congruential_generator(a, c, m, x0, n):
    sequence = [x0]
    for _ in range(n):
        x_next = (a * sequence[-1] + c) % m
        sequence.append(x_next)
    return sequence

a = 65539
c = 0
m = 2 ** 31
x0 = 1
n = 10

sequence = linear_congruential_generator(a, c, m, x0, n)

for i, x in enumerate(sequence):
    print(f"x{i} = {x}")
```
![image](https://github.com/user-attachments/assets/07810a6c-5272-469e-bac7-d371efb2ed26)  
It looks 'random'  
But there are only odd numbers.  
If the seed is an even number, and there will be all even numbers.  

The normalized chart :  
```
import matplotlib.pyplot as plt

def linear_congruential_generator(a, c, m, x0, n):
    sequence = [x0]
    for _ in range(n):
        x_next = (a * sequence[-1] + c) % m
        sequence.append(x_next)
    return sequence

a = 69069
c = 0
m = 2 ** 31
x0 = 1
n = 10000

sequence = linear_congruential_generator(a, c, m, x0, n)

sequence_normalized = [x / m for x in sequence]

plt.plot(sequence_normalized)
plt.xlabel('n')
plt.ylabel('x(normalize)')
plt.title('Linear Congruential Generator Sequence (Normalized)')
plt.show()
```
![5](https://github.com/user-attachments/assets/3599a9d9-3144-439c-a70f-086b9d01db59) 

## Q6. 

### Questions 

![image](https://github.com/user-attachments/assets/e00e2cca-6f75-4f4b-a6cd-65324c1975a7)

### Answers

![image](https://github.com/user-attachments/assets/ad358e4b-9b60-4afe-9ffb-7a55c5f041d0)


## Q7. 

### Questions 

![image](https://github.com/user-attachments/assets/e83745ed-a711-42c0-a065-1cc0e58f720e)

### Answers

![image](https://github.com/user-attachments/assets/8527414d-bdb4-4a3a-bfe0-e381918d2858)

## Q8. 

### Questions 

![image](https://github.com/user-attachments/assets/c12aa6f1-ffd9-4b53-919d-0ee1aee17325)

### Answers

![image](https://github.com/user-attachments/assets/fcf5fa5e-c57c-456d-9c5f-5c3faf586ca9)
