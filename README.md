Shopify Developer Test – Fashion Store

This repository contains both parts of the Shopify Developer Test:

Part A – Project Scoping

Part B – Product Page Development (Figma Implementation)

The original test brief is provided here:

Shopify Developer Test-Feb26

Repository Structure
/docs
Scope.pdf → Part A (Scoping Document)

/sections
/snippets
/assets
/templates

README.md → Project overview (this file)
Development Store Access

Preview URL:
https://your-store.myshopify.com

Store Password:
Shared separately in submission email for security best practice.

Collaborator access has been granted to:
jill@bacreative.com.au

Part A – Scoping

The complete scope document is included in:

/docs/Scope.pdf

This document includes:

Theme recommendation

Migration strategy

Estimated hours per template

Custom feature breakdown

Suggested apps

Implementation sequencing

Scoping was approached as if this were a real client project with budget constraints, as requested in the brief

Shopify Developer Test-Feb26

Part B – Product Page Development

The Product Detail Page (PDP) was built based on the provided Figma design.

Scope included:

Product media

Size variants

Color swatches using sibling products

Short description

USP icons

Conditional accordion blocks

“You may like” section

Product-specific image + text section

Global CTA section

Implementation Details

1. Product Media

Uses Shopify product.media

Responsive layout

Thumbnail support

Structured to support video media extension

2. Size Variants

Standard Shopify variant picker

Dynamic price updates

Fully compatible with add-to-cart logic

3. Color Swatches (Sibling Products)

Requirement: Colors are separate products.

Implemented using metafield-driven grouping.

Recommended metafield:

custom.sibling_group

All sibling products share the same group value.

Swatch behavior:

Click → navigates to sibling product

Active swatch highlighted

URL updates correctly

4. Short Product Description

Displayed near title and pricing.

Recommended data source:

product.metafields.custom.short_description 5. USP Icons

Implemented using flexible section blocks.

Recommended scalable approach:

Metaobject for reusable USP entries

Linked via product metafield reference

6. Product Accordions

Accordion sections render only if content exists.

Recommended metafields:

custom.fabric_details
custom.size_guide
custom.care_instructions
custom.shipping_returns

If metafield is empty → section does not render.

7. Image + Text Section

The “Our Dresses Are Built Different” block can be structured using:

Recommended Architecture

Metaobject Definition:

Heading

Subheading

Body text

Image

Background color

Linked via product metafield reference.

This enables:

Per-product variation

No hardcoded content

Clean admin workflow

8. Typography Differences (If Not Fully Matched)

If fonts differ from Figma:

Implementation approach:

Upload font files to theme assets

Define @font-face in base stylesheet

Update typography variables in settings_schema.json

Apply via CSS variables globally or scoped to PDP

This keeps typography centralized and scalable.

QA Checklist

Variant selection updates price correctly

Swatch navigation works

Active swatch highlighted

Empty accordion sections hidden

Add to cart functions correctly

Recommended products display

No console errors

Responsive behavior maintained

Future PDP Enhancements
Conversion Improvements

Sticky Add to Cart

Low stock messaging

Delivery estimate

Free shipping progress bar

Review rating integration

Fashion Enhancements

Model height + size worn

Enhanced size guide modal

True-to-size indicator

Fabric feature icons

Complete the look section

Visual Improvements

Image zoom

Swipe gallery on mobile

Product video

Swatch hover preview

Smooth accordion animation

Revenue Enhancements

Bundle discounts

Frequently bought together

Cart drawer upsell

Recently viewed products

Trust Enhancements

Secure checkout badges

Easy returns messaging

Payment badges

Testimonials

Technical Approach

Shopify OS 2.0 section-based architecture

Modular Liquid snippets

Metafield & metaobject-driven structure

Conditional rendering for clean UX

Minimal reliance on third-party apps
