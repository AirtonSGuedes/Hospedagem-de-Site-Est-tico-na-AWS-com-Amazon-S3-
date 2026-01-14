# 🌐 Site Estático Hospedado no Amazon S3 (AWS Free Tier)

Este projeto apresenta a implementação de um site estático hospedado no Amazon S3, utilizando exclusivamente serviços compatíveis com a AWS Free Tier. A solução faz uso da infraestrutura serverless da AWS, eliminando a necessidade de servidores e garantindo baixo custo, simplicidade e alta disponibilidade.

O site está acessível publicamente por meio do endpoint de hospedagem estática do Amazon S3.

## Visão Geral do Projeto

Para a conclusão deste projeto, foi necessário criar e configurar um bucket do Amazon S3 para hospedagem de site estático, ajustar permissões de acesso público de forma controlada, configurar usuários e políticas no AWS Identity and Access Management (IAM), publicar arquivos HTML, CSS e imagens no bucket e habilitar o recurso de Static Website Hosting do S3. Também foi implementado um mecanismo de atualização do site para facilitar manutenções futuras.

O resultado final é um site funcional, acessível via navegador, hospedado integralmente na nuvem da AWS.

## Arquitetura Utilizada

A arquitetura do projeto é simples e eficiente, composta principalmente pelo Amazon S3 para armazenamento e hospedagem do site estático e pelo AWS IAM para gerenciamento de permissões e segurança. Todos os recursos utilizados estão dentro dos limites da AWS Free Tier.

## Estrutura do Projeto

O projeto está organizado com um diretório principal contendo os arquivos do site estático, incluindo a página principal em HTML, arquivos de estilo CSS e imagens. Também há um script responsável por automatizar a atualização do conteúdo publicado no Amazon S3, além do arquivo README para documentação.

## Segurança e Permissões

Durante o desenvolvimento do projeto, foi criado um usuário IAM dedicado exclusivamente às operações relacionadas ao Amazon S3. A esse usuário foi atribuída uma política gerenciada que concede acesso completo ao serviço S3. As permissões do bucket foram ajustadas para permitir acesso público apenas aos objetos necessários para o funcionamento do site, seguindo boas práticas de segurança e separação de responsabilidades.

## Publicação e Acesso ao Site

Após a publicação dos arquivos no bucket e a ativação da hospedagem de site estático, o site passou a ficar disponível publicamente através do endpoint padrão do Amazon S3 no formato:  
http://<nome-do-bucket>.s3-website-us-west-2.amazonaws.com

Esse endpoint permite que qualquer usuário acesse o site diretamente pelo navegador.

## Atualização e Manutenção

Para facilitar a manutenção do site, foi criado um script de atualização que permite sincronizar as alterações realizadas localmente com o conteúdo hospedado no Amazon S3. Esse processo torna a atualização do site mais rápida, reduz erros manuais e melhora a produtividade durante alterações frequentes no conteúdo.

## Otimização do Processo de Deploy

O processo de deploy foi otimizado para evitar o envio desnecessário de arquivos que não sofreram alterações, reduzindo o tempo de publicação e o consumo de recursos. Essa abordagem torna a solução mais eficiente e adequada para ambientes reais, mesmo em projetos simples.

## Custos

Este projeto utiliza apenas serviços compatíveis com a AWS Free Tier, não exigindo a execução contínua de instâncias EC2, uso de bancos de dados ou serviços pagos adicionais. Isso torna a solução ideal para sites institucionais simples, portfólios pessoais e landing pages.

## Principais Aprendizados

Com este projeto, foi possível consolidar conhecimentos sobre hospedagem de sites estáticos na AWS, uso do Amazon S3 como solução serverless, gerenciamento de permissões com IAM, automação de atualizações de conteúdo e aplicação de boas práticas em cloud computing.

## Licença

Este projeto foi desenvolvido para fins educacionais e demonstrativos.
