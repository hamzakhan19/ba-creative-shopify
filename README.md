# Full Stack Developer Test -- Fashion Store

This repository contains both parts of the Full Stack Developer Test:

- **Part A -- Project Scoping**
- **Part B -- Product Page Development (Figma Implementation)**

---

# Repository Structure

/docs\
Scope.pdf → Part A (Scoping Document)

/sections\
/snippets\
/assets\
/templates

README.md → Project overview

---

# Development Store Access

Preview URL:\
https://lola-dev-test-2.myshopify.com/
Store Password:\
Shared separately in submission email (security best practice).

Collaborator added:\
jill@bacreative.com.au

---

# Part A – Scoping

The complete scoping document is included in:

/docs/Scope.pdf

This document outlines a structured migration and build plan based on the provided brief. It includes:

- Theme recommendation (Horizon – OS 2.0)
- Migration approach for products, customers and orders (last 12 months)
- Estimated hours per phase and template
- Custom feature breakdown with suggested apps
- QA, UAT and deployment considerations
- Proposed project timeline

Estimates reflect practical delivery experience and include risk considerations for order migration and launch.

# Part B -- Product Page Development

The Product Detail Page (PDP) was built based on the provided Figma design.

Scope included:

- Product gallery
- Size variants
- Color swatches using sibling products
- Short description
- USP icons
- Conditional accordion blocks
- "You may like" section
- Product-specific image + text section
- Global CTA section

---

# Implementation Details

## Product Media

- Uses Shopify product.media
- Responsive layout
- Thumbnail support

## Size Variants

- Standard Shopify variant picker
- Dynamic price updates
- Fully compatible with add-to-cart logic

## Color Swatches

Color swatches work by detecting the “Color/Colour” variant option and replacing the default variant
Size link (Next to Size):- custom.size_guide

## Short Product Description

Recommended source: product.metafields.custom.introduction
UPS Icons:- Metafield: custom.usp_icons and MetaObject:- usp_icons

## Product Accordions

Recommended metafields:- custom.product_details - custom.size_fit -
custom.shipping_and_returns

## Image + Text Section

Created section and connected it to the customizer so its easy for the user to add the relevant content

# QA Checklist

- Variant selection updates price correctly
- Swatch navigation works
- Active swatch highlighted
- Empty accordion sections hidden
- Add to cart functions correctly
- Recommended products display
- Responsive behavior maintained

---

# Future PDP Enhancements

Conversion: - Sticky Add to Cart - Low stock messaging - Delivery
estimate - Free shipping progress bar - Review rating integration

Fashion: - Model height + size worn - Enhanced size guide modal -
True-to-size indicator - Fabric highlight icons - Complete the look
section

Revenue: - Bundle discounts - Frequently bought together - Cart drawer
upsell - Recently viewed products

Trust: - Secure checkout badges - Easy returns messaging - Payment
badges - Testimonials

---

# Technical Approach

- Shopify OS 2.0 section-based architecture
- Modular Liquid snippets
- Metafield & metaobject-driven structure
- Conditional rendering for clean UX
- Minimal reliance on third-party apps
