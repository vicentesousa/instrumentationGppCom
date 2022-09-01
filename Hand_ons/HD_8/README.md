# **Hands-On 8: Marcadores.**

Os HSAs N934xC têm, cada um, um total de seis marcadores que podem ser usados ​​em modo normal ou em modo delta. Além da tabela de marcadores e pesquisa de pico, cada N934xC HSA também possui um
recurso de tabela de picos que pesquisa automaticamente 10 sinais de pico máximo ou mínimo simultaneamente e é atualizado após cada varredura.

Nesta demonstração, usaremos a tabela de picos para encontrar os valores absolutos do sinal FM
das bandas laterais.

## Etapas para a USRP:

Com o auxílio de um Universal Software Radio Peripheral (USRP) e atrvés dos sotware GNURadio, defina uma frequência central de 2 GHz, amplitude -10 dBm, desvio de 100 kHz, taxa de 30 kHz, sinal FM.

- (Conferir o circuito com GNURadio)

![](/Imagens/HD8/gnuradiocircuit.png)

## Etapas para os marcadores:

- **1.** Selecione **Freq**

![](/Imagens/Teclas/freq.png)

- **2.** Coloque o valor de **2**

- **3.** Selecione para medir em **GHz**

Com isso, você selecionou a frequência 2 GHz. 

- **4.** Aperte em **Span**

![](/Imagens/Teclas/span.png)

- **5.** Coloque o valor de **500**

- **6.** Selecione para **KHz**

Com isso, você ajustou o span para que o sinal preencha a tela.

- **7.** Aperte em **Amptd**

![](/Imagens/Teclas/ampld.png)

- **8.** Coloque em **Ref Level**

- **9.** Utilize a numeração **10** e coloque para **dBm**

- **10.** Aperte em **Shift** e logo logo em seguida aperte em **Peak**

![](/Imagens/Teclas/shift.png)

![](/Imagens/Teclas/marker.png)

- **11.** Pressione a opção **Peak Search**

Para medir a amplitude de pico absoluta das bandas laterais FM usando os picos da
tabela de pesquisa.

- **12.** Pressione a opção **More 1 of 2**, depois em **Peak Table** e finalmente em **Peak Table On**

Sua tela deverá ser semelhante a tela abaixo:

![](/Imagens/HD8/telapicos.png)

Para desativar a tabela, bastar realizar o seguinte procedimento:

- **13.** Selecione **Shift** e depois pressione a opção **Peak**

![](/Imagens/Teclas/shift.png) 

![](/Imagens/Teclas/marker.png)

- **14.** Depois, utilize as opções em sequência **More 1 of 2**, **Peak Table** e **Peak Table Off**

___

**OBS 1:** Enquanto a tabela está ativa, é possível mudar o critério dos marcadores

[Shift], [Peak], {More 1 of 2}, {Peak Criterion}, o usuário pode definir o limite de pico
limite, limite de excursão de pico e tipo de pico.

**OBS 2:** Eqnaunto a tabela a tabela está ativa, é possível exportar os dados para uma tabela CSV.

[Shift], [Peak], {More 1 of 2}, {Peak Table}, {Export Table to CSV}, input file 
name, [Enter].

Videos Relacionados:

- 
- 