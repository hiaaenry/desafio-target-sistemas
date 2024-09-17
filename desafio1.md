# Desafio 1

## Trecho de código

```javascript
int INDICE = 12, SOMA = 0, K = 1;

enquanto K < INDICE faça
{
    K = K + 1;
    SOMA = SOMA + K;
}

imprimir(SOMA);
```

No loop, enquanto `K` for menor que 12, o valor de `K` é incrementado em 1 e o valor da `SOMA` é atualizado com a soma de `K`.

| Iteração     | K   | SOMA |
| ------------ | --- | ---- |
| 1ª iteração  | 2   | 2    |
| 2ª iteração  | 3   | 5    |
| 3ª iteração  | 4   | 9    |
| 4ª iteração  | 5   | 14   |
| 5ª iteração  | 6   | 20   |
| 6ª iteração  | 7   | 27   |
| 7ª iteração  | 8   | 35   |
| 8ª iteração  | 9   | 44   |
| 9ª iteração  | 10  | 54   |
| 10ª iteração | 11  | 65   |
| 11ª iteração | 12  | 77   |

No final do processo, o valor de `SOMA` será 77.
