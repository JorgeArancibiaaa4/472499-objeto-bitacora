### texto de arriba


![texto alternativo](./imagenes/color.avif)

## probando ahora una imagen


## como agregar codigos de proccesing

```processing
// respiración animada con colores

int[] calma = {14, 16, 18, 15, 17, 19, 13, 20, 16, 18};
int[] agitado = {28, 30, 32, 29, 31, 33, 27, 34, 30, 32};

color[] calmaColores = {
  color(255, 182, 193), // rosado pastel
  color(144, 238, 144), // verde claro
  color(255, 200, 120), // naranja suave
  color(173, 216, 230)  // celeste
};

color[] agitadoColores = {
  color(180, 0, 0),     // rojo
  color(90, 0, 0),      // rojo oscuro
  color(60, 0, 80),     // morado oscuro
  color(120, 120, 120)  // gris
};

void setup() {
  size(800, 600);
}


void draw() {
  background(255);

  noStroke();

  // CALMA (izquierda)
  for (int i = 0; i < calma.length; i++) {

    float x = 200;
    float y = 50 + i * 50;

    float base = map(calma[i], 12, 20, 20, 60);
    float velocidad = map(calma[i], 12, 20, 0.02, 0.08);
    float tamaño = base + sin(frameCount * velocidad) * 10;

    fill(calmaColores[i % calmaColores.length]);

    circle(x, y, tamaño);
  }

  // AGITADO (derecha)
  for (int i = 0; i < agitado.length; i++) {

    float x = 600;
    float y = 50 + i * 50;

    float base = map(agitado[i], 25, 35, 20, 60);
    float velocidad = map(agitado[i], 25, 35, 0.08, 0.2);
    float tamaño = base + sin(frameCount * velocidad) * 10;

    fill(agitadoColores[i % agitadoColores.length]);

    circle(x, y, tamaño);
  }
}

```
