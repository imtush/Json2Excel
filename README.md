# JSON to Excel Converter

A simple tool to convert JSON data into Excel spreadsheets.

## How It Works

This converter takes your JSON data and transforms it into a downloadable Excel file (.xlsx format).

## Input Format

### Best Results
For optimal conversion, structure your JSON as an **array of objects**:

```json
[
  {
    "name": "John Doe",
    "age": 30,
    "city": "New York"
  },
  {
    "name": "Jane Smith",
    "age": 25,
    "city": "Los Angeles"
  }
]
```

### What Happens During Conversion

- **Array of objects**: Each object becomes a row in the Excel file
- **Object keys**: Automatically become column headers
- **Single object**: Converts to a single-row table
- **Malformed data**: Fields with extra quotes or formatting issues are automatically ignored

## Example

**Input JSON:**
```json
[
  {"product": "Laptop", "price": 999, "stock": 15},
  {"product": "Mouse", "price": 25, "stock": 50}
]
```

**Output Excel:**
| product | price | stock |
|---------|-------|-------|
| Laptop  | 999   | 15    |
| Mouse   | 25    | 50    |

## Tips

- Ensure your JSON is valid before conversion
- Use consistent keys across all objects for clean columns
- Nested objects and arrays may require flattening for best results
- The tool handles common formatting issues automatically

## Common Use Cases

- Exporting API responses to Excel
- Converting configuration files to spreadsheets
- Data analysis and reporting
- Sharing data with non-technical team members

## Limitations

- Very large JSON files may take longer to process
- Complex nested structures work best when flattened
- Special characters in keys become column headers as-is
