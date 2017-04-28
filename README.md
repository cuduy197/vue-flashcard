# Vue Flashcard :zap:

![Image flashcard](https://media.giphy.com/media/3og0ICaNlqFKHKlXKo/giphy.gif)
+ This is [on GitHub](https://github.com/cuduy197/vue-flashcard)  so let me know if I've b0rked it somewhere, give me a star :star: if you like it 

### :white_check_mark: Install :ok_hand:
``` npm i vue-flashcard```

### :white_check_mark: Usage :mortar_board:
- Add it to  your component  :tada:

![Usage image](https://media.giphy.com/media/l1BgQGZQxJcXNiwk8/giphy.gif)

```javascript
import vueFlashcard from 'vue-flashcard';

export default {

components : { vueFlashcard }

}
```

### :white_check_mark: Example :four_leaf_clover: 

```html
<vue-flashcard 
front="hello this is a flashcard" 
back="with animation">
</vue-flashcard>
```
### :white_check_mark: :book: Props: 
+ `front` ( Front text) [default: ""]
+ `back` (Back text) [default: ""]

+ `imgFront` (Image front ) [default: ""]
+ `imgBack` (Image back)  [default: ""]

+ `colorFront` (Color front card ) [default: "white"]
+ `colorBack` (Color back card ) [default: "green"]

+ `colorTextFront` (Color text front card ) [default: "black"]
+ `colorTextBack` (Color text back card ) [default: "white"]

+ `textSizeFront` (Text size front card ) [default: "2em"]
+ `textSizeBack` (Text size back card )  [default: "2em"]

+ `headerFront` (header front text ) [default: "Do you know?"]
+ `headerBack` (header back text )  [default: "Answer"]

+ `footerFront` (footer front text  [default: "Click to show Back"]
+ `footerBack=` (footer back text ) [default: "Click to show Front"]


## Make with my old laptop :octocat:  

[![NPM](https://nodei.co/npm/vue-flashcard.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/vue-flashcard/)