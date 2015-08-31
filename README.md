#  Mailto Spam Control (msc.js)

Mailto spam control é um script simples para prevenir que _spambots_ capturem um email no mailto link  

[Ver exemplo](http://avelarfortunato.com/msc/mailto-spam-control.html)

### Como Usar
1 *HTML* - Adicione a função `spamControl` ao atributo href do seu link, com os argumentos: usuário e dominio. Adicione também o atributo `rel` com valor `nofollow` para previnir que motores de busca sigam seu link. Exemplo:   
```
<a href='javascript:spamControl("user", "gmail.com")'  rel="nofollow">
```

2 *JS* - Implemente a função `spamControl` que vai ouvir o evento click do link e usar o window.location para retornar a localização do objeto e montar o mailto link:
```
function spamControl(user,domain) {
	getString = ‘mailto:’ + user + ‘@‘ + domain;
	window.location = getString;
}
```  

3 *Conclusão* - O resultado final monta um link de email,`usuario@gmail.com`, no cliente de email padrão.  

Fique a vontade para usar e contribuir com melhorias
