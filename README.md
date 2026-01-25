<!-- ╔══════════════════════════════ BEG ══════════════════════════════╗ -->

<br>
<div align="center">
    <p>
        <img src="./assets/img/logo.png" alt="logo" style="" height="60" />
    </p>
</div>

<div align="center">
    <img src="https://img.shields.io/badge/v-0.2.1-black"/>
    <a href="https://github.com/mineui-org"><img src="https://img.shields.io/badge/🔥-@mineui-black"/></a>
    <br>
    <img src="https://img.shields.io/badge/classes-7000+-blue" alt="Total Classes" />
    <img src="https://img.shields.io/github/issues/mineui-org/utils?style=flat" alt="Github Repo Issues" />
    <img src="https://img.shields.io/github/stars/mineui-org/utils?style=social" alt="GitHub Repo stars" />
</div>
<br>

<!-- ╚═════════════════════════════════════════════════════════════════╝ -->



<!-- ╔══════════════════════════════ DOC ══════════════════════════════╗ -->

- ## Overview 👀

    - #### Why ?
        > Complete utility-first CSS system with 7000+ classes. RTL-first with logical properties, responsive variants, dark mode support, and state variants (hover, focus, active). More comprehensive than Tailwind with better organization.

    - #### When ?
        > Use for rapid UI development with utility classes. Build entire interfaces without writing custom CSS. Perfect for teams who want consistency and speed.

    <br>
    <br>

- ## Quick Start 🔥

    > install [`hmm`](https://github.com/minejs-org/hmm) first.

    ```bash
    # in your terminal
    hmm i @mineui/utils @mineui/tokens @mineui/semantic
    ```

    ```scss
    # in your `.scss` files
    @use "./node_modules/@mineui/utils/dist/scss/index.scss";
    ```

    <div align="center"> <img src="./assets/img/line.png" alt="line" style="display: block; margin-top:20px;margin-bottom:20px;width:500px;"/> </div>
    <br>


    - ### Basic Example

        ```html
        <div class="flex items-center justify-between p-6 bg-surface rounded-lg shadow-md">
          <h2 class="text-2xl font-bold text-1">Title</h2>
          <button class="px-6 py-3 bg-brand text-inverse rounded-md hover:bg-brand-hover transition">
            Click Me
          </button>
        </div>
        ```

    - ### Responsive Example

        ```html
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
          <div class="p-4 bg-surface rounded">Card 1</div>
          <div class="p-4 bg-surface rounded">Card 2</div>
          <div class="p-4 bg-surface rounded">Card 3</div>
        </div>
        ```

    <br>
    <br>

- ## Documentation 📑

    - ### API ⛓️

    - #### Display & Layout

        | Category     | Classes                                                                                                                                                | Use Case                     |
        | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------- |
        | **Display**  | `block`, `inline-block`, `inline`, `flex`, `inline-flex`, `grid`, `inline-grid`, `table`, `table-row`, `table-cell`, `flow-root`, `contents`, `hidden` | Control element display type |
        | **Position** | `static`, `fixed`, `absolute`, `relative`, `sticky`                                                                                                    | Element positioning context  |

        ---

    - #### Spacing (Margin & Padding)

        | Property     | Scale                     | Classes                                                                                         | RTL Support |
        | ------------ | ------------------------- | ----------------------------------------------------------------------------------------------- | ----------- |
        | **Margin**   | 0-64 (0.25rem increments) | `m-{0-64}`, `mx-{0-64}`, `my-{0-64}`, `ms-{0-64}`, `me-{0-64}`, `mt-{0-64}`, `mb-{0-64}`        | ✔️ Logical   |
        | **Negative** | 0-64                      | `-m-{0-64}`, `-mx-{0-64}`, `-my-{0-64}`, `-ms-{0-64}`, `-me-{0-64}`, `-mt-{0-64}`, `-mb-{0-64}` | ✔️ Logical   |
        | **Auto**     | -                         | `m-auto`, `mx-auto`, `my-auto`, `ms-auto`, `me-auto`, `mt-auto`, `mb-auto`                      | ✔️ Logical   |
        | **Padding**  | 0-64 (0.25rem increments) | `p-{0-64}`, `px-{0-64}`, `py-{0-64}`, `ps-{0-64}`, `pe-{0-64}`, `pt-{0-64}`, `pb-{0-64}`        | ✔️ Logical   |

        ---

    - #### Sizing (Width & Height)

        | Type                  | Classes                                                                                                                                    | Notes                 |
        | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | --------------------- |
        | **Width - Full**      | `w-auto`, `w-full`, `w-screen`, `w-min`, `w-max`, `w-fit`                                                                                  | Responsive utilities  |
        | **Width - Fractions** | `w-1/2`, `w-1/3`, `w-2/3`, `w-1/4`, `w-2/4`, `w-3/4`, `w-1/5`, `w-2/5`, `w-3/5`, `w-4/5`, `w-1/6`, `w-5/6`, `w-1/12`                       | Fractional widths     |
        | **Width - Fixed**     | `w-{0,1,2,3,4,6,8,10,12,16,20,24,32,40,48,56,64}`                                                                                          | Token-based values    |
        | **Min/Max Width**     | `min-w-0`, `min-w-full`, `min-w-{min,max,fit}`, `max-w-{none,full,min,max,fit}`, `max-w-{xs-7xl}`, `max-w-prose`                           | Container constraints |
        | **Height**            | `h-auto`, `h-full`, `h-screen`, `h-min`, `h-max`, `h-fit`, `h-1/2`, `h-1/3`, `h-2/3`, `h-1/4`, `h-3/4`, `h-1/5`, `h-2/5`, `h-3/5`, `h-4/5` | Similar to width      |
        | **Size (W+H)**        | `size-{0,1,2,3,4,6,8,10,12,16,20,24,32,40,48,56,64}`, `size-auto`, `size-full`                                                             | Combined sizing       |

        ---

    - #### Flexbox

        | Property        | Classes                                                                                                    | Purpose                |
        | --------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------- |
        | **Direction**   | `flex-row`, `flex-row-reverse`, `flex-col`, `flex-col-reverse`                                             | Child layout direction |
        | **Wrap**        | `flex-wrap`, `flex-wrap-reverse`, `flex-nowrap`                                                            | Content wrapping       |
        | **Basis**       | `basis-0`, `basis-auto`, `basis-full`, `basis-{1,2,3,4,6,8,10,12,16,24,32}`, `basis-{1/2,1/3,2/3,1/4,3/4}` | Flex item base size    |
        | **Grow/Shrink** | `grow`, `grow-0`, `shrink`, `shrink-0`                                                                     | Flex expansion         |
        | **Shorthand**   | `flex-1`, `flex-auto`, `flex-initial`, `flex-none`                                                         | Quick flex settings    |
        | **Justify**     | `justify-{start,end,center,between,around,evenly,stretch}`                                                 | Horizontal alignment   |
        | **Align Items** | `items-{start,end,center,baseline,stretch}`                                                                | Vertical alignment     |
        | **Align Self**  | `self-{auto,start,end,center,stretch,baseline}`                                                            | Individual item align  |
        | **Gap**         | `gap-{0,1,2,3,4,5,6,8,10,12,16,20,24}`, `gap-x-{...}`, `gap-y-{...}`                                       | Space between children |

        ---

    - #### Grid

        | Property         | Classes                                                                | Max Values   |
        | ---------------- | ---------------------------------------------------------------------- | ------------ |
        | **Columns**      | `grid-cols-{1-12}`                                                     | 12 columns   |
        | **Col Span**     | `col-span-{1-12}`, `col-span-full`, `col-auto`                         | 12 span      |
        | **Col Position** | `col-start-{1-13}`, `col-end-{1-13}`, `col-start-auto`, `col-end-auto` | 13 positions |
        | **Rows**         | `grid-rows-{1-6}`                                                      | 6 rows       |
        | **Row Span**     | `row-span-{1-6}`, `row-span-full`, `row-auto`                          | 6 span       |
        | **Row Position** | `row-start-{1-7}`, `row-end-{1-7}`, `row-start-auto`, `row-end-auto`   | 7 positions  |
        | **Flow**         | `grid-flow-{row,col,dense}`, `grid-flow-{row,col}-dense`               | -            |
        | **Auto Sizing**  | `auto-cols-{auto,min,max,fr}`, `auto-rows-{auto,min,max,fr}`           | -            |

        ---

    - #### Typography

        | Category                 | Values             | Classes                                                                       | RTL Safe  |
        | ------------------------ | ------------------ | ----------------------------------------------------------------------------- | --------- |
        | **Font Family**          | Sans, Serif, Mono  | `font-{sans,serif,mono}`                                                      | ✔️         |
        | **Font Size**            | xs-9xl             | `text-{xs,sm,base,md,lg,xl,2xl-9xl}`                                          | ✔️         |
        | **Font Weight**          | thin-black         | `font-{thin,extralight,light,normal,medium,semibold,bold,extrabold,black}`    | ✔️         |
        | **Font Style**           | -                  | `italic`, `not-italic`                                                        | ✔️         |
        | **Line Height**          | 6 preset + numeric | `leading-{none,tight,snug,normal,relaxed,loose,3-10}`                         | ✔️         |
        | **Letter Spacing**       | 6 preset           | `tracking-{tighter,tight,normal,wide,wider,widest}`                           | ✔️         |
        | **Text Alignment**       | 6 directions       | `text-{start,end,left,center,right,justify}`                                  | ✔️ Logical |
        | **Text Color**           | Semantic           | `text-{1,2,3,4,inverse,brand,success,warning,error,info,current,transparent}` | ✔️         |
        | **Decoration**           | -                  | `underline`, `overline`, `line-through`, `no-underline`                       | ✔️         |
        | **Decoration Style**     | 5 types            | `decoration-{solid,double,dotted,dashed,wavy}`                                | ✔️         |
        | **Decoration Thickness** | auto-8px           | `decoration-{auto,from-font,0,1,2,4,8}`                                       | ✔️         |
        | **Transform**            | 4 types            | `uppercase`, `lowercase`, `capitalize`, `normal-case`                         | ✔️         |
        | **Overflow**             | -                  | `truncate`, `text-ellipsis`, `text-clip`                                      | ✔️         |
        | **Wrap**                 | 4 types            | `text-{wrap,nowrap,balance,pretty}`                                           | ✔️         |
        | **Whitespace**           | 6 types            | `whitespace-{normal,nowrap,pre,pre-line,pre-wrap,break-spaces}`               | ✔️         |
        | **Word Break**           | 4 types            | `break-{normal,words,all,keep}`                                               | ✔️         |
        | **Hyphens**              | 3 types            | `hyphens-{none,manual,auto}`                                                  | ✔️         |

        ---

    - #### Backgrounds & Borders

        | Category           | Variants    | Classes                                                                                                                                             |
        | ------------------ | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
        | **Color**          | 11 semantic | `bg-{page,surface,raised,brand,brand-subtle,success,success-subtle,warning,warning-subtle,error,error-subtle,info,info-subtle,current,transparent}` |
        | **Attachment**     | 3 types     | `bg-{fixed,local,scroll}`                                                                                                                           |
        | **Position**       | 9 positions | `bg-{bottom,center,left,left-bottom,left-top,right,right-bottom,right-top,top}`                                                                     |
        | **Repeat**         | 6 types     | `bg-{repeat,no-repeat,repeat-x,repeat-y,repeat-round,repeat-space}`                                                                                 |
        | **Size**           | 3 types     | `bg-{auto,cover,contain}`                                                                                                                           |
        | **Clip**           | 4 types     | `bg-clip-{border,padding,content,text}`                                                                                                             |
        | **Origin**         | 3 types     | `bg-origin-{border,padding,content}`                                                                                                                |
        | **Border Width**   | 5 values    | `border-0`, `border`, `border-2`, `border-4`, `border-8`                                                                                            |
        | **Border Sides**   | 6 logical   | `border-{x,y,s,e,t,b}`                                                                                                                              |
        | **Border Color**   | 8 semantic  | `border-{c1,c2,c3,brand,success,warning,error,current,transparent}`                                                                                 |
        | **Border Style**   | 6 types     | `border-{solid,dashed,dotted,double,groove,ridge,inset,hidden,none}`                                                                                |
        | **Border Radius**  | 9 values    | `rounded-{none,sm,base,md,lg,xl,2xl,3xl,full}`                                                                                                      |
        | **Radius Corners** | Logical     | `rounded-{s,e,t,b}`, `rounded-{ss,se,ee,es}`                                                                                                        |

        ---

    - #### Animations 🎬

        | Category            | Classes                                      | Description          |
        | ------------------- | -------------------------------------------- | -------------------- |
        | **Basic**           | `animate-{none,spin,ping,pulse,bounce}`      | Standard animations  |
        | **Fades**           | `animate-fade-{in,out}`                      | Opacity transitions  |
        | **Slides**          | `animate-slide-in-{up,down,left,right}`      | Directional entrance |
        | **Zooms**           | `animate-zoom-{in,out}`                      | Scale transitions    |
        | **Duration**        | `duration-{75,100,150,200,300,500,700,1000}` | Animation length     |
        | **Delay**           | `delay-{75,100,150,200,300,500,700,1000}`    | Start delay          |
        | **Timing Function** | `ease-{linear,in,out,in-out}`                | Speed curve          |
        | **Fill Mode**       | `fill-{forwards,backwards,both,none}`        | End state behavior   |

        ---

    - #### Effects & Filters

        | Feature                 | Values/Range    | Classes                                                                                                                                                       | Use Case              |
        | ----------------------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------- |
        | **Shadow**              | 8 levels        | `shadow-{none,xs,sm,md,lg,xl,inner}`                                                                                                                          | Depth & elevation     |
        | **Opacity**             | 0-100 (5% step) | `opacity-{0,5,10,20,25,30,40,50,60,70,75,80,90,95,100}`                                                                                                       | Transparency          |
        | **Mix Blend**           | 16 modes        | `mix-blend-{normal,multiply,screen,overlay,darken,lighten,color-dodge,color-burn,hard-light,soft-light,difference,exclusion,hue,saturation,color,luminosity}` | Blend effects         |
        | **Bg Blend**            | 16 modes        | `bg-blend-{...same as above...}`                                                                                                                              | Background blend      |
        | **Blur**                | 8 levels        | `blur-{none,sm,base,md,lg,xl,2xl,3xl}`                                                                                                                        | Blur effect           |
        | **Brightness**          | 11 levels       | `brightness-{0,50,75,90,95,100,105,110,125,150,200}`                                                                                                          | Brightness adjust     |
        | **Contrast**            | 7 levels        | `contrast-{0,50,75,100,125,150,200}`                                                                                                                          | Contrast adjust       |
        | **Grayscale**           | 2 states        | `grayscale-0`, `grayscale`                                                                                                                                    | Desaturate            |
        | **Invert**              | 2 states        | `invert-0`, `invert`                                                                                                                                          | Invert colors         |
        | **Saturate**            | 5 levels        | `saturate-{0,50,100,150,200}`                                                                                                                                 | Color saturation      |
        | **Sepia**               | 2 states        | `sepia-0`, `sepia`                                                                                                                                            | Sepia tone            |
        | **Hue Rotate**          | 6 angles        | `hue-rotate-{0,15,30,60,90,180}`                                                                                                                              | Hue shift             |
        | **Backdrop Blur**       | 6 levels        | `backdrop-blur-{none,sm,base,md,lg,xl}`                                                                                                                       | Frosted glass         |
        | **Backdrop Brightness** | 5 levels        | `backdrop-brightness-{50,75,100,125,150}`                                                                                                                     | Background brightness |
        | **Backdrop Contrast**   | 5 levels        | `backdrop-contrast-{50,75,100,125,150}`                                                                                                                       | Background contrast   |

        ---

    - #### Transforms & Transitions

        | Category       | Values        | Classes                                                                                        |
        | -------------- | ------------- | ---------------------------------------------------------------------------------------------- |
        | **Scale**      | 0.5-1.5       | `scale-{0,50,75,90,95,100,105,110,125,150}`, `scale-{x,y}-{0,50,75,90,95,100,105,110,125,150}` |
        | **Rotate**     | 0-180°        | `rotate-{0,1,2,3,6,12,45,90,180}`, `-rotate-{1,2,3,6,12,45,90,180}`                            |
        | **Translate**  | -100% to 100% | `translate-{x,y}-{0,1,2,3,4,6,8,12,16,1/2,full}`, `-translate-{...}`                           |
        | **Skew**       | 0-12°         | `skew-{x,y}-{0,1,2,3,6,12}`, `-skew-{...}`                                                     |
        | **Origin**     | 9 positions   | `origin-{center,top,top-right,right,bottom-right,bottom,bottom-left,left,top-left}`            |
        | **Transition** | 6 types       | `transition-{none,all,colors,opacity,shadow,transform}`                                        |
        | **Duration**   | 75-700ms      | `duration-{75,100,150,200,300,500,700}`                                                        |
        | **Timing**     | 4 functions   | `ease-{linear,in,out,in-out}`                                                                  |
        | **Delay**      | 75-700ms      | `delay-{75,100,150,200,300,500,700}`                                                           |

        ---

    - #### Layout Utilities

        | Feature             | Classes                                                                                          | RTL Safe  |
        | ------------------- | ------------------------------------------------------------------------------------------------ | --------- |
        | **Inset**           | `inset-{0,auto}`, `inset-{x,y}-{0,auto}`, `start/end/top/bottom-{0,auto,1-16,full}`              | ✔️ Logical |
        | **Float**           | `float-{start,end,left,right,none}`                                                              | ✔️ Logical |
        | **Clear**           | `clear-{start,end,left,right,both,none}`                                                         | ✔️ Logical |
        | **Overflow**        | `overflow-{auto,hidden,clip,visible,scroll}`, `overflow-{x,y}-{auto,hidden,clip,visible,scroll}` | ✔️         |
        | **Overscroll**      | `overscroll-{auto,contain,none}`, `overscroll-{x,y}-{auto,contain,none}`                         | ✔️         |
        | **Scroll**          | `scroll-{auto,smooth}`                                                                           | ✔️         |
        | **Z-Index**         | `z-{0,10,20,30,40,50,60,70,80,90,100,auto}`, `z-{dropdown,sticky,fixed,modal,popover,tooltip}`   | ✔️         |
        | **Visibility**      | `visible`, `invisible`, `collapse`                                                               | ✔️         |
        | **Isolation**       | `isolate`, `isolation-auto`                                                                      | ✔️         |
        | **Object Fit**      | `object-{contain,cover,fill,none,scale-down}`                                                    | ✔️         |
        | **Object Position** | `object-{bottom,center,left,left-bottom,left-top,right,right-bottom,right-top,top}`              | ✔️         |
        | **Aspect Ratio**    | `aspect-{auto,square,video,4-3,21-9,portrait}`                                                   | ✔️         |
        | **Columns**         | `columns-{auto,1,2,3,4}`                                                                         | ✔️         |
        | **Break**           | `break-{before,after,inside}-{auto,avoid,page,column}`                                           | ✔️         |

        ---

    - #### Interactions

        | Category               | Values       | Classes                                                                                    |
        | ---------------------- | ------------ | ------------------------------------------------------------------------------------------ |
        | **Cursor**             | 10 types     | `cursor-{auto,default,pointer,wait,text,move,help,not-allowed,none,grab,grabbing}`         |
        | **Pointer Events**     | 2 states     | `pointer-events-{none,auto}`                                                               |
        | **Resize**             | 4 types      | `resize-{none,both,y,x}`                                                                   |
        | **User Select**        | 4 types      | `select-{none,text,all,auto}`                                                              |
        | **Appearance**         | 2 types      | `appearance-{none,auto}`                                                                   |
        | **Will Change**        | 4 properties | `will-change-{auto,scroll,contents,transform}`                                             |
        | **Content Visibility** | 3 states     | `content-{auto,hidden,visible}`                                                            |
        | **Touch Action**       | 9 actions    | `touch-{auto,none,pan-x,pan-left,pan-right,pan-y,pan-up,pan-down,pinch-zoom,manipulation}` |

        ---

    - #### State Variants

        | State           | Coverage                                                  |
        | --------------- | --------------------------------------------------------- |
        | **Hover**       | Background, Opacity, Scale, Shadow, Translate, Brightness |
        | **Focus**       | Outline, Ring, Scale                                      |
        | **Active**      | Scale, Opacity, Background                                |
        | **Disabled**    | Opacity, Cursor                                           |
        | **Group Hover** | Multiple child effects                                    |
        | **First/Last**  | Margin, Radius                                            |
        | **Odd/Even**    | Background (striped tables)                               |
        | **Placeholder** | Text color, Opacity                                       |
        | **File Input**  | Border, Background, Color                                 |
        | **Peer**        | Sibling state reaction                                    |

        ---

    - #### Responsive Variants

        | Breakpoint | Width  | Prefix   |
        | ---------- | ------ | -------- |
        | Mobile     | 0px    | *(none)* |
        | Tablet     | 640px  | `sm:`    |
        | Medium     | 768px  | `md:`    |
        | Large      | 1024px | `lg:`    |
        | XLarge     | 1280px | `xl:`    |
        | 2XLarge    | 1536px | `2xl:`   |

        > **Responsive Classes Available**: Display, Flexbox, Grid, Width, Text, Spacing, Alignment, and more!

        ---

    - #### Dark Mode & Theme

        | Feature         | Classes                      |
        | --------------- | ---------------------------- |
        | **Dark Mode**   | 20+ utility variants         |
        | **Light Only**  | `dark:hidden`                |
        | **Dark Only**   | `dark:block`                 |
        | **Auto Switch** | Data attribute & system pref |

        ---

    - #### RTL & Accessibility

        | Feature           | Support              |
        | ----------------- | -------------------- |
        | **RTL-Aware**     | ✔️ Logical properties |
        | **Flex Reverse**  | ✔️ Available          |
        | **Icon Flip**     | ✔️ Available          |
        | **Screen Reader** | ✔️ `sr-only` class    |
        | **Skip Link**     | ✔️ Included           |
        | **Focus Visible** | ✔️ Ring support       |

        ---

    - #### Advanced Features

        | Feature               | Classes                                                   | Purpose                                   |
        | --------------------- | --------------------------------------------------------- | ----------------------------------------- |
        | **Container**         | `.container`                                              | Responsive max-width wrapper with padding |
        | **Space Between**     | `space-x-{...}`, `space-y-{...}`                          | Gap between flex/grid children            |
        | **Motion Safe**       | `motion-safe:animate-spin`, `motion-safe:animate-bounce`  | Respect prefers-reduced-motion            |
        | **Print**             | `print:block`, `print:hidden`, `print:flex`, `print:grid` | Print-specific styles                     |
        | **Container Queries** | `sm:grid-cols-2`, `md:grid-cols-3`, `lg:grid-cols-4`      | Modern container-based responsive         |

    <div align="center"> <img src="./assets/img/line.png" alt="line" style="display: block; margin-top:20px;margin-bottom:20px;width:500px;"/> </div>
    <br>

    - ### Categories 📋

        - #### 1. Layout & Display

            ```html
            <!-- Display -->
            <div class="block">Block</div>
            <div class="flex">Flex</div>
            <div class="grid">Grid</div>
            <div class="hidden">Hidden</div>

            <!-- Position -->
            <div class="relative">Relative</div>
            <div class="absolute top-0 start-0">Absolute</div>
            <div class="fixed bottom-4 end-4">Fixed</div>
            <div class="sticky top-0">Sticky</div>
            ```

        - #### 2. Flexbox

            ```html
            <div class="flex flex-col items-center justify-between gap-4">
              <div class="flex-1">Item 1</div>
              <div class="flex-none">Item 2</div>
            </div>
            ```

        - #### 3. Grid

            ```html
            <div class="grid grid-cols-3 gap-4">
              <div class="col-span-2">Wide</div>
              <div>Narrow</div>
            </div>
            ```

        - #### 4. Spacing (RTL-Aware!)

            ```html
            <!-- Padding -->
            <div class="p-4">All sides</div>
            <div class="px-6 py-3">Horizontal & Vertical</div>
            <div class="ps-4 pe-8">Start & End (RTL-aware!)</div>

            <!-- Margin -->
            <div class="m-4">All sides</div>
            <div class="mx-auto">Center</div>
            <div class="ms-4 me-auto">Start & End (RTL-aware!)</div>

            <!-- Negative spacing -->
            <div class="-mt-4">Negative margin</div>
            ```

        - #### 5. Sizing

            ```html
            <!-- Width -->
            <div class="w-full">100%</div>
            <div class="w-1/2">50%</div>
            <div class="w-64">256px</div>

            <!-- Height -->
            <div class="h-screen">100vh</div>
            <div class="h-full">100%</div>

            <!-- Size (w+h together) -->
            <div class="size-16">64x64px</div>
            ```

        - #### 6. Typography

            ```html
            <!-- Font -->
            <p class="font-sans text-base font-normal leading-normal">Text</p>
            <h1 class="text-4xl font-bold">Heading</h1>

            <!-- Alignment (RTL-aware) -->
            <p class="text-start">Aligned to start</p>
            <p class="text-center">Centered</p>

            <!-- Colors (Semantic) -->
            <p class="text-1">Primary text</p>
            <p class="text-brand">Brand color</p>
            ```

        - #### 7. Backgrounds

            ```html
            <div class="bg-surface">Surface</div>
            <div class="bg-brand">Brand color</div>
            <div class="bg-gradient">Gradient</div>
            ```

        - #### 8. Borders (RTL-Aware!)

            ```html
            <!-- Border -->
            <div class="border border-1 rounded-lg">Bordered</div>

            <!-- Sides (RTL-aware) -->
            <div class="border-t border-b">Top & Bottom</div>
            <div class="border-s">Start (left in LTR, right in RTL)</div>

            <!-- Radius -->
            <div class="rounded-full">Circle</div>
            <div class="rounded-t-lg">Top rounded</div>
            ```

        - #### 9. Effects

            ```html
            <!-- Shadow -->
            <div class="shadow-lg">Large shadow</div>

            <!-- Opacity -->
            <div class="opacity-50">50% opacity</div>

            <!-- Filters -->
            <img class="blur-sm grayscale" />
            <div class="backdrop-blur-lg">Backdrop blur</div>
            ```

        - #### 10. Transforms

            ```html
            <!-- Scale -->
            <div class="scale-110">110% size</div>

            <!-- Rotate -->
            <div class="rotate-45">45 degrees</div>

            <!-- Translate -->
            <div class="translate-x-4 translate-y-2">Moved</div>
            ```

    <div align="center"> <img src="./assets/img/line.png" alt="line" style="display: block; margin-top:20px;margin-bottom:20px;width:500px;"/> </div>
    <br>

    - ### Responsive Variants 📱

        > Use `sm:`, `md:`, `lg:`, `xl:`, `2xl:` prefixes for responsive design.

        ```html
        <!-- Hidden on mobile, visible on tablet+ -->
        <div class="hidden md:block">Visible on tablet</div>

        <!-- Responsive grid -->
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
          <div>Item</div>
        </div>

        <!-- Responsive text -->
        <h1 class="text-2xl md:text-4xl lg:text-6xl">Responsive</h1>

        <!-- Responsive spacing -->
        <div class="p-4 md:p-8 lg:p-12">Content</div>
        ```

        **Breakpoints:**
        - `sm`: 640px
        - `md`: 768px
        - `lg`: 1024px
        - `xl`: 1280px
        - `2xl`: 1536px

    - ### State Variants 🎯

        - #### Hover

            ```html
            <button class="bg-brand hover:bg-brand-hover hover:scale-105 transition">
              Hover me
            </button>

            <div class="opacity-50 hover:opacity-100">Fade in</div>
            <img class="hover:scale-110 hover:rotate-3 transition" />
            ```

        - #### Focus

            ```html
            <input class="focus:ring focus:border-brand" />
            <button class="focus:outline-none focus:ring-2">Focus</button>
            ```

        - #### Active

            ```html
            <button class="active:scale-95 active:opacity-80">
              Press me
            </button>
            ```

        - #### Disabled

            ```html
            <button class="disabled:opacity-50 disabled:cursor-not-allowed" disabled>
              Disabled
            </button>
            ```

        - #### Group Hover

            ```html
            <div class="group">
              <img class="group-hover:scale-105 transition" />
              <p class="group-hover:text-brand">Hover parent</p>
            </div>
            ```

    - ### Dark Mode 🌙

        ```html
        <!-- Auto switches with theme -->
        <div class="bg-surface text-1 dark:bg-raised dark:text-2">
          Content adapts to theme
        </div>

        <!-- Show/hide based on theme -->
        <div class="block dark:hidden">Light only</div>
        <div class="hidden dark:block">Dark only</div>
        ```

    - ### RTL Support 🌍

        ```html
        <!-- Automatic with logical properties -->
        <div class="ps-4 pe-8">
          <!-- Padding-left: 16px in LTR -->
          <!-- Padding-right: 16px in RTL -->
        </div>

        <!-- RTL-specific -->
        <div class="rtl:flex-row-reverse">
          Reversed in RTL
        </div>

        <svg class="rtl:rotate-180">
          <!-- Icons flip in RTL -->
        </svg>
        ```

    - ### Container 📦

        ```html
        <div class="container">
          <!-- Responsive max-width with padding -->
          <!-- Centers content automatically -->
        </div>
        ```

    - ### Accessibility ♿

        ```html
        <!-- Screen reader only -->
        <span class="sr-only">For screen readers</span>

        <!-- Skip link -->
        <a href="#main" class="sr-only focus:not-sr-only">
          Skip to main content
        </a>

        <!-- Focus visible -->
        <button class="focus:ring">Keyboard accessible</button>
        ```

    <div align="center"> <img src="./assets/img/line.png" alt="line" style="display: block; margin-top:20px;margin-bottom:20px;width:500px;"/> </div>
    <br>

    - ### Related 🔗

        - ##### [@mineui/tokens](https://github.com/mineui-org/tokens)
            > Design tokens used by utilities

        - ##### [@mineui/semantic](https://github.com/mineui-org/semantic)
            > Semantic variables for theming

        - ##### [@mineui/reset](https://github.com/mineui-org/reset)
            > CSS reset to use with utilities

<!-- ╚═════════════════════════════════════════════════════════════════╝ -->



<!-- ╔══════════════════════════════ END ══════════════════════════════╗ -->

<br>
<br>

---

<div align="center">
    <a href="https://github.com/maysara-elshewehy"><img src="https://img.shields.io/badge/by-Maysara-black"/></a>
</div>

<!-- ╚═════════════════════════════════════════════════════════════════╝ -->