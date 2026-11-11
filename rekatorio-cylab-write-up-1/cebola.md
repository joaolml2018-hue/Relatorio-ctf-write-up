# Relatório CTF

**Nome:** João Lucas Marques de Lima

---

## Desafio: Cebola Criptográfica

### Análise do Desafio

O desafio apresentava uma mensagem indicando que a informação poderia estar escondida em várias camadas de codificação.

Foi fornecido um arquivo chamado `flag.txt`, contendo uma sequência formada apenas por `0` e `1`. O objetivo era identificar as camadas de codificação e decodificá-las até encontrar a flag.

### Analisando o Arquivo

Ao abrir o arquivo `flag.txt`, foi encontrada uma sequência de números binários:

```text
00110101 00110010 00100000 00110110 01100010 00100000
00110111 00111000 00100000 00110100 00110010 00100000
00110101 00110010 00100000 00110011 00110011 ...
```

### Resolvendo

Utilizando o site **dCode**, foi possível identificar as diferentes camadas de codificação.

#### Primeira Parte

A primeira camada foi identificada como ASCII em formato binário. Após a conversão, foi obtido:

```text
52 6b 78 42 52 33 74 45 4d 58 59 7a 63 6a 55 30 ...
```

#### Segunda Parte

Após realizar uma nova conversão, foi obtido:

```text
RkxBR3tEMXYzcjU0c19jNG00RDQ1fQ==
```

#### Terceira Parte

A última camada foi identificada como Base64. Após a decodificação, foi encontrada a flag:

```text
FLAG{D1v3r54s_c4m4D45}
```

### Resolução

O processo de decodificação foi:

**Binário → ASCII → ASCII → Base64 → Flag**

### Flag

A flag encontrada foi:

```text
FLAG{D1v3r54s_c4m4D45}
```
