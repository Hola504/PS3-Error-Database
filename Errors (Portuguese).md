# Erros de sistema PS3 e RPCS3 - Explicação

Este documento fornece uma visão geral dos diferentes erros de sistema relacionados à PlayStation 3 e ao emulador RPCS3.

---

## BSOD (Tela Azul da Morte)
- **Descrição:** Corrompe (ou apaga) linhas no arquivo de backup `Xregistry.sys` localizado em `dev_flash2/etc/backup/`, e também remove o `Xregistry.sys` principal de `dev_flash2/etc/`.

---

## BSOD Grave
- **Descrição:** Remove o arquivo `libuserdata.sprx` (ou semelhante) de `dev_flash/sys/external/`.

---

## RSOD (Tela Vermelha da Morte)
- **Descrição:**
  - No RPCS3: Não pode ser simulado.
  - Em um PS3 real: Apague o arquivo `vsh.self` localizado em `dev_flash/vsh/module/`.

---

## "Ocorreu um erro grave"
- **Descrição:** Semelhante ao RSOD.
  - No RPCS3: Pode ser reproduzido.
  - Causa: Corrupção no arquivo `sys_init_osd.self` em `dev_flash/vsh/module/`.

---

## "Não foi possível iniciar. Nenhum disco rígido apropriado foi encontrado."
- **Descrição:**
  - PS3 real: Remover fisicamente o HDD ou SSD.
  - RPCS3: Tente corromper arquivos em `dev_hdd0`, os resultados variam.

---

## RSOD Grave
- **Descrição:** Muito raro. Ocorre quando quase todos os arquivos críticos do sistema estão corrompidos, exceto o XMB.

---

## "O sistema de arquivos do disco rígido está corrompido e será restaurado"
- **Descrição:**
  - No RPCS3: Apagar a pasta `dev_hdd0`.
  - Em um PS3 real: Corromper arquivos dentro de `dev_hdd0` ou formatar o HDD de maneira inadequada.

---

## "Dados corrompidos"
- **Descrição:** Corromper o arquivo `EBOOT.BIN` de qualquer aplicativo causará essa mensagem.

---

## YLOD (Luz Amarela da Morte)
- **Descrição:** Não pode ser simulado. Ocorre quando as conexões físicas da GPU ou CPU se quebram devido ao calor ou à idade.

---

## GLOD (Luz Verde da Morte)
- **Descrição:** Semelhante ao YLOD, mas menos grave.

---

## GARLOD (Luz Verde e Vermelha da Morte)
- **Descrição:** Pode ocorrer por superaquecimento ou danos físicos. Pode estar relacionado ao YLOD.

---

## Semi-brick
- **Descrição:** Ocorre quando uma atualização do sistema falha ou arquivos não-críticos são corrompidos.
  - Não exibe "Erro grave".

---

## Brick Completo
- **Descrição:** Falha total. Ocorre com YLOD/GLOD/GARLOD. A PS3 se torna inutilizável (sem imagem, sem resposta).
  - Única solução: Regravar a NAND/NOR com hardware especial.
  - Pode estar acompanhado por BSOD.

---

## Falhas Visuais (Glitches)
- **Descrição:** Ocorrem quando elementos gráficos do sistema (XMB, WAVE, ícones) estão corrompidos.
  - Se for muito grave, indica falta de arquivos gráficos essenciais.

---

## Falhas de Áudio
- **Descrição:** Os sons do XMB ou do sistema estão corrompidos ou ausentes.
  - RPCS3: Instalar firmware 2.80 ou inferior.
  - PS3 real: Remover arquivos `.arc` de som ou arquivos de áudio do sistema.

---

## "O disco deve ser formatado"
- **Descrição:** Aparece após uma formatação falhada ou incompleta.
  - Pode ser simulado corrompendo o disco propositalmente.

---

## Códigos de erro (ex: 800017, 8007E21G)
- **Descrição:** Geralmente causados por RAPs ausentes, ativação HEN falha, ou CFW mal instalado.
  - A gravidade depende do código.

---

## Loop de Inicialização
- **Descrição:** O sistema reinicia continuamente e não carrega o XMB.
  - No RPCS3: Apagar quase tudo menos `vsh.self`.
  - No PS3 real: Corromper arquivos críticos de boot em `dev_flash`.

---

## Congelamento Total
- **Descrição:** Causado por sobrecarga de RAM ou CPU.
  - Também pode ocorrer por plugins bugados como `PS3xPAD` em sistemas modificados.

---

## Dados Incompatíveis
- **Descrição:** Inserir um disco PS2 em modelos não compatíveis (CECH(D–K)).

---

## Erro de Leitura de Disco
- **Descrição:** Disco sujo, arranhado, ou unidade de disco com defeito.
  - Ícone do disco pode não aparecer.

---

## Sessão Desconectada
- **Descrição:** Acontece ao iniciar o HEN ou desconectar a PSN.
  - Apenas uma notificação, sem risco real.

---

*Sinta-se livre para contribuir ou adicionar outros erros que não estejam listados aqui!*
