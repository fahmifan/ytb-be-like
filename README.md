# Ytb be Like

This tutorial will try to make a layout for youtube. We will go from mobile layout through desktop layout.

## Part 00

In this part we import the bootstrap grid css and will make the layout without styling, just using some placeholder and bootstrap-grid.

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

- Here we see after class css `row` it follows by class `col`. This is the pattern to use in bootstrap.

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

- Add this css class to the `header`

    ```html
    <header class="bg-red white bold">
    ```

- Then we will styling the navbar too. add this to `custom.css` after `.white{}`

    ```css
    ...
    /* Alignment */
    .center {
        margin: 0 auto !important;
    }

    /* Components */
    .navbar {
        padding-top: 1em;
        padding-bottom: 1em;
    }
    ```

- Add those class to `<nav>`
    
    ```html
    <nav class="navbar row center">
    ```

7. Now your `index.html` should looks something like this 

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta http-equiv="X-UA-Compatible" content="ie=edge">
        <title>Ytb be Like</title>

        <!-- Import css -->
        <link rel="stylesheet" href="assets/bootstrap-4.1.3-dist/css/bootstrap-grid.min.css">
        <link rel="stylesheet" href="assets/custom/custom.css">

    </head>
    <body>
        
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
    </body>
    </html>
    ```
- And your `custom.css`
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

    /* Alignment */
    .center {
        margin: 0 auto !important;
    }

    /* Components */
    .navbar {
        padding-top: 1em;
        padding-bottom: 1em;
    }
    ```

## Part 01
We will make the main feed here. Just collection of video cards
We will using image [placeholder](https://placeholder.com/) for simplicity.

1. We begin with add `<main></main>` tag under `<header>` tag. In the `<main>` tag, add `container` class

    ```html
    ...
    </header>
    
    <!-- Ytb feed -->
    <main class="container">
    </main>
    ```

2. Then we will make a cards componenet for the video list. Add this code to `<main>`. We add class `row` too.

    ```html
    <div class="row">
    </div>
    ```

- This is used for framing the cards

3. The video list in youtube are contains a profile pic, video thumbnail, and some description. Let's add it under the `div` we make it earlier. For simplicity we'll use the placeholder image (you need to connect to internet)

    ```html
    <!-- index.html -->
    <img class="col" src="https://via.placeholder.com/350x150" alt="">

    <div class="row">
        
        <!-- profile pic -->
        <span class="col-2">
            <div class="bg-red profile-pic"></div>
        </span>

        <!-- description -->
        <div class="col-10">
            <p>This is desription of the video</p>
            <small>This is the sub desription of the video</small>
        </div>
    </div>
    ```

- We also need to add css to make the profile pic rounded.

    ```css
    /* Components */
    ...

    .profile-pic {
        border-radius: 200%;
        width: 36px;
        height: 36px;
    }
    ```



## Part 02

## Part 03
We replace the Home, History, and Profile with icons