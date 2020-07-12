![Bitly URL shortener field](https://docrdsfx76ssb.cloudfront.net/static/1594322618/pages/wp-content/uploads/2019/02/bitly.png)

# Bitly field ReactJS
ReactJS component to create and get shorter URL via Bitly.

## Install
`npm install bitly-field-react`

## Usage
```javascript
import BitlyField from 'bitly-field-react';

...

<BitlyField
  config={{
      accessToken: {YOUR_BITLY_ACCESS_TOKEN},
  }}
  onSuccess={(response) => callback(response)}
  onError={(error) => callback(error)}
/>

...
```

## Docs
```javascript
config: {
  accessToken: {YOUR_BITLY_ACCESS_TOKEN}
}

onSuccess => response = {
  id: String, // bit.ly/3g8v5gj
  link: String, // https://bit.ly/3g8v5gj
  long_url: String, // http://masso.sk/
  deeplinks: Array, // []
  custom_bitlinks: Array, // []
  created_at: String, // 2020-06-29T14:04:03+0000
  archived: Boolean, // true || false
  tags: Array, // []
  references: Object, // {group: ""}
};
```

### Props
| NAME | TYPE | DEFAULT VALUE |
|:-------------|:-------------|:-------------|
|config|Object (required)||
|onSuccess|Function (required)||
|onError|Function|() => null|
|placeholder|String|null|
|inputClassName|String|null|
|buttonClassName|String|null|