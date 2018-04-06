# Matemáicas Discretas :octocat:

Proyecto del primer parcial de Matemáticas Discretas. Para visitar el sitio/proyecto, de click [aquí](https://topi99.github.io/MatematicasDiscretas/).

Realizado por Topiltzin Hernández Mares y Carlos Alfonso Sánchez Rosales.

## 1. IPO

### 1.1. Ejercicios de Lógica Matemática y Condicionales.

**Input** 

Cadena de carácteres, puede ser cualquiera, no hay restricción (`p, q, r, s, ∧, ¬, ∨, →`). 

**Process**

```javascript 
var resp, resps = ['r∧q','q ∧ ¬p','¬q ∧ ¬p'];
let getAnswers = () => {
  $('.append').remove();
    for(var i of [1,2,3]) {
      $('.'+i).append('<span class="append">'+($('#'+i).val().replace(/\s+/g, '')===resps[i-1]).toString()+'</span>');
    }
  }
``` 

**Output**

Como output, se agregará una linea de téxto abajo de la pregunta. Si es correcta, será `true`, si no, `false`.

### 1.2. Ejercicios de Tablas de Verdad.

**Input** 

Respuesta correcta o falsa, pueden ser `t`, `T`, `f` o `F`. 

**Process**

```javascript 
var resp, resps = ['T','F','T', 'T', 'T', 'T', 'T', 'T', 'T', 'F', 'F', 'F', 'F', 'T', 'T', 'F' ];

let getAnswers = () => {
  for(var i of [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16]) {
    if($('#'+i).val().replace(/\s+/g, '').toUpperCase()===resps[i-1]) {
      $('#'+i).css({'background-color':'rgb(191, 255, 126)'});
      console.log($('#'+i).val());
      $('#'+i).prop('disabled',true);
    } else {
      $('#'+i).css({'background-color':'rgb(255, 179, 179)'});
      console.log($('#'+i).val());
    }
}
``` 

**Output**

Como output, el input en donde se escribio la respuesta cambiará de color. Si es correcta, será verde y no se podrá modificar. Si es incorrecta, cambiará a rojo y de podrá editar la respuesta.

### 1.3. Ejercicios de Equivalencias lógicas y Argumentos.

**Input** 

En estos ejercicios solo hay 2 inputs, que son 2 `radio buttons` por pregunta, uno para cada respuesta, correcta o incorrecta.

**Process**

```javascript 
var resp, resps = ['¬p ∧ ¬q','r','t'];
let getAnswers = () => {
  $('.append').remove();
  for(var i of [1,2,3]) {
    resp = $('input[name='+i+']:checked');
    if(resp.val()===resps[i-1]) {
      $('label[for="'+i+'"]').append('<span class="append good"> Bien ;D</span>');
    } else {
      $('label[for="'+i+'"]').append('<span class="append wrong"> Mal D:</span>');
    }
  }
}
``` 

**Output**

Como output, se agregará una linea de téxto al lado de la pregunta. Si es correcta, será `Bien ;D`, si no, `Mal D:`.

## 2. Guía de usuario

1. Esta es la página principal, donde podemos visualizar los menus que tenemos. 

![image](https://firebasestorage.googleapis.com/v0/b/chatdemo-43f97.appspot.com/o/Captura%20de%20pantalla%202018-02-14%20a%20la(s)%2017.59.28.png?alt=media&token=9fb79f75-6754-42b5-9efb-7736d25cf96e)

1. Deslizando la pantalla, obtenemos un menu, de los temas que abarcamos de *Matematicas discretas*, esto para tener una clasificación de los temas. A parte de que esten ordenados, para que el alumno pueda consultarlo con orden. Para abrir algun tema, es necesario que muevas el mouse, al recuadro, y te menciona el tema que abarca esa seccion. Le das clic en "APRENDER", para poder abrir la pestaña. _Esto abarca a los demas recuadros o temas_.

![image](https://firebasestorage.googleapis.com/v0/b/chatdemo-43f97.appspot.com/o/Captura%20de%20pantalla%202018-02-14%20a%20la(s)%2017.59.40.png?alt=media&token=60019533-166a-48d2-af85-bf1e2c1654fe)


1. Ya abierto la pestaña del tema, podemos ver una presentación, la cual nos brinda infomación acerca del área en que nos enfoncaremos.

![image](https://firebasestorage.googleapis.com/v0/b/chatdemo-43f97.appspot.com/o/Captura%20de%20pantalla%202018-02-14%20a%20la(s)%2017.59.46.png?alt=media&token=a67a5621-ffe3-4cf9-89d1-634b24b29435)

1. Terminando de analizar la presentación, puedes deslizar la pantalla para realizar un ejercicio, en el cual *verificarás si entendiste o aun tienes fallas en el tema*. Para esto te indicará que estas incorrecto en la respuesta(s)

![image](https://firebasestorage.googleapis.com/v0/b/chatdemo-43f97.appspot.com/o/Captura%20de%20pantalla%202018-02-14%20a%20la(s)%2017.59.48.png?alt=media&token=d20bf056-02bc-444a-8efc-6d16a96db6b4)

1. Finalmente, siempre puedes regresar a la pagina de inicio, y accesar a cualquier curso, como en el ejemplo de está guia.
