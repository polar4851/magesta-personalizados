# Magestà Personalizados

Aplicação web local para organizar produtos personalizados, estimar custos e formar preços de venda.

## Executar
```bash
npm install
npm run dev
``

## Gerar build de produção
```bash
npm run build
``

## Módulos

- **Visão geral:** indicadores de catálogo, custo unitário, faturamento potencial e lucro estimado.
- **Produtos:** cadastro, edição, pesquisa e exclusão; composição por materiais, mão de obra, máquina/energia e embalagem.
- **Precificação:** cálculo por divisor, considerando taxas de pagamento, impostos e margem sobre o preço de venda.
- **Calculadora 3D:** custo do filamento por grama, peso utilizado, tempo, energia, depreciação, refugo, mão de obra, embalagem, taxas e margem. Permite transformar a simulação em produto.
- **Máquinas:** cadastro de preço de aquisição, vida útil em horas, manutenção prevista, potência e tarifa de energia; estimativa de custo-hora com depreciação, manutenção e energia.
- **Insumos:** biblioteca com preço de compra, quantidade/rendimento, unidade e controle simples de estoque e estoque mínimo. Ao informar o nome de um insumo cadastrado na composição do produto, o custo unitário e a unidade são preenchidos automaticamente como cópia no produto.
- **Pedidos:** registro por produto e quantidade, cliente opcional e status (pendente, em produção, concluído ou cancelado).
- **Relatórios:** resumo de valores estimados e exportação do catálogo para CSV.
- **Configurações:** backup completo em JSON, restauração e limpeza dos dados.

## Cálculo de preço

O preço sugerido usa:

`Preço = custo total ÷ (1 − taxa de pagamento − impostos − margem)`

Os percentuais são informados como números percentuais. A soma precisa ser menor que 100%. O lucro apresentado desconta o custo, taxa de pagamento e impostos.

Na calculadora 3D, o refugo é aplicado ao custo de filamento; energia é calculada por potência média × tempo × tarifa do kWh; depreciação é preço da impressora dividido pela vida útil estimada em horas.

## Armazenamento e limitações

- Os dados são salvos no LocalStorage do navegador e dispositivo atual.
- Não há conta de usuário, servidor, sincronização entre dispositivos ou backup automático na nuvem.
- Limpar os dados do navegador pode apagar os cadastros. Exporte backups regularmente.
- Os insumos cadastrados formam uma biblioteca de referência: o custo de cada material no produto ainda é informado no cadastro do produto, não é atualizado automaticamente a partir do estoque.
- Pedidos guardam cópias do preço, custo e lucro estimado do produto no momento do registro. Alterar o catálogo depois não recalcula pedidos antigos.
- O estoque é um controle manual; registrar pedidos não baixa automaticamente os insumos.
- Custos, tributos, consumo, vida útil e preços dependem dos dados informados. Valide as tarifas, taxas e obrigações fiscais aplicáveis ao seu negócio.

Os produtos de demonstração são exemplos editáveis, não cotações de fornecedores nem recomendações de preço de mercado.
