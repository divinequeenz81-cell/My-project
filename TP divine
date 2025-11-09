#include<iostream>
#include<cmath>
typedef struct point
{
   double x ,y;
}point;
 
typedef struct vect
{
   double dx, dy;
 
}vect;
 
void translation (point &B ,point &A , vect u)
{
 
  B.x= A.x + u.dx;
  B.y =A.y + u.dy;
 
}
 
void homothetie(point &B ,point &A ,point &O, double k)
{
   
   B.x=O.x+k*(A.x-O.x);
   B.y=O.y+k*(A.y-O.y);
   
}
 
void rotation(point &r,point &A,point &O, double G)
{
   
   r.x=O.x+((A.x-O.x)*cos(G))-((A.y-O.y)*sin(G));
   r.y=O.y+((A.x-O.x)*sin(G))-((A.y-O.y)*cos(G));
   
}
 void statut(int& a)
 {
 
   std::cout<<" bienvenue dans mon code que souhaitez vous faire \n";
    std::cout<<"1: une translation ?\n";
    std::cout<<"2: une homothetie ?\n";
     std::cout<<"3: une rotation ?\n";
     std::cout<<"4: une addition de vecteur ?\n";
      std::cout<<"5: une soustraction de vecteur ?\n";
      std::cout<<"6: produit scalaire de vecteur ?\n";
      std::cout<<"7:la norme de vecteur?\n";
       std::cout<<"8:determinant de vecteur?\n";
        std::cout<<"9:creation de vecteur?\n";
     std::cin>>a;
     
 }
 void demande(point &C){
   std::cout<<"entrer la coordonnee en x  du point \n";
   std::cin>>C.x;
   std::cout<<"entrer la coordonnee en y  du point \n";
    std::cin>>C.y;
 }
 
 void demande1(vect &u){
   std::cout<<"entrer la coordonnee en x  du vecteur \n";
   std::cin>>u.dx;
   std::cout<<"entrer la coordonnee en y  du vecteur \n";
    std::cin>>u.dy;
 }
 void demande2(point &C){
   std::cout<<"entrer la coordonnee en x  du centre \n";
   std::cin>>C.x;
   std::cout<<"entrer la coordonnee en y  du centre \n";
    std::cin>>C.y;
 }
  void affichage(point &b){
   std::cout<<"la translation de c par u donne\n"<<b.x<<std::endl;
   std::cout<<"la translation de c par u donne\n"<<b.y<<std::endl;
  }
    void affichage1(vect &b){
   std::cout<<"le resultat sur x donne\n"<<b.dx<<std::endl;
   std::cout<<"la resultst sur y donne\n"<<b.dy<<std::endl;
  }
 
  void add( vect& s, vect &a , vect &b){
   s.dx=a.dx+b.dx;
   s.dy=a.dy+b.dy;
  }
   void sous( vect &d, vect &a , vect &b){
   d.dx=a.dx-b.dx;
   d.dy=a.dy-b.dy;
  }
 
  void prod_scal(double &s,vect &a, vect& b){
   s=(a.dx*b.dx)+(a.dy*b.dy);
  }
 
  void norme(double &r,vect &a,vect &b){
   r=((pow(b.dx-a.dx,2) )- (pow(b.dy-a.dy,2)));
  }
 
  void det_vect(double &s,vect &a,vect &b){
   s=(a.dx*b.dy-a.dy*b.dx);
  }
 
  void creer_vect(vect &s ,point  &b,point &a)
  {
    s.dx=b.x-a.x;
    s.dy=b.y-a.y;
  }
 
int main()
{
   int st;
   point C;
   vect U;
   vect U1;
   vect U2;
   point b;
   point c;
   point O;
   double k;
   double g;
   double sol;  
   double s;
   double t;
   double j;
   statut(st);
 
   
   
   
   if(st==1)
   {
     
      demande(C);
      demande1(U);
      translation(b,C,U);
      affichage(b);
     
   }
   
   else if(st==2)
   {
       demande(C);
       demande2(O);
       std::cout<<"entrer le rapport\n";
       std::cin>>k;
       homothetie(c,C,O,k);
       affichage(c);
 
   }
   else if(st==3)
   {
       demande(C);
       demande2(O);
       std::cout<<"entrer l'angle\n";
       std::cin>>g;
       rotation(c,C,O,g);
       affichage(c);

   } else if(st==4)
   {
      demande1(U1);
      demande1(U2);
      add(U,U1,U2);
      affichage1(U);
 
   }else if(st==5)
   {
      demande1(U1);
      demande1(U2);
      sous(U,U1,U2);
      affichage1(U);
   }
    else if(st==6)
   {
      demande1(U1);
      demande1(U2);
      prod_scal(sol,U1,U2);
     std::cout<<"le produit scalaire donne "<<sol<<"\n";
   }
    else if (st==7)
    {
      demande1(U1);
      demande1(U2);
      norme(sol,U1,U2);
      std::cout<<"la norme donne "<<sol<<"\n";
    }
    else if (st==8)
    {
      demande1(U1);
      demande1(U2);
      det_vect(sol,U1,U2);
      std::cout<<"le determinant donne "<<sol<<"\n";
    }
    else if (st==9)
    {
      demande1(U1);
      demande1(U2);
      creer_vect(U,b,C);
      affichage1(U);
    }
 
   
    return 0;
