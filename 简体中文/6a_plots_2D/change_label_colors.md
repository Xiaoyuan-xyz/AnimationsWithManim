# 在 `GraphScene` 中更改标签的颜色

在`CONFIG`字典中加入：
```python
    "x_label_color":RED,
    "y_label_color":BLUE
```
并在 `setup_axes` 方法中将：
```python
            x_label = TextMobject(self.x_axis_label)
            # 和
            y_label = TextMobject(self.y_axis_label)
```
改为：
```python
            x_label = TextMobject(self.x_axis_label,color=self.x_label_color)
            # 和
            y_label = TextMobject(self.x_axis_label,color=self.y_label_color)
```
效果：

<p align="center"><img src ="/English/6a_plots_2D/gifs/ChanceColorLabels.png" /></p>
