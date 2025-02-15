# Telephone Package

## Overview

The Telephone Package is a JavaScript implementation of a telephone system that allows users to add, remove, and dial phone numbers. It also utilizes the Observer design pattern to notify observers whenever a phone number is dialed.

## Features

- **Add Phone Number**: Add new phone numbers to the system.
- **Remove Phone Number**: Remove existing phone numbers.
- **Dial Phone Number**: Dial a previously added phone number.
- **Observer Pattern**: Notify observers when a phone number is dialed.

## Requirements

- JavaScript (ES6)
- A modern web browser or Node.js environment

## Installation

1. Clone the repository or download the files.
2. Open the `telephonePackage.js` file in a text editor.

## Usage

### Example Code

Here's a simple example of how to use the Telephone Package:

```javascript
// Create a new Telephone instance
const telephone = new Telephone();

// Create observers
const phoneNumberObserver = new PhoneNumberObserver();
const dialingObserver = new DialingObserver();

// Add observers to the telephone instance
telephone.addObserver(phoneNumberObserver);
telephone.addObserver(dialingObserver);

// Add a phone number
telephone.addPhoneNumber('2347023232');

// Dial the phone number
telephone.dialPhoneNumber('2347023232');

// Remove the phone number
telephone.removePhoneNumber('2347023232');

// Try dialing a removed phone number
telephone.dialPhoneNumber('2347023232');
