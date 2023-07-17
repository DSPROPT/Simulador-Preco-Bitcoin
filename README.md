[!Geek4Maniacs]()

# Simulação de Preço de Bitcoin

Este script é escrito em Python e utiliza as bibliotecas pandas, numpy, pycoingecko e matplotlib. O principal objetivo do script é simular o preço futuro do Bitcoin ao longo dos próximos 365 dias e calcular os potenciais retornos de um investimento de €10,000.

## Funcionalidades

1. O script começa importando as bibliotecas necessárias: pandas e numpy para manipulação de dados e cálculos, pycoingecko para buscar dados de criptomoedas e matplotlib para visualização de dados.

2. Verifica se a biblioteca pycoingecko está instalada. Se não estiver, o script irá instalá-la.

3. O CoinGeckoAPI é inicializado para recuperar os dados históricos de preço do Bitcoin em Euros nos últimos 1700 dias.

4. Estes dados são convertidos em um DataFrame do pandas, e a coluna 'time' é convertida de milissegundos para um formato de data-hora padrão.

5. O script então calcula o retorno logarítmico diário dos preços do Bitcoin. Este é um método comum usado em finanças para comparar retornos de diferentes ativos, pois normaliza os retornos de preços.

6. O script simula o preço do Bitcoin nos próximos 365 dias usando uma simulação de Monte Carlo. A simulação de Monte Carlo é uma técnica matemática que permite contabilizar o risco na análise quantitativa e na tomada de decisão. Ela fornece um intervalo de possíveis resultados e as probabilidades de ocorrerem para qualquer escolha de ação. Neste caso, é usada para prever futuras ações de preços com base em dados históricos.

7. A simulação é realizada 1000 vezes, com cada simulação criando uma série de preços a partir do último preço conhecido e gerando um novo preço a cada dia com base na mudança diária de preço calculada.

8. Estas simulações são armazenadas num DataFrame, e o script calcula os cenários de preço mais provável, mais alto e mais baixo.

9. O script então plota estes cenários para visualizar as simulações, o cenário de preço mais provável, mais alto e mais baixo para o Bitcoin.

10. Finalmente, o script calcula os retornos potenciais num investimento de €10,000 para cada um destes cenários e imprime-os.

## Importante
Tenha em mente que as previsões são sempre incertas e dependem muito das suposições que você faz, como usar dados históricos para prever retornos futuros. O futuro nem sempre se parece com o passado.

## Dependências
- pandas
- numpy
- pycoingecko
- matplotlib

## Como executar

1. Instale as dependências usando pip:
    ```
    pip install pandas numpy pycoingecko matplotlib
    ```

2. Execute o script:
    ```
    python script_name.py
    ```
Substitua "script_name.py" pelo nome do arquivo que contém o script.

## Contribuições
As contribuições para este projeto são bem-vindas. Sinta-se à vontade para abrir um problema ou fazer um pull request.

## Licença
Este projeto é licenciado sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.
