<h1>Tutorial Mini Projeto: Site Híbrido com Astro - Hotel Paraíso</h1>
	<h2>Descrição do objetivo</h2>
		<p>O objetivo deste projeto é demonstrar a utilização do framework Astro no desenvolvimento de um site híbrido, 
		apresentando suas principais características, vantagens e possibilidades de uso. A proposta foi desenvolvida como 
		forma de aplicar, na prática, os conceitos relacionados ao Astro e à arquitetura híbrida de sites, temas abordados 
		na disciplina.<br>
		A abordagem híbrida busca resolver um problema comum no desenvolvimento de sites: encontrar um equilíbrio entre 
		velocidade e interatividade. Sites totalmente estáticos costumam ser muito rápidos, mas possuem limitações quando 
		é necessário adicionar funcionalidades mais interativas. Já os sites totalmente dinâmicos oferecem mais recursos, 
		porém podem consumir mais recursos do sistema e apresentar um desempenho inferior. Os sites híbridos combinam os 
		pontos positivos dessas duas abordagens, permitindo que apenas as partes que precisam de interação sejam dinâmicas.<br>
		Nesse cenário, o Astro se destaca por gerar páginas estáticas por padrão e adicionar recursos dinâmicos somente 
		quando necessário. Isso reduz a quantidade de código executado no navegador, melhora o tempo de carregamento das 
		páginas e proporciona uma experiência mais rápida e agradável para o usuário, principalmente em dispositivos mais 
		simples ou conexões de internet mais lentas.<br>
		Dessa forma, este projeto tem como finalidade demonstrar, na prática, os conceitos de desenvolvimento híbrido 
		utilizando Astro, mostrando como essa tecnologia pode contribuir para a criação de aplicações web mais rápidas, 
		organizadas, escaláveis e eficientes quando comparadas a modelos tradicionais de desenvolvimento.</p>
	<h2>Descrição para instalação dos softwares necessários</h2>
		<h3>1. Instalar o Node.js</h3>
			<p>O Astro depende do Node.js para funcionar. Portanto, o primeiro passo é instalar essa ferramenta.Node.js é um 
			ambiente de execução que permite rodar JavaScript fora do navegador. Além disso, ele instala automaticamente o NPM 
			(Node Package Manager), que será utilizado para baixar bibliotecas e dependências do projeto.<br>Dentro do navegador 
			de internet e acessamos o link: https://nodejs.org, na página inicial, selecionamos a versão recomendada (LTS). Após 
			baixar o arquivo, seguimos as etapas do assistente de instalação, aceitando os termos de uso e avançando pelas telas 
			até iniciar a instalação. Aguardamos a conclusão do processo e finalizamos clicando em "Finish".Após a instalação, 
			abrimos o Prompt de Comando (Windows) e executamos os comandos "node -v" e "npm -v" para verificar se a instalação 
			foi concluída corretamente.Foram exibidas as versões do Node.js e do NPM, confirmando que ambos estavam instalados 
			corretamente e prontos para uso.</P>
	<h2>Passo-a-Passo para o desenvolvimento</h2>
		<h3>Criar uma Pasta e um Projeto Astro</h3>
			<p>Para evitar problemas de sincronização com serviços como OneDrive, criamos os projetos diretamente no disco local. 
			Foi aberto o Prompt de Comando e digitado cd \ para acessar a raiz do disco C. Em seguida, foi criada uma pasta para 
			organizar os projetos com o comando "mkdir Projetos". Após a criação, entrou-se nessa pasta digitando "cd Projetos". 
			Como tudo ocorreu corretamente, o terminal exibiu "C:\Projetos>", indicando que estavamos na pasta onde os projetos 
			seriam armazenados e desenvolvidos.<br>
			Para criar o projeto base do site, foi executado no Prompt de Comando o comando "npm create astro@latest hotel-teste" 
			e pressionado Enter. Esse comando utilizou o Astro para gerar automaticamente todos os arquivos e pastas necessários 
			para iniciar o desenvolvimento. Após a execução, foi aberto um assistente de configuração com algumas perguntas sobre 
			como o projeto deveria ser criado. Durante a criação do projeto, o Astro apresentou perguntas de configuração. Na opção 
			“How would you like to start your new project?”, foi escolhida a opção “Use minimal (empty) template”, utilizando as 
			setas do teclado e pressionando Enter. Esse modelo cria um projeto vazio, ideal para quem deseja aprender e desenvolver 
			o site do zero.<br>
			Em seguida, quando apareceu a pergunta “Install dependencies? (recommended)”, foi selecionada a opção “Yes” para que o 
			Astro instalasse automaticamente as bibliotecas necessárias ao funcionamento do projeto.<br>
			Por fim, quando apareceu a pergunta “Initialize a new git repository?”, foi selecionada a opção “Yes” para criar um 
			repositório Git, permitindo o controle de versões e o acompanhamento das alterações realizadas no projeto ao longo do 
			desenvolvimento.<br>
			Após a criação do projeto, foi acessada a pasta gerada utilizando o comando "cd hotel-teste". Para confirmar que os 
			arquivos haviam sido criados corretamente, foi executado o comando "dir", que exibiu a estrutura do projeto, incluindo 
			arquivos como "package.json", "astro.config.mjs" e as pastas "src" e "public". A presença desses itens indicou que o projeto 
			havia sido configurado com sucesso.<br>
			Para iniciar o ambiente de desenvolvimento, foi executado o comando "npm run dev". O Astro criou um servidor local que 
			permitiu visualizar o site em tempo real durante o desenvolvimento. Após alguns segundos, foi exibida uma mensagem 
			informando que o servidor estava pronto, juntamente com um endereço semelhante a http://localhost:4321/. Em seguida, esse 
			endereço foi aberto no navegador para visualizar o projeto em funcionamento.</p>
		<h3>Abrindo o Projeto no VS Code</h3>
			<p>Após criar o projeto, foi aberto o VS Code e selecionada a opção "Open Folder". Em seguida, navegou-se até a pasta 
			"C:\Projetos\hotel-teste" e clicou-se em Selecionar Pasta para carregar todos os arquivos do projeto no editor.<br>
			Foi observada a estrutura básica do projeto Astro, organizada em algumas pastas principais. A pasta "src" continha o 
			código-fonte do site, enquanto "src/pages" armazenava as páginas da aplicação. Verificou-se também que cada arquivo 
			com extensão ".astro" criado nessa pasta se transformava automaticamente em uma rota do site. Por exemplo, o arquivo 
			"index.astro" correspondia à página inicial (/), enquanto "sobre.astr"o gerava a rota "/sobre".<br>
			Também foi observado que a pasta "public" era utilizada para armazenar arquivos estáticos, como imagens, ícones, 
			documentos e outros recursos que poderiam ser acessados diretamente pelo navegador. Essa organização facilitava o 
			desenvolvimento e a manutenção do projeto.</p>
		<h3>Implementação do Site Híbrido com Astro</h3>
			<p>Após a instalação e configuração do Astro, iniciou-se a estruturação do site do hotel utilizando os recursos oferecidos pelo framework. O primeiro passo foi a criação de um layout principal, localizado na pasta src/layouts. Esse layout foi desenvolvido para armazenar elementos que se repetem em todas as páginas do site, como a barra de navegação (Navbar), o rodapé (Footer), o título da página e a estrutura básica em HTML. Dessa forma, evitou-se a repetição de código, tornando o projeto mais organizado e facilitando futuras alterações.<br>
			Em seguida, foram criadas as páginas do site dentro da pasta src/pages. Cada página foi construída utilizando arquivos com extensão .astro, que permitem combinar HTML, CSS e JavaScript de forma simples. Todas as páginas passaram a utilizar o layout principal por meio da importação do componente Layout.astro, garantindo uma aparência padronizada em todo o sistema. Além disso, foram criados componentes reutilizáveis na pasta src/components, como a Navbar, o Footer e os cartões de quartos, demonstrando uma das principais vantagens do Astro: a reutilização de código.<br>
			Para atender ao requisito de um site híbrido, foi implementada uma funcionalidade dinâmica na página de reservas. Embora a maior parte do site seja estática, oferecendo carregamento rápido e melhor desempenho, a área de reservas utiliza JavaScript para interagir com o usuário em tempo real. Nessa funcionalidade, o visitante pode selecionar uma data, escolher um quarto, informar a quantidade de diárias e visualizar automaticamente o valor total da hospedagem sem a necessidade de recarregar a página. Essa interação caracteriza a parte dinâmica do projeto.<br>
			A página de reservas também foi desenvolvida utilizando recursos do Astro, combinando conteúdo estático com comportamento dinâmico. O JavaScript foi responsável por capturar os valores informados pelo usuário, realizar cálculos automaticamente e exibir uma mensagem de confirmação da reserva. Dessa forma, foi possível demonstrar na prática o conceito de site híbrido: um sistema que mantém a velocidade e simplicidade de páginas estáticas, mas que também oferece interatividade por meio de funcionalidades executadas no navegador.<br>
			Por fim, após a conclusão do desenvolvimento, o projeto foi publicado utilizando a plataforma Vercel. Durante o processo de deploy, foram realizados ajustes na estrutura dos componentes e na organização dos arquivos do Astro para garantir que o sistema fosse compilado corretamente. Com isso, o site ficou disponível online, demonstrando o funcionamento de um projeto desenvolvido com Astro e evidenciando como a arquitetura híbrida permite unir desempenho, organização e interatividade em uma mesma aplicação.</p>
	</h2>