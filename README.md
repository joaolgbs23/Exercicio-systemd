# Exercicio-systemd

## Descrição do problema
Como analista de plantão, preciso gerenciar um serviço (usei o SSH como exemplo): saber se está rodando, pará-lo, investigar o motivo de uma queda, reiniciá-lo e garantir que ele suba sozinho quando a máquina reiniciar.

## Conceito central
Um serviço tem dois estados independentes: se está rodando agora e se sobe no boot.

Caso o serviço esteja rodando naquele momento veremos em verde a tag (running) caso esteja desligado veremos (dead).
Agora falando sobre o boot temos o estado disable ou enable que dizem se este serviço ira ligar junto da maquina, sendo que disable o operador terá que fazer o comando manualmente e o enabled o serviço iniciara dentro do boot.
Para monitorarmos estas tarefas podemos utilizar o status que dá a situação em tempo real e o journalctl que mostra o log (histórico de ações daquele serviço).

## Comandos usados

 ```
systemctl start ssh
systemctl restart ssh
systemctl stop ssh
systemctl enable ssh
systemctl disable ssh
systemctl status ssh
journalctl -u ssh

 ```

## O que cada comando faz
systemctl start ssh: inicia o serviço chamado ssh
systemctl restart ssh: reinicia o serviço 
systemctl stop ssh: para o serviço chamado ssh
systemctl enable ssh: faz com que o serviço seja inciciado junto ao boot
systemctl disable ssh: faz com que o serviço precise ser iniciado manualmente
systemctl status ssh: mostra o atual estado do serviço 
journalctl -u ssh: mostra o log de tudo que aconteceu com o serviço

## O que aprendi

Aprendi a iniciar, reiniciar e parar um serviço, como fazer para subir junto ao boot do computador ou como fazer não iniciar
Além de aprender e identificar erros por log 
