---
project: motorin
purpose: Vue 3 + Bootstrap automotive marketplace practice project
---
# motorin-prd.md — Product Requirements

## Product
A automotive marketplace web application for learning Vue 3, Bootstrap 5, and API consumption.

## Target Audience
Junior frontend developer candidates being evaluated for Vue 3 proficiency.

## Core Features

### 1. Car Listing Display
- Display a grid/card layout of vehicle listings
- Each listing shows: photo, title, price, mileage, year, favorite button
- Responsive grid layout using Bootstrap

### 2. Filtering & Search
- Filter by price range (Bootstrap form-range)
- Filter by vehicle type/brand using form-select
- Client-side filtering of listings

### 3. Favorite System
- Toggle favorite status on individual listings
- Visual indicator (heart icon, color change)
- Persistent state via localStorage

### 3. API Consumption (Phase C)
- Replace seed-data.html/localStorage with real API fetch
- Handle loading, error, and empty states
- Proper error handling with try/catch

### 4. API Endpoint
- Rest API providing vehicle listing data
- JSON format with: id, title, price, mileage, year, photoUrl, isFavorite, createdAt

### 5. UI/Styling (DESIGN.md tokens)
- Primary: #1A2E4C (deep automotive navy)
- Accent: #D62828 (alert/CTA red)
- Surface: #FFFFFF (cards)
- Canvas: #F5F6F8 → page background
- Text primary: #111418
- Text muted: #5B6470
- Success: #1F883D → "available now"
- Warning: #B98900 → "pending"

###Responsive & Accessibility
- Mobile-first responsive design
- 44px minimum touch targets
- Tabular numbers (font-variant-numeric: tabular-nums) for price/mileage
- Aspect ratio 16:9 for car photos

###Technical Requirements
- Vue 3 Composition API with `<script setup>`
- Bootstrap 5 for layout and components
- Vue Router for navigation
- Fetch API for API consumption
- localStorage for client-side state persistence
- Responsive design mobile-first
- Accessible interactive elements (44px minimum touch targets)

###Styling Approach
- Use Bootstrap 5 utilities as primary styling mechanism
- Override only via CSS variables matching DESIGN.md tokens
- Tabular numbers on price and mileage fields
- Aspect ratio 16:9 on car photo containers
- 44px minimum touch target size
- Concentric radius system (card radius slightly larger than inner elements)
- Scale(0.97) press feedback on buttons