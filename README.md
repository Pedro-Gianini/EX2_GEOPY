#Solução dos exercícios da segunda aula do curso GeoPY

Bibliotecas usadas:
shapely.geometry ; re ; shapely.geometry ; matplotlib.pyplot ; pandas ; contextily ; numpy

Funções usadas:
re.split ; import Polygon ; .set_crs ; .to_file ; .plot(ax=ax) ; .savefig ; txt_path ; import LineString ; import MultiLineString
index() ; read() ; .loc ; .head() ; cx.add_basemap ; min() ; max() ; mean()

Conteúdos abordados :
Leitura de arquivos do google drive usando a função read(); manipulaçãoe quebra do arquivo de texto usando a função re.split(r'[\[\]]',conteudo) ;
Criação loops usando a função index(); plotagem de geometrias Linhas e Polígonos; plotagem de mapas usando a matplotlib.pyplot;
Conversão e Adição de colunas ao Geodataframe; Converteção e definição dos sistema de coordenadas usando a função set_crs;
Salvar shapefiles pelo comando to_file('nome do arquivo'); Medindo a distância mínima, máxima e a média com o uso das fuções min(), max() e numpy.mean().

