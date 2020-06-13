# matrix_jordan
Inverse of a matrix by Gauss Jordan
#include<iostream>
using namespace std;
main()
{
int n,i,j,t,q;
float k;
cout<<"Enter the order of the matrix";
cin>>n;
cout<<"enter the elements";
float a[n][n];
float b[n][n];
for (i=0;i<n;i++){
        for(j=0;j<n;j++){
         cin>>a[i][j];
        }
}

float x,y;
for(i=0;i<n;i++){
    for(j=0;j<n;j++){
        if(i==j)
        {
            b[i][j]=1;
        }
        else
            b[i][j]=0;
    cout<<b[i][j]<<"\t";
    }
    cout<<"\n";
}
for(j=0;j<n;j++){
        t=a[j][j];
    for(i=0;i<n;i++){
    	if(i!=j){
		
        k=t*a[i][j];
        if(k!=0)
		{
		
            x=k/t;
            y=k/a[i][j];
            for(q=0;q<n;q++){
                b[i][q]=y*b[i][q]-x*b[j][q];
                a[i][q]=y*a[i][q]-x*a[j][q];}
            }
        }
    }
}
for(i=0;i<n;i++){
	t=a[i][i];
	for(j=0;j<n;j++){
		if(t>0||t<0){
			a[i][j]=a[i][j]/t;
			b[i][j]=b[i][j]/t;
		}
	}
}
for(i=0;i<n;i++){
	for(j=0;j<n;j++){
		cout<<b[i][j]<<"\t";
	}
	cout<<"\n";
}
for(i=0;i<n;i++){
	for(j=0;j<n;j++){
		cout<<a[i][j]<<"\t";
	}
	cout<<"\n";
}
}
