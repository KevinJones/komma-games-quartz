
Use this filter:
```javascript
.where(b => b["release-date"] < new Date("1983-07-01"))
```

```dataviewjs

function expressDate(dateString, detail) {
    const date = new Date(dateString);
    let output = "";

    switch (detail) {
        case "y":
            output = date.getFullYear().toString();
            break;
        case "m":
            output = `${date.toLocaleString("default", { month: "long" })} ${date.getFullYear().toString()}`;
            break;
        case "d":
            output = `${date.toLocaleString("default", { month: "long" })} ${date.getDate().toString()}, ${date.getFullYear().toString()}`;
            break;
        default:
            throw new Error("Level of date detail must be 'y', 'm', or 'd'.");
        }

    return output;
}

const query = b => b["release-date"] < new Date("1983-07-01")
const pages = dv.pages('"gamerecs"')
const data = pages
    .where(query)
	.sort(b => b["release-date"])
	.map(b => [b.file.link, b.developer, b.publisher, b.hours, expressDate(b["release-date"], b["date-spec"]), b["play-today"]])
const count = data.length
const hrs = pages
	.where(query)
	.map(b => b.hours).array().reduce((acc, obj) => acc + (obj || 0), 0)
const headers = ["File", "Developer", "Publisher", "Hours", "Release Date", "Play Today"]

// then render it as desired.
dv.table(headers, data)
dv.paragraph(`Totals: ${count} games, ${hrs.toFixed(1)} hours.`)

```

