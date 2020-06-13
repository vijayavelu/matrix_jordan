# matrix_jordan
Inverse of a matrix by Gauss Jordan
Main code involves differencing the elements of the row according to the diagnoal elements by making up and down of the diagnol elements to zero.
for(j=0;j<n;j++){
        t=a[j][j];
    for(i=0;i<n;i++){
    	if(i!=j){
		
        k=t*a[i][j];--------->(like LCM but instead of seperate function,simple multplication works)
        if(k!=0)------------>(to ensure 0 must not occur in the denominator)
		{
		
            x=k/t;
            y=k/a[i][j];
            for(q=0;q<n;q++){
                b[i][q]=y*b[i][q]-x*b[j][q];---------------->(differencing the elements)
                a[i][q]=y*a[i][q]-x*a[j][q];}
            }
        }
    }
}

once this for loop has been runned,it gives diagnol elements alone in the given matrix.
To make it identity,divide the row by the diagnol number.
for(i=0;i<n;i++){
	t=a[i][i];
	for(j=0;j<n;j++){
		if(t>0||t<0){
			a[i][j]=a[i][j]/t;----------->making unity matrix
			b[i][j]=b[i][j]/t;
		}
	}
}

















