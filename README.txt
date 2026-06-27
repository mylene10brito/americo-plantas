MeuSistema - Distribuicao Windows
=================================

Como executar
-------------
1. Abra esta pasta no Windows.
2. Execute o arquivo:

   MeuSistema.exe

Nao e necessario instalar Java no computador de destino. Esta distribuicao foi
gerada com jpackage e inclui uma runtime Java propria na pasta "runtime".

Como distribuir
---------------
Copie a pasta "dist" inteira para o computador de destino, mantendo esta
estrutura:

  dist/
    MeuSistema.exe
    app/
      AmericoPlantasMedicinais.jar
      MeuSistema.cfg
    runtime/
      ...
    README.txt

Nao mova apenas o arquivo MeuSistema.exe isoladamente, pois ele precisa das
pastas "app" e "runtime" ao lado dele.

Detalhes tecnicos
-----------------
- Empacotador usado: jpackage.
- Classe principal configurada: Main.
- JAR principal: AmericoPlantasMedicinais.jar.
- Runtime incorporada: Java 26.0.1.
- Interface: Java Swing, sem console do Windows.
- Bibliotecas e recursos: incluidos no JAR principal, incluindo driver MySQL,
  Jakarta Mail/Activation e img/logo.jpeg.

Observacao de compatibilidade
-----------------------------
O JAR recebido foi compilado com class file version 70.0, equivalente a Java 26.
Por isso a runtime incorporada tambem e Java 26. Para gerar uma distribuicao
com runtime Java 17, seria necessario recompilar o projeto original a partir dos
arquivos-fonte usando Java 17 ou a opcao --release 17.

