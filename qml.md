# Qml Style and theme
- ققط می توان از یک style استفاده کرد.
- در یک style می توان theme آن را تغییر داد. [Light, Dark]
- برای تغییر style همه فرم ها باید مجددا طراحی شوند.
- با یک style باید UI Kit طراحی شود و از UI Kit استفاده شود.
- اگر از UI Kit استفاده شود، نیازی به طراحی مجدد همه فرم ها برای style جدید نیست و با style جدید فقط باید UI Kit طراحی شود، چون در همه فرم ها از کامپوننت های UI Kit استفاده شده است.
- تغببر UI Kit در Qml به یکی از روش های زیر امکان پذیر است:
- - استفاده از Loader : یک متغییر را چک کند اگر مساوی UI Kit بود کامپوننت آن را لود کند
- - فقط پوشه UI Kit مورد نظر در Resource قرار بگیرد
- - روش دوم بصورت runtime : در لینک دوم زیر 

### Links
- https://wiki.qt.io/Qml_Styling
- https://stackoverflow.com/questions/36335481/dynamically-change-qml-theme-at-runtime

# Kdab Introduction to Qt/Qml
### 37 Layouts
- x, y
- anchors
- positioners 
- - row
- - column
- - grid
- layouts

**implicit vs prefered**
- implicit: Creator component
- prefered: User component

attach properties

layout.aligment: Qt.AlignTop

**Layout vs Positioner**
- Layout: resize child
- Layout: cell aligment
- Layout: target specific x
- Layout: span
- Positioner: don't have any of above


- resize items
- - fill, width, height
- bounderies 
- - [min, max] -> width, height
- - implicit [min, max] -> width, height
- preference تقدم اولویت


### 19 Sizing Components
### 17 Custom Components
### 8 Item Transformations
### 9 Custom Transformations
### 40 Signal or Method
- Function priorites
- Macro
- Functor , Lambda
### 38 to 43
