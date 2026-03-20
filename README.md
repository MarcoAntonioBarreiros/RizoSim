# 🌱 DarwinRizo — Simulador Ecológico da Rizosfera

**Rizosfera v6e** · Grade Espacial · Difusão · Homeostase · Frequência-Dependente · Teia Trófica

> Simulação interativa do ecossistema da rizosfera com 13 guildas microbianas, física Verlet, cinética de Michaelis-Menten e difusão espacial de nutrientes.

🔗 **[Abrir Simulação →](https://marcoantoniobarreiros.github.io/DarwinRizo/)**

---

## 📸 Visão Geral

Simulação em tempo real do ecossistema rizosférico baseada em princípios ecológicos e bioquímicos reais:

- **13 guildas funcionais**: Pseudomonas, Bacillus, Azospirillum, Methylobacterium, Trichoderma, Rhizobium, Patógeno, Cianobactéria, Protozoário, Nematóide, Saprófito, Micorriza e Arthrobotrys
- **Planta com Lei de Liebig**: crescimento limitado pelo nutriente mais escasso (N, P, Fe)
- **Grade espacial 2D**: nutrientes com coeficientes de difusão reais (NO₃⁻ >> NH₄⁺ >> PO₄³⁻)
- **Física Verlet**: organismos com morfologias distintas (bacilos, radiais, ramificados, planárias, cefalópodes, artrópodes)
- **Inoculação interativa**: clique/toque no solo para adicionar organismos específicos
- **Diagnóstico inteligente**: recomendações de inoculação baseadas no estado nutricional da planta

## 🧬 Guildas Microbianas

| Guilda | Função | Tipo |
|--------|--------|------|
| Pseudomonas | Sideróforo Fe³⁺→Fe²⁺ | PGPB |
| Bacillus | Solubilização de fosfato | PGPB |
| Azospirillum | Fixação N₂ + AIA | PGPB |
| Methylobacterium | Fototrófico + AIA | PGPB |
| Trichoderma | Biocontrole antipatógeno | PGPB |
| Rhizobium | Fixação simbiótica (nódulo) | PGPB |
| Patógeno | Oportunista | Parasita |
| Cianobactéria | Fotossíntese + N₂ | Autotrófico |
| Protozoário | Predador de bactérias | Predador |
| Nematóide | Herbívoro de raízes | Herbívoro |
| Saprófito | Decompositor de C orgânico | Saprófito |
| Micorriza | Extensão radicular para P | PGPB |
| Arthrobotrys | Fungo nematófago (armadilha) | PGPB |

## ⚗️ Modelo Biogeoquímico

- **Nitrificação**: NH₄⁺ → NO₃⁻ (aeróbia)
- **Fixação biológica de N₂**: Azospirillum, Rhizobium, Cianobactéria
- **Solubilização de P**: PO₄ ligado → PO₄ livre (Bacillus, Micorriza)
- **Sideróforos**: Fe³⁺ → Fe²⁺ (Pseudomonas)
- **Produção de AIA**: auxina com janela ótima e fitotoxicidade por excesso
- **Mineralização**: C orgânico → NH₄⁺ + PO₄
- **Lixiviação**: dependente do tipo de solo (arenoso > franco > argiloso)
- **Sinalização planta-micróbio**: flavonoides (N↓), ácidos orgânicos (P↓), ácido salicílico (patógenos)
- **Competição ecológica**: intra-guilda forte (exclusão competitiva), inter-guilda fraca
- **Reciclagem de nutrientes**: morte microbiana → detritos + nutrientes ao solo

## 📱 Responsivo e Touch

- **Desktop**: sidebar lateral com todos os controles
- **Paisagem mobile**: sidebar deslizante com botão ☰
- **Retrato mobile**: toolbar fixa no rodapé + bottom sheet com painéis colapsáveis
- **Touch**: tap para inoculação/seleção, pan com 1 dedo, pinch-zoom com 2 dedos

## 🎮 Controles

| Ação | Desktop | Mobile |
|------|---------|--------|
| Navegar | Arrastar | 1 dedo |
| Zoom | Scroll | 2 dedos (pinch) |
| Inocular | Selecionar guilda + clicar | Selecionar na toolbar + tocar |
| Selecionar organismo | Clicar (modo seleção) | Tocar (modo seleção) |
| Reset zoom | Duplo-clique | — |

## 🛠 Tecnologia

- **Zero dependências** — HTML + CSS + JS puro, arquivo único
- **Canvas 2D** com transformações de câmera (pan/zoom)
- **Verlet integration** para física de corpos articulados
- **Spatial hashing** para detecção de colisão O(n)
- **Michaelis-Menten** para todas as cinéticas enzimáticas
- **Laplaciano discreto** para difusão de nutrientes na grade

## 📄 Licença

Este projeto está licenciado sob **[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)** — uso educacional e acadêmico livre, uso comercial requer autorização.

Desenvolvido por **Prof. Dr. Marco Antonio B. Barreiros** · Grupo **FIXTEC** · UFPR Campus Palotina

---

*Parte do ecossistema [RizoWiki](https://marcoantoniobarreiros.github.io/RizoWiki/) — Plataforma educacional sobre bioinoculantes.*
