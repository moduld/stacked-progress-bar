Stacked and not stacked progress bar

Angular 4 and higher. But you can try it on previous versions.

## Installation

```bash
$ npm install stacked-progress-bar
```

## Usage

First need to import `ProgressBarModule` to your module;

```ts
import { ProgressBarModule } from 'stacked-progress-bar';

@NgModule({
  imports: [
    // ...
    ProgressBarModule
  ]
})
```

In your template if you want to use it in horizontal mode

```html
  <stacked-progressbar
          [progressValue]="20"
          [progressColor]="'27a5f9'"
          [position]="'horizontal'"
          [stacked]="true"
          [height]="10"
          [transition]="1"></stacked-progressbar>
```

In your template if you want to use it in vertical mode

```html
<div class="vertical" #container>
  <stacked-progressbar
          [progressValue]="35"
          [progressColor]="'ffbe00'"
          [position]="'vertical'"
          [stacked]="true"
          [width]="10"
          [container]="container"
          [transition]="1"></stacked-progressbar>
</div>
```
- **[progressValue]**: number `0.0` to `100.0`. Value of progress. 

    Will be converted to width in % of container, where progress bar is placed (in horizontal mode).
    Will be converted to height in % of container, where progress bar is placed (in vertical mode).
    Default is `0`;
    
- **[progressColor]**: string. Background color of progress. Default is white.

- **[position]**: string. Position of progress bar `horizontal` or `vertical`. Default is `horizontal`.

- **[stacked]**: boolean. Stacked mode switcher. If `true` - progress bars will place one by one.
    If `false` - progress bars will place next to each other. Default is `true`.
    
- **[height]**: number. If `position` - horizontal, you can set height of progress bar in pixels. 
    By default - progress bar will get 100% of container height.
    
- **[width]**: number. If `position` - vertical, you can set width of progress bar in pixels. 
    By default - progress bar will get 100% of container width.
    
- **[container]**: HTMLElement. If `position` - vertical, you can sent reference to container, where progress bar is placed.
    It will rotate the container to 180 degree.  
    
- **[transition]**: number. Transition of progress bar (in seconds). Default is `0`       
