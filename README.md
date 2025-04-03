# Implementação da Camada de Enlace

Este projeto implementa uma comunicação simples na camada de enlace usando dois processos: **remetente** e **destinatário**.

## Visão Geral

- **Remetente:**  
  Lê uma sequência de bits (payload) da entrada padrão, calcula e insere os bits de paridade usando o código de Hamming, monta um frame com cabeçalho e terminador, e envia o frame pela saída padrão.

- **Destinatário:**  
  Lê o frame completo da entrada padrão, identifica o cabeçalho e o terminador para extrair o payload, detecta e corrige erros de 1 bit (usando o código de Hamming), e exibe a mensagem original.

## Como Executar

Para testar a comunicação completa, utilize:
```bash
python3 remetente.py "01101001" | python3 destinatario.py
