# Matemáicas Discretas :octocat:

Proyecto del primer parcial de Matemáticas Discretas

## IPO

### Ejercicios de Lógica Matemática

**Input** 

Respuesta correcta (`r∧q`) 

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

## Guía de usuario

1. Esta es la página principal, donde podemos visualizar los menus que tenemos. 

![image](https://firebasestorage.googleapis.com/v0/b/chatdemo-43f97.appspot.com/o/Captura%20de%20pantalla%202018-02-14%20a%20la(s)%2017.59.28.png?alt=media&token=9fb79f75-6754-42b5-9efb-7736d25cf96e)

1. Deslizando la pantalla, obtenemos un menu, de los temas que abarcamos de *Matematicas discretas*, esto para tener una clasificación de los temas. A parte de que esten ordenados, para que el alumno pueda consultarlo con orden. Para abrir algun tema, es necesario que muevas el mouse, al recuadro, y te menciona el tema que abarca esa seccion. Le das clic en "APRENDER", para poder abrir la pestaña. _Esto abarca a los demas recuadros o temas_.

![image](https://firebasestorage.googleapis.com/v0/b/chatdemo-43f97.appspot.com/o/Captura%20de%20pantalla%202018-02-14%20a%20la(s)%2017.59.40.png?alt=media&token=60019533-166a-48d2-af85-bf1e2c1654fe)


1. Ya abierto la pestaña del tema, podemos ver una presentación, la cual nos brinda infomación acerca del área en que nos enfoncaremos.

![image](https://firebasestorage.googleapis.com/v0/b/chatdemo-43f97.appspot.com/o/Captura%20de%20pantalla%202018-02-14%20a%20la(s)%2017.59.46.png?alt=media&token=a67a5621-ffe3-4cf9-89d1-634b24b29435)

1. Terminando de analizar la presentación, puedes deslizar la pantalla para realizar un ejercicio, en el cual *verificarás si entendiste o aun tienes fallas en el tema*. Para esto te indicará que estas incorrecto en la respuesta(s)

![image](https://firebasestorage.googleapis.com/v0/b/chatdemo-43f97.appspot.com/o/Captura%20de%20pantalla%202018-02-14%20a%20la(s)%2017.59.48.png?alt=media&token=d20bf056-02bc-444a-8efc-6d16a96db6b4)

1. Finalmente, siempre puedes regresar a la pagina de inicio, y accesar a cualquier curso, como en el ejemplo de está guia.
