<h1 align="center">ern-phone-input</h1>

## Overview
ern-phone-input stands out as a user-friendly input field for phone numbers, seamlessly predicting the country and formatting the entered phone number accordingly by default.For international phone numbers, users can effortlessly choose their country from a dropdown menu.

By incorporating the prop `format='NATIONAL'` and specifying a `defaultCountry='DE'`, the input field showcases its simplicity by automatically formatting the entered phone number in the national format supported by the default country.


## Installation
npm:
```sh
npm i -S react-phonenr-input
```

yarn:
```sh
yarn add react-phonenr-input
```

#### Props:
<table style="font-size: 12px">
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Default</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>onChange</td>
    <td>(data: PhoneNumber) => void</td>
    <td>required</td>
    <td>The function/method that returns the entered phonenumber or phonenumber object</td>
  </tr>
  <tr>
    <td>withCountryMeta</td>
    <td>boolean</td>
    <td>false</td>
    <td>
      changes the retuned value into an Object that contains the phonenumber and the country information.
      eg.:
      <pre>
        {
          phoneNumber: "+49 176 12345678",
          country: {
            name: "Germany (Deutschland)"
            iso2: "DE"
          }
        }
      </pre>
    </td>
  </tr>
  <tr>
    <td>className</td>
    <td>string</td>
    <td>undefined</td>
    <td>Adds a custom class to the Phonenumber Input Field</td>
  </tr>
  <tr>
    <td>defaultCountry</td>
    <td>IsoCode</td>
    <td>undefined</td>
    <td>Sets the default country (use iso alpha-2 country code e.g 'US', 'GB', 'DE')</td>
  </tr>
  <tr>
    <td>disabled</td>
    <td>boolean</td>
    <td>false</td>
    <td>Disables the Phonenumber Input Field</td>
  </tr>
  <tr>
    <td>format</td>
    <td>NumberFormat</td>
    <td>'INTERNATIONAL'</td>
    <td>One of: 'INTERNATIONAL', 'NATIONAL'. Sets the format of the entered  phonenumber, in case of 'NATIONAL' the defaultCountry must be set</td>
  </tr>
  <tr>
    <td>initialValue</td>
    <td>string</td>
    <td>undefined</td>
    <td>Sets the initial Value of the Phonenumber Input. This is usefull in case you need to set a phonenumber stored for example in a database</td>
  </tr>
  <tr>
    <td>placeholder</td>
    <td>string</td>
    <td>undefined</td>
    <td>Sets the Placeholder text</td>
  </tr>
  <tr>
    <td>preferredCountries</td>
    <td>IsoCode[]</td>
    <td>undefined</td>
    <td>Lets you restrict the country dropdown to a specific list of countries (use iso alpha-2 country code e.g 'US', 'GB', 'DE')</td>
  </tr>
  <tr>
    <td>regions</td>
    <td>"asia" | "europe" | "africa" | "north-africa" | "oceania" | "america" | "carribean" | "south-america" | "ex-ussr" | "european-union" | "middle-east" | "central-america" | "north-america" | Region[]</td>
    <td>undefined</td>
    <td>Lets you restrict the country dropdown to a list of countries in the specified regions</td>
  </tr>
</table>

###### In addition to the here listed Props you can pass all other properties that can be used on a normal Html input field

#### Code example:
```tsx
import React, { useState } from 'react'
import { PhoneInput, PhoneNumber } from 'react-phonenr-input';

const Example = () => {
  const [value, setValue] = useState<PhoneNumber>('')

  const handleChange = (phoneNumber: PhoneNumber) => {
    // Do something with the phoneNumber
    setValue(phoneNumber)
  }

  return (
    <div>
      <PhoneInput onChange={handleChange}/>
    </div>
  )
}
```

#### Optimized for Mobile usage

<img src="https://raw.githubusercontent.com/KaiHotz/React-PhoneNr-Input/master/styleguide/mobile.png" width="200" alt="mobile">


## Support
If you like the project and want to support my work, you can buy me a coffee :)

[![paypal](https://img.shields.io/badge/donate-paypal-blue.svg)](https://paypal.me/kaihotz)