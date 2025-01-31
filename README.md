# React-Time-Picker-Input

Simple and light time picker for React app.

No moment.js needed

## Installation

npm install react-time-picker-input <br/>
yarn add react-time-picker-input

## Import

import TimePicker from 'react-time-picker-input'

## Demo

[See Demo](https://ornaldo-rp-r.github.io/react-time-picker-test/)

## Usage

Here's an example of basic usage:

```JSX
import React, { useState } from 'react';
import TimePicker from 'react-time-picker-input';

function TimePickerTest() {
const [value, setValue] = useState('10:00');

    return (
        <div>
            <TimePicker
                onChange={(newValue)=>setValue(value)}
                value={value}
            />
        </div>
    );

}
```

## Custom styling

### If Default styles not applied :

#### Download and import on desired location :

[Default Styles File](https://github.com/Ornaldo-RP-R/React-Time-Picker-Input/blob/main/src/lib/components/TimeInput.css)

### Edit Style for Desktop:

#### Input wrapper

```css
.react-time-input-picker {
  // css code here
}
```

#### Hour input :

```css
.react-time-input-picker #react-time-input-picker__hourInput {
  // css code here
}
```

#### Minute input :

```css
.react-time-input-picker input#react-time-input-picker__minuteInput {
  // css code here
}
```

#### AmPm input :

```css
.react-time-input-picker input#react-time-input-picker__amPm {
  // css code here
}
```

#### Focus style:

```css
.react-time-input-picker input:focus {
  // css code here
}
or 
.react-time-input-picker input(//inputSelector):focus
{
  // css code here
}
```

### Edit Styles on Mobile :

#### Input wrapper

```css
.input-time-mobile {
  // css here
}
```

## Props

| PropName     | Type     | default        | description                                                                                                                    |
| ------------ | -------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| onChange     | function | (newValue)=>{} | function that access newValue (new date) param it returns time string if it is valid or if any of parts is empty does not fire |
| value        | String   | "- -"          | Defines default value of TimePicker. Required format ("HH:mm") ex("22:04") -> always 24Hour format                             |
| hour12Format | boolean  | false          | make it true to make input 12HourFormat support see on demo example                                                            |
| allowDelete  | boolean  | false          | make it true if you want to allow user to delete hour and minute using Backspace                                               |
