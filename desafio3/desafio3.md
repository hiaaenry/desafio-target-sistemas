# Desafio 3

## Faturamento diário

```javascript
function calculateRevenue(dailyRevenue) {
  let validRevenue = dailyRevenue.filter((f) => f > 0);

  let minRevenue = Math.min(...validRevenue);
  let maxRevenue = Math.max(...validRevenue);

  let totalRevenue = validRevenue.reduce((acc, val) => acc + val, 0);
  let annualAverage = totalRevenue / validRevenue.length;

  let daysAboveAverage = validRevenue.filter((f) => f > annualAverage).length;

  return {
    minRevenue: minRevenue,
    maxRevenue: maxRevenue,
    daysAboveAverage: daysAboveAverage,
  };
}

let dailyRevenue = [0, 100, 200, 0, 300, 400, 0, 150, 0, 250, 0];

let result = calculateRevenue(dailyRevenue);

console.log("Menor faturamento: " + result.minRevenue);
console.log("Maior faturamento: " + result.maxRevenue);
console.log("Dias acima da média: " + result.daysAboveAverage);
```
