# Custom ID

A tiny (3 KB), unique but customizable, 🤠 human-friendly but secure, encrypted but beautiful,🐱‍🐉 string ID generator for JavaScript 🎉🎉🎉

# Use Case

As it's human-friendly you can use it as an OTP(one-time password), transaction ID, activation code, SMS code, Invitation key, React component key, Database random ID etc. Your imagination is your limitation. 🎉🎉

## Installation

```bash
npm i custom-id
```

Yarn installation

```bash
yarn add custom-id
```

## Usage

You can generate an ID instantly by giving an empty object as the argument. 👀👀👀

```js
var customId = require("custom-id");

customId({}); // An automatic 8 string ID will be generated
```

The custom ID will be generated in this format -

✌✌ 2 Number + 2 String + 2 Number + 2 String ✌✌

All those number and string will be generated randomly. We use the cryptographic method for generating ids.

# Customizable

The most beautiful & unique advantage of this library is its customizability.

```js
customId({
  name: "Md. Fazlul Karim", // Optional
  email: "fazlulkarimrocky@gmail.com", // Optional
  randomLength: 2, // Optional
  lowerCase: true // Optional
});
```

## API

## customId.name (optional)

You can provide a name for randomization. We sanitize the string by removing space, full stop or any special characters. Then we randomize those words and select the strings from those words.

If no name is provided, we just select two random alphabets.

```js
customId({
  name: "Md. Fazlul Karim" // Optional
});
```

## customId.email (string || optional)

You can provide an email too. We sanitize the email and convert it to a string by removing space or any special characters. Then we randomize those words and select the strings from those words.

If no email is provided, we just select two random alphabets.

```js
customId({
  email: "fazlulkarimrocky@gmail.com" // Optional
});
```

## customId.randomLength (number || optional)

Okay... we need flexibility sometimes. Our automatic structure is -

✌✌ 2 Number + 2 String + 2 Number + 2 String ✌✌

We can alter this behavior as we wish. if we pass customId.randomLength the value of 4 the result will be -

✌✌ 4 Number + 4 String + 4 Number + 4 String ✌✌

Power is in your hand. You can make it super strong or super easy. It's your call. Use long key combination for really important random number. And use small key combination like 4K8L for OTP or inivitaion code.

```js
customId({
  randomLength: 4 // Optional
});
```

## customId.lowerCase (boolean || optional)

We sanitize your string by toUpperCase() method. So every ID created is always in uppercase format. But you may want it in lowercase format. You have the freedom. 😎😎

```js
customId({
  lowerCase: true // Optional
});
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate. 🏃‍🏃‍

## License

[MIT](https://choosealicense.com/licenses/mit/)
