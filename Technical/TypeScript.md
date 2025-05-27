# 常用的内置工具类型（Record、Partial 、 Required 、 Readonly、 Pick 、 Exclude 、 Extract 、 Omit）的使用

  

  

type Point = { x: number; y: number; c:number };

`//type`定义的类型可以通过交叉类型（`&`）来进行复用，而`interface`定义的类型则可以通过继承（`extends`）  

type Coordinate = Point & {}  

interface prop1 extends Point

  

`//Omit`和`Pick`分别用于排除和选择类型中的属性  

Omit(Point,'c'){ e: number}

interface Props1 extends Pick<Point, 'x' | 'y'> { e: string; }  

  

// 通过使用`type`关键字定义基础类型，我们可以避免类型被意外修改，进而增强代码的稳定性和可维护性。

type BaseProps<T> = {}  

  

//通过定义函数签名的方式

type GreetFunction = { (name: string): string; (age: number): string; };

const greet: GreetFunction = (value: any): string => {