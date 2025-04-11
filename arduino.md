# Arduino


## 1. Arduino简介  

Arduino是一种开源电子原型平台，旨在为开发者和爱好者提供简易的工具来构建互动项目。Arduino拥有多种开发板（如Arduino UNO、Mega等）和丰富的附加模块，支持多种编程语言，以Arduino C为主，适合从初学者到专业开发者的多种需求。Arduino平台因其易用性和灵活性而受到全球用户的青睐，可以广泛应用于自动化、机器人、智能家居、物联网等多个项目。  

Arduino的主要特点包括：  
- **开放源代码**：用户可以自由使用和修改Arduino的代码与硬件设计。  
- **丰富的社区支持**：广泛的在线资源和活跃的社区，用户可以轻松找到教程和项目案例。  
- **灵活性**：支持大量传感器和模块，用户可以按需组合以实现各种功能。  
- **易于上手**：直观的编程环境和大量的学习材料，使得即使是编程新手也能快速入门。  

## 2. 连接图  

![](media/1b9d0cc7630fadf2af933d8235bc0cb3.png)  

## 3. 测试代码  

```cpp  
int ledPin = 13; // 定义数字口13  
int inputPin = 3; // 定义数字口3  

void setup() {  
    pinMode(ledPin, OUTPUT); // 将ledPin设置为输出  
    pinMode(inputPin, INPUT); // 将inputPin设置为输入  
}  

void loop() {  
    int val = digitalRead(inputPin); // 设置数字变量val，读取到数字口3的值  
    if (val == LOW) { // 当val为低电平时，LED亮起  
        digitalWrite(ledPin, HIGH); // LED亮起  
    } else {  
        digitalWrite(ledPin, LOW); // LED变暗  
    }  
}  
```  

## 4. 测试结果  

按照上图接好线，烧录好代码；上电后，按下按键后，Arduino UNO板上的D13指示灯亮起。  

## 5. 加强训练  

**代码：**  

```cpp  
int led = 13; // 定义LED引脚  
int inputPin = 3; // 定义输入引脚  
int x; // 定义变量x  

void setup() {  
    pinMode(led, OUTPUT); // 将LED引脚设置为输出  
    pinMode(inputPin, INPUT); // 将输入引脚设置为输入  
}  

void loop() {  
    int val = digitalRead(inputPin); // 读取输入引脚的值  
    if (val == 0) { // 当输入值为0时  
        x++; // 计数加1  
        digitalWrite(led, HIGH); // LED亮起  
        delay(500); // 延迟500毫秒  
    }  
    if (x == 2) { // 当计数达到2时  
        digitalWrite(led, LOW); // LED熄灭  
        x = 0; // 重置计数  
        delay(500); // 延迟500毫秒  
    }  
}  
```  

## 结果  

上传代码后，按一下按键LED灯亮起，再按一下按键LED灯熄灭。实现这个功能的关键在于变量x，值得深入思考。





