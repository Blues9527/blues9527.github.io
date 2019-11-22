
[参考文档](https://juejin.im/post/5cf868f2e51d45775e33f529)

### 1.基本对齐方式

ConstraintLayout属性 | 注释
---|---
app:layout_constraintBottom_toBottomOf  | 自身底部与目标底部对齐
app:layout_constraintBottom_toTopOf     | 自身底部与目标顶部对齐
app:layout_constraintLeft_toLeftOf      | 自身左部与目标左部对齐
app:layout_constraintLeft_toRightOf     | 自身左部与目标右部对齐
app:layout_constraintRight_toRightOf    | 自身右部与目标右部对齐
app:layout_constraintRight_toLeftOf     | 自身右部与目标左部对齐
app:layout_constraintTop_toTopOf        | 自身顶部与目标顶部对齐
app:layout_constraintTop_toBottomOf     | 自身顶部与目标低部对齐

constraintXXXX：表示自身的某个部分

toXXXOf：表示要对齐目标的某个部分

### 2.偏移量

ConstraintLayout属性 | 注释
---|---
app:layout_constraintHorizontal_bias    | 水平方向偏移量
app:layout_constraintVertical_bias      | 垂直方向偏移量

取值范围在0f-1.0f，0f即代表向左对齐，1.0f表示向右对齐，0.5f表示居中对齐

### 3.margin
margin生效的前提是必须要有对应的约束，比如margin_bottom必须要有constraintBottom_toXXof

### 4.宽高设置

ConstraintLayout属性 | 注释
---|---
app:layout_constraintWidth_default | 约束布局宽
app:layout_constraintHeight_default | 约束布局高

约束布局的宽高模式分为三种：spread，wrap，percent，使用时要将layout_width/layout_height设置为0dp


```
spread：类似于view的match，约束条件下的最大尺寸
wrap：类似于view的wrap，自适应大小，不超过约束条件的最大尺寸
percent：利用百分比来设置空间的宽高，通过app:layout_constraintWidth_percent设置比例大小，0f-1.0f
```

通过app:layout_constraintDimensionRatio可以指定view的宽高比例。可以通过W/H来指定那一边来通过约束条件来确定宽高。如：

```
app:layout_constraintDimensionRatio="W,2:1" 对应的layout_width="0dp"
app:layout_constraintDimensionRatio="H,2:1" 对应的layout_height="0dp"
```
设置最大最小值：
```
app:layout_constraintHeight_min
app:layout_constraintWidth_min
app:layout_constraintHeight_max
app:layout_constraintWidth_max
```
### 5.约束链

```
链式排布
app:layout_constraintHorizontal_chainStyle
app:layout_constraintVertical_chainStyle
上述属性取值：
spread：view之间均匀分布
spread_inside：除了约束链的头部和尾部贴在两边，其余均匀分布
packed：所有view紧贴在一起，默认居中

```

```
设置权重
pp:layout_constraintHorizontal_weight
app:layout_constraintVertical_weight
使用时要将对应的layout_withd/layout_height设置为0dp
```

### 6.圆形布局

ConstraintLayout属性 | 注释
---|---
app:layout_constraintCircle| 圆心
app:layout_constraintCircleRadius | 半径
app:layout_constraintCircleAngle |角度

### 7.Group
### 8.Guideline
### 9.Barrier



