# JSON

Package: https://www.nuget.org/packages/Newtonsoft.Json

## Dump object to JSON 

```csharp

List<int> numbs = new List<int>() { 1, 3, 4, 5, 6 };
string json = JsonConvert.SerializeObject(numbs);

// Output: [1,3,4,5,6]
```

