# Testes com k6
O k6 é uma ferramenta de teste de carga de código aberto e gratuita, com isso será capaz de detectar regressões de desempenho e problemas mais cedo, permitindo construir sistemas mais resilientes e aplicativos robustos. Portanto o k6 utiliza a linguagem JavaScript para a criação dos cenários de teste.

## Instalação
- [k6 docs](https://k6.io/docs/get-started/installation/)
- Ou usando o docker `image: loadimpact/k6

## Rodar os testes
- Teste de carga
```bash
docker compose run k6 run /scripts/teste-carga.js
```

- Teste de pico
```bash
docker compose run k6 run /scripts/teste-pico.js
```

## Resultados
- [Dashboard](http://localhost:3030/d/k6/k6-load-testing-results?orgId=1&refresh=5s)
```bash
#checks.........................:  43.59% ✓  936       ✗ 1211  15M
#checks.........................: 100.00% ✓ 4594       ✗ 0     50m
```

## Links
- [Conhecendo o K6 para o teste de carga](https://medium.com/xp-inc/conhecendo-o-k6-para-testes-de-carga-943a0489de1e)
