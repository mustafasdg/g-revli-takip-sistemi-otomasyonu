# görevli-takip-sistemi-otomasyonu

#include <iostream>
#include <locale.h>
#include <time.h>
#include <stdlib.h>

using namespace std;



string operatorBul(string numara)
{
	string numara_basi=numara.erase(3,numara.size());
	string op;
	
	if(numara_basi=="535")op="turkcell";
	else if(numara_basi=="506")op="ttnet";
	else if(numara_basi=="540")op="vodofone";
	else op="yapancı";
	
	return op;	
	
}

int main() {
    setlocale(LC_ALL, "Turkish");
    
    string numara;
    
    cout<<"numara giriniz";
    cin>>numara;
    
    cout<<operatorBul(numara);



    system("pause");
    return 0;
}

