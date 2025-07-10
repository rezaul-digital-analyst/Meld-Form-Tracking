# Meld Form Tracking with Google Tag Manager

This template demonstrates how to track a form submission using a custom `dataLayer.push()` and Google Tag Manager (GTM).

## Features

- Vanilla JavaScript – no dependencies
- Captures form data as an object
- Pushes custom event: `meld_form_submit` with all form fields
- GTM-ready integration

## Setup

1. Replace `GTM-XXXXXXX` with your Google Tag Manager ID.
2. In GTM:
   - Create a **Custom Event Trigger** for `meld_form_submit`
   - Create **Data Layer Variables** for `formData.name`, `formData.email`, etc.
   - Create a **GA4 Event Tag** (or other destination) and map fields.

## Example dataLayer Push

```json
{
  "event": "meld_form_submit",
  "formData": {
    "name": "Jane Doe",
    "email": "jane@example.com",
    "message": "Hello there!"
  }
}
