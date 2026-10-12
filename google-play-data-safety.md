# PAZ — Formulário Data Safety (Google Play)
## Respostas prontas para o console da Play Store

> **App:** PAZ — Escudo Inteligente de Chamadas  
> **Versão:** 2.7  
> **Desenvolvedor:** Aistudio / Tekno Parts  
> **Política de Privacidade:** https://joel-luz.github.io/PAZ---Comparativo/privacy.html

---

## 1. DADOS PESSOAIS (Personal Information)

| Pergunta | Resposta | Observação |
|---|---|---|
| Coleta dados pessoais? | ❌ **NÃO** | O app não tem cadastro, login ou formulário |
| Nome | ❌ Não | — |
| E-mail | ❌ Não | — |
| IDs de usuário | ❌ Não | — |
| Endereço | ❌ Não | — |
| Telefone | ❌ Não | (processa número da chamada apenas localmente, nunca armazena como dado do usuário) |
| Raça / Etnia | ❌ Não | — |
| Religião | ❌ Não | — |
| Orientação sexual | ❌ Não | — |
| Dados genéticos | ❌ Não | — |
| Dados de saúde | ❌ Não | — |
| Dados financeiros | ❌ Não | O app não processa pagamentos (a assinatura PRO será gerenciada pela própria Google Play futuramente) |
| Informações de autenticação | ❌ Não | — |

---

## 2. DADOS DE LOCALIZAÇÃO (Location Data)

| Pergunta | Resposta | Observação |
|---|---|---|
| Coleta localização? | ❌ **NÃO** | App nunca solicita permissão de localização |
| Localização aproximada | ❌ Não | — |
| Localização precisa (GPS) | ❌ Não | — |

---

## 3. CONTATOS (Contacts)

| Pergunta | Resposta | Observação |
|---|---|---|
| Acessa contatos? | ⚠️ **SIM, com permissão** | Acessa a **agenda local do aparelho** apenas se o usuário **autorizar** (READ_CONTACTS). Consulta é **100% local**, nada sai do aparelho. Usuário pode desativar a qualquer momento. |

---

## 4. FOTOS E MÍDIA (Photos & Media)

| Pergunta | Resposta |
|---|---|
| Fotos ou vídeos | ❌ Não |
| Áudio / Gravações | ❌ Não (as chamadas NÃO são gravadas, apenas silenciadas ou rejeitadas) |
| Arquivos | ❌ Não |

---

## 5. MENSAGENS (Messages)

| Pergunta | Resposta | Observação |
|---|---|---|
| SMS / Mensagens | ❌ Não | App não acessa mensagens. A regra de "código SMS" apenas permite chamadas de códigos conhecidos. |
| Outros conteúdos | ❌ Não | — |

---

## 6. ATIVIDADE NO APP (App Activity)

| Pergunta | Resposta | Observação |
|---|---|---|
| Histórico de chamadas | ⚠️ **SIM, local apenas** | O histórico fica **no banco Room do próprio aparelho**. Nunca é enviado para servidor. Máximo de 60 dias (PRO) ou 3 dias (FREE). |
| Interações no app | ❌ Não | — |
| Pesquisas | ❌ Não | — |
| Comentários | ❌ Não | — |
| Tráfego de rede | ❌ Não | (a única requisição é para a lista pública de patrocinadores no Supabase) |

---

## 7. DADOS DO DISPOSITIVO (Device Data)

| Pergunta | Resposta | Observação |
|---|---|---|
| Armazenamento / logs | ❌ Não | Apenas os próprios dados locais (histórico + preferências). |
| Sistema operacional | ❌ Não | — |
| Hardware | ❌ Não | — |

---

## 8. COMPARTILHAMENTO COM TERCEIROS

| Pergunta | Resposta | Observação |
|---|---|---|
| Compartilha dados com terceiros? | ❌ **NÃO** | Nenhum dado sai do aparelho, exceto a requisição pública à API do Supabase para os patrocinadores. |
| Supabase? | ⚠️ Apenas consulta pública (leitura) à tabela `sponsors`. Sem autenticação, sem escrita. | — |

---

## 9. CRIPTOGRAFIA EM TRÂNSITO

| Pergunta | Resposta |
|---|---|
| Dados são transmitidos criptografados (HTTPS)? | ✅ **SIM** — a única comunicação (Supabase) usa HTTPS |

---

## 10. DIREITO DE EXCLUSÃO

| Pergunta | Resposta | Observação |
|---|---|---|
| Usuário pode solicitar exclusão de dados? | ✅ **SIM** | Ao desinstalar o app, **todos os dados locais são automaticamente apagados** pelo Android. Também pode limpar nas configurações. Não há dados em servidores para excluir. |

---

## Resumo Visual (o que marcar no console)

```
🔴 PESSOAIS        → Nada coletado
🔴 LOCALIZAÇÃO     → Não coleta
🟡 CONTATOS        → Sim (local, com permissão do usuário, apenas consulta, sem enviar)
🔴 FOTOS/MÍDIA     → Não
🔴 MENSAGENS       → Não
🟡 HISTÓRICO       → Sim (local, no aparelho, nunca enviado)
🔴 DISPOSITIVO     → Não
🔴 TERCEIROS       → Não compartilha
✅ CRIPTOGRAFIA    → HTTPS
✅ EXCLUSÃO        → Sim (desinstalar apaga tudo)
```