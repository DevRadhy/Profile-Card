# Profile Card

---

Olá, vim mostrar esse projeto com HTML, CSS e JS. É um projeto de um perfil com Hover effect onde irá mostrar o link para suas redes, como por exemplo o **Github**.

<p align="center">
    <img src="https://user-images.githubusercontent.com/50425715/87857948-02f54480-c901-11ea-99de-32500faa27dd.gif" alt="Profile">
</p>

## Estrutura do Projeto

```
index.html
style.css
```

## Criando o Card

Em `index.html` você deverá ter essa estrutura.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://unpkg.com/feather-icons"></script>
    <link rel="stylesheet" href="style.css">
    <title>Profile Card</title>
</head>
<body>
    <div class="wrapper">
        <div class="card">
            <div class="image"></div>
            <div class="icons">
                <a href="https://github.com/DevRadhy/"><i class="icon" data-feather="github"></i></a>
                <a href="https://www.linkedin.com/in/lucas-jantsch-guedes-53262515a/"><i class="icon" data-feather="linkedin"></i></a>
                <a href="https://www.instagram.com/dev.radhy"><i class="icon" data-feather="instagram"></i></a>
            </div>
        </div>
    </div>

    <script>
        feather.replace()
    </script>
</body>
</html>
```

Aqui começamos com a estrutura padrão do `HTML`.

Temos um `<script src="https://unpkg.com/feather-icons"></script>` para poder acessar os icones do `Feather Icons`.

Temos um `<link rel="stylesheet" href="style.css">` que leva para nosso `style.css`, onde será feito o estilo do card.

No `body` temos uma `div` principal com a classe `wrapper`, logo a baxio se encontra nossa `div.card`, onde ficará nossa imagem e nossos icones.

---

## Estilo

Aqui iremos dar estilo a nosso card e adicionar o efeito.

```css
:root {
    --primaryColor: #7b68ee;
    --secundaryColor: #eeeeee;
}

* {
    margin: 0;
    padding: 0;
}

.wrapper {
    position: relative;
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.card {
    position: relative;
    overflow: hidden;
    width: 200px;
    height: 200px;
}

.image {
    width: 100%;
    height: 100%;
    background-color: var(--secundaryColor);
    transition: all 1s;
}

.icons {
    width: 200px;
    height: 200px;
    background-color: var(--primaryColor);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: absolute;
    top: 0;
    transform: translateX(-95%);
    transition: transform 1s;
}

.icon {
    font-size: 20px;
    margin: 10px;
    color: #ffffff;
}

.card:hover .icons {
    transform: translateX(0%);
}

.card:hover .image {
    opacity: 0.6;
}
```

## Resultado

E agora temos nosso resultado =)

![Profile](https://user-images.githubusercontent.com/50425715/87857948-02f54480-c901-11ea-99de-32500faa27dd.gif)
