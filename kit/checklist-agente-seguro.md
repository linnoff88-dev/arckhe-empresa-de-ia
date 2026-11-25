# Checklist do agente seguro

Antes de ligar um agente de IA que trabalha sozinho na sua empresa, marque o que já está garantido.
Regra de fundo: **privilégio mínimo**, ou seja, o agente só acessa o que a tarefa precisa, e alguém acompanha.

- [ ] **1. A tarefa do agente está escrita.** Ele sabe o que faz, o que nêo faz e quando passa para uma pessoa.
- [ ] **2. Acesso só ao que a tarefa precisa.** Pastas, planilhas e contas específicas. Nunca a senha do dono nem o e-mail inteiro.
- [ ] **3. Senhas fora da conversa.** Chaves e senhas ficam guardadas num cofre ou configuraçêo, nunca coladas no texto do agente.
- [ ] **4. Açêo sem volta pede aprovaçêo.** Pagar, apagar, enviar em massa ou mudar preço só com uma pessoa confirmando.
- [ ] **5. Roda separado.** Numa conta, máquina ou ambiente isolado, nêo no computador pessoal com tudo aberto.
- [ ] **6. Lista de sites e sistemas permitidos.** Ele só conversa com os serviços que a tarefa usa.
- [ ] **7. Tudo fica registrado.** Cada açêo vira um registro, e alguém olha esse registro toda semana.
- [ ] **8. Dados de cliente no mínimo.** Só o necessário, e você sabe onde ficam guardados (LGPD).
- [ ] **9. Texto de fora nêo é ordem.** E-mail, site ou mensagem de cliente é informaçêo; o agente nêo obedece instruções escondidas nesses textos.
- [ ] **10. Botêo de desligar e plano para o erro.** Você sabe como parar o agente, quem responde ao cliente e como corrigir.

**Resultado**
- 0 a 5 marcados: **nêo ligue ainda.** Resolva os itens que faltam antes de o agente tocar em cliente ou dinheiro.
- 6 a 8: **piloto só com supervisêo.** Uma pessoa olha cada resposta enquanto você fecha o resto.
- 9 ou 10: **pronto para o piloto.** Siga medindo e revisando o registro toda semana.

**Obrigatórios:** os itens 2, 4 e 10. Sem qualquer um deles, o máximo é **piloto só com supervisêo**, mesmo com 9 marcados.

Base: princípio do privilégio mínimo e OWASP Top 10 for Agentic Applications 2026 (genai.owasp.org), traduzidos para quem nêo é técnico.
Versêo interativa: https://linnoff88-dev.github.io/
