seguindo exemplo daqui: https://developer.adobe.com/commerce/php/tutorials/backend/create-custom-rest-api/

1. Criar pasta em app/code/<org>/<módulo>
2. Criar arquivos padroẽs de módulos: registration.php, etc/di.xml, etc/module.xml
3. Definir interfaces numa pasta Api/ (sugestão: request, response e repositórios necessários
4. Definir modelos implementando as interfaces em Model/Api
5. Mapear endpoints pra módulos em etc/webapi.xml

Detalhes:
- Objetos com interfaces ganham uma Factory gerada automaticamente (se não precisar de funcionalidade específica), esses são passados por injeção de dependência no construtor do ProductRepository do exemplo
- Getters e Setters também não precisam ser especificados pra vários custom_attributes de objetos que implementam a ObjectInterface, por isso no ProductRepository do exemplo o product->getDescription() não existe, mas funciona
