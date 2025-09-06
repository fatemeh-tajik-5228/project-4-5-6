# project-4-5-6
#include <iostream>
using namespace std;
// matris asli va bastar baztabi va tagharoni va terayayi
int main() {
    int n ;
	cout << "andaze matris ra vared kon(satr=sotoon)" << "\n" ;
	cin >> n ;
	
	int matris[n][n] ;
	cout << "matris rabeteh ra vared kon(0 or 1)" << "\n" ;
	for(int i=0 ; i<n ; i++) {
		cout << "satr" << i+1 << ": \n" ;
		for(int j=0 ; j<n ; j++) {
			cin >> matris[i][j] ;
		}
		cout << "\n" ;
	}
	
    cout << "matris asli:\n";
    for(int i = 0; i < n ; i++) {
        for(int j = 0; j < n ; j++) {
            cout << matris[i][j] << " ";
        }
        cout << endl;
    }
    cout << endl;
    
    // 1. bastar baztabi
    int a[3][3];
    for(int i = 0; i < n; i++) {
        for(int j = 0; j < n; j++) {
            a[i][j] = matris[i][j];
        }
        a[i][i] = 1;  // ghotr ra 1 mikonam
    }
    
    cout << "bastar baztabi:\n";
    for(int i = 0; i < n; i++) {
        for(int j = 0; j < n; j++) {
            cout << a[i][j] << " ";
        }
        cout << endl;
    }
    cout << endl;
    
    // 2. bastar taghoroni
    int b[3][3];
    for(int i = 0; i < n; i++) {
        for(int j = 0; j < n; j++) {
            b[i][j] = matris[i][j];
            if(matris[i][j] == 1) {
                b[j][i] = 1; // rabete makos ra ezafe mikonim
            }
        }
    }
    
    cout << "bastar taghoroni:\n";
    for(int i = 0; i < n; i++) {
        for(int j = 0; j < n ; j++) {
            cout << b[i][j] << " ";
        }
        cout << endl;
    }
    cout << endl;
    
    // 3. bastar tarayayi
    int c[3][3];
    for(int i = 0; i < n; i++) {
        for(int j = 0; j < n ; j++) {
            c[i][j] = matris[i][j];
            if(c[i][j] = 1) {
            	for(int k = 0; k < n; k++) {
            		if(c[j][k] = 1) c[i][k] = 1 ;
				}
			}
        }
    }
    cout << "bastar tarayayi:\n";
    for(int i = 0; i < n; i++) {
        for(int j = 0; j < n; j++) {
            cout << c[i][j] << " ";
        }
        cout << endl;
    }
    
    return 0;
}
