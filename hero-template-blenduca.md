# Blenduca Hero Template

## Objetivo

Hero premium responsiva para landing pages de experts da Blenduca.

Estrutura:
- Conteúdo alinhado à esquerda
- Foto/persona alinhada à direita
- Overlay escuro no fundo
- CTA forte e destacado
- Adaptação elegante entre desktop, tablet e mobile

---

# Estrutura Visual

## Desktop
- Texto ocupa aproximadamente 40% da largura
- Imagem ocupa aproximadamente 60%
- Hero full viewport (`min-height: 100vh`)
- Foto alinhada à direita
- Conteúdo centralizado verticalmente

## Tablet
- Mantém composição horizontal
- Reduz espaçamentos
- Reduz tamanho tipográfico
- Preserva hierarquia visual

## Mobile
- Layout vira coluna
- Foto sobe
- Conteúdo desce
- Overlay aumenta intensidade
- Texto centralizado visualmente
- CTA ocupa largura maior

---

# Regras Importantes

- Nunca inverter imagem e texto
- Nunca remover overlay escuro
- Nunca usar imagem sem profundidade
- Sempre utilizar imagem editorial/profissional
- CTA deve permanecer acima da dobra
- Headline deve ter no máximo 2 ou 3 linhas no desktop
- Não deixar a foto cortar rosto ou mãos
- Priorizar contraste forte entre texto e fundo

---

# Estrutura HTML

```html
<section class="hero">
  <div class="hero-overlay"></div>

  <div class="hero-content">
    <img src="/logo.svg" alt="Logo" class="hero-logo" />

    <h1>
      A Evolução Exige
      <span>Coragem.</span>
    </h1>

    <p class="hero-subtitle">
      Chegou a Hora de Parar de Apagar Incêndios e
      Começar a Liderar o Futuro da Sua Empresa.
    </p>

    <p class="hero-description">
      Descubra a raiz dos seus desafios com uma Sessão Estratégica
      e Diagnóstica Personalizada.
    </p>

    <button>
      AGENDAR SESSÃO DIAGNÓSTICA
    </button>
  </div>

  <div class="hero-image">
    <img src="/placeholder-hero.jpg" alt="Expert" />
  </div>
</section>
```

---

# Estrutura CSS

```css
.hero {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: space-between;
  min-height: 100vh;
  overflow: hidden;
  background: #0e0e0e;
}

.hero-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(
    90deg,
    rgba(0,0,0,.75) 0%,
    rgba(0,0,0,.45) 45%,
    rgba(0,0,0,.15) 100%
  );
  z-index: 1;
}

.hero-content {
  position: relative;
  z-index: 2;
  width: 42%;
  padding-left: 8vw;
}

.hero-image {
  width: 58%;
  height: 100vh;
}

.hero-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center top;
}

.hero h1 {
  font-size: clamp(3rem, 5vw, 5.5rem);
  line-height: .95;
  color: white;
}

.hero h1 span {
  color: #D6B06A;
}

.hero-subtitle {
  margin-top: 24px;
  font-size: 1.3rem;
  color: rgba(255,255,255,.92);
}

.hero-description {
  margin-top: 20px;
  color: rgba(255,255,255,.7);
}

.hero button {
  margin-top: 36px;
  height: 60px;
  padding: 0 32px;
  border-radius: 14px;
  border: none;
  background: #D6B06A;
  color: white;
  font-weight: 700;
  cursor: pointer;
}

@media (max-width: 768px) {
  .hero {
    flex-direction: column;
    justify-content: flex-end;
  }

  .hero-content {
    width: 100%;
    padding: 32px;
    position: absolute;
    bottom: 0;
  }

  .hero-image {
    width: 100%;
    height: 100vh;
  }

  .hero-overlay {
    background: linear-gradient(
      180deg,
      rgba(0,0,0,.15) 0%,
      rgba(0,0,0,.75) 65%,
      rgba(0,0,0,.95) 100%
    );
  }

  .hero h1 {
    font-size: 3.2rem;
  }

  .hero button {
    width: 100%;
  }
}
```

---

# Placeholder de Imagem

Utilizar inicialmente:

`/placeholder-hero.jpg`

Depois substituir manualmente pela imagem da cliente.

A imagem ideal:
- Retrato profissional
- Fundo corporativo/editorial
- Pessoa olhando para câmera
- Luz quente/cinematográfica
- Muito espaço negativo à esquerda
- Enquadramento vertical

---

# Prompt para Agentes

Criar uma hero premium seguindo EXATAMENTE esta estrutura:
- Conteúdo à esquerda
- Pessoa à direita
- Overlay escuro sofisticado
- Responsividade idêntica ao template Blenduca
- Mobile deve manter sensação editorial
- Não alterar alinhamentos-base
- Não centralizar conteúdo no desktop
- Preservar hierarquia tipográfica
- Preservar área segura da imagem
