<p align="center">
  <a href="https://www.medusajs.com">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://user-images.githubusercontent.com/59018053/229103275-b5e482bb-4601-46e6-8142-244f531cebdb.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://user-images.githubusercontent.com/59018053/229103726-e5b529a3-9b3f-4970-8a1f-c6af37f087bf.svg">
    <img alt="Medusa logo" src="https://user-images.githubusercontent.com/59018053/229103726-e5b529a3-9b3f-4970-8a1f-c6af37f087bf.svg" width="150">
    </picture>
  </a>
</p>

<h1 align="center">
  Medusa Eats - Food Delivery Platform
</h1>

<p align="center">
An Uber Eats style delivery platform running on Medusa 2.0 and Next.js 14.</p>

<p align="center">
  <a href="https://railway.app/template/QvfPwp?referralCode=-Yg50p">
    <img src="https://railway.app/button.svg" alt="Deploy on Railway">
  </a>
</p>

<p align="center">
  <a href="https://github.com/medusajs/medusa/blob/master/CONTRIBUTING.md">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat" alt="PRs welcome!" />
  </a>
  <a href="https://discord.gg/xpCwq3Kfn8">
    <img src="https://img.shields.io/badge/chat-on%20discord-7289DA.svg" alt="Discord Chat" />
  </a>
  <a href="https://twitter.com/intent/follow?screen_name=medusajs">
    <img src="https://img.shields.io/twitter/follow/medusajs.svg?label=Follow%20@medusajs" alt="Follow @medusajs" />
  </a>
</p>

## Overview

Medusa Eats is a complete food delivery platform built with:

- [Medusa 2.0](https://medusajs.com/) - Open-source commerce engine
- [Next.js 14](https://nextjs.org/) - React framework for the frontend
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS framework
- [TypeScript](https://www.typescriptlang.org/) - Typed JavaScript

## Features

### Platform Features
- **Restaurant Marketplace** - Browse and order from multiple restaurants
- **Realtime Order Tracking** - Live updates on order status for customers, restaurants, and drivers
- **Multi-dashboard System** - Separate interfaces for customers, restaurants, and drivers
- **User Role Management** - Different access levels and features based on role
- **Authentication** - Secure login and account management
- **Medusa Workflows** - Automated order processing flows
- **Realtime Updates** - Server Sent Events for live status changes

### Customer-Facing Features
- **Restaurant Browsing** - Discover restaurants with intuitive interface
- **Menu Navigation** - Browse restaurant menus with food categories
- **Order Management** - Add items to cart and place orders
- **Order Tracking** - Real-time updates on order preparation and delivery status
- **Checkout Process** - Streamlined ordering experience

### Restaurant Partner Features
- **Order Management Dashboard** - Accept and process incoming orders
- **Order Status Updates** - Mark orders as in preparation, ready for pickup
- **Restaurant Profile Management** - Manage restaurant information and menu

### Driver Features
- **Order Claiming** - See and claim available deliveries
- **Delivery Management** - Track active deliveries with status updates
- **Delivery Workflow** - Step-by-step process from pickup to delivery

## Project Structure

The project consists of two main directories:

- `/backend` - Contains the Medusa 2.0 project with all the customizations
- `/frontend` - Contains the Next.js 14 project for all user interfaces

## Quickstart

### Install Dependencies

Use Yarn to install dependencies in both directories:

```bash
# In /frontend
yarn

# In /backend
yarn
```

### Set Up Environment Variables

Copy the template environment files:

```bash
# In /frontend
cp .env.template .env

# In /backend
cp .env.template .env
```

### Set Up and Seed the Database

1. Create a Postgres database called `medusa-eats`
2. Run the setup script:

```bash
# In /backend
yarn setup-db
```

This creates an admin user with:
- Email: admin@email.com
- Password: supersecret

### Start Development Servers

**Start Medusa backend:**
```bash
# In /backend
yarn dev
```
The Medusa server runs on http://localhost:9000

**Start Next.js frontend:**
```bash
# In /frontend
yarn dev
```
The Next.js frontend runs on http://localhost:3000

### Create User Accounts

#### Create Restaurant Admin Account
1. Go to http://localhost:3000/signup
2. Select 'I'm a restaurant'
3. Select your restaurant
4. Complete the form and create account
5. Access restaurant dashboard at http://localhost:3000/dashboard/restaurant

#### Create Driver Account
1. Go to http://localhost:3000/signup
2. Select 'I'm a driver'
3. Complete the form
4. Access driver dashboard at http://localhost:3000/dashboard/driver

### Full Delivery Workflow Tutorial

> To experience the entire workflow, you'll need multiple browsers or incognito windows to log in as different users.

1. **Place an order:**
   - Go to http://localhost:3000/
   - Select a restaurant
   - Add menu items with the + buttons
   - Click the shopping bag icon
   - Go to checkout and place order
   - View the live order status dashboard

2. **Restaurant accepts order:**
   - Log in to restaurant dashboard at http://localhost:3000/dashboard/restaurant
   - Accept the incoming order 

3. **Driver claims delivery:**
   - Log in to driver dashboard at http://localhost:3000/dashboard/driver
   - Claim the available order
   - Follow prompts to update delivery status

4. **Track in realtime:**
   - All dashboards update in realtime as the order progresses
   - Each user can see appropriate status updates and actions

## Deployment

The easiest way to deploy is using Railway's one-click deployment:

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/template/QvfPwp?referralCode=-Yg50p)

## Requirements

- **Node.js** - v18 or newer
- **PostgreSQL** - Running on default port
- **Redis** - Running on default port

## Resources

### Learn more about Medusa
- [Website](https://www.medusajs.com/)
- [GitHub](https://github.com/medusajs)
- [2.0 Documentation](https://docs.medusajs.com/v2)

### Learn more about Next.js
- [Website](https://nextjs.org/)
- [GitHub](https://github.com/vercel/next.js)
- [Documentation](https://nextjs.org/docs)
