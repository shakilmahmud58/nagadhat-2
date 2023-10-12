### sub string searching in a string with c++
```cpp number
#include<iostream>
using namespace std;

int main()
{
    string str1, str2;
    int counts =0;
    cin>>str1>>str2;
    int str1_length = str1.length();
    int str2_length = str2.length();
    for(int i=0;i<str1_length;i++)
    {
        if(str1[i]==str2[0])
        {
            int tmp=0;
            for(int j=1;j<str2_length;j++)
            {

                if(str2[j]==str1[i+j])
                {
                    tmp++;
                }
            }
            if(tmp==str2_length-1)
            {
                counts++;
            }
        }
    }
    cout<<counts;
    return 0;
}

```

#### First I have created two string type variable, and take input from the user. str1 is the first string from where the sub string is searchedand str2 is the sub string, counts is the output which represent the number of presence of the sub string. str1_length and str2_length is the length of str1 and str2. Then go through str1 and find the first match, if any character of str1 match with the first character of str2, then we try to match the other character of str2 with the str1.tmp is a temporary variable which is initailly 0. In the second for loop we started to match from the second character of str2 with the st1 and if it matched tmp increased. so at last of the second for loop if the number of tmp is equal to the number of (str2_length-1), that means a full match of str2 in str1 then we increased the counts variable. at last counts represent the number of str2 in str1.