# Iterate over any JSON structure

```js
const convert = (data) => {
    if (typeof data === "string") {
        // string
    } else if (typeof data === "number") {
        // number
    } else if (typeof data === "boolean") {
        // boolean
    } else if (data === null) {
        // null
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
