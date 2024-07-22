#########################################################################################################################################################################################

O que foi utilizado:
ANGULAR é uma plataforma de desenvolvimento de software de código aberto que permite a criação de aplicações web dinâmicas e escaláveis. Desenvolvido e mantido pelo Google, Angular se destaca por sua abordagem estruturada e suas ferramentas integradas, facilitando o desenvolvimento de aplicações de alta qualidade e complexidade. No cerne do Angular está o conceito de Single Page Application (SPA), onde a interação do usuário com a aplicação ocorre sem a necessidade de recarregar a página inteira. Isso é possível graças à utilização de uma arquitetura baseada em componentes, onde cada componente é uma unidade reutilizável e independente que encapsula a lógica, o template e os estilos associados. Angular utiliza TypeScript, uma linguagem de programação que é um superconjunto do JavaScript. TypeScript adiciona tipagem estática e outras funcionalidades ao JavaScript, permitindo um desenvolvimento mais robusto e menos propenso a erros.

TYPESCRIPT

TypeScript é uma linguagem de programação desenvolvida pela Microsoft que se apresenta como um superconjunto do JavaScript. Isso significa que todo código JavaScript é também código TypeScript válido, mas TypeScript adiciona recursos adicionais que não estão presentes no JavaScript, com o objetivo de tornar o desenvolvimento mais robusto e menos propenso a erros.

RXJS, que significa Reactive Extensions for JavaScript, é uma biblioteca para programação reativa baseada em observables. Desenvolvida por Microsoft, RxJS é amplamente utilizada em aplicações web modernas para lidar com eventos assíncronos e dados reativos de forma eficaz.

#########################################################################################################################################################################################

Dependências (dependencies)
1. **`@angular/animations`**:
   - Usado para animações em Angular.
   - **Arquivo Utilizado**: `app.module.ts` (importação de `BrowserAnimationsModule`).

2. **`@angular/common`**:
   - Fornece funcionalidades comuns de Angular como pipes, diretivas e serviços.
   - **Arquivo Utilizado**: `app.module.ts` (importação de `HttpClientModule`).

3. **`@angular/compiler`**:
   - Fornece a capacidade de compilar templates Angular.
   - **Arquivo Utilizado**: Não diretamente visível no código fornecido, mas essencial para o funcionamento do Angular.

4. **`@angular/core`**:
   - Contém as funcionalidades principais do Angular, como o decorador `@NgModule`.
   - **Arquivo Utilizado**: Todos os arquivos que utilizam o decorador `@Component` e `@NgModule` (`app.module.ts`, `app.component.ts`, `weather-home.component.ts`, etc.).

5. **`@angular/forms`**:
   - Fornece funcionalidades para formulários, como `ngModel` para binding.
   - **Arquivo Utilizado**: `weather-home.component.ts` (uso de `[(ngModel)]`), `app.module.ts` (importação de `FormsModule`).

6. **`@angular/platform-browser`**:
   - Contém funcionalidades para renderizar a aplicação no navegador.
   - **Arquivo Utilizado**: `app.module.ts` (importação de `BrowserModule`).

7. **`@angular/platform-browser-dynamic`**:
   - Utilizado para compilar a aplicação no navegador.
   - **Arquivo Utilizado**: Não diretamente visível no código fornecido, mas essencial para a inicialização da aplicação Angular.

8. **`@angular/router`**:
   - Fornece funcionalidades de roteamento.
   - **Arquivo Utilizado**: `app-routing.module.ts` (importação de `RouterModule`).

9. **`@fortawesome/angular-fontawesome`**:
   - Integra Font Awesome com Angular.
   - **Arquivo Utilizado**: `app.module.ts` (importação de `FontAwesomeModule`), `weather-home.component.html` (uso de `<fa-icon>`).

10. **`@fortawesome/fontawesome-svg-core`**:
    - Núcleo para o Font Awesome SVG.
    - **Arquivo Utilizado**: Usado internamente pelo `@fortawesome/angular-fontawesome`.

11. **`@fortawesome/free-solid-svg-icons`**:
    - Contém ícones sólidos do Font Awesome.
    - **Arquivo Utilizado**: `weather-home.component.ts` (importação de `faMagnifyingGlass`).

12. **`rxjs`**:
    - Biblioteca para programação reativa.
    - **Arquivo Utilizado**: `weather-home.component.ts` (uso de operadores RxJS como `takeUntil`).

13. **`tslib`**:
    - Fornece utilitários TypeScript que ajudam a reduzir o código gerado pelo compilador.
    - **Arquivo Utilizado**: Usado internamente pelo TypeScript.

14. **`zone.js`**:
    - Biblioteca que ajuda a detectar mudanças e atualizações no Angular.
    - **Arquivo Utilizado**: Usado internamente pelo Angular para detecção de mudanças.
#########################################################################################################################################################################################

Claro, aqui está a explicação de como e onde cada dependência é utilizada em seu código Angular:

### 1. `@angular/core`
- **`@Component`, `inject`, e `CommonModule`**:
  - Usado em todos os componentes (`app.component.ts`, `todo-form.component.ts`, `header.component.ts`) para definir a configuração do componente, injetar serviços e importar módulos comuns.

### 2. `@angular/common`
- **`CommonModule`**:
  - Usado em `todo-form.component.ts` e `header.component.ts` para fornecer diretivas Angular comuns como `ngIf` e `ngFor`.

### 3. `@angular/forms`
- **`FormControl`, `FormGroup`, `Validators`, `FormsModule`, `ReactiveFormsModule`**:
  - Usado em `todo-form.component.ts` para criar e gerenciar formulários reativos, aplicar validações e importar módulos necessários para formulários.

### 4. `@angular/platform-browser/animations`
- **`provideAnimations`**:
  - Usado em `app.config.ts` para habilitar as animações no aplicativo.

### 5. `@angular/material/button`, `@angular/material/card`, `@angular/material/form-field`, `@angular/material/input`, `@angular/material/icon`, `@angular/material/tabs`, `@angular/material/dialog`, `@angular/material/divider`
- **Componentes de Material Design**:
  - **`MatButtonModule`**: Usado para botões em `todo-form.component.html`, `todo-card.component.html`, e `header.component.html`.
  - **`MatCardModule`**: Usado para criar cartões em `todo-card.component.html`.
  - **`MatFormFieldModule`** e **`MatInputModule`**: Usado para criar campos de formulário em `todo-form.component.html`.
  - **`MatIconModule`**: Usado para ícones em vários lugares, como em botões em `todo-card.component.html` e `header.component.html`.
  - **`MatTabsModule`**: Usado para criar abas em `todo-card.component.html`.
  - **`MatDialogModule`**: Usado para criar e gerenciar diálogos em `header.component.ts` e `todo-form.component.ts`.
  - **`MatDividerModule`**: Usado para adicionar divisores em `header.component.ts`.

### 6. `src/app/services/todo-signals.service`
- **`TodoSignalsService`**:
  - Usado em `todo-form.component.ts` e `todo-card.component.ts` para gerenciar e atualizar o estado dos todos e interagir com o armazenamento local.

### 7. `src/app/models/model/todo.model`
- **`Todo`**:
  - Usado em `todo-signals.service.ts` e `todo-card.component.ts` para definir e manipular a estrutura dos objetos de tarefas.

### 8. `src/app/models/enum/todoKeyLocalStorage`
- **`TodoKeyLocalStorage`**:
  - Usado em `todo-signals.service.ts` e `todo-card.component.ts` para definir e acessar a chave usada para armazenar a lista de tarefas no armazenamento local.

### 9. `@angular/core/testing`, `@angular/platform-browser` e `@angular/core`
- **`TestBed`, `ComponentFixture`, `By`**:
  - Usado em todos os arquivos de teste (`*.spec.ts`) para configurar e testar os componentes.
    
#########################################################################################################################################################################################
