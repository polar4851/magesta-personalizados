# Magestà Personalizados

Aplicação web de gestão e precificação para produtos personalizados.

## Executar
```bash
npm install
npm run dev
```

## Build
```bash
npm run build
```

## Recursos
- Dashboard com indicadores de custo, faturamento potencial e lucro estimado.
- Cadastro, edição, exclusão e pesquisa de produtos.
- Composição de custo por materiais, quantidades e unidades.
- Custos de mão de obra, máquina/energia e embalagem.
- Cálculo de preço com taxas, impostos e margem pelo método divisor.
- Backup e restauração em JSON.
- Persistência local com LocalStorage.
- Interface responsiva.

## Dados
Os dados ficam no navegador e dispositivo em que foram cadastrados. Não há sincronização entre dispositivos nem backup automático em nuvem. Exporte backups regularmente em Configurações.

Os produtos de exemplo são ilustrativos e editáveis. Não são cotações de fornecedores nem recomendação de preço de mercado.

## Próximas evoluções
- Cadastro de máquinas com depreciação, manutenção e custo/hora.
- Biblioteca de insumos ligada aos produtos.
- Calculadora detalhada de impressão 3D.
- Relatórios e exportação CSV.
- Gestão de pedidos e histórico de preços.
