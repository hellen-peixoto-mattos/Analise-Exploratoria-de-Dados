# Análise Exploratória de Dados de Logística(Loggi)  
## Loggi
Com as informações extraídas do portfólio Loggi Benchmark for Urban Deliveries (BUD) da startup Loggi, foi feita uma análise detalhada, envolvendo visualizações gráficas e insights específicos para o Distrito Federal.<br>      

> Acesse o link do repositório no GitHub: https://github.com/loggi/loggibud 


<br>A figura a seguir ilustra a dimensão do problema para a cidade do Rio de Janeiro. Cada ponto azul representa um ponto de entrega que deve ser alocado a um veículo para que a entrega seja realizada. Veículos pertencem a hubs de distribuição regionais espalhados pela cidade

<div align="center">
<img src="https://github.com/hellen-peixoto-mattos/Analise-Exploratoria-de-Dados/assets/154277472/57186d9f-48c6-4eba-97e8-38b03ce8d535" width="800px" />
</div><br>

> Este projeto foi desenvolvido utilizando as seguintes tecnologias:
- Python
- Google Colab
- Pandas
- Seaborn
- Os
- Visualização de gráficos
- Insights

<br>O dado bruto é um arquivo do tipo JSON com uma lista de instâncias de entregas:
> Onde:
* **name**: uma string com o nome único da instância;
* **region**: uma string com o nome único da região do hub; 
* **origin**: um dict com a latitude e longitude da região do hub;
* **vehicle_capacity**: um int com a soma da capacidade de carga dos veículos do hub;
* **deliveries**: uma list de dict com as entregas que devem ser realizadas.                         

> Sendo que:
* **id**: uma string com o id único da entrega; 
* **point**: um dict com a latitude e longitude da entrega; 
* **size**: um int com o tamanho ou a carga que a entrega ocupa no veículo. 

```json
[
  {
    "name": "cvrp-0-df-0",
    "region": "df-0",
    "origin": {"lng": -47.802664728268745, "lat":-15.657013854445248},
    "vehicle_capacity": 180,
    "deliveries": [
      {
          "id": "ed0993f8cc70d998342f38ee827176dc",
          "point": {"lng": -47.7496622016347,
          "lat": -15.65879313293694},
          "size": 10
      },
      {
          "id": "c7220154adc7a3def8f0b2b8a42677a9",
          "point": {"lng": -47.75887552060412, "lat": -15.651440380492554},
          "size": 10
      },
    ]
  }
]              
