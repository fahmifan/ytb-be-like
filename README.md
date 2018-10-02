# Ytb be Like

## Part 00
This tutorial will try to make a layout for youtube. We will go from mobile layout through desktop layout.

## Part 01
In this part we import the bootstrap grid css and will make the layout without styling, just using some placeholder and bootstrap-grid.

- The styling i used is using atom css kind of and per components

1. Import the bootstrap grid css located in `assets/bootstrap-4.1.3-dist/css/bootstrap-grid.min.css`. By adding this code inside the `<head></head>` tag

```html
<link rel="stylesheet" href="assets/bootstrap-4.1.3-dist/css/bootstrap-grid.min.css">
```

2. Then add header tag inside `<body></body>`
```html
<header>
</header>
```

3. Now we will make the container inside the `<header></header>` by adding this code
```html
<div class="container">
</div>
```  

4. Inside the container (the `div`) we will add a navbar. With three nav-items inside it. 

```html
<nav class="row">
    <div class="col">
        Home
    </div>
    <div class="col">
        Profile
    </div>
    <div class="col">
        History
    </div>
</nav>
``` 

5. To make it looks nice we will add some styling. 

- Make a new folder in `assets` folder called `custom`. And in `custom`
 folder make a css file called `custom.css`.
 
-  Open `custom.css` and add the following code

    ```css
    /* Reset */
    * {
        margin: 0;
        padding: 0;
    }

    /* Font */
    * {
    font-family: Arial, Helvetica, sans-serif;  
    }

    .bold {
        font-weight: bold;
    }

    /* Colors */
    .bg-red {
        background: #d32f2f;
    }
    .white {
        color: #fff;
    }
    ``` 

7. Now your code should looks something like this 
```html
<header class="bg-red white bold">
    <div class="container">
        <nav class="navbar row center">

            <div class="col">
                Home
            </div>
            <div class="col">
                Profile
            </div>
            <div class="col">
                History
            </div>

        </nav>
    </div>
</header>
```

## Part 02
We will make the main feed here. Just collection of video cards
We will using image [placeholder](https://placeholder.com/) for simplicity

## Part 03
We replace the Home, History, and Profile with icons