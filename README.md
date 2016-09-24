#  Mailto Spam Control (msc.js)

Mailto spam control é um script simples para prevenir que _spambots_ capturem um email no mailto link  

[Ver exemplo](http://avelarfortunato.com/msc/msc.html)  
[Blog Post](https://medium.com/@avelarfortunato/2-truques-para-evitar-spam-em-seu-site-d2cd0b858479)

### Como Usar
1 *HTML* - Chame a função `spamControl` ao atributo href do seu link, com os argumentos: usuário e dominio. Adicione também o atributo `rel` com valor `nofollow` para previnir que motores de busca sigam seu link. Exemplo:   
```
<a href='javascript:spamControl("user", "gmail.com")'  rel="nofollow">
```

2 *JS* - A função `spamControl` vai ouvir o evento de click do link e usar o window.location para retornar a localização do objeto e montar o mailto link:
```
function spamControl(user,domain) {
	getString = ‘mailto:’ + user + ‘@‘ + domain;
	window.location = getString;
}
```  
3 *Conclusão* - O resultado final monta um link de email,`user@gmail.com`, no cliente de email padrão.  

Fique a vontade para usar e contribuir com melhorias
