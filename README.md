# WorkAgent

Workspace de agentes de IA, baseado no [OpenDots](https://github.com/CopilotKit/OpenDots), com foco na evolução da experiência mobile.

## Estado inicial

- Código original preservado no histórico Git; licença MIT e avisos originais mantidos.
- Nome do pacote, título da página e marca exibida na interface alterados para WorkAgent.
- Branch de trabalho: `workagent/bootstrap`.
- Fork: https://github.com/miguelltasso-dom/WorkAgent. O remoto `origin` aponta para WorkAgent e `upstream` para CopilotKit/OpenDots.
- A interface existente já possui regras responsivas. O redesenho mobile ainda não foi implementado ou testado em aparelhos reais.

## Executar localmente

Requisitos: Node.js 24 ou superior e npm.

```bash
git clone https://github.com/miguelltasso-dom/WorkAgent.git
cd WorkAgent
npm ci
cp .env.example .env
npm run dev
```

Abra http://127.0.0.1:5173. A interface pode abrir em modo de configuração sem chaves. Para conversas, configure o provedor de modelo e CopilotKit Intelligence conforme [docs/SETUP.md](docs/SETUP.md). Voz, Slack e computadores de agentes têm configuração própria. Não coloque credenciais no Git.

## Validação da preparação

Formatação, lint, TypeScript, 156 testes em 34 arquivos e build de produção passaram com Node.js 24.19.0. Neste ambiente com proxy obrigatório, os testes de transporte precisaram excluir apenas o host de fixture `public.example` do proxy para alcançar o servidor local do teste. Não foram alterados testes nem código de transporte. O build emitiu avisos de tamanho de alguns pacotes JavaScript; otimização de carregamento fica para a etapa mobile. Integrações reais e uso em aparelhos não foram testados.

## Próxima etapa proposta

Validar navegação, chat, teclado virtual, documentos, aprovações e chamadas em telas de celular; depois decidir os ajustes de interface e a instalação como PWA. Essa etapa ainda está pendente.

## Origem e licença

Base inicial: commit `b01ac1f6a903e5e56c119d960901353ac0a3d171` de CopilotKit/OpenDots. A documentação original está preservada em [docs/UPSTREAM_README.md](docs/UPSTREAM_README.md). Consulte [LICENSE](LICENSE), [docs/SETUP.md](docs/SETUP.md) e [CONTRIBUTING.md](CONTRIBUTING.md).
