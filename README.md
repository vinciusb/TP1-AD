# PDI
O [PDI](https://help.hitachivantara.com/Documentation/Pentaho/9.3/Products/Pentaho_Data_Integration) é o Pentaho Data Integration, uma ferramenta de ETL, também conhecida como KETTLE. O PDI é dividido em 3 partes principais: Spoon, Kitchen e Pan.

</br>  

## Spoon
>O Spoon é uma ferramenta que permite os desenvolvedores criarem transformations e jobs através de uma interface visual user friendly.  
>
>Transformations se referem a processos de extração, processamento e carregamento de dados.  
>
>Jobs são usados pra coordenarem as fontes, dependencias e execuções das atividades e transformações do ETL.

### Vars
`C:\Users\<username>\.kettle\kettle.properties`  
Só é carregado quando o Spoon é aberto.

Hop podem ser de 3 tipos: Incodicionais, ....  
Job Entry

</br>  

## Kitchen
>A Kitchen é uma versão CLI (Command Line) do PDI. Com essa ferramenta é possível rodar tarefas e jobs através de qualquer command prompt ou terminal.  
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