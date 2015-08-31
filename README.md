#  Mailto Spam Control (msc.js)

Função simples para prevenir que _spambots_ capturem um email
Fique a vontade para usar e contribuir com melhorias

[Ver exemplo](http://avelarfortunato.com/mailto-spam-control/mailto-spam-control.html)

### Como Usar
1 (HTML) Chame a função `spamControl` no atributo href da sua link tag, com 2 argumentos: o primeiro é o usuário e o segundo o dominio. Exemplo:
`<a href=‘javascript:spamControl(“usuario”, “gmail.com”)’ rel=“nofollow”>`

2 (JS) No JS adicione a declaração a seguir:
```
function spamControl(usuario,domino) {
	getString = ‘mailto:’ + usuario + ‘@‘ + domino;
	window.location = getString;
}
```

3 (Teste) O resultado final deve montar um mailto link `usuario@gmail.com` no do cliente de email padrão.