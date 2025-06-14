#### Application.UserName
**Consulta do Nome do Usuário**: Você pode recuperar o nome do usuário atual registrado no Office para exibi-lo em mensagens, relatórios ou logs, como:
```vb
MsgBox "O nome do usuário atual é: " & Application.UserName
```

---

**Personalização da Configuração**: O nome registrado pode ser alterado programaticamente, o que é interessante em cenários onde múltiplos usuários compartilham a mesma estação de trabalho:
```vb
Application.UserName = "Ricardo"
MsgBox "O nome foi atualizado para: " & Application.UserName
```

```ad-info
collapse: closed

Você pode conferir o nome do usuário que estiver registrado no sistema em:
1. Arquivo
2. Opções
3. Geral
4. Nome do Usuário
```
