# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|1200:12                  | 	1204:24                |
|1201:34	                 |   1205:68                |            
|1202:12	                 |   1206:00                |
|1203:34	                 |   1207:C4                |

#### Manual Calculations
![WhatsApp Image 2025-09-01 at 8 52 41 PM (1)](https://github.com/user-attachments/assets/cb2f34fc-700e-43ea-9863-d32068c3bb3e)


## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (236)" src="https://github.com/user-attachments/assets/7bc8c6cf-006f-4339-bb1f-e8f4530e987a" />

<img width="640" height="480" alt="Screenshot (235)" src="https://github.com/user-attachments/assets/a822fab0-2736-49b8-8e3c-ecb12257f817" />


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,1200H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|1200:12                  |  00:1204                 |
|1202:34                  |  00:1205                 |
|1202:12                  |  00:1206                 |
|1202:34                  |  C4:1207                 |

#### Manual Calculations
![WhatsApp Image 2025-09-01 at 8 52 41 PM](https://github.com/user-attachments/assets/d100523b-c347-457c-849d-c5f4b07b8893)


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (238)" src="https://github.com/user-attachments/assets/140d3f1b-61f6-4005-bab9-92674543c141" />

<img width="640" height="480" alt="Screenshot (237)" src="https://github.com/user-attachments/assets/808830fb-042c-4c08-8c6a-d4dd3b0aa907" />



## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|1200:12                  |  44:1204                 |
|1202:34                  |  51:1205                 |
|1202:12                  |  97:1206                 |
|1202:34                  |  0A:1207                 |

#### Manual Calculations
![WhatsApp Image 2025-09-01 at 8 52 40 PM (1)](https://github.com/user-attachments/assets/f158dfd2-5d98-41ef-a5b9-c328d462efb1)


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (240)" src="https://github.com/user-attachments/assets/1f85197c-8be3-4b2e-89a7-74f4cfcb824f" />

<img width="640" height="480" alt="Screenshot (239)" src="https://github.com/user-attachments/assets/2e1e6746-0bd1-48e0-8acb-fc4687ba85cb" />



## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|1200:12                  |  00:1204                 |
|1202:34                  |  01:1205                 |
|1202:12                  |  00:1206                 |
|1202:34                  |  00:1207                 |

#### Manual Calculations
![WhatsApp Image 2025-09-01 at 8 52 40 PM](https://github.com/user-attachments/assets/255f5a2a-3134-43f5-b8e2-5a6407e93080)


## OUTPUT FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (242)" src="https://github.com/user-attachments/assets/4c5f0a65-68f2-4e8f-80d4-d75598834c5b" />

<img width="640" height="480" alt="Screenshot (241)" src="https://github.com/user-attachments/assets/458f1846-f0bd-4db6-a1be-7c0225fe9d3e" />





## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
