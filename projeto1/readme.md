# projeto iot com esp32, dht22 e mqtt

este projeto utiliza um esp32 com sensor dht22 para monitorar temperatura e umidade em tempo real, enviando os dados para um broker mqtt. a leitura pode ser visualizada por meio de um painel web ou outra aplicação cliente mqtt.

##  componentes utilizados

- esp32
- sensor dht22
- jumpers
- conexão wi-fi

##  bibliotecas necessárias (arduino ide)

- `wifi.h`
- `pubsubclient.h`
- `dht.h`

instale a biblioteca do dht e do pubsubclient pela **gerenciador de bibliotecas** da arduino ide.

##  como funciona

1. o esp32 conecta ao wi-fi.
2. lê os dados do sensor dht22.
3. publica os dados nos tópicos mqtt:

   - `meuprojeto/temperatura`
   - `meuprojeto/umidade`

4. os dados podem ser acessados por clientes mqtt (como um painel web ou aplicativo).

##  tópicos mqtt usados

- `meuprojeto/temperatura` → valor da temperatura em °c
- `meuprojeto/umidade` → valor da umidade em %

##  configuração no código

edite essas variáveis com suas informações de rede:

```cpp
const char* ssid = "*
