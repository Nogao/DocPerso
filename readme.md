# Front

## Bem

* Block
* Element `__`
* Modifier `--`

```html
<ul class="headerNav">
  <li class="headerNav__item">
    <a href="/a-propos" class="headerNav__itemLink">
      A propos
    </a>
  </li>
  <li class="headerNav__item">
    <a href="/home" class="headerNav__itemLink headerNav__itemLink--active">
      Accueil
    </a>
  </li>
  <li class="headerNav__item">
    <a href="/account" class="headerNav__itemLink headerNav__itemLink--isDisabled">
      Mon compte
    </a>
  </li>
</ul>
```

```css
.headerNav {
  display: flex;
  justify-content: space-between;
  &--xmas {
    background: red;
  }
  &__item {
    list-style: none;
  }
  &__itemLink {
    text-decoration: none;
    &--isDisabled {
      color: grey;
    }
    &--isActive {
      color: green;
    }
  }
}
```

# Pseudo attribut ::after & ::before

Les pseudos attributes 'before' et 'after' sont essentiellement utilisés pour
ajouter des éléments dans le DOM sans que cela est un impact sur le référencement
ou votre HTML.

### **ATTENTION**
* Il est obligatoire d'avoir un 'content: ''' afin que vous after/before s'affichent,
* Vous pouvez leur donner une taille, une position
* essentiellement utilisé

```html
<section class="cover">
  <h2 class="cover__title">Présentation</h2>
</section>
```

```css
.cover {
  &__title {
    font-size: 24px;
    color: #bbb;
    text-align: absolute;
    position: relative;
    &::before,
    &::after {
      content: '';
      position: absolute;
      top: 0;
      width: 50px;
      height: 50px;
      background: green;
    }
    &::before {
      left: 0;
    }
    &::after {
      right: 0;
    }
  }
}
```

### Les unités

### REM

L'unité de mesure REM est basée sur la taille de l'élément racine du HTML.

Par défaut, la taille du <html> est de 16px, ce qui veut dire que '1rem = 16px'

Pour éviter de  devoir faire des calculs afin de respecter les tailles relatives
à votre maquette, vous pouvre ré-écrire cette -font-size' afin que '1rem = 10px'

Le REM scale avec la page quand tu zoom
```css
  html {
    /*
    override de la valeur par défaut
    afin que 1rem = 16px;
    */
    font-size: 62.5%;
  }

  .mainTitle {
    /* 24px */
    font-size: 2.4rem
  }

  .cover {
    /* 320px */
    width: 32rem;
  }
```
### EM


### WM


## FlexboxGrid
*[Documentation](http://flexboxgrid.com/)*


*[TRÈS IMPORTANT, questions entretien](https://github.com/h5bp/Front-end-Developer-Interview-Questions)*

# CSS NEXT
*[Lien utile, futur CSS](http://cssnext.io/)*


# JavaScript

## Framework :
    - React
    - Vue



# Back

## Installer Composer


* Ouvrir le terminal --> Go dans la racine

```
php -r "if (hash_file('SHA384', 'composer-setup.php') === '544e09ee996cdf60ece3804abc52599c22b1f40f4323403c44d44fdfdd586475ca9813a858088ffbc1f233e9b180f061') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
php composer-setup.php --install-dir=bin --filename=composer
Vérifie si composer est bien installer
```

# Job

* chooseyourboss
* Indeed
* welcometothejungle
