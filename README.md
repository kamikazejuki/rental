# rental
Program rental mobil belum fix


#include<iostream.h>
#include<string.h>
#include<conio.h>
#include<stdio.h>
#include<time.h>

void delay(unsigned int mseconds)
{
clock_t goal=mseconds+clock();
while(goal>clock());
}

void main()
{

char jns[5][20];
float hrg[5],jumhar[5],sewa[5];
float jumbay,bny,pajak;
int i,g,lama[5],pilih[5];
int k;


char mad;
mad='Y';
while(mad=='Y' || mad=='y')
{
clrscr();

for(k=1;k<10;k++)
{
 delay(120);
 gotoxy(k-1,3);cout<<' ';
 gotoxy(k,3);cout<<" SELAMAT DATANG DI RENTAL MOBIL YOYO ";
}
 cout<<endl<<endl;
 gotoxy(2,11);cout<<" | -------------------------------------------------------------------| "<<endl;
 gotoxy(2,12);cout<<" |    No Plat        |   Nama Mobil  |  |   Supir    |  Harga Sewa    | "<<endl;
 gotoxy(2,13);cout<<" |--------------------------------------------------------------------| "<<endl;
 gotoxy(2,14);cout<<" |   1. BM 1113 QW   | Avanza        |  |   Anton    |   Rp.250.000   | "<<endl;
 gotoxy(2,15);cout<<" |   2. BM 1111 ER   | Inova         |  |   Juki     |   Rp.500.000   | "<<endl;
 gotoxy(2,16);cout<<" |   3. BM 1101 RO   | Apv           |  |   Wandi    |   Rp.250.000   | "<<endl;
 gotoxy(2,17);cout<<" | -------------------------------------------------------------------| "<<endl;

for(i=1;i<=g;i++)
{
 gotoxy(3,1);cout<<"Nama \t\t\t\t: ";
 gotoxy(3,2);cout<<"Pilih Mobil [1/2/3]";cin>>pilih;
 gotoxy(3,3);cout<<"Berapa Lama Sewa \t: ";cin>>lama;
}

switch (pilih[i])
{
case 1:
strcpy(jns[i],"Avanza");
sewa[i]=2500;
break;

case 2:
strcpy(jns[i],"Inova");
sewa[i]=5000;
break;

case 3:
strcpy(jns[i],"Jazz");
sewa[i]=4000;
break;

default:
strcpy(jns[i],"Mobil Tidak Tersedia");
sewa[i]=0;
break;
}

jumhar[i]=bny[i]*hrg[i];
cout<<endl;
}
clrscr();
gotoxy(4,4);cout<<"SELAMAT DATANG DI RENTAL MOBIL YOYO"<<endl;
gotoxy(4,5);cout<<"===============================================";
gotoxy(4,6);cout<<"No Jenis  Berapa  Banyak  Jumlah";
gotoxy(4,7);cout<<"   Mobil   Lama Sewa       Harga";
gotoxy(4,8);cout<<"===============================================";

for(i=1;i<=k;i++)
{
gotoxy(5,8+i);cout<<i;
gotoxy(10,8+i);cout<<jns[i];
gotoxy(20,8+i);cout<<hrg[i];
gotoxy(29,8+i);cout<<bny[i];
gotoxy(37,8+i);cout<<jumhar[i];
jumbay = jumbay + jumhar[i];
}
gotoxy(4,14);cout<<"===========================================";

if(jumbay>=100000)
	dis = 0.2*jumbay;
else
	dis= 0;
pajak = 0.1 * jumbay;
totbay = (jumbay + pajak) - dis;

gotoxy(4,16);cout << " Jumlah Bayar Rp: " <<jumbay;
gotoxy(4,17);cout << " Jumlah Pajak Rp: " <<pajak;
gotoxy(4,18);cout << " Total Bayar Rp:  " << totbay;

gotoxy(4,22);cout<<"Apakah Mau Mengulangi Program Rental Mobil ini (Y/T) :";cin>>mad;

clrscr();
cout<<endl<<endl;
cout<<"TERIMA KASIH SUDAH MENYEWA MOBIL KAMI :)";
}
}
