# Conversor de Texto para Negrito Matemático Unicode  MATHEMATICAL-BOLDIFY 𝐛𝐨𝐥𝐝

[![Versão](https://img.shields.io/badge/versão-1.1.0-blue.svg)](https://github.com/SEU_USUARIO/SEU_REPOSITORIO)
[![Licença](https://img.shields.io/badge/licença-MIT-green.svg)](LICENSE)
[![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
[![CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)


![image](https://github.com/user-attachments/assets/a010320a-5c2b-4e1b-a879-2e449076e6fa)

Uma ferramenta web simples, que pode ser usado offline para transformar texto e números em seus equivalentes **Mathematical Bold** e **Mathematical Bold Digits** do padrão Unicode. Ideal para estilizar textos em redes sociais, documentos ou onde quer que caracteres Unicode especiais sejam suportados.

## ✨ Funcionalidades

* **Conversão Instantânea:** Transforma letras (A-Z, a-z) e números (0-9) para o formato negrito matemático Unicode.
* **Suporte a Acentos:** Tenta aplicar o negrito à letra base de caracteres acentuados (ex: "é" se torna "𝐞́"). A renderização pode variar conforme o ambiente.
* **Interface Intuitiva:** Design limpo e fácil de usar, com campos para entrada, saída e botões de ação claros.
* **Funcionamento Offline:** Salve o arquivo HTML e use-o diretamente no seu navegador, sem necessidade de conexão com a internet.
* **Botão de Copiar:** Copie facilmente o texto transformado para a área de transferência.
* **Estilização Moderna:** Interface agradável utilizando Tailwind CSS.
* **Responsivo:** Adaptável a diferentes tamanhos de tela.

## 🚀 Como Usar

1.  **Download ou Clone:**
    * Baixe o arquivo `transformador_unicode.html` (ou o nome que você deu ao arquivo principal HTML).
    * Ou clone este repositório:
        ```bash
        git clone [https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git](https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git)
        cd SEU_REPOSITORIO
        ```
2.  **Abra no Navegador:**
    * Abra o arquivo `transformador_unicode.html` em qualquer navegador moderno (Google Chrome, Firefox, Microsoft Edge, Safari, etc.).
3.  **Utilize:**
    * **Digite ou cole** o texto desejado na caixa "Texto Original".
    * Clique no botão "**Transformar Texto**".
    * O texto convertido aparecerá na caixa "Texto Transformado".
    * Clique em "**Copiar Resultado**" para copiar o texto para sua área de transferência.

Pronto! O texto transformado pode ser colado onde você desejar.

## 🛠️ Como Funciona

A ferramenta utiliza JavaScript para mapear caracteres alfanuméricos comuns para seus correspondentes Unicode no bloco "Mathematical Alphanumeric Symbols".

* **Caracteres Padrão:** Letras (A-Z, a-z) e dígitos (0-9) são diretamente substituídos pelos seus equivalentes "Mathematical Bold".
    * Ex: `A` → `𝐀` (U+1D400), `1` → `𝟏` (U+1D7CF)
* **Caracteres Acentuados:** Para caracteres acentuados (como `á`, `é`, `õ`), a lógica é:
    1.  O caractere é normalizado usando `String.prototype.normalize('NFD')`. Isso decompõe o caractere em sua letra base e seus diacríticos (acentos) combinatórios. Por exemplo, `é` (U+00E9) se torna `e` (U+0065) + `´` (U+0301 - acento agudo combinatório).
    2.  A formatação "Mathematical Bold" é aplicada à letra base (ex: `e` → `𝐞`).
    3.  O diacrítico combinatório é então anexado à letra base em negrito (ex: `𝐞` + `´` → `𝐞́`).
    * **Nota:** A renderização final desta combinação (letra em negrito + acento) pode variar ligeiramente dependendo do sistema operacional, navegador e fontes instaladas. Em alguns casos, o acento pode não se alinhar perfeitamente.

Caracteres que não possuem um mapeamento definido (como espaços, pontuação especial, etc.) são mantidos no texto original.

## 🎨 Customização

* **Estilos:** A interface é estilizada com [Tailwind CSS](https://tailwindcss.com/). Você pode modificar as classes diretamente no HTML para alterar a aparência. Para uso offline completo e modificações extensas no CSS, você pode configurar o Tailwind localmente ou substituir por um arquivo CSS personalizado.
* **Mapeamento de Caracteres:** Os mapeamentos Unicode estão definidos no objeto `mathematicalBoldChars` dentro da tag `<script>` no arquivo HTML. Você pode estender ou modificar este objeto se necessário.

## 🔧 Desenvolvimento

Sinta-se à vontade para abrir *issues* para relatar bugs ou sugerir novas funcionalidades. *Pull requests* são bem-vindos!

1.  Faça um *fork* do projeto.
2.  Crie uma nova *branch* (`git checkout -b feature/nova-feature`).
3.  Faça suas alterações e *commits* (`git commit -am 'Adiciona nova feature'`).
4.  Faça o *push* para a *branch* (`git push origin feature/nova-feature`).
5.  Abra um *Pull Request*.

## 📄 Licença

Este projeto é distribuído sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

---

Feito com ❤️ e código!
