# Machinist-MR9S
Original Bios Machinist X99 MR9S

# Códigos de Erro da Placa-Mãe X99

## Erros de CPU
- **FF, 00, C0, D0, CF, F1:** CPU falhou (ou sem código, indicando o mesmo problema)
- **00, CO, CF, F1, FD:** CPU não está funcionando, verificar circuitos relacionados e BIOS
- **C0, 2A:** CPU emitiu instruções de endereçamento, BIOS não está funcionando
- **C1, D3, D4, B0:** CPU funcionou, verificar a memória

## Erros de Memória
- **C1, C6, C3, D3, D4, D6, D8, B0, A7, E1:** Memória insuficiente ou problemas relacionados
- **C1, C3, C6:** Verificar as rotas da memória, BIOS, ponte norte
- **C1-05:** Ciclo de salto ruim, BIOS ruim, ponte sul ruim ou I/O
- **B0:** Ponte norte quebrada

## Erros de Placa Gráfica
- **24, 25, 26, 01, 0A, 0B, 2A, 2B, 31:** Placa gráfica não boa o suficiente
- **25:** Problemas na fonte de alimentação AGP, ponte norte quebrada
- **2D:** Pressão na linha AD do AGP, verificar a fonte de alimentação da ponte norte
- **0D, 2B:** Flash o BIOS, gerador de relógio quebrado, problemas na fonte de alimentação da ponte norte
- **31:** Falha na placa gráfica

## Outros Erros
- **50:** Falha na fonte de alimentação de I/O ou na própria I/O, falha na ponte sul ou na BIOS
- **41:** Flash BIOS, problemas no jumper A18, desconexão de PCB, I/O, ponte sul
- **C1-05, 20:** Ciclo de salto de I/O ruim ou interface defeituosa
- **26, 85, 8E, 7F, 4E, 42, 32:** Detectar gráficos
- **03, 04, 05, 06, 07, 08, 09, 0A, 0B, 0C, 0D, 0E, 0F, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 1A, 1B, 1C, 1D, 1E, 1F, 20, 21, 22, 23, 27, 28, 29, 2A, 2B, 2C, 2D, 2E, 2F, 30, 33, 34, 35, 36, 37, 38, 39, 3A, 3B, 3C, 3D, 3E, 40, 42, 43, 44, 45, 46, 47, 48, 49, 4A, 4B, 4C, 4D, 4F, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 5A, 5B, 5C, 60, 61, 62, 63, 64, 65, 66, 67, 68, 6A, 6C, 6E, 70, 72, 74, 76, 7A, 7C, 7E, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 8A, 8B, 8C, 8D, 8E, 8F, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 9A, 9B, 9C, 9D, 9E, 9F, A0, A1, A2, A3, A4, A5, A6, A7, A8, A9, AA, AC, AE, B0, B2, B4, B6, B8, BC, BE, BF, C0, C1, C3, C5, C6, CA, CC, EE, FF:** Códigos Especiais e Indicações de Normalidade

- **"00", "FF" e outros códigos de início** podem ter três significados:
  1. Aparecer após outros códigos indica que a placa-mãe está OK.
  2. Aparecer sem erros no CMOS, indicando que pequenas falhas não afetarão a auto-verificação do BIOS.
  3. Aparecer imediatamente ao ligar a máquina, sem mudança, indica que a placa-mãe não está funcionando.

## Erros em Diferentes BIOS
- **Award BIOS:** Falha no autoteste de memória, verificar circuito de controle de memória da placa-mãe e slots de memória
- **Phoenix BIOS:** "55, AA" no setor de inicialização indicam falha na auto-verificação
