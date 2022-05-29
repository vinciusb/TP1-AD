# PDI
&ensp;&ensp;&ensp;&ensp;O [PDI](https://help.hitachivantara.com/Documentation/Pentaho/9.3/Products/Pentaho_Data_Integration) é o Pentaho Data Integration, uma ferramenta de ETL também conhecida como KETTLE. O PDI é dividido em 3 partes principais: Spoon, Kitchen e Pan.

</br>  

## Spoon
>&ensp;&ensp;&ensp;&ensp;O Spoon é uma ferramenta que permite os desenvolvedores criarem transformations e jobs através de uma interface visual e componentes visuais.  
>
>&ensp;&ensp;&ensp;&ensp;Transformations se referem a processos de extração, processamento e carregamento de dados.  
>
>&ensp;&ensp;&ensp;&ensp;Jobs são usados pra coordenarem as fontes, dependencias e execuções das atividades e transformações do ETL.

* ### Vars
  É possível definir variaveis do sistema para serem acessados por qualquer job ou transformation. Para fazer isso basta acessar o arquivo
  `C:\Users\<username>\.kettle\kettle.properties` e adicionar uma variavel no seguinte formato:
  * `VAR_NAME=VAR_VALUE` como por exemplo `PROJ_ROOT=D:/Users/vinic/Documents/UFMG/Semestres/4_semestre/AD/TP1/Exemplo`

* ### Steps
  &ensp;&ensp;&ensp;&ensp;Um step é uma unidade de processamento de uma transformation. A imagem a seguir apresenta 2 steps, um leitor de arquivo CSV e uma step que executa alguma formula em específico.  
  </br><img src="./img/Steps.png"></br>  
* ### Hops  
  &ensp;&ensp;&ensp;&ensp;Hops são o que liga steps e job entries entre si criando o caminho de dados do processo. Na imagem anterior é possível ver um hop, que no Spoon é representado por uma seta indicando o fluxo de onde a informação sai e para onde a informação vai.  
  &ensp;&ensp;&ensp;&ensp;Os Hops podem ser de 3 tipos: Unconditional, Follow when result is true and Follow when result is false. A imagem a seguir apresenta os 3.  
  </br><img src="./img/Hops.png"></br>  
  &ensp;&ensp;&ensp;&ensp;Embora os hops deem uma sensação que a execução dos steps se deem na ordem indicada por seu fluxo, isso nem sempre é verdade pois quase sempre serão executados em paralelo.
* ### Job Entries
  &ensp;&ensp;&ensp;&ensp;Job Entries são a menor unidade de processamento de um Job. Portanto, Job Entries podem ser tanto Steps como Transformations em si.

</br>  

## Kitchen
>&ensp;&ensp;&ensp;&ensp;A Kitchen é uma versão CLI (Command Line) do PDI. Com essa ferramenta é possível rodar tarefas e jobs através de qualquer command prompt ou terminal.  
* `Um exemplo de execução no Windows:`
  ```
  D:
  cd D:\Users\vinic\Documents\UFMG\Semestres\4_semestre\AD\TP1\Exemplos 
  C:\PDI_pentaho\data-integration\Kitchen.bat /file Hello.kjb list /norep  
  ```  
  O formato do comando é:  
    * `PDI_PATH\Kitchen.bat /file <job or transformation file> <arguments> /norep`  
    Onde /norep significa que não se deseja conectar no repositório

  </br>
## Instalação
* Para instalar o PDI clique [aqui](https://www.ericknishimoto.com.br/como-instalar-o-pentaho-data-integration-pdi-no-windows/) e siga o tutorial.

* Para instalar o Pentaho server, caso desejado, basta baixar o [pentaho-server-ce](https://sourceforge.net/projects/pentaho/files/Pentaho-9.3/server/) (que é a Comunity Edition).