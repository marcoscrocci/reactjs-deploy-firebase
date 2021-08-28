# Como publicar um Website React no Host do Firebase

	- Criar um projeto Reactjs:
npx create-react-app react-deploy-firebase

cd react-deploy-firebase


	- Criar um novo projeto no site do Firebase:
https://console.firebase.google.com/

	- Instalar o Firebase Tools globalmente no computador:
npm install firebase-tools -g

	- Efetuar a autenticação no Firebase pelo console:
firebase login

	- Efetuar a autenticação no navegador quando solicitado.
	
	- Gerar os arquivos estáticos do projeto para produção (este comando deve gerar a pasta build):
npm run build

	- Inicializar o projeto Firebase dentro do projeto Reactjs:
firebase init

	- Selecionar as opções:
	· Hosting: Configure and deploy Firebase Hosting sites (pressionando tecla espaço)
	→ Use an existing project (nesta etapa também será possível criar um novo projeto pelo console)
	→ reactjs-deploy-firebase (projeto que eu criei previamente no site do Firebase)
	→ What do you want to use as your public directory? build (trocar public por build)
	→ Configure as a single-page app (rewrite all urls to /index.html)? Yes
	→ Set up automatic builds and deploy with GitHub? No
	→  File build/index.html already exists. Overwrite? N

	- Se o firebase não perguntar sobre qual projeto será utilizado, selecionar com o comando (deve ser o Project ID):
firebase use reactjs-deploy-firebase

	- Efetuar o deploy do projeto para o Firebase:
firebase deploy

	- Acessar o site que foi gerado no Firebase com o deploy:
https://reactjs-deploy-firebase.web.app/

Fonte - Youtube: Fast React Website Deployment With Firebase


---


