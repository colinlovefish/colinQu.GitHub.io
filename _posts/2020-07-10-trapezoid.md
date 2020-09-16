---
layout: post
title:  "绘制梯形"
date:   2020-07-15 09:30:51 +0800
categories: [iOS]
pin: true
---
梯形绘制比较简单，主要是定位出四个点，用bezier画线连上即可
```

  func drawTrapezoid(view: UIView, color: UIColor) {
        let finalSize = CGSize.init(width: view.bounds.size.width, height: view.bounds.size.height)
        let layerHeight = finalSize.height
        let layer = CAShapeLayer()
        let bezier = UIBezierPath()
        bezier.move(to: CGPoint.init(x: 0, y: finalSize.height - layerHeight))
        bezier.addLine(to: CGPoint.init(x: 0, y: finalSize.height - 1))
        bezier.addLine(to: CGPoint.init(x: finalSize.width - 15, y: finalSize.height - 1))
        bezier.addLine(to: CGPoint.init(x: finalSize.width , y: finalSize.height - layerHeight))
        bezier.addLine(to: CGPoint.init(x: 0 , y: 0))
        layer.path = bezier.cgPath
        layer.fillColor = color.cgColor
        view.layer.addSublayer(layer)
    }


```