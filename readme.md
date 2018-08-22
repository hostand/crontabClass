# Crontab Class
Classe PHP para visualizar, adicionar, editar e excluir jobs da Crontab no Linux.

## Detalhes
Utilizo nos meus projetos quando há necessidade de controlar tarefas agendadas via Cron.

## Testes
Testada com sucesso com PHP 5.6+ em Apache 2.4/Linux Ubuntu

## Exemplos de uso 
- Inicializando a classe
``` php
<?php 

$cron = new Crontab();

?>

``` 
- getJobs() -- Retorna um array de tarefas agendadas (cronjobs) existentes. Cada item do array é uma string (cronjob).
``` php
<?php 

$crontabl = $cron->getJobs();

print_r($crontabl);


?>
```    
- saveJobs($jobs = array()) -- Salve o array $jobs com as tarefas agendadas no crontab para que elas sejam executadas pelo servidor. Atenção pois ela irá sobreescrever a Crontab e todos os jobs existentes no são apagados e substituídos pelo conteúdo do array $jobs.

- doesJobExist($job = '') -- Verifica se um job existe. Passar na variável $job a sintaxe da entrada na Crontab.

- addJob($job = '') -- Adiciona uma nova entrada (job) na Crontab.

- removeJob($job = '') -- Remove um job da Crontab. 

