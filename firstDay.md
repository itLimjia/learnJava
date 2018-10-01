1. ARRAY:

 - 数组声明和初始化
    + 数组声明语法  
     类型 数组名；  
	     举例:  
	     ```int[] arrayName;```
    + 数组初始化语法  
	 动态初始化：arrayName = new type[length] ;  
	 举例：  
	 ```arrayName = new int[5]; ```  
	 静态初始化：arrayName = new type[] {element,element,....}  
	 举例：  
	 ```arrayName = new int[] {1,23,43,34}```  
	+ 使用数组的简单实例：(使用字符数组存储字符并输出)
	 ```	
			class ArrayDemo
			{
				public static void main(String[] args) 
				{
					char[] charSave = new char[3];
					charSave[0] = 'A';
					charSave[1] = 'B';
					charSave[2] = 'C';
					int i;
					for(i=0;i<3;i++)
					{
						System.out.println(charSave[i]);
					}
				}
			}
	
	     
	 ```
2. Java类、对象的简单介绍
 - 简单来说，类就是个体的共性地方。  
 类是用于创建一组特定对象的所有特性。使用面向对象语言编写程序时，  
 并不定义各个对象，而是定义各个类。Java类包含两种不同的信息：属性和行为。
 - 现在给个实例让大家感受一下：  
 
 ```  
		class  MarsRobot {
			String status;
			int speed;
			float temperature;
			void checkTemperature() {
				if (temperature < -80)
					{
						status = "returning home";
						speed = 5;
					}
			}
			void showAttributes() {
				System.out.println("Status: " + status);
				System.out.println("Speed: " + speed);
				System.out.println("Temperature: " + temperature);
			}
		}
		class  MarsApplication
		{
			public static void main(String[] args) 
			{
				MarsRobot spirit = new MarsRobot();
				spirit.status = "exploring";
				spirit.temperature = -60;
				spirit.speed = 2;
				spirit.showAttributes();
				System.out.println("Increasing speed to 3.");
				spirit.speed = 3;
				spirit.showAttributes();
				System.out.println("Changing temperature to -90");
				spirit.temperature = -90;
				spirit.showAttributes();
				System.out.println("Checking the temperature.");
				spirit.checkTemperature();
				spirit.showAttributes();
				
			}
		}

 ```