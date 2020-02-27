
![heart](https://i.postimg.cc/2yt76fSc/heart.gif)

### **pour voir l'implementation final [Heart](https://www.mar1n.com/css/heart/)**

# *la recette*
[x] faire le coeur
```css
.corazon {
    position: relative;
    width: 100px;
    height: 100px;
    background: #e54a27;
    transform: rotate(45deg) translate(10px,10px);
    animation: animationHeart 1s ease-in-out infinite;
   left:20%;
    z-index: 3;
}
.corazon::before{
    content: '';
    width: 100%;
    height: 100%;
    background: #e54a27;
    position: absolute;
    top: -50%;
    left: 0;
    border-radius: 50%;
    z-index: -1;
}
.corazon:after{
    content: '';
    width: 100%;
    height: 100%;
    background: #e54a27;
    position: absolute;
    bottom: 0%;
    right: 50%;
    border-radius: 50%;
    z-index: -1;
}
```
> d'abord il faut faire un carre avec 100px de dimention sur les cote; le couleur es red/rouge (#e54a27); ce carre on le fait une rotation de 45 deg; faire les deux oreilles du coeur, on va faire avec le class corazon un before et after (deux circule de meme taille), sa position sera tout en haut une -50% et l'autre 50%.  

[x] animation du coeur 
```css
@keyframes animationHeart {
    0%
    {
        
        transform: rotate(45deg) translate(10px,10px) scale(1);
    }
    25%
    {
      
        transform: rotate(45deg) translate(10px,10px) scale(1);
    }
    30%
    {
        
        transform: rotate(45deg) translate(10px,10px) scale(1.4);
    }
   
    50%
    {
        
        transform: rotate(45deg) translate(10px,10px) scale(1.2);
    }
    
    75%
    {
        
        transform: rotate(45deg) translate(10px,10px) scale(1.4);
    }
    90%
    {
        transform: rotate(45deg) translate(10px,10px) scale(1);
    }
    
    100%
    {
        
        transform: rotate(45deg) translate(10px,10px) scale(1);
    }
}
```
> il faut reflechir comme on voudrais que le couer se bouge! en ce cas; on va changer seulement son scale a maximun 1.4 de son scale original comme s'il se dilate ou se contrer.  

[x] repeter le meme code pour un coeur plus grand qui sera le Background 

```css
.corazonBg{
    position: relative;
    top: 40vh;
    left: 45vw;
    transform-origin: center;
    width: 200px;
    height: 200px;
    background: #ee6661;
    transform: rotate(45deg) ;
    z-index: -3;
    animation: big 5s linear infinite;
}
.corazonBg::before{
    content: '';
    width: 100%;
    height: 100%;
    background: #ee6661;
    position: absolute;
    top: -50%;
    left: 0;
    border-radius: 50%;
    z-index: -1;
    animation: big1 5s linear infinite;
}
.corazonBg:after{
    content: '';
    width: 100%;
    height: 100%;
    background: #ee6661;
    position: absolute;
    bottom: 0%;
    right: 50%;
    border-radius: 50%;
    z-index: -1;
    animation: big1 5s linear infinite;
}
@keyframes big1 {
    
    33%{
        
        background: #db463a;
    }
    
    
    66%{
        
   
        background: #af2f26;
    }
    
    
    99%{
        
        background: #ee6661;
    }
    
}
@keyframes big {
    0%{
        transform: rotate(45deg) scale(0.8);
    }
    33%{
        transform: rotate(45deg) scale(10);
        background: #db463a;
    }
    35%{
        transform: rotate(45deg) scale(1);
        
    }
    
    66%{
        
        transform: rotate(45deg) scale(10);
        background: #af2f26;
    }
    68%{
        
        transform: rotate(45deg) scale(0.8);
    }
    99%{
        transform: rotate(45deg) scale(10);
        background: #ee6661;
    }
    100%{
        
    }
}
```
>la difference dans ce couer par rapport a le premier c'est que  la taille sera un peu plus grand et dans sont animation la scale sera si grand pour couvrir tout le scran. change dans les different couleur de rouge pour faire un effect plus jolie :smile:

[x] faire les yeux et la bouche
```css
.face{
    width: 50px;
    height: 50px;
    position: absolute;

}
.eyeL{
    width: 35px;
    height: 10%;
    background: transparent;
    position: absolute;
    top: 45%;
    left: 35%;
    border-radius: 50%;
    z-index: 20;
    box-shadow: 0px -10px #474747;
    animation: faceanima 1s linear infinite;
   
}
.eyeR{
    width: 35px;
    height: 10%;
    background: transparent;
    position: absolute;
    top: 45%;
    left: 65%;
    border-radius: 50%;
    z-index: 20;
    box-shadow: 0px -10px #474747; 
    animation: faceanima 1s linear infinite;
}
.mouth{
    width: 35px;
    height: 10%;
    background: transparent;
    position: absolute;
    top: 45%;
    left: 50%;
    border-radius: 50%;
    z-index: 20;
    box-shadow: 0px 10px #474747; 
    animation: faceanima 1s linear infinite;
}
``` 
[x] animation pour le visage
```css
@keyframes faceanima {
    0%
    {
        
        transform: scale(1);
    }
    25%
    {
      
        transform: scale(1);
    }
    30%
    {
        
        transform: scale(1.5);
    }
   
    50%
    {
        
        transform: scale(1.2);
    }
    
    75%
    {
        
        transform: scale(1.5);
    }
    90%
    {
        transform: scale(1);
    }
    
    100%
    {
        
        transform: scale(1);
    }
}
```
>parait a le scale du premier coeur

resultat [mar1n]. c'est le moment de faire rouler votre imagination!!
 
:smile::smile::smile::smile::smile:

