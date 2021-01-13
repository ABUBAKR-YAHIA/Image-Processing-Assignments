Skip to content
Search or jump to…

Pull requests
Issues
Marketplace
Explore
 
@ABUBAKR-YAHIA 
Learn Git and GitHub without any code!
Using the Hello World guide, you’ll start a branch, write comments, and open a pull request.


ABUBAKR-YAHIA
/
Image-Processing-Assignments
1
00
Code
Issues
Pull requests
Actions
Projects
Wiki
Security
Insights
Settings
Image-Processing-Assignments/Operator_Overoading.cpp
@ABUBAKR-YAHIA
ABUBAKR-YAHIA Update Operator_Overoading.cpp
Latest commit 4868579 20 minutes ago
 History
 1 contributor
167 lines (122 sloc)  2.89 KB
  
#include "bits/stdc++.h" 
#include <vector>
#define rows 5
#define cols 5 
using namespace std; 
int N; 

class Matrix { 
	int arr[rows][cols]; 
public: 
	void input(vector<vector<int> >& A); 
	//void display() ; 
	void operator=(Matrix x);
	void operator+(Matrix x); 
	void operator-(Matrix x); 
	void operator*(Matrix x);
	
}; 

void Matrix::input(vector<vector<int> >& A) 
{ 
	for (int i = 0; i < rows; i++) { 

		for (int j = 0; j < cols; j++) { 

			arr[i][j] = A[i][j]; 
		} 
	}
 
} 

void Matrix::operator=(Matrix x) 
{ 
	// Travarse the Matrix x 
	for (int i = 0; i < rows; i++) { 
		for (int j = 0; j < cols; j++) { 
			arr[i][j] =  x.arr[i][j]; 
		} 
	}
	
	for (int i = 0; i < rows; i++) { 

		for (int j = 0; j < cols; j++) { 

			// Print the element 
			cout << arr[i][j] << ' '; 
		} 
		cout << endl; 
	} 
	cout <<"#######################"<< endl; 

} 

void Matrix::operator+(Matrix x) 
{ 

	int mat [rows][cols]; 
	for (int i = 0; i < rows; i++) { 
		for (int j = 0; j < cols; j++) { 
			mat[i][j] = arr[i][j]+ x.arr[i][j]; 
		} 
	} 
   for (int i = 0; i < rows; i++) { 

		for (int j = 0; j < cols; j++) { 
			cout << mat[i][j] <<"\t"; 
		} 
		cout << endl; 
	} 
	cout <<"#######################"<< endl; 
} 


void Matrix::operator-(Matrix x) 
{ 

	int mat[rows][cols]; 


	for (int i = 0; i < rows; i++) { 

		for (int j = 0; j < cols; j++) { 
			mat[i][j] = arr[i][j] 
						- x.arr[i][j]; 
		} 
	} 
for (int i = 0; i < rows; i++) { 

		for (int j = 0; j < cols; j++) { 

			cout << mat[i][j] << ' '; 
		} 
		cout << endl; 
	} 
	cout <<"#######################"<< endl; 

} 


void Matrix::operator*(Matrix x) 
{ 

	int mat[rows][cols]; 
	for (int i = 0; i < rows; i++) { 

		for (int j = 0; j < cols; j++) { 
			mat[i][j] = 0; 

			for (int k = 0; k < rows; k++) { 
				mat[i][j] += arr[i][k] 
							* (x.arr[k][j]); 
			} 
		} 
	} 

for (int i = 0; i < rows; i++) { 

		for (int j = 0; j < cols; j++) { 

			cout << mat[i][j] <<"\t"; 
		} 
		cout << endl; 
	} 
	cout <<"#######################"<< endl; 

} 

int main() 
{ 

vector<vector<int> > v1 (rows, vector<int> (cols, 0));
vector<vector<int> > v2(rows, vector<int> (cols, 0)) ;
	
		for (int i = 0; i < v1.size(); i++) { 
		
		for (int j = 0; j < v1[i].size(); j++) { 
			v1[i][j] = i+j+1; 
			cout<<v1[i][j]<<" ";
		} 
		cout<<endl;

	} 
	
	Matrix m1, m2; 
	m1.input(v1); 
	cout << "intializing Second Matrix using assignment Operator"<<endl;
	m2 = m1;
	cout << "Addition of two given"
		<< " Matrices is : \n"; 
	m1 + m2; 

	cout << "Substraction of two given"
		<< " Matrices is : \n"; 
	m1 - m2; 

	cout << "Multiplication of two"
		<< " given Matrices is : \n"; 
	m1* m2; 

	return 0; 
} 


OUTPUT 

![image](https://user-images.githubusercontent.com/72355871/104428845-f3eb0880-55aa-11eb-9d4d-7bf9b662c3cb.png)

© 2021 GitHub, Inc.
Terms
Privacy
Security
Status
Help
Contact GitHub
Pricing
API
Training
Blog
About

![image](https://user-images.githubusercontent.com/72355871/104429514-b33fbf00-55ab-11eb-8719-633b4539dc66.png)
