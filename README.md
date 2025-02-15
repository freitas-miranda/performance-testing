# Performance Testing

Este repositório contém exemplos e scripts para realizar testes de carga e desempenho utilizando diversas ferramentas populares, como K6, JMeter e ApacheBench (AB). Nosso objetivo é fornecer recursos e guias práticos para ajudar desenvolvedores e engenheiros de desempenho a avaliar e melhorar a escalabilidade e a robustez de suas aplicações.

## Ferramentas Incluídas

### K6
[K6](https://k6.io/) é uma ferramenta moderna de teste de carga que permite escrever scripts de teste em JavaScript. É conhecida por sua simplicidade e eficiência.

**Aplicação Comum:**
- Testes de carga contínuos em pipelines de CI/CD.
- Simulação de cenários complexos de usuários.

**Como Executar:**
```bash
docker compose run k6 run /scripts/teste-carga.js
```

### JMeter
[Apache JMeter](https://jmeter.apache.org/) é uma ferramenta amplamente utilizada para testes de carga e desempenho. Suporta uma ampla gama de protocolos e é altamente configurável.

**Aplicação Comum:**
- Testes de carga em aplicações web e serviços REST.
- Simulação de cargas pesadas e análise de desempenho.

**Como Executar:**
```bash
# Exemplo de comando para executar um teste com JMeter
jmeter -n -t /path/to/test-plan.jmx -l /path/to/results.jtl
```

### ApacheBench (AB)
[ApacheBench (AB)](https://httpd.apache.org/docs/2.4/programs/ab.html) é uma ferramenta simples para realizar testes de carga em servidores web. É útil para testes rápidos e básicos de desempenho.

**Aplicação Comum:**
- Testes rápidos de desempenho em endpoints HTTP.
- Avaliação inicial de capacidade de resposta do servidor.

**Como Executar:**
```bash
# Exemplo de comando para executar um teste com ApacheBench
ab -n 1000 -c 10 http://example.com/
```

## Estrutura do Repositório
- **k6**: Scripts e documentação para testes com K6.
- **jmeter**: Planos de teste e documentação para JMeter.
- **ab**: Comandos e documentação para ApacheBench.

## Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests para melhorar este repositório.
