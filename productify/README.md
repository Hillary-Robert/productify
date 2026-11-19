# Productify

An e-commerce web app built with Next.js, TypeScript and Redux Toolkit. It loads real product data from the [DummyJSON Products API](https://dummyjson.com/products) and lets users search, filter and sort products, manage a cart and go through a checkout flow.

## Features

- **Product catalogue:** products load from the DummyJSON API, with loading, empty and error states
- **Search and filters:** search by keyword and filter by category
- **Sorting:** sort by price or rating, ascending or descending
- **Infinite scroll or pages:** users can switch between infinite scroll and page-by-page loading
- **Category and product pages:** a page for each category and a detail page for each product
- **Cart:** add and remove items and change quantities; the cart is kept in Redux and saved to `localStorage`, so it survives a page reload
- **Checkout:** order summary with shipping and tax, form validation, and a confirmation page with an order number
- **Responsive design:** layout styled with Tailwind CSS for mobile and desktop

## Tech stack

- **Framework:** Next.js 15 (Pages Router)
- **UI:** React 19, Tailwind CSS 4, Lucide icons
- **Language:** TypeScript
- **State management:** Redux Toolkit, with the cart saved to `localStorage`
- **Data:** DummyJSON Products API

## Project structure

```
productify/
├── components/    Header, Hero, ProductGrid, ProductCard, Filter, SortBar, Footer
├── pages/
│   ├── index.tsx            Home page with the product catalogue
│   ├── category/[slug].tsx  Products in one category
│   ├── products/[id].tsx    Product detail page
│   ├── cart.tsx             Cart
│   ├── checkout.tsx         Checkout form and order summary
│   └── checkout/success.tsx Order confirmation
├── store/         Redux store and cart slice (add, remove, update, save)
├── interface/     TypeScript types
├── constants/     Static content such as hero slides
├── public/        Images
└── styles/        Global styles
```

## Getting started

Clone the repository and open the app folder:

```bash
git clone https://github.com/Hillary-Robert/productify.git
cd productify/productify
```

Install dependencies and start the development server:

```bash
npm install
npm run dev
```

The app runs at http://localhost:3000.

## How it works

- **Browsing:** the home page fetches products from DummyJSON. Search and category choices build the API request, with `limit` and `skip` for pagination, and the loaded products are then sorted in the browser.
- **Cart:** product cards and detail pages dispatch Redux actions to add items. The cart slice saves its state to `localStorage` after every change and loads it again when the app starts.
- **Checkout:** the checkout page calculates shipping (free over $100) and 8% tax, validates the form, clears the cart and redirects to a confirmation page. No real payment is taken.

## Possible improvements

- User accounts and order history
- Payment integration with a provider such as Stripe
- Unit and component tests
- Multi-language and multi-currency support

## Author

**Hillary Robert**
- GitHub: [Hillary-Robert](https://github.com/Hillary-Robert)
- LinkedIn: [hillaryrobert30](https://www.linkedin.com/in/hillaryrobert30/)
