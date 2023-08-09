/_SELETOR: NOT_/
No CSS para remover botões da tela. Através de modificações no arquivo style.css, os botões são estilizados com base em classes como .running e .music-on. Isso permite ocultar ou exibir os botões de acordo com o estado do temporizador, melhorando a interação com o aplicativo.

/_SR ONLY_/
O objetivo é tornar a experiência mais inclusiva para usuários com deficiência visual, proporcionando uma melhor compreensão dos botões por meio de recursos de leitura de tela.

Ao aplicar o diff do código fornecido, podemos observar as modificações feitas nos arquivos index.html e style.css.

No arquivo index.html, foi adicionada a classe sr-only às tags <span> dentro dos botões. Essa classe é utilizada para ocultar visualmente o texto dos botões, mas ainda assim torná-lo disponível para leitura de tela. Além disso, foram adicionadas descrições acessíveis para cada botão, como "Ativar / desativar light mode", "Iniciar contador", "Pausar contador", "Ajustar contador", "Reiniciar contador", "Iniciar música" e "Parar música".

No arquivo style.css, foi criada uma classe .sr-only para estilizar os elementos com a classe correspondente. Essa classe define propriedades como largura e altura de 1 pixel, posicionamento absoluto, efeitos de margem e preenchimento negativos, além de remover a aparência padrão do elemento. Essas propriedades garantem que o conteúdo seja ocultado visualmente, mas permaneça acessível para leitores de tela.

Essas modificações visam garantir que os botões sejam adequadamente identificados e entendidos pelos usuários com deficiência visual, melhorando a experiência de acessibilidade do aplicativo FocusTimer.

/_estado da aplicação_/

será criado um novo arquivo chamado state.js no diretório FocusTimer, que irá exportar um objeto contendo as propriedades do estado da aplicação. Esse objeto incluirá informações como os minutos, segundos, status de execução e o status de mudo do timer.

No arquivo index.js, importaremos o módulo state e utilizaremos as propriedades minutes e seconds para atualizar o estado do timer quando a função start for chamada. Através do objeto state, teremos acesso às informações atualizadas do timer, permitindo que possamos manipulá-las e realizar operações de controle.

O resultado dessa aula é a criação do arquivo state.js no diretório FocusTimer, contendo um objeto que representa o estado da aplicação. Além disso, no arquivo index.js, utilizamos o estado para atualizar as propriedades minutes e seconds ao chamar a função start, e em seguida, imprimimos o estado atualizado no console.

/_Dataset para controle das ações_/

aprenderemos a utilizar o atributo data dos elementos HTML para controlar as ações dos botões. O objetivo é associar um valor personalizado a cada botão para identificar a ação correspondente quando um botão for clicado.

Durante a aula, faremos modificações no arquivo index.html. Adicionaremos o atributo data-action a cada botão, atribuindo um valor específico para indicar a ação correspondente. Por exemplo, definiremos data-action="toggleRunning" para o botão de iniciar e pausar o contador, data-action="set" para o botão de ajustar o contador e assim por diante.

No arquivo events.js, faremos modificações para capturar o valor do atributo data-action quando um botão for clicado. Utilizaremos a propriedade dataset do elemento alvo do evento para obter o valor do atributo data-action. Em seguida, realizaremos um console.log para exibir a ação correspondente no console.

O resultado dessa aula é a adição do atributo data-action a cada botão no arquivo index.html e a modificação da função registerControls no arquivo events.js para capturar e exibir a ação correspondente quando um botão for clicado.

/_Conectando as primeiras ações_/

Nesta aula do projeto FocusTimer, aprenderemos a conectar as primeiras ações aos eventos dos botões. O objetivo é fazer com que as ações correspondentes sejam executadas quando um botão for clicado.

Durante a aula, criaremos um novo arquivo chamado actions.js no diretório FocusTimer. Nesse arquivo, implementaremos a função toggleRunning que será responsável por alternar a execução do timer. No exemplo fornecido, a função simplesmente exibirá uma mensagem no console para indicar que a ação foi acionada.

No arquivo events.js, faremos modificações para importar o módulo actions que contém as funções de ação. Em seguida, atualizaremos a função registerControls para executar a ação correspondente quando um botão for clicado. Utilizaremos a ação como uma chave para obter a função correspondente do objeto actions e chamá-la.

O resultado dessa aula é a criação do arquivo actions.js com a função toggleRunning, e a modificação da função registerControls no arquivo events.js para executar a ação correspondente quando um botão for clicado.

/_Alterando o estado da aplicação conforme a ação_/

Nesta aula do projeto FocusTimer, aprenderemos a alterar o estado da aplicação conforme a ação realizada pelo usuário nos botões. O objetivo é modificar o estado do timer e controlar a aparência do aplicativo com base nas ações executadas.

O resultado dessa aula é a modificação do arquivo actions.js, adicionando as implementações das funções toggleRunning, reset, set e toggleMusic, que alteram o estado do timer e controlam as classes CSS correspondentes.

Essas modificações permitem que o estado da aplicação seja atualizado conforme as ações realizadas pelos usuários nos botões, proporcionando uma experiência interativa e visualmente coerente no projeto FocusTimer.

/_Atualizando o display do contador_/

Nesta aula do projeto FocusTimer, aprenderemos a atualizar o display do contador para exibir o tempo restante de forma adequada. O objetivo é garantir que os minutos e segundos sejam exibidos corretamente no formato de dois dígitos, preenchendo com zero à esquerda, quando necessário.

Durante a aula, faremos modificações nos arquivos elements.js, index.js e criaremos um novo arquivo chamado timer.js.

No arquivo elements.js, adicionaremos as constantes minutes e seconds, que correspondem aos elementos HTML onde o tempo restante será exibido.

No arquivo index.js, importaremos o módulo timer e chamaremos a função updateDisplay logo após definir os valores iniciais dos minutos e segundos. Isso permitirá que o display seja atualizado de acordo com os valores iniciais do contador.

No arquivo timer.js, criaremos a função updateDisplay, que recebe os parâmetros minutes e seconds. Essa função atualiza os elementos el.minutes e el.seconds (obtidos do arquivo elements.js) com o tempo atualizado do contador. Os valores de minutos e segundos são padronizados para dois dígitos, preenchendo com zero à esquerda, usando o método padStart.

O resultado dessa aula é a criação do arquivo timer.js, contendo a função updateDisplay, e as modificações nos arquivos elements.js e index.js. Agora, o display do contador será atualizado corretamente com os valores dos minutos e segundos.

/_Estruturando o countdown_/

Nesta aula do projeto FocusTimer, aprenderemos a atualizar o display do contador para exibir o tempo restante de forma adequada. O objetivo é garantir que os minutos e segundos sejam exibidos corretamente no formato de dois dígitos, preenchendo com zero à esquerda, quando necessário.

Durante a aula, faremos modificações nos arquivos elements.js, index.js e criaremos um novo arquivo chamado timer.js.

No arquivo elements.js, adicionaremos as constantes minutes e seconds, que correspondem aos elementos HTML onde o tempo restante será exibido.

No arquivo index.js, importaremos o módulo timer e chamaremos a função updateDisplay logo após definir os valores iniciais dos minutos e segundos. Isso permitirá que o display seja atualizado de acordo com os valores iniciais do contador.

No arquivo timer.js, criaremos a função updateDisplay, que recebe os parâmetros minutes e seconds. Essa função atualiza os elementos el.minutes e el.seconds (obtidos do arquivo elements.js) com o tempo atualizado do contador. Os valores de minutos e segundos são padronizados para dois dígitos, preenchendo com zero à esquerda, usando o método padStart.

O resultado dessa aula é a criação do arquivo timer.js, contendo a função updateDisplay, e as modificações nos arquivos elements.js e index.js. Agora, o display do contador será atualizado corretamente com os valores dos minutos e segundos.

/_Logica do countdown_/

Nesta aula do projeto FocusTimer, implementamos a lógica do countdown, que consiste na contagem regressiva dos minutos e segundos do timer.

No arquivo actions.js, adicionamos a chamada da função updateDisplay no método reset, para atualizar o display quando o timer for resetado.

No arquivo timer.js, implementamos a função countdown que decrementa os valores de minutos e segundos a cada segundo. Se os segundos chegam a zero, decrementamos os minutos e ajustamos os segundos para 59. Se os minutos chegam a zero, chamamos a função reset para encerrar o countdown.

Essas modificações permitem que o projeto FocusTimer execute a contagem regressiva corretamente, atualizando o display do contador e finalizando a contagem quando o tempo definido for atingido.

/_Alterando contéudo de uma tag com contenteditable_/

Na aula, aprenderemos a utilizar o atributo contenteditable para permitir que o usuário edite o conteúdo de uma tag específica. O objetivo é proporcionar uma forma interativa para o usuário personalizar o tempo exibido no contador.

Durante a aula, faremos modificações no arquivo actions.js.

No arquivo actions.js, adicionaremos a função set para habilitar a edição do conteúdo dos minutos. Utilizaremos o método setAttribute para definir o atributo contenteditable como true na tag dos minutos, possibilitando que o usuário possa editar esse valor.

O resultado dessa aula é a adição da função set no arquivo actions.js, que habilita a edição do conteúdo dos minutos por meio do atributo contenteditable.

Essa modificação permite que o projeto FocusTimer ofereça a funcionalidade de edição interativa do tempo, proporcionando ao usuário a capacidade de personalizar os valores exibidos no contador de forma flexível.

/_Limpando o conteúdo de uma tag com evento de focus_/

Nesta aula, aprendemos a limpar o conteúdo de uma tag quando ela recebe o foco do usuário. Fizemos alterações nos arquivos actions.js, events.js e index.js.

No arquivo actions.js, adicionamos o método focus() à função set() para que o campo dos minutos receba automaticamente o foco quando ativado.

No arquivo events.js, criamos a função setMinutes() para adicionar um ouvinte de evento de foco à tag dos minutos. Quando o campo recebe o foco, o conteúdo existente é limpo, deixando-o em branco para que o usuário possa inserir um novo valor.

No arquivo index.js, chamamos a função setMinutes() na função start() para registrar o evento de foco e limpar o conteúdo dos minutos.

Essas modificações permitem uma melhor experiência do usuário, tornando mais fácil a inserção de novos valores nos minutos, pois o conteúdo existente é apagado automaticamente quando o campo é ativado.

/_Aceitando apenas números no contador_/

Nesta aula do projeto FocusTimer, implementamos a funcionalidade que permite apenas a inserção de números no campo dos minutos do contador. Para isso, adicionamos um manipulador de evento onkeypress ao campo dos minutos no arquivo events.js.

Com essa modificação, garantimos que apenas números sejam aceitos como entrada no campo dos minutos, impedindo a inserção de caracteres não numéricos. Isso ajuda a manter a integridade dos dados e a coerência das informações inseridas no contador.

/_Finalizando a escolha dos minutos do temporizador_/

Nesta aula, concluímos a funcionalidade de seleção dos minutos para o temporizador. Realizamos alterações no arquivo events.js para finalizar a escolha dos minutos.

No arquivo events.js, importamos o módulo state para acessar o estado da aplicação e o módulo updateDisplay para atualizar a exibição do contador. Também adicionamos um manipulador de evento blur ao campo dos minutos.

Quando o campo dos minutos perde o foco (evento blur), capturamos o valor inserido pelo usuário. Em seguida, verificamos se o valor é maior que 60, pois o temporizador só suporta até 60 minutos. Caso seja maior, definimos o valor como 60.

Atualizamos o estado da aplicação com os minutos escolhidos e os segundos definidos como zero. Em seguida, chamamos a função updateDisplay para refletir as alterações na exibição do contador.

Por fim, removemos o atributo contenteditable do campo dos minutos para impedir edições posteriores.
