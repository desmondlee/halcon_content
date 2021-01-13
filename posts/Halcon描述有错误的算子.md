---
date: 2021-01-08
title: "Halcon描述有错误的算子"
tags: [
	"官方", "有误"
]
---



## 1. hom_mat2d_translate

定义： ```hom_mat2d_translate( : : HomMat2D, Tx, Ty : HomMat2DTranslate)```

错误：Tx, Ty反了，应该是```hom_mat2d_translate( : : HomMat2D, Ty, Tx : HomMat2DTranslate)```

## 2. affine_trans_point_2d

定义：```affine_trans_point_2d( : : HomMat2D, Px, Py : Qx, Qy)```

错误：Px, Py反了，Qx, Qy反了，应该是```affine_trans_point_2d( : : HomMat2D, Py, Px : Qy, Qx)	```

**综上，Halcon算子中，总是先用y坐标(Row)， 再用x坐标(Column)**