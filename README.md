# devin-ui

#### Installation
```
npm install devin-ui
```
#### Usage
##### 1. import all components
```javascript
import DevinUi from '../dist/devin-ui'
Vue.use(VueRouter)
```

##### 2. the usage of transition-box
```javascript
        <transition-box ref="transitionBox" :navList='navList' @tap="switchNav" :isfull="true"
        :banner="true" :showBoxHeight="400" :fixBox="true" :fixWidth="0" >
            <template slot="fix_box">
                <div class="box" style="background-color:blue">
                fix block
                </div>
            </template>
            <template slot-scope="row" :slot="item.name" v-for="item in navList">
                <div  class="box">
                    {{row}}
                </div>
            </template>
        </transition-box>
        <p>Curent Index:{{swiperIndex}}</p>
        <button @click="start">start loading</button>
        <button @click="close">close loading</button>

        <button @click="prev">prev</button>
        <button @click="next">next</button>
```
![](https://github.com/Rise-Devin/devin-ui/blob/master/demo/assets/box1.gif?raw=true)

##### The attributes of <transition-box>(<transition-box>标签的属性)
属性名(attribute name) | 属性值(value) | 类型(type) | demo
-------- | -------------------------- | ------- | --------
navList | 控制tab切换(your data of Tab button) | array | [{name:'name1',class:'fa fa-list-alt'}]   
navdisabled | 是否需要允许点击tab进行切换(whether can switch throuth click the tab) |boolean | true
isfull | 是否填满nav ( whether to fill the nav) | boolean | true
banner | 是否需要banner (whether need banner) |boolean | true
isremove | 是否需要remove该元素 (whether need to remove the element) |boolean | true
removeClass | 移除按键样式(the css of btn ) |string | glyphicon glyphicon-remove
fixBox | 是否需要固定block (whether need to fix block) |boolean | true
fixWidth | 固定block的宽度(the width of fixed block) |boolean | true
loadingColor | the background color of loading block |string | #f6f7f8


##### The event




