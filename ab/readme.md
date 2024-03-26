# Testes com ApacheBench (ab)

- É uma ferramenta para avaliar seu servidor HTTP.
- Ele foi projetado para dar uma ideia do desempenho do servidor Apache. 
- Mostra especialmente quantas solicitações por segundo seu servidor é capaz de atender.

## Instalação
```bash
sudo apt-get install apache2-utils
```

## Para testar
- `-n 100` = Representa o número de requisições, no caso 100 requisições.
- `-c 10` = Representa o número de concorrências, ou seja, 10 requisições simultâneas
- Lembre-se de colocar a / no final da url, somente assim o ab entenderá como uma url válida.
```bash
ab -n 100 -c 10 http://localhost:3131/pix/token/
ab -n 20000 -c 500 http://localhost:3131/pix/token/
```

- Ver métricas de cada requisição
```bash
ab -n 10 -c 2 -g ./ab/out.data.txt http://localhost:3131/pix/charge/ && cat ./ab/out.data.txt
```

## Resultados

### Intormações retornadas pelo ab
- `Server Software`      É o nome do servidor web retornado no cabeçalho HTTP do primeiro retorno bem-sucedido.
- `Server Hostname`      É o endereço DNS ou IP fornecido na linha de comando.
- `Server Port`          É a porta à qual ab está se conectando. Se nenhuma porta for fornecida na linha de comando, o padrão será 80 para HTTP e 443 para HTTPS.
- `Document Path`        Este é o URI da solicitação analisado na string da linha de comando.
- `Document Length`      É o tamanho em bytes do primeiro documento retornado com sucesso.
- `Concurrency Level`    Este é o número de clientes simultâneos (equivalente a navegadores web) usados ​​durante o teste.
- `Time Taken for Tests` É o tempo decorrido desde o momento em que a primeira conexão do soquete é criada até o momento em que a última resposta é recebida.
- `Complete Requests`    O número de respostas bem-sucedidas recebidas.
- `Failed Requests`      O número de solicitações que foram consideradas falhas.
- `Total Transferred`    O número total de bytes recebidos do servidor. Este número é essencialmente o número de bytes enviados pela rede.
- `HTML Transferred`     O número total de bytes do documento recebidos do servidor. Este número exclui bytes recebidos em cabeçalhos HTTP
- `Requests per second`  Este é o número de solicitações por segundo. Este valor é o resultado da divisão do número de solicitações pelo tempo total gasto.
- `Time per request`     O tempo médio gasto por solicitação. 
- `Transfer rate`        A taxa de transferência calculada pela fórmula leitura total / 1024 / tempo gasto.


### Cabeçalhos das colunas no arquivo out.data
- `starttime` Esta é a data e hora em que a chamada foi iniciada.
- `seconds`   O mesmo que starttime, mas no formato de carimbo de data/hora Unix.
- `ctime`     Este é o tempo de conexão.
- `dtime`     Este é o Tempo de Processamento.
- `ttime`     Este é o Tempo Total (é a soma de ctime e dtime, matematicamente ttime = ctime + dtime).
- `wait`      Este é o tempo de espera.


## Links
- [https://httpd.apache.org/docs/2.4/programs/ab.html](https://httpd.apache.org/docs/2.4/programs/ab.html)
- [Testes de performance com ApacheBench](https://medium.com/netcoders/testes-de-performance-com-apachebench-5d948d0443b8)
