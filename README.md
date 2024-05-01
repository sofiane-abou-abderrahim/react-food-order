# Time To Practice: Food Order App

## Components, State, Context, Effects, HTTP Requests & More!

- Building a Complete Project From the Ground Up
- Building & Configuring Components
- Using State & Context
- Managing HTTP Requests & Side Effects

# A Challenge For You

## Build a "Food Order" web app

- Use the starting project attached to this lecture
- Add components for displaying products, the cart (in a modal) and a checkout form (also in a modal)
- Fetch the (dummy) meals data from the backend & show it on the screen (Get /meals)
- Allow users to add & remove products to / from the cart
- Send cart data along with user data (full name, email, street, postal code, city) to the backend (POST /orders)
- Handle loading & error states

# Steps

## 0. Starting Project

1. run `npm install` in the `backend` folder
2. run `npm install` in the main project folder (frontend)
3. run `npm start` in the `backend` folder
4. run `npm run dev` in the main project folder (frontend)
5. create a `README.md` file

## 1. Planning the App & Adding a First Component

1. add a `components` folder
2. inside of it, add a `Header.jsx` file
3. use this header in the `App.jsx` component

## 2. Fetching Meals Data (GET HTTP Request)

1. add a new `Meals.jsx` component
2. send a GET HTTP request to the dummy backend from inside `Meals.jsx`
3. output the meals items (just the names for now) from inside `App.jsx`

## 3. Adding a "MealItem" Component

1. add a `MealItem.jsx` file
2. output the `<MealItem>` component in `Meals.jsx`
3. prepend the image source data in `MealItem.jsx` to load the images from the backend

## 4. Formatting & Outputting Numbers as Currency

1. add a new `util` folder & add a new `formatting.js` file inside it for formatting the price
2. use the `currencyFormatter` function in `MealItem.jsx`

## 5. Creating a Configurable & Flexible Custom Button Component

1. add a `UI` subfolder inside the `components` folder for UI core generic building blocks
2. add a new `Button.jsx` inside that `UI` folder
3. use this `<Button>` component in your app, for example:
   1. a text only button style in the `Header.jsx`component
   2. an other button style in the `MealItem.jsx` component

## 6. Getting Started with Cart Context & Reducer

1. use React's context feature to manage the cart data in a more general centralized way
   1. add a `store` folder
   2. inside it, add a `CartContext.jsx` file where you manage this cart data & this cart context
2. use React's Reducer feature instead of State

## 7. Finishing & Using the Cart Context & Reducer

1. finish the cart logic inside the `cartReducer` function in `CartContext.jsx`
2. connect the cart logic with help of `useContext()` to the different components
   1. use the `useReducer()` hook correctly inside of the `CartContextProvider` component
   2. pass the cart context value to the `<CartContext.Provider>` component
3. use the cart context inside of the other components
   1. wrap all your components with the `<CartContextProvider>` component in `App.jsx`
   2. use the cart context in `MealItem.jsx` to update your cart
   3. access the cart context in `Header.jsx` to display the number of meals in the cart
