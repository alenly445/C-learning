```
void quicksort(vector<int>& str,int l,int r){
    if(l>r) return;
    int i=l,j=r;
    int pivot=str[l];
    while(i<j){
        while(i<j&&str[j]>=pivot) j--;
        str[i]=str[j];
        while(i<j&&str[i]<=pivot) i++;
        str[j]=str[i];
        
    }
    str[i]=pivot;
    quicksort(str,i+1,r);
    quicksort(str,l,i-1);
}
```
