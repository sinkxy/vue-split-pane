# Vue Split Pane

Split-Pane component built with vue2.0, can be split vertically or horizontally,and change the size dynamically.


### How to use?
```bash
npm install vue-splitpane

#import
import splitPane from 'vue-splitpane'

# use as global component
Vue.component('split-pane', splitPane);
```

### Example

```html
   <split-pane @resize="resize" :set-percent="value" :min-percent='20' :default-percent='30' split="vertical">
      <template slot="paneL">
        A
      </template>
      <template slot="paneR">
        B
      </template>
    </split-pane>
```

```html
  //nested
   <split-pane @resize="resize" :set-percent="value" :min-percent='20' :default-percent='30' split="vertical">
      <template slot="paneL">
        A
      </template>
      <template slot="paneR">
        <split-pane split="horizontal">
          <template slot="paneL">
           B
          </template>
          <template slot="paneR">
            C
          </template>
        </split-pane>
      </template>
    </split-pane>
```

### Options
|    Property    |    Description   |   type   |	default	|
| -----------------  | ---------------- | :--------: | :----------: |
| split       | the split type |String [horizontal,vertical] |must choose one type |
| min-percent         | paneL min-percent           |Number | 10 |
| max-percent         | paneL max-percent           |Number | 90 |
| set-percent         | dynamic change paneL value  |Number | 10 |

