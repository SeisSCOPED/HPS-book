o add logos of sponsors at the bottom of each page in your Jupyter Book, you can use custom HTML and CSS. Here’s how you can do it step-by-step:

Add the Sponsor Logos: Place the sponsor logos in the _static directory of your Jupyter Book.

Create a Custom Footer: Add custom HTML for the footer in a file, for example, custom_footer.html.

Include the Custom Footer in Your Book: Update the _config.yml file to include the custom footer.

Style the Footer: Add CSS to style the footer and logos.

# Step 1: Add the Sponsor Logos
Place your sponsor logos in the _static directory of your Jupyter Book. For example, you might have:

```shell
_static/
  sponsor1.png
  sponsor2.png
  sponsor3.png
```
# Step 2: Create a Custom Footer
Create a file named ```custom_footer.html``` in the ```_static directory``` with the following content:
```html
<div class="sponsor-logos">
  <p>Our Sponsors:</p>
  <img src="_static/sponsor1.png" alt="Sponsor 1" class="sponsor-logo">
  <img src="_static/sponsor2.png" alt="Sponsor 2" class="sponsor-logo">
  <img src="_static/sponsor3.png" alt="Sponsor 3" class="sponsor-logo">
</div>
```

# Step 3: Include the Custom Footer in Your Book
Update your ```_config.yml``` file to include the custom footer. Add the following lines under the html section:
```yml
html:
  use_edit_page_button: true
  use_issues_button: true
  use_repository_button: true
  home_page_in_navbar: false
  extra_footer:
    - custom_footer.html
```

# Step 4: Style the Footer
Create a ```custom_styles.css``` file in the ```_static directory``` with the following content to style the footer and logos:
```css
.sponsor-logos {
  text-align: center;
  padding: 20px;
  background-color: #f9f9f9; /* Adjust the background color as needed */
  border-top: 1px solid #ddd; /* Optional: Add a border at the top */
}

.sponsor-logos p {
  font-size: 16px;
  margin-bottom: 10px;
}

.sponsor-logo {
  max-height: 50px; /* Adjust the height as needed */
  margin: 0 10px;
  vertical-align: middle;
}
```
## Update _config.yml to Include the Custom CSS
Add the custom CSS file to the extra_head section in your ```_config.yml``` file:
```yml
html:
  use_edit_page_button: true
  use_issues_button: true
  use_repository_button: true
  home_page_in_navbar: false
  extra_head:
    - <link rel="stylesheet" href="_static/custom_styles.css">
  extra_footer:
    - custom_footer.html
```

## Final _config.yml Excerpt
Here’s how the relevant part of your _config.yml file should look:
```yml 
html:
  use_edit_page_button: true
  use_issues_button: true
  use_repository_button: true
  home_page_in_navbar: false
  extra_head:
    - <link rel="stylesheet" href="_static/custom_styles.css">
  extra_footer:
    - custom_footer.html
```
By following these steps, you will have added sponsor logos at the bottom of each page in your Jupyter Book, styled to match your website's design.