# cnab-php — Constituição do Módulo

> SDK PHP para geração e leitura de arquivos CNAB (remessa/retorno bancário). Biblioteca legada — não modificar sem aprovação.

## Identidade
- Módulo: cnab-php — SDK CNAB bancário (remessa e retorno)
- Fork: `zucchetti-pos/cnab-php`
- Parte do monorepo: zweb-projects

## Stack
- **Linguagem:** PHP ≥5.4
- **Dependências:** `zucchetti-pos/cnab-yaml` · `mustangostang/spyc`
- **Testes:** PHPUnit 3.7 + PHP Code Coverage 1.2
- **Gerenciador:** Composer

## Estrutura de pastas
```
cnab-php/
├── src/
│   └── Cnab/
│       ├── Factory.php        # Fábrica de remessas/retornos
│       ├── Banco.php          # Constantes de bancos
│       ├── CodigoCarteira.php # Carteiras bancárias
│       ├── Especie.php        # Espécies de documento
│       ├── Instrucao.php      # Instruções bancárias
│       ├── Format/            # Formatadores CNAB 240/400
│       ├── Remessa/           # Geração de arquivos de remessa
│       └── Retorno/           # Leitura de arquivos de retorno
├── tests/                     # Testes PHPUnit
└── phpunit.xml.dist
```

## Comandos do projeto
```bash
# Instalar dependências
composer install

# Executar testes
vendor/bin/phpunit
```

## Restrições
- **SDK legado (PHP 5.4)** — evitar introduzir sintaxe PHP >5.4 sem validar retrocompatibilidade
- SDK externo (fork) — modificações exigem aprovação explícita
- Dados bancários (agência, conta, CNPJ do beneficiário) nunca em logs ou testes com dados reais
- Arquivos CNAB de produção (remessa/retorno) nunca commitar no repositório
