# Productify

An e-commerce web app built with Next.js, TypeScript and Redux Toolkit. Users can search, filter and sort a product catalogue, view product details, manage a cart and go through a checkout flow. Product data comes from the [DummyJSON Products API](https://dummyjson.com/products).

The app code is in the [`productify/`](productify) folder.

## Features

- Product catalogue with search, category filter and sorting by price or rating
- Infinite scroll or page-by-page loading, which the user can switch between
- Category pages and product detail pages
- Cart with quantity updates, stored in Redux and saved to `localStorage` so it survives a page reload
- Checkout with order summary, shipping and tax calculation, form validation and a confirmation page
- Loading, empty and error states for every API request
- Responsive layout styled with Tailwind CSS

## Tech stack

Next.js 15 (Pages Router) · React 19 · TypeScript · Redux Toolkit · Tailwind CSS 4 · DummyJSON API

## Run locally

```bash
git clone https://github.com/Hillary-Robert/productify.git
cd productify/productify
npm install
npm run dev
```

The app runs at http://localhost:3000.

## Project structure

```
productify/
├── components/   UI parts: header, hero, product grid and cards, filters, sort bar
├── pages/        Home, category, product detail, cart, checkout and success pages
├── store/        Redux store and cart slice
├── interface/    TypeScript types
└── constants/    Static content such as hero slides
```

## Notes

This project started as my capstone for the ALX ProDev Frontend Engineering programme. Checkout is a demo: no real payment is taken.

## Author

Hillary Robert · [GitHub](https://github.com/Hillary-Robert) · [LinkedIn](https://www.linkedin.com/in/hillaryrobert30/)
