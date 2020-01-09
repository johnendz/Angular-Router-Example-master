## Configurar e Instalar dependencias 
```
npm install -g @angular/cli
```

### Cria um novo projeto chamado "Angular-app"
```
ng new Angular-app
```

### Criar 2 componentes (paginas)
```
ng g c home
ng g c about
```

### Iniciar um servidor de desenvolvimento
```
ng serve
```

### Compilar app para produção
```
ng build
//compilar app para colocar em uma pasta diferente ex:localhost:5000/dashboard
ng build --deploy-url /dashboard/
```

### Configurar direcionamento das paginas
```
// routerConfig.ts

import { Routes } from '@angular/router';
import { HomeComponent } from './components/home/home.component';
import { AboutComponent } from './components/about/about.component';
import { DashboardComponent } from './components/dashboard/dashboard.component';

const appRoutes: Routes = [
  { path: 'home', 
    component: HomeComponent 
  },
  {
    path: 'about',
    component: AboutComponent
  },
  { path: 'dashboard',
    component: DashboardComponent
  }
];
export default appRoutes;
```

### Registrar modulo na aplicacao
```
// app.module.ts

import appRoutes from './routerConfig';

imports: [
    BrowserModule,
    RouterModule.forRoot(appRoutes)
],
```

## Executar testes de unidade

`ng test` para executar os testes de unidade via [Karma](https://karma-runner.github.io).

## Executar testes de ponta a ponta

`ng e2e` para executar os testes de ponta a ponta via [Protractor](http://www.protractortest.org/).

### Personalizar configuração
Ver [Referência de configurações](https://github.com/angular/angular-cli/blob/master/README.md).
