# ContaE app

## Iniciar o aplicativo

Execute os comandos dentro da pasta `contae-app`:

```bash
npm install
npm start
```

O comando `npm start` inicia o Expo e mostra as opções para abrir o app no
Expo Go, emulador Android, simulador iOS ou navegador.

## Conexão com a API

O dashboard consulta `http://10.141.246.75:8000/api/transas`. Inicie o Laravel
na pasta da API, acessível pela rede local:

```bash
php artisan serve --host=0.0.0.0 --port=8000
```

O endereço IP configurado no dashboard precisa continuar sendo o IP atual do
computador na mesma rede do dispositivo. A API usa a tabela `transas`; o campo
`desc` do banco é apresentado como `descricao` para o app. Atualmente, a tabela
não possui vínculo com `users`.

Para conferir a conexão MySQL e o estado das migrations, execute na pasta da
API:

```bash
php artisan db:show
php artisan migrate:status
```
