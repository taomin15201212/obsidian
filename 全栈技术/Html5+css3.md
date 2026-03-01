盒模型BFC

容器的属性

- flex-direction
    
- flex-wrap
    
- flex-flow
    
- justify-content
    
- align-items
    
- align-content
    

  

项目的属性

- order
    
- flex-grow
    
- flex-shrink
    
- flex-basis
    
- flex
    
- align-self
    

## 1.用到的基本属性：

### 1.flex-direction: 设置主轴的方向

通过使用flex-direction属性可以实现控制子元素使用的是行排列还是列排列

```
flex-direction: row; // 行排列
flex-direction: column; // 列排列
```

还提供了两个reverse属性 能自动翻转元素！

### 2.justify-content: 设置主轴上的元素排列方式

```
justify-content: flex-start; // 如果是x轴 从左到右 y轴 从上到下
justify-content: flex-end;// x轴：从右到左 y轴：从下到上
justify-content: center;// 全部居中
justify-content: space-around;// 环绕排列 平分剩余空间
justify-content: space-between;// 保证两边贴边的情况下 再平分剩余空间
```

### 3.flex-wrap：设置子元素是否换行

很多场景下 比如一行我们原先只有3个元素 但突然来了四个元素 默认情况下 第四个元素是会直接缩小宽度/高度来满足摆放的

使用flex-wrap属性可以设置是否换行

```
flex-wrap: wrap; //换行
flex-wrap: nowrap; //不换行(默认)
```

### 4.align-items： 设置侧轴的方向（y轴）

```
align-items: flex-start; // 如果是x轴 从左到右 y轴 从上到下
align-items: flex-end;// x轴：从右到左 y轴：从下到上
align-items: center;// 全部居中
align-items: space-around;// 环绕排列 平分剩余空间
align-items: space-between;// 保证两边贴边的情况下 再平分剩余空间
```

### 5.align-centent： 设置侧轴的方向（y轴）（多行）

```
align-items: flex-start; // 如果是x轴 从左到右 y轴 从上到下
align-items: flex-end;// x轴：从右到左 y轴：从下到上
align-items: center;// 全部居中
align-items: space-around;// 环绕排列 平分剩余空间
align-items: space-between;// 保证两边贴边的情况下 再平分剩余空间
align-items: stretch;// 设置子元素高度平分父级元素高度
```

  

  

画中画

document.querySelectorAll('video')[0].requestPictureInPicture(); 

Emmet

select>option[value=$]{$}*31});

  

  

CSS

less

& /deep/ 

& > em

深度解析 >>>

  

//模糊遮罩

backdrop-filter:saturate(150%) blur(8px);  

  

变灰

filter: progid:DXImageTransform.Microsoft.BasicImage(grayscale=1);

-webkit-filter: grayscale(100%);

  

高亮

box-shadow:rgba(0, 0, 0, 0.1) 0px 2px 5px, rgba(225, 225, 225, 0.5) 0px 0.5px 1px inset  

  

径向渐变

conic-gradient(from -44.73deg at 60.34% 50%, #f55200 -49.59deg, #aa0afa 9.4deg, #06f 155.37deg, #fff 215.4deg, #f55200 310.41deg, #aa0afa 369.4deg), linear-gradient(180deg, hsla(0, 0%, 100%, .16), hsla(0, 0%, 100%, .056) 49.32%, hsla(0, 0%, 100%, .16)) !important

  

pointer-events: none;

background-image: linear-gradient(90deg, rgb(208, 243, 170) 3%, rgb(5, 219, 240) 82%);

background-image: linear-gradient(119deg,#2d94ff,#ac98ff 28%,#2d94ff 57%,#ac98ff 87%)

background-image: linear-gradient(90deg,#2d94ff 4%,#ac98ff 95%)

transition: all 0.3s ease 0s;

transform: rotateY(240deg) translateZ(150px) scale(0.925);

animation: rotate_0 10s linear .5s infinite;

transform: rotateY(0deg) translateZ(150px);

animation: rotate_1 10s linear .5s infinite;

transform: rotateY(120deg) translateZ(150px) scale(0.925);

animation: rotate_2 10s linear .5s infinite;



毛玻璃效果

backdrop-filter: saturate(150%) blur(24px);  

首字母大写

text-transform: capitalize;  

[https://beamcast.app/](https://beamcast.app/)  

文字颜色渐变

 {

    

1. background: linear-gradient(
    
      
    
    90.06deg
    
    , #2f5cfe .05%, #32e3fb 97.77%);
2.  -webkit-background-clip: text;
3.  background-clip: text;
4.  -webkit-text-fill-color: transparent;
5. text-fill-color: transparent;
6.  -webkit-user-select: none;
7. -moz-user-select: none;
8.  user-select: none;
9.  animation: hue 10s linear infinite;

}

  

  

###背景网格

.grid {  
height: 200px;  
width: 100%;  
background-image:  
linear-gradient(to right, rgb(203 213 225) 1px, transparent 1px),  
linear-gradient(to bottom, rgb(203 213 225) 1px, transparent 1px);  
background-size: 20px 20px;  
background-position: center center;  
}  

  

###四周线性渐变

.grid {  
-webkit-mask-image: linear-gradient(to bottom,transparent,#fff 50px calc(100% - 50px),transparent),linear-gradient(to right,transparent,#fff 50px calc(100% - 50px),transparent);  
mask-image: linear-gradient(to bottom,transparent,#fff 50px calc(100% - 50px),transparent),linear-gradient(to right,transparent,#fff 50px calc(100% - 50px),transparent);  
mask-composite: intersect;  
-webkit-mask-composite: source-in, xor;  
}  

  

###网状点阵背景

.grid {  
height: 200px;  
background-image: radial-gradient(circle, rgb(203 213 225) 2px, #fff 2px);  
background-size: 20px 20px;  
background-position: center center;  
}  

  

  

background-clip:text;  
![](https://app.yinxiang.com/shard/s46/res/0279915f-58a9-490e-8492-9574a06d9d9b/gradient.png)