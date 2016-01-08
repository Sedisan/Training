#include <iostream>

#include <sstream>
using namespace std;

/*
Plan dzialania:
*
*1. Pobrac wartosc
*2. Zapisac do stringa
*3. Kazda iteracje z stringa do inta
*4. W incie pomnozyc kazda wartosc
*5. Nastepnie dodac wartosci
*6. Zamienic z inta na stringa i sprawdzic czy liczba jest 0.
*7. Jesli tak, wypisz D. Inaczej N
*
*/
string convertInt(short number)
{
   std::stringstream ss;//create a stringstream
   ss << number;//add number to the stream
   return ss.str();//return a string with the contents of the stream
}
int main()
{short t;std::cin>>t;

   for(int i=0;i<t;i++)
   {
       int *tablica=new int [11];



            std::string t;
            std::cin>>t;
                short wynik=0;
            for(int j=0;j<11;j++){




          //  Sleep(1000);

            if(j==1||j==5)
            {
                    tablica[j]=t[j]-'0';
                tablica[j+1]=t[j+1]-'0';
                tablica[j+2]=t[j+2]-'0';

               tablica[j]*=3;
               tablica[j+1]*=7;
               tablica[j+2]*=9;


            }
            if(j==9)
            {
            tablica[j]=t[j]-'0';

                tablica[j]*=3;

            }
           if(j==0||j==4||j==8||j>9){tablica[j]=t[j]-'0';}

           wynik+=tablica[j];
            }

            std::string n=convertInt(wynik);

            if(n[n.length()-1]=='0')std::cout<<'D'<<'\n';
            else std::cout<<'N'<<'\n';


            delete [] tablica;
   }

 




/*
std::string myStream;
std::cin>>myStream;
std::istringstream buffer(myStream);
int value[17];
buffer >> value[0];
std::cout<<value[0];

    std::cout<<"UWAGA: "<<'\n';

char literka;
    cin >> literka;
    int x = static_cast<int>(literka);
    cout << endl << x << endl;

    int i=30,*wsk;

    wsk=&i;
    *wsk=300;


    std::cout<<i<<'\n';
*/
    cout << "Hello world!" << endl;
    return 0;
}
