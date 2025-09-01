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
|1203:34	                 |   1207:D6                |

#### Manual Calculations

![WhatsApp Image 2025-09-01 at 8 52 41 PM (1)](https://github.com/user-attachments/assets/74b5cb4f-4480-45ec-8575-104e8f8982e1)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (235)" src="https://github.com/user-attachments/assets/52b72ccd-9e3d-4317-8930-d7df8be74f60" />


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
![WhatsApp Image 2025-09-01 at 8 52 41 PM](https://github.com/user-attachments/assets/cea051b0-64ec-4c19-8018-1c142f15c37a)



## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (237)" src="https://github.com/user-attachments/assets/2d7ee3c4-85fa-480e-b905-d40ce58731c9" />


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

![WhatsApp Image 2025-09-01 at 8 52 40 PM (1)](https://github.com/user-attachments/assets/1482811e-bdd5-4064-8e60-4a9f14f6fc05)


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (239)" src="https://github.com/user-attachments/assets/24b7036d-3238-4644-8612-f1ca1f858ebb" />


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

![WhatsApp Image 2025-09-01 at 8 52 40 PM](https://github.com/user-attachments/assets/914e33f7-5856-4f85-858d-f0f7555973d7)

## OUTPUT FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (241)" src="https://github.com/user-attachments/assets/520f14f8-aebd-49f9-b36b-8ce0f9d05c4f" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
