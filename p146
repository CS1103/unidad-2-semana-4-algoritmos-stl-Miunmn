
#include <algorithm>
#include <string>
#include <iostream>
#include <vector>
 using namespace std;
template<class BidirIt>
bool next_permutation(BidirIt first, BidirIt last)
{
    if (first == last) return false;
    BidirIt i = last;
    if (first == --i) return false;
 
    while (1) {
        BidirIt i1, i2;
 
        i1 = i;
        if (*--i < *i1) {
            i2 = last;
            while (!(*i < *--i2))
                ;
            std::iter_swap(i, i2);
            std::reverse(i1, last);
            return true;
        }
        if (i == first) {
            std::reverse(first, last);
            return false;
        }
    }
}

void ingreso(string &s, vector<string> &arr)
{ int i =0;
  do {
    
    cin>>s;
    std::next_permutation(s.begin(),s.end());
    arr[i]=s;
    i++;
  }while(s!="#");
  
}
void imprimir(vector<string> &arr){
for (int i = 0; i < arr.size(); ++i)
  {
    if (arr[i]=="#"){
      cout<<"No successor!"<< endl;
      break;
    }
    cout << arr[i] << " "<<endl;
  }
}
int main()
{   vector<string> arr (20);
    string s;
    ingreso(s, arr);
    imprimir(arr);
}
