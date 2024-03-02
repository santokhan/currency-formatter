In JavaScript, you can format currency using various methods. One common way is to use the `Intl.NumberFormat` object, which provides built-in support for formatting numbers, including currency. Here's an example of how you can use it to format currency:

```javascript
// Format currency using Intl.NumberFormat
function formatCurrency(amount, currencyCode, locale) {
    // If locale is not provided, default to the user's browser locale
    locale = locale || navigator.language || 'en-US';

    // Create number formatter instance
    const formatter = new Intl.NumberFormat(locale, {
        style: 'currency',
        currency: currencyCode,
    });

    // Format the amount
    return formatter.format(amount);
}

// Example usage:
const amount = 12345.67;
const currencyCode = 'USD';
console.log(formatCurrency(amount, currencyCode)); // Output: $12,345.67
```

This code creates a function `formatCurrency` that takes the amount, currency code, and locale (optional) as parameters and returns the formatted currency string. It uses the `Intl.NumberFormat` object with the specified options to format the currency. If locale is not provided, it defaults to the user's browser locale.

You can call this function with the amount and currency code you want to format, like in the example usage above.
