<div align="center">

## Draw a moving starfield on a form


</div>

### Description

It draws a moving starfield on a form with simple VB graphics methods and a timer control.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Theo Kandiliotis](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/theo-kandiliotis.md)
**Level**          |Unknown
**User Rating**    |6.0 (604 globes from 101 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Games](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/games__1-38.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/theo-kandiliotis-draw-a-moving-starfield-on-a-form__1-906/archive/master.zip)





### Source Code

```
How to draw a moving starfield
This example shows how to design a moving star field ,the standard animated background used in most space shoot'em up games.You know,the one that asteroids of all kinds of sizes zip by with various speeds,creating a 3D effect.Here we go:
1.Create a Timer control. 2.Make these settings through the Properties Window:
Form1.WindowStart = 2
Form1.Backcolor = &H00000000& (that's black)
Timer1.Interval = 1
3.The algorythm is kinda complicated to explain in spoken words,so I'll leave it up to you to figer out what's going on.
Dim X(50), Y(50), pace(50), size(50) As Integer
Private Sub Form_Activate()
Randomize
For I = 1 To 50
x1 = Int(Form1.Width * Rnd)
y1 = Int(Form1.Height * Rnd)
pace1 = Int(500 - (Int(Rnd * 499)))
size1 = 16 * Rnd
X(I) = x1
Y(I) = y1
pace(I) = pace1
size(I) = size1
Next
End Sub
Private Sub Timer1_Timer()
For I = 1 To 50
Circle (X(I), Y(I)), size(I), BackColor
Y(I) = Y(I) + pace(I)
If Y(I) >= Form1.Height Then Y(I) = 0: X(I) = Int(Form1.Width * Rnd)
Circle (X(I), Y(I)), size(I)
Next
End Sub
```

