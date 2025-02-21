# 🎁 Juego del Amigo Secreto

Este es un proyecto simple en **JavaScript, HTML y CSS** para organizar un **juego del Amigo Secreto**. Los participantes pueden ingresar nombres a una lista y luego sortear aleatoriamente un amigo secreto.

## 🚀 Características
- 📌 Permite añadir nombres a una lista.
- 🎲 Sortea aleatoriamente un amigo secreto.
- 🔄 Muestra el resultado en pantalla.

## 📜 Requisitos
Para ejecutar este proyecto, solo necesitas un navegador web moderno como **Google Chrome**, **Firefox** o **Edge**.

## 🛠 Tecnologías utilizadas
- **HTML** → Estructura de la página.
- **CSS** → Estilos básicos.
- **JavaScript** → Lógica del juego.

## 📌 Cómo usarlo
1. Escribe el nombre de un participante en el campo de texto.
2. Pulsa el botón **Añadir Amigo** para guardarlo en la lista.
3. Repite el proceso para todos los participantes.
4. Pulsa el botón **Escoger Amigo Secreto** para realizar el sorteo.
5. El resultado se mostrará en pantalla.

## 📂 Estructura del Proyecto
```
📂 amigo-secreto
├── 📜 index.html
├── 📜 styles.css
└── 📜 script.js
```

## 📜 Código Principal
### `script.js`
```javascript
let lista_amigos = [];

function texto_para_elemento(elemento, texto) {
    let variableHTML = document.getElementById(elemento);
    variableHTML.innerHTML = texto;
}

function limpiar_input() {
    document.getElementById('amigo').value = '';
}

function añadir_amigo() {
    let nombre = document.getElementById('amigo').value;
    if (isNaN(nombre)) {
        if (nombre === '') {
            alert("Debe ingresar un string.");
        } else {
            lista_amigos.push(nombre);
        }
    } else {
        alert("Debe ingresar un string.");
    }
    texto_para_elemento('lista_Amigos', `Amigos: ${lista_amigos.join(', ')}`);
    limpiar_input();
}

function escoger_amigo() {
    if (lista_amigos.length < 2) {
        alert("Ingrese más de dos amigos para escoger su amigo secreto.");
    } else {
        let amigo_escogido = lista_amigos[Math.floor(Math.random() * lista_amigos.length)];
        texto_para_elemento('resultado', `Su amigo secreto es: ${amigo_escogido}`);
    }
}
```

## 🎯 Mejoras futuras
✅ Implementar un sistema para evitar que alguien se asigne a sí mismo.
✅ Mejorar la interfaz con **CSS**.
✅ Añadir opción para reiniciar el sorteo.

## 📜 Licencia
Este proyecto es de código abierto y está disponible bajo la licencia **MIT**.

---
💡 ¡Diviértete con el juego del Amigo Secreto! 🎉

