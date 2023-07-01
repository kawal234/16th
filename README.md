# 16th
#include<iostream>
#include<vector>
using namespace std;

// Q1. given a boolean 2d array where each row is sorted. Find the row with maximum number of 1s

// int maxOnes(vector<vector<int>> &V){

//     int maxOne = INT8_MIN;
//     int maxOneRow = -1;
//     int columns = V[0].size();
//     for(int i=0;i<V.size();i++){
//         for(int j=0;j<V[i].size();j++){
//             if(V[i][j]==1){
//                 int noofOnes=columns-j;
//                 if(noofOnes>maxOne){
//                     maxOne=noofOnes;
//                     maxOneRow=i;
//                 }
//                 break;
//             }
//         }
//     }
//     return maxOneRow;
// }

// int main(){
//     int n,m;
//     cin>>n>>m;

//     vector<vector<int >> vec(n, vector<int> (m));
//     for(int i=0;i<n;i++){
//         for(int j=0;j<m;j++){
//             cin>>vec[i][j];
//         }
//     }
//     int res = maxOnes(vec);
//     cout<<res<<endl;
//     return 0;
// }



// Another method for the above problem


// int left_most(vector<vector<int>> &V){

//     int leftMost = -1;
//     int maxOne = -1;

//     // finding left most one in 0th row
//     for(int j=V[0].size();j>=1;j--){
//         if(V[0][j]==1){
//             leftMost = j;

//         }else{
//             break;
//         }
//     }
//     //check rest of the rows for lrft most ones
//     for(int i=1;i<V.size();i++){
//         while(j>=0 && V[i][j] == 1){
//             leftMost=j;
//             j--;
//         }
//     }
//     return maxOne;
// }
// int main(){
//     int n,m;
//     cin>>n>>m;

//     vector<vector<int >> vec(n, vector<int> (m));
//     for(int i=0;i<n;i++){
//         for(int j=0;j<m;j++){
//             cin>>vec[i][j];
//         }
//     }
//     int res = maxOnes(vec);
//     cout<<res<<endl;
//     return 0;
// }



// Rotation of MAtrix


void rotateMatrix(vector<vector<int>> &v){
    // transpose
    for(int i=0;i<n;i++){
        for(int j=0;j<nj++){
            swap(vec[i][j],vec[j][i]);
        }
    }
    // reverse every row
    for(int i=0;i<n;i++){
        reverse_iterator(vec[i].begin(),vec[i].end());
    }
}
int main(){
    int n;
    cin>>n;

    vector<vector<int>> vec(n,vector<int> (n));

    for(int i=0;i<n;i++){
        for(int j=0;j<nj++){
            cin>>vec[i][j];
        }
    }

    rotateMatrix(vec);

    for(int i=0;i<n;i++){
        for(int j=0;j<nj++){
            cout<<vec[i][j];
        }cout<<endl;
    }
    return 0;
}
