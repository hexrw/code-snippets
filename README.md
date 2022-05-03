# Iterate over any JavaScript structure

```js
const convert = (data) => {
    if (typeof data === "string") {
        // convert the string
    } else if (typeof data === "number") {
        // convert the number
    } else if (typeof data === "boolean") {
        // convert the boolean
    } else if (typeof data === "object") {
        if (Array.isArray(data)) {
            return data.map(convert)
        } else {
            const result = {}
            for (const key in data) {
                result[key] = convert(data[key])
            }
            return result
        }
    }
}
```
