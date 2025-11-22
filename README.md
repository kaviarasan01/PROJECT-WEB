# Project Responsive Web Design using Bootstrap
## Date: 18/11/25

## AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.


## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Design a navigation bar with links: Inspiration, Find Work, Learn Design, Go Pro, Sign In, Sign Up.

### Step 5:
Add a catchy headline with a search bar.

### Step 6:
Use ```<div>``` containers for each dribbble shot thumbnail.

### Step 7:
Include designer name and likes count below each image.

### Step 8:
Include text like “Find your next design inspiration” with a button (“Join Dribbble” or “Explore”).

### Step 9:
Create a footer with your name and register number.

### Step 10:
Publish the website in the LocalHost.

## PROGRAM :
index.html
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <meta name="description" content="" />
    <meta
      name="author"
      content="Mark Otto, Jacob Thornton, and Bootstrap contributors"
    />
    <meta name="generator" content="Astro v5.13.2" />
    <title>Lounge Restaurant</title>
    <link
      rel="canonical"
      href="https://getbootstrap.com/docs/5.3/examples/product/"
    />
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/js/bootstrap.bundle.min.js" integrity="sha384-FKyoEForCGlyvwx9Hj09JcYn3nv7wiPVlz7YYwJrWVcXK/BmnVDxM+D2scQbITxI" crossorigin="anonymous"></script>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-sRIl4kxILFvY47J16cr9ZwB07vP4J8+LH7qKQnuqkuIAvNWLzeN8tE5YBujZqJLB" crossorigin="anonymous">
    <meta name="theme-color" content="#712cf9" />
    <link href="styles.css" rel="stylesheet" />
    <style>
      .bd-placeholder-img {
        font-size: 1.125rem;
        text-anchor: middle;
        -webkit-user-select: none;
        -moz-user-select: none;
        user-select: none;
      }
      @media (min-width: 768px) {
        .bd-placeholder-img-lg {
          font-size: 3.5rem;
        }
      }
      .b-example-divider {
        width: 100%;
        height: 3rem;
        background-color: #0000001a;
        border: solid rgba(0, 0, 0, 0.15);
        border-width: 1px 0;
        box-shadow:
          inset 0 0.5em 1.5em #0000001a,
          inset 0 0.125em 0.5em #00000026;
      }
      .b-example-vr {
        flex-shrink: 0;
        width: 1.5rem;
        height: 100vh;
      }
      .bi {
        vertical-align: -0.125em;
        fill: currentColor;
      }
      .nav-scroller {
        position: relative;
        z-index: 2;
        height: 2.75rem;
        overflow-y: hidden;
      }
      .nav-scroller .nav {
        display: flex;
        flex-wrap: nowrap;
        padding-bottom: 1rem;
        margin-top: -1px;
        overflow-x: auto;
        text-align: center;
        white-space: nowrap;
        -webkit-overflow-scrolling: touch;
      }
      .btn-bd-primary {
        --bd-violet-bg: #712cf9;
        --bd-violet-rgb: 112.520718, 44.062154, 249.437846;
        --bs-btn-font-weight: 600;
        --bs-btn-color: var(--bs-white);
        --bs-btn-bg: var(--bd-violet-bg);
        --bs-btn-border-color: var(--bd-violet-bg);
        --bs-btn-hover-color: var(--bs-white);
        --bs-btn-hover-bg: #6528e0;
        --bs-btn-hover-border-color: #6528e0;
        --bs-btn-focus-shadow-rgb: var(--bd-violet-rgb);
        --bs-btn-active-color: var(--bs-btn-hover-color);
        --bs-btn-active-bg: #5a23c8;
        --bs-btn-active-border-color: #5a23c8;
      }
    </style>
  </head>
  <body>
    <svg xmlns="http://www.w3.org/2000/svg" class="d-none">
      <symbol id="check2" viewBox="0 0 16 16">
        <path
          d="M13.854 3.646a.5.5 0 0 1 0 .708l-7 7a.5.5 0 0 1-.708 0l-3.5-3.5a.5.5 0 1 1 .708-.708L6.5 10.293l6.646-6.647a.5.5 0 0 1 .708 0z"
        ></path>
      </symbol>
      <symbol
        id="aperture"
        fill="none"
        stroke="currentColor"
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        viewBox="0 0 24 24"
      >
        <circle cx="12" cy="12" r="10"></circle>
        <path
          d="M14.31 8l5.74 9.94M9.69 8h11.48M7.38 12l5.74-9.94M9.69 16L3.95 6.06M14.31 16H2.83m13.79-4l-5.74 9.94"
        ></path>
      </symbol>
      <symbol id="cart" viewBox="0 0 16 16">
        <path
          d="M0 1.5A.5.5 0 0 1 .5 1H2a.5.5 0 0 1 .485.379L2.89 3H14.5a.5.5 0 0 1 .49.598l-1 5a.5.5 0 0 1-.465.401l-9.397.472L4.415 11H13a.5.5 0 0 1 0 1H4a.5.5 0 0 1-.491-.408L2.01 3.607 1.61 2H.5a.5.5 0 0 1-.5-.5zM3.102 4l.84 4.479 9.144-.459L13.89 4H3.102zM5 12a2 2 0 1 0 0 4 2 2 0 0 0 0-4zm7 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4zm-7 1a1 1 0 1 1 0 2 1 1 0 0 1 0-2zm7 0a1 1 0 1 1 0 2 1 1 0 0 1 0-2z"
        ></path>
      </symbol>
      <symbol id="chevron-right" viewBox="0 0 16 16">
        <path
          fill-rule="evenodd"
          d="M4.646 1.646a.5.5 0 0 1 .708 0l6 6a.5.5 0 0 1 0 .708l-6 6a.5.5 0 0 1-.708-.708L10.293 8 4.646 2.354a.5.5 0 0 1 0-.708z"
        ></path>
      </symbol>
    </svg>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <div class="container-fluid">
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav mx-auto">
            <li class="nav-item">
              <a class="nav-link active px-4" aria-current="page" href="#">Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link px-4" href="menu/index.html">Menu</a>
            </li>
            <li class="nav-item">
              <a class="nav-link px-4" href="about.html">About</a>
            </li>
            <li class="nav-item">
              <a class="nav-link px-4" href="contact.html">Contact Us</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <main class="content">
      <div
        class="hero-section position-rela tive overflow-hidden text-center text-white"
        style="background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('menu.png') center/cover; min-height: 600px; display: flex; align-items: center; justify-content: center;"
      >
        <div class="container">
          <div class="col-lg-8 mx-auto p-4">
            <h1 class="display-2 fw-bold mb-4">30% Off This Weekend</h1>
            <h3 class="fw-normal mb-5" style="color: #e0e0e0;">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec mattis.
            </h3>
            <div class="d-flex gap-3 justify-content-center flex-wrap">
              <a class="btn btn-outline-light btn-lg px-4" href="menu/index.html">
                See our new menu
              </a>
              <a class="btn btn-light btn-lg px-4" href="#">
                Book your table now
              </a>
            </div>
          </div>
        </div>
      </div>
      
      <div class="container my-5">
        <div class="row g-4">
          <div class="col-md-4">
            <div class="card h-100 shadow-sm">
              <img src="menu.png" class="card-img-top" alt="Grilled skewers" />
              <div class="card-body text-center">
                <h3 class="card-title">Our New Menu</h3>
                <p class="card-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec mattis.</p>
                <a href="menu/index.html" class="btn btn-primary">See our new menu</a>
              </div>
            </div>
          </div>
          <div class="col-md-4">
            <div class="card h-100 shadow-sm">
              <img src="table.png" class="card-img-top" alt="Table setting" />
              <div class="card-body text-center">
                <h3 class="card-title">Book a table</h3>
                <p class="card-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec mattis.</p>
                <a href="#" class="btn btn-primary">Book your table now</a>
              </div>
            </div>
          </div>
          <div class="col-md-4">
            <div class="card h-100 shadow-sm">
              <img src="chef.png" class="card-img-top" alt="Chef preparing food" />
              <div class="card-body text-center">
                <h3 class="card-title">Opening Hours</h3>
                <p class="card-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec mattis.</p>
                <ul class="list-unstyled mt-3">
                  <li>Mon - Fri: 7am - 10pm</li>
                  <li>Sat: 9am - 11pm</li>
                  <li>Sun: 2pm - 9pm</li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </main>
    <footer class="bg-dark text-white text-center py-4 mt-5">
      <div class="container">
        <p class="mb-0">Designed and Developed by <span class="text-info">Kaviyarasan Ranganathan</span></p>
      </div>
    </footer>
    <script
      src="../assets/dist/js/bootstrap.bundle.min.js"
      class="astro-vvvwv3sm"
    ></script>
  </body>
</html>
```

styles.css
```css
                * {
                margin: 0;
                padding: 0;
                box-sizing: border-box;
                }

                body,h1 {
                font-family: 'Segoe UI', sans-serif;
                background-color: #fff8f0;
                color: #333;
                }

                header {
                background-color: #2e2e2e;
                color: white;
                padding: 1rem 2rem;
                display: flex;
                justify-content: space-between;
                align-items: center;
                }

                .logo {
                font-size: 1.5rem;
                font-weight: bold;
                }

                nav ul {
                list-style: none;
                display: flex;
                gap: 1.5rem;
                }

                nav a {
                color: white;
                text-decoration: none;
                font-weight: 500;
                }

                .banner {
                background: url('pasta.jpg') center/cover no-repeat;
                color: white;
                padding: 4rem 2rem;
                text-align: center;
                }

                .banner-text {
                background-color: rgba(0, 0, 0, 0.6);
                display: inline-block;
                padding: 1rem 2rem;
                border-radius: 8px;
                }

                .content {
                display: flex;
                justify-content: space-around;
                padding: 2rem;
                gap: 2rem;
                flex-wrap: wrap;
                }

                .card {
                background-color: white;
                padding: 1rem;
                border-radius: 10px;
                box-shadow: 0 0 10px rgba(0,0,0,0.1);
                width: 300px;
                text-align: center;
                }

                .card img {
                width: 100%;
                border-radius: 8px;
                }

                .card h3 {
                margin: 1rem 0 0.5rem;
                }

                .card p {
                font-size: 0.9rem;
                margin-bottom: 1rem;
                }

                .card a {
                color: #007b5e;
                text-decoration: none;
                font-weight: bold;
                }

                .hours {
                list-style: none;
                padding: 0.5rem 0;
                font-size: 0.9rem;
                }

                html, body {
        height: 100%;
        margin: 0;
        display: flex;
        flex-direction: column;
        }

        .wrapper {
        flex: 1;
        }

        /* Footer stays at bottom */
        footer {
        text-align: center;
        padding: 1rem;
        background-color: #f0f0f0;
        font-size: 0.9rem;
        }

        footer span {
        color: red;
        font-weight: bold;
        }

        .contact-section {
        background-color: #fff8f0;
        padding: 2rem;
        max-width: 600px;
        margin: 2rem auto;
        border-radius: 10px;
        box-shadow: 0 0 10px rgba(0,0,0,0.1);
        text-align: center;
        }

        .contact-section h2 {
        font-size: 1.8rem;
        color: #3e5e52;
        margin-bottom: 1rem;
        }

        .contact-section p {
        font-size: 1rem;
        color: #333;
        margin: 0.5rem 0;
        }

        .contact-section h3 {
        font-size: 1.2rem;
        color: #007b5e;
        margin-top: 1.5rem;
        }

```


## OUTPUT:
<img width="1910" height="522" alt="image" src="https://github.com/user-attachments/assets/32bfc610-9685-453b-a3e0-bd8743c18af5" />



## RESULT:
The project for responsive web design in creating a clone of dribble.com is completed successfully.
