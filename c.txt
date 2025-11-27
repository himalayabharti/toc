//union intersection concatenation
#include <iostream>
#include <cstring>
using namespace std;
int unionLanguage(char* w) {
    int len = strlen(w);
    if (w[0]=='a') return 1;
    if (w[len-1]=='b') return 1;
    return 0;
}
int intersectionLanguage(char* w) {
    int len = strlen(w);
    if (w[0]=='a' && w[len-1]=='b') return 1;
    return 0;
}
int concatenationLanguage(char* w) {
    int len = strlen(w);
    if (w[0]=='a' && w[len-1]=='b') return 1;
    return 0;
}
int main() {
    char w[100];
    cout<<"Enter string: ";
    cin>>w;

    cout<<"Union: "<<(unionLanguage(w)?"Accepted":"Rejected")<<"\n";
    cout<<"Intersection: "<<(intersectionLanguage(w)?"Accepted":"Rejected")<<"\n";
    cout<<"Concatenation: "<<(concatenationLanguage(w)?"Accepted":"Rejected")<<"\n";
    return 0;
}
