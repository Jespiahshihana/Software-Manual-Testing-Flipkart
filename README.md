# FLIPKART APPLICATION TESTING
> This is an ongoing manual testing project for Flipkart's e-commerce 
> platform. Modules covered so far: Authentication, Login, Product Search, 
> Cart, and Checkout.


## USER STORIES

### USER STORY 1: App Launch
  As a user, I want to open the application to buy products.

Acceptance Criteria:
  App should be installed
  The application should open the correct application
  App should open without crash
  App should load within acceptable time (eg: 2 to 5 seconds)
  App should work after reinstall

QA Test Scenarios:
  Verify the app is launched
  Verify the app launch time
  Verify the app behaviour while network on/off
  Verify the app after reinstall
  Verify the app launch after force close
  Verify the app by notification launch
  Verify the app after update

### USER STORY 2: Splash Screen
As a user, I want to see the splash screen, so that I know the app is loading.

Acceptance Criteria: 
  Splash screen should appear on app launch
  Splash screen should display the logo correctly
  Splash screen should navigate to home page
  Splash screen duration should be within acceptable time
  No freezing or blank screen

QA Test Scenarios:
  Verify the splash screen is appeared
  Verify the duration of splash screen
  Verify no freezing or blank screen
  Verify the navigation after splash screen
  Verify splash screen don’t repeat after opening the app after minimizing the screen 
  Verify the behaviour while on/off of the internet

### USER STORY 3: User Registration 
As a new user, I want to register for the flipkart application, so that I can create an application for shopping.

Acceptance Criteria:
  User can enter email/mobile number
  User enter OTP
  Account should created successfully

QA Test Scenarios
  Register valid details
  Register invalid OTP
  Register valid OTP
  Register with empty fields


### USER STORY 4: User Login
As a registered user, I want to login into the flipkart account.

Acceptance Criteria: 
  User enter email/phone
  User enter password
  Login with valid credentials works
  Login with invalid credentials shows error
  OTP login option works
  Forget password option works
  Submit button works

QA Test Scenarios: 
  Login with invalid credentials
  Login with valid credentials
  Login with empty fields 

### USER STORY 5: Home page
As a registered user, I want to navigate to the home page so that I can search for products or categories.

Acceptance Criteria:
  User should be redirected to home page after login
  Home page should loaded within acceptable duration
  Categories and images should be loaded within acceptable duration
  Search bar should be displayed
  Play, Categories, Account, Cart icons should be displayed
  Display the details within accepted duration after reload
  Banners should be displayed properly
  Specific category icon should be displayed

QA Test Scenario:
  Verify the user is redirected to the home page after login
  Verify the loading duration of the home page
  Verify if the categories and images are loaded within acceptable duration
  Verify the product listing
  Verify the search bar is displayed
  Verify session handling
  Verify responsive behaviour
  Verify the Play, Categories, Account, Cart icons are displayed
  Verify the banners are displayed correctly
  Verify the UI elements of the home page
  Verify the navigation functionality 
  Verify the behaviour of the home page while on/off the network.

### USER STORY 6: Product Search
As a user, I need to search the product so that I can find the items quickly.
Acceptance Criteria:
  Search bar accepts input field
  Shows relevant suggestions while typing
  Show relevant result
QA Test Scenarios:
  Search valid product
  Search invalid or random text
  Auto suggestions are shown

### USER STORY 7: Add to Cart	
  As a user, I want to add products to the cart, so that I can purchase them later.
  
Acceptance Criteria:
  Product added successfully message should display
  Cart count updates
  Cart can remove items
  
QA Test Scenarios:
  Add a product to the cart
  Add multiple products
  Remove the product from the cart
  Check the cart count updates

### USER STORY 8: Place Order
  As a user, I place an order to check if the product is successfully placed.
  
Acceptance Criteria:
  User select product
  User select address
  User choose payment option
  Order success message shows
  
QA Test Scenarios:
  Place an order with address and check the option to change the address
  Place order with COD
  Place order with UPI or online payment
  Check if the payment option changes
  Cancel order

## TEST PLAN

### OBJECTIVE
  The objective of the test plan is to verify the functionalities of the Flipkart application such as user registration, user login, product search, add to cart and order placement. The goal is to ensure the application works correctly and provides smooth user experience. 

### SCOPE
  #### Included:
    1.User Registration
    2.Login
    3.Product Search
    4.Add to Cart
    5.Place order
  #### Excluded:
    1.Backend or API
    2.Internal Process of Payment Gateway
    3.Security Test

### TEST TYPES
	Functional Testing
	UI Testing
	Usability Testing

### TEST APPROACH
	Manual testing will be performed in the Flipkart mobile application.
	Test cases will be created based on the user scenario and executed step by step.
	Any deviations from expected results will be identified as bug and documented. 

### RISKS AND ASSUMPTIONS
	Risks:
    Network issues may affect testing
    Payment failures 
	Assumptions:
    Application is stable
    Test environment is properly setup


## TEST SCENARIOS AND TEST CASES

| TEST ID | TEST SCENERIO                                     | TEST DESCRIPTION                                                                    | PRECONDITIONS                                                                                                                          | TEST STEPS                                                                                         | EXPECTED RESULT                                                                         | ACTUAL RESULT                                                                             | STATUS |
| ------- | ------------------------------------------------- | ----------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ------ |
| TC_01   | User Registration                                 | Verify the registration of new user                                                 | App installed and user should not already be registred                                                                                 | 1. Click the app icon and open the app. 2. Click create account                                    | Account created successfully                                                            | Account created successfully                                                              | Pass   |
| TC_02   | User Login with valid credentials                 | Verify the user login with valid credentials                                        | App installed and user registration is success                                                                                         | 1. Click login button 2. Login with valid email and password.                                      | User should login successfully                                                          | User logged in successfully                                                               | Pass   |
| TC_03   | User Login with invalid credentials               | Verify the user login with invalid credentials                                      | App installed and user registration is success                                                                                         | 1. Click login button 2. Login with invalid email or invalid password.                             | Should show the error message                                                           | Error message is shown                                                                    | Pass   |
| TC_04   | Product Search with valid input                   | Verify the search with valid input which shows relevant results                     | User is on Flipkart home page with active internet connection                                                                          | 1. Click the search bar 2. Enter the valid input and search                                        | Should show the relevant results of the product                                         | Relevant result of the product is shown                                                   | Pass   |
| TC_05   | Product Search with invalid input                 | Verify the search with invalid input or random text                                 | User is on Flipkart home page with active internet connection                                                                          | 1. Click the search bar 2. Enter the invalid input or random text and search                       | Should show relevant suggestions or products if possible or “no result”                 | “No Results Found” message with product suggestions related to the input                  | Pass   |
| TC_06   | Add Product to Cart                               | Verify the item is added to cart and cart count is updated                          | User should be logged in and product should be available                                                                               | 1. Choose a product 2. Click add to cart button 3. Cart count is updated                           | Shows “item added to cart” message and display product in cart with updated cart count. | Showed “item added to cart” message and displayed product in cart with updated cart count | Pass   |
| TC_07   | Remove product from cart                          | Verify the item is removed from the cart and cart count is updated                  | User should be logged in and cart should contain at least one product                                                                  | 1. Click remove product option in my cart page 2. Item removed                                     | Shows “item removed from cart” message and update the cart count                        | Showed “item removed from cart” message and updated the cart count                        | Pass   |
| TC_08   | Place order with COD payment option               | Verify the order placement with the COD payment option available for the product    | User should be logged in. Product added to cart. Delivery address should be available. COD option should be available for the product. | 1. Click place order button 2. Give valid address 3. Choose COD option for payment 4. Order placed | Shows “order placed successfully” message with order summary                            | Showed “order placed successfully” message with order summary                             | Pass   |
| TC_09   | Place order with online payment option (cash/UPI) | Verify the order placement with the online payment option available for the product | User should be logged in. Product added to cart. Valid payment method available for the product (Card or UPI)                          | 1. Click place order button 2. Give valid address 3. Choose online payment option 4. Order placed  | Shows “order placed successfully” message with order summary                            | Showed “order placed successfully” message with order summary                             | Pass   |
| TC_10   | Cancel Order                                      | Verify the product can be cancelled after placing the order.                        | User should be logged in. User should have at least one placed order. Order status should allow cancellation.                          | 1. Click cancel order option 2. Order cancelled                                                    | Order cancelled and shows “order cancelled” message if not shipped.                     | Order cancelled and showed “order cancelled” message                                      | Pass   |


	
## BUG IDENTIFICATION	

	
### BUG 1: Wishlist back navigation delay
P1 (High)
Description: Delay while navigating back from wishlist collection 
Impact: Navigation delay + decrease user experience 
Severity: P1(high)
Priority: Highest (must fix immediately)

### BUG 2: Review Page Back Navigation Issue 
P1(High)
Description: Back navigation stuck after submitting review 
Impact: Navigation delay + decrease user experience
Severity: P1(high)
Priority: Highest (must fix immediately)

### BUG 3: Order Success Page Back Issue (P0) 
P0(Critical)
Description: Unable to navigate back from order success page 
Impact:  Navigation block + user frustration 
Severity: P0(critical)
Priority: Highest (must fix immediately)

### BUG 4: Slow Loading of Product Images 
P1(High)
Description:Product images take time to load 
Impact: Slow UI + Engagement Drop 
Severity: P1(high)
Priority: Highest (must fix immediately)


## BUG REPORTING

### BUG 1: ORDERS BACK NAVIGATION DELAY

TITLE/SUMMARY
  Delay while navigating back from Orders page 
STEPS TO REPRODUCE:
  Open Flipkart app
  Go to orders section
  Tap on any product
  Press back button
EXPECTED VS ACTUAL RESULT 
	Expected: Instant navigation back to Orders or home page
  Actual: Delay observed while navigating back
SEVERITY JUSTIFICATION
  Navigation delay affects user experience
  Impacts smooth browsing experience
  Can cause user frustration during shopping journey

SCREENSHOT

<img width="720" height="1612" alt="order back page delay image" src="https://github.com/user-attachments/assets/7821f35d-778e-4e34-a7d2-3a5988476eff" />


### BUG 2: REVIEW PAGE BACK NAVIGATION ISSUE

TITLE
  Back navigation stuck after submitting review 
STEPS TO REPRODUCE:
  Open product page
  Submit a review
  Try to navigate back
EXPECTED VS ACTUAL RESULT 
	Expected: User should return to home page or product page 
  Actual: Back navigation is stuck or delayed 
SEVERITY JUSTIFICATION
  Impacts trust and usability of review feature
  Reduces user interaction with ratings system

SCREENSHOT

<img width="714" height="1599" alt="REVIEW PAGE BACK NAVIGATION ISSUE" src="https://github.com/user-attachments/assets/34825331-ed5b-40c6-afcb-ae58ee93ad13" />



### BUG 3: ORDER SUCCESS PAGE BACK ISSUE

TITLE
  Unable to navigate back from Order Success page 
STEPS TO REPRODUCE:
  Place an order
  Reach order success page
  Swipe back or press back button
EXPECTED VS ACTUAL RESULT 
  Expected: Navigate back to home page 
  Actual: User remains stuck unless clicking “Continue Shopping” 
SEVERITY JUSTIFICATION
  Breaks standard mobile back gesture behavior
  High risk of user drop-off after purchase

SCREENSHOT

<img width="540" height="1077" alt="ORDER SUCCESS PAGE BACK ISSUE" src="https://github.com/user-attachments/assets/ca1958cb-c7cb-4157-9a5a-1f3219a8dba5" />


### BUG 4: SLOW LOADING OF PRODUCT IMAGES

TITLE
  Product images load slowly in product page 
STEPS TO REPRODUCE:
  Open Flipkart app
  Search product
  Open any product
Scroll through product images
EXPECTED VS ACTUAL RESULT 
	Expected: Images load instantly or preload smoothly 
  Actual: Images take time or appear blank initially
SEVERITY JUSTIFICATION
  Affects shopping experience
  Reduces engagement 

SCREENSHOT
	
<img width="714" height="1599" alt="SLOW LOADING OF PRODUCT IMAGES" src="https://github.com/user-attachments/assets/5b416124-bd66-4b10-a762-493b217cab94" />





## PRODUCT IMPROVEMENT 

### 1. IMPROVE BACK NAVIGATION EXPERIENCE 

Problem: 
	Users face delays and issues while navigating back from wishlist, review, and order pages. 

Improvement Suggestions:
 	Instant response when user presses back
  Consistent navigation across all pages
Benefit:
 	Better user experience and smooth flow of the application

### 2. ENHANCE PAGE LOADING PERFORMANCE

Problem:
	Some pages take time to load. 

Improvement Suggestions:
 	Use faster loading techniques 
Benefit:
 	Faster apps lead to happy users which increase engagement.

### 3. IMPROVE USER CONTROL ON ORDER SUCCESS PAGE

Problem:
	Users cannot go back from the order success page using normal navigation. 

Improvement Suggestions:
 	Allow proper and flexible back navigation 
Benefit:
 	Gives users better control and flexibility


