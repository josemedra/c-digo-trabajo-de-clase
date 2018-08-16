# c-digo-trabajo-de-clase
tarea 1

#include <iostream>
#include <math.h>

using namespace std;

#define alpha 1.24

unsigned int var;

void calcParabolico(void);
void print_results(void);
void lib_func1();
void otros_calculos(void);

int main()
{
    unsigned short int des = -5;
  //  lib_func1();
    var = 100;

    var += des;

    //Calculando los parametros en la Tierra con g = 9.8 m/s*s
    calcParabolico();
    print_results();

    //Calculando los parametros en la Luna con g = 1.62 m/s*s
    calcParabolico();
    print_results();
    otros_calculos();


    return 0;
}

void calcParabolico(void)
{
    const float g = 9.8;
    char x, y, vx, vy,v0;
    float vx0, vy0,y0;

float ALPHA = 200;
double t=30;
v0,vx=50;

    vx0 = v0 * cos(ALPHA);
    vy0 = v0 * sin(ALPHA);

    vx = vx0;
    vy = vy0-g*t;

    x = vx*t;
    y = y0+vy0*t-(g*pow(t,2)/2);
}

void print_results(void)

{
    double vx,vy,x,y;
    std::cout<<"Los resultados del calculo parabolico son: "<<std::endl;
    std::cout<<"Velocidad en x: "<<vx<<", ";
    std::cout<<"Velocidad en y: "<<vy<<", ";
    std::cout<<"Posicion en x: "<<x<<", ";
    std::cout<<"Posicion en y: "<<y<<std::endl;
}

void otros_calculos(void)


{
     
    // Serie simple (1/[(x^2) + (x+1)]) para x entre 1 y 199
    for(int x=1; x<200; x++){
    
    

       static float c=0;
        c= 1/(pow (x,2)+(x+1));
    
    
        cout<<"el numero es:"<<c<<"\n";
    }


    float r =7;
    double volumen = 0;
    float pi=3.1416;
   volumen = (4/3)*(pi)*pow(r,3);
    
    //cout<<"el volumen de la esfera es"<<Volumen<<"\n";

    /* Volumen de la esfera */
      //Agregue aqui la formula
      

    /* Raices de la ecuacion (3*x^2) + (5*x) + 8  = 0 */
      //Agregue aqui la formula
      float raizmas=0,  raizmenos=0;
      raizmas= (-5+sqrt(pow(5,2)-4*3*8))/6;
      raizmenos= (-5-sqrt(pow(5,2)-4*3*8))/6;
       cout<<"el valor de raizmas es:"<<raizmas<<"\n";
        cout<<"el valor de raizmenos es:"<<raizmenos<<"\n";


    /* Impedancia tipica de una linea de transmision
     * Z0 = [(R+wL)/(G+wC)]^(1/2)
     * w = frecuencia angular = 2*pi*f, f = 10kHz */
        //Agregue aqui la formula
      float z0,fa,f=10000,R=10,wL=30,G=14,wC=11,z=0,w=0;
       w= fa =(2)*pi*f;
        cout<<"la frecuencia  es:"<<w<<"\n";
       
        z0=(R+wL)/sqrt(G+wC);
       

    /* Constante de fase de una fibra optica
     * B = {[((a^2)-(b^2))*c+(b^2)]^(1/2)}*betacero
     * betacero = w*(mu*epsi)^(1/2)
     * w = frecuencia angular = 2*pi*f, f = 5GHz
     * mu = 0.00000125664
     * epsi = 0.00000000000088542  */
     double mu = 0.00000125664, epsi = 0.00000000000088542;
     float betacero, B, a=3, b=3, c=4,C;
     double xx;
     xx= 2*pi*5000000;
     
     betacero= fa*sqrt(mu*epsi);
     
     B=pow((pow(a,2)-pow(b,2))*C+pow(b,2),1/2)*betacero;
     
     cout<<"la constante de fase es "<<B;
}
