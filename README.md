## Solução dos exercícios da segunda aula do curso GeoPY

Bibliotecas usadas:
geopandas ; shapely.geometry ; google.colab ; re ; shapely.geometry ; matplotlib.pyplot ; pandas ; contextily ; numpy

Funções aprendidas:



dados.iterrows()
re.split ; import Polygon ; .set_crs ; .to_file ; .plot(ax=ax) ; .savefig ; gpd.GeoDataFrame() ; gdf['geometry']=None ; gdf.loc[0,'geometry']=plg ; gdf.to_file() ; gdf.set_crs(crs='epsg:29183') ; txt_path ; import LineString ; import MultiLineString
index() ; read() ; .loc ; .head() ; cx.add_basemap ; min() ; max() ; mean()

Conteúdos abordados :
# Exercício 1 #
Este código tem como objetivo criar um polígono a partir de uma lista de coordenadas, inserir o polígono em um geodataframe, salvar o polígono em um shapefile e plotar e salvar uma figura do polígono. 
Primeiro, o código monta o acesso ao Google Drive e instala a biblioteca Geopandas. Em seguida, é definido o local em que o arquivo com as coordenadas está localizado e o arquivo é aberto e lido. Para manipular o arquivo, é importada a biblioteca re para operações com operações regulares (regex). É utilizada a função `re.split` para quebrar o texto em múltiplos subtextos, onde a quebra é feita onde houver o símbolo `[` e o símbolo `]`. 
Depois, é usado um loop para verificar em quantos e quais itens o texto foi subdividido. As coordenadas de x e y são obtidas e transformadas em números decimais. As coordenadas são combinadas em tuplas para gerar o polígono. 
Em seguida, é criado um GeoDataFrame, uma coluna padrão para geometrias é adicionada e a geometria do polígono é inserida na primeira linha da coluna `geometry`. Depois, é conferido o sistema de coordenadas e definido o sistema de coordenadas. O GeoDataFrame é exportado para um shapefile e plotado, sendo que a figura é salva como uma imagem jpg.

# Exercício 2 #
Este código consiste em criar pontos a partir de um conjunto de dados e plotá-los em um mapa. O código é dividido em várias etapas:
- Os dados são lidos a partir de um arquivo CSV usando a biblioteca pandas.
- Uma coluna vazia chamada "geometry" é criada no dataframe.
- Para cada registro do dataframe, é criado um objeto do tipo LineString que conecta a origem e o destino da escooter, e esse objeto é armazenado na coluna "geometry".
- O dataframe é convertido em um Geodataframe e é definido um sistema de coordenadas (Lat Long WGS84) para ele.
- O Geodataframe é salvo como um shapefile.
- É criada uma figura com um mapa de fundo usando as bibliotecas matplotlib e contextily. As linhas das escooters são adicionadas ao eixo de plotagem e o mapa de fundo é adicionado usando o contexto do contextoily.

# Exercício 3 #
O código tem como objetivo calcular a distância percorrida por patinetes elétricos. Primeiramente, o Geodataframe é reprojetado para o sistema de coordenadas EPSG:32612 (UTM Zona 12N), para que seja possível calcular as distâncias em metros. 
Em seguida, uma coluna vazia chamada "dist" é criada para armazenar as distâncias percorridas. O loop "for" itera sobre cada linha do Geodataframe, calculando o comprimento das linhas entre origem e destino e armazenando o resultado na coluna "dist". 
Após o cálculo das distâncias, o código extrai a menor, a maior e a média das distâncias percorridas pelos patinetes elétricos. A distância mínima e máxima são calculadas utilizando as funções "min" e "max", enquanto a distância média é calculada utilizando a função "mean" da biblioteca NumPy.
