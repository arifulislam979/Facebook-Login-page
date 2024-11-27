# Facebook-Login-page


## 1. Boilerplate HTML Structure
**Explanation:**
* Every HTML document starts with a boilerplate structure:
  * `<!DOCTYPE html>`: Specifies the document type as HTML5.
  * `<html>`: The root element of the document.
  * `<head>`: Contains metadata and links to stylesheets.
  * `<body>`: Contains all visible content and structure.

**Code:**

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Facebook Login</title>
  <link rel="stylesheet" href="styles.css"> <!-- Links the CSS file -->
</head>
<body>
  <!-- Content will go here -->
</body>
</html>
```

---

## 2. Container Div
**Explanation:**
* The container div is a wrapper that contains all the content on the page.
* It uses Flexbox to align its child elements (left-section and right-section) horizontally.
* This structure divides the page into two sections:
  * Left: Facebook logo and tagline.
  * Right: Login form and links.
  
**Code:**

```
<div class="container">
  <!-- Left Section -->
  <div class="left-section">
    <h1>facebook</h1>
    <p>Connect with friends and the world around you on Facebook.</p>
  </div>

  <!-- Right Section -->
  <div class="right-section">
    <div class="login-box">
      <form>
        <input type="text" placeholder="Email or Phone" class="input-box" required>
        <input type="password" placeholder="Password" class="input-box" required>
        <button type="submit" class="login-btn">Log In</button>
        <a href="#" class="forgot-password">Forgotten password?</a>
        <hr>
        <button type="button" class="create-account-btn">Create New Account</button>
      </form>
    </div>
    <p><a href="#" class="create-page">Create a Page</a> for a celebrity, brand or business.</p>
  </div>
</div>
```

CSS Code for `container`:

```
.container {
  display: flex;
  width: 80%;
  max-width: 1100px;
  justify-content: space-between;
  align-items: center;
  margin: auto;
  height: 100vh;
}
```

---

## 3. Left Section
**Explanation:**
*The `left-section` contains:
  * A heading (`h1`) styled with the Facebook blue color.
  * A paragraph (`p`) to display a short description.
* Width: Occupies 50% of the container to maintain balance with the right section.

**Code:**

```
<div class="left-section">
  <h1>facebook</h1>
  <p>Connect with friends and the world around you on Facebook.</p>
</div>
```

CSS Code for `left-section`:

```
.left-section {
  width: 50%;
}

.left-section h1 {
  color: #1877f2;
  font-size: 3rem;
  margin-bottom: 10px;
}

.left-section p {
  font-size: 1.2rem;
  color: #606770;
}
```

---

## 4. Right Section
**Explanation:**
* The `right-section` contains:
  1. **Login Box:**
    * Two input fields for email/phone and password.
    * A "Log In" button styled like Facebook’s login button.
  2. Forgot Password Link:
    * A clickable link for password recovery.
  3. Create New Account Button:
    * A green button for signing up new users.
  4. Create Page Link:
    * A small text link to guide users to create a new page.

**Code:**

```
<div class="right-section">
  <div class="login-box">
    <form>
      <input type="text" placeholder="Email or Phone" class="input-box" required>
      <input type="password" placeholder="Password" class="input-box" required>
      <button type="submit" class="login-btn">Log In</button>
      <a href="#" class="forgot-password">Forgotten password?</a>
      <hr>
      <button type="button" class="create-account-btn">Create New Account</button>
    </form>
  </div>
  <p><a href="#" class="create-page">Create a Page</a> for a celebrity, brand or business.</p>
</div>
```

**CSS Code for** `right-section`:

```
.right-section {
  width: 35%;
}

.login-box {
  background-color: #ffffff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  text-align: center;
}
```

--- 

## 5. Input Fields and Buttons
**Explanation:**
1. Input Fields:
  * Styled to have consistent width, padding, and borders.
  * Placeholder text explains their purpose (e.g., "Email or Phone").
2. Login Button:
  * Styled with Facebook's blue color (#1877f2) and bold text.
  * Changes color slightly on hover for better interactivity.
3. Create Account Button:
  * Styled with a green background (#42b72a) and bold text.
  * Changes color slightly on hover.

**Code:**

```
<input type="text" placeholder="Email or Phone" class="input-box" required>
<input type="password" placeholder="Password" class="input-box" required>
<button type="submit" class="login-btn">Log In</button>
<a href="#" class="forgot-password">Forgotten password?</a>
<hr>
<button type="button" class="create-account-btn">Create New Account</button>
```

CSS Code for Inputs and Buttons:

```
/* Input Fields */
.input-box {
  width: 100%;
  padding: 10px;
  margin-bottom: 15px;
  border: 1px solid #dddfe2;
  border-radius: 5px;
  font-size: 1rem;
}

/* Login Button */
.login-btn {
  width: 100%;
  padding: 10px;
  background-color: #1877f2;
  color: #ffffff;
  font-size: 1rem;
  font-weight: bold;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.login-btn:hover {
  background-color: #165cbb;
}

/* Create Account Button */
.create-account-btn {
  width: 100%;
  padding: 10px;
  background-color: #42b72a;
  color: #ffffff;
  font-size: 1rem;
  font-weight: bold;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.create-account-btn:hover {
  background-color: #36a420;
}
```

---

## 6. Links and Divider
**Explanation**:
1. Forgot Password Link:
  * Styled with a smaller font size and Facebook's blue color.
  * Adds an underline on hover.
2. Create Page Link:
  * Provides additional functionality to guide users.
3. Divider:
  * A thin line (<hr>) separates the login form from the "Create Account" button.

**Code**:

```
<a href="#" class="forgot-password">Forgotten password?</a>
<hr>
<p><a href="#" class="create-page">Create a Page</a> for a celebrity, brand or business.</p>
```

**CSS Code for Links and Divider:**

```
.forgot-password {
  display: block;
  margin: 10px 0;
  font-size: 0.9rem;
  color: #1877f2;
  text-decoration: none;
}

.forgot-password:hover {
  text-decoration: underline;
}

.create-page {
  font-size: 0.9rem;
  color: #1877f2;
  text-decoration: none;
}

.create-page:hover {
  text-decoration: underline;
}

/* Divider Line */
hr {
  margin: 15px 0;
  border: 0;
  height: 1px;
  background-color: #dddfe2;
}
```
---
By following this step-by-step breakdown, you can understand each section of the webpage and how its functionality and appearance are implemented. Let me know if you’d like further clarification or additions!
