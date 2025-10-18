# HTML/CSS Code Explanations

This document breaks down three different HTML/CSS exercises, explaining the "What, Why, and How" for each.

## Exercise 2: Bootstrap Survey Form

### What is it?
This is an HTML file that creates a survey form. It includes text fields (First Name, Last Name, etc.), radio buttons (How did you hear about us?), checkboxes (Would you like to receive announcements?), and a dropdown menu (Please contact me by:).

### Why was it built this way?
This code uses the **Bootstrap** CSS framework. The "why" is to build a clean, responsive, and professionally styled form **without writing complex custom CSS**. Bootstrap provides pre-made classes for layout (like grids) and form styling, which saves a lot of time.

### How does it work?
1.  **Bootstrap CDN:** The file links to the Bootstrap CSS library via a CDN (Content Delivery Network) in the `<head>`:
    ```html
    <link rel="stylesheet" href="[https://cdn.jsdelivr.net/npm/bootstrap@4.6.2/dist/css/bootstrap.min.css](https://cdn.jsdelivr.net/npm/bootstrap@4.6.2/dist/css/bootstrap.min.css)">
    ```
2.  **Bootstrap Grid System:** It uses `<div class="row">` and `<div class="col">` to automatically align the labels and input fields side-by-side in a two-column grid.
3.  **Bootstrap Form Classes:**
    * `.form-control` is applied to `<input>` tags to make them styled and full-width.
    * `.form-check-inline` and `.form-check-input` are used to style the radio buttons and lay them out horizontally.
    * `.form-check` is used for the stacked checkboxes.
4.  **Custom Styling:** A small `<style>` tag is used to add custom styles not covered by Bootstrap, like setting the logo width and changing the heading colors to `#1e9690`.

<details>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="[https://cdn.jsdelivr.net/npm/bootstrap@4.6.2/dist/css/bootstrap.min.css](https://cdn.jsdelivr.net/npm/bootstrap@4.6.2/dist/css/bootstrap.min.css)">
    <title>Survey Form</title>
    <style>
        body {
            padding: 20px;
        }

        .survey-container img {
            width: 150px; 
            margin-bottom: 15px;
        }

        .survey-container h2 {
            color: #1e9690;
            padding-bottom: 10px;
        }

        .survey-container h3 {
            color: #1e9690; 
            margin-top: 25px;
            margin-bottom: 15px;
        }
    </style>
</head>
<body>
    <div class="survey-container">
        <img src="logo-hcmiu.png" alt="Ho Chi Minh City International University Logo">
        <h2>Survey</h2>
        <p>If you have a moment, we'd appreciate it if you would fill out this survey.</p>
        <form action="" method="post">
            <h3>Your information:</h3>
            <div class="row">
                <div class="col">
                    <label for="fname">First Name:</label>
                </div>
                <div class="col">
                    <input type="text" class="form-control" id="fname" name="first_name">
                </div>
            </div>
            </form>
    </div>
</body>
</html>
