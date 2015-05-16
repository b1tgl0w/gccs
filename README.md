# gccs
Print summary of errors in gcc/g++.
# usage
g++ main.cpp 2>&1 | ./gccs.pl
# example
int main() {  
    int; //missing identifier  
    int missingsemicolon  
}  
$ g++ main.cpp 2>&1 | ./gccs.pl  
main.cpp: In function ‘int main()’:  
main.cpp:2:5: error: declaration does not declare anything [-fpermissive]  
     int; //missing identifier  
     ^  
main.cpp:4:1: error: expected initializer before ‘}’ token  
 }  
 ^  
Summary of Errors  
main.cpp: 2 4  
# to do  
* Lines with multiple errors print once
* Option to include warnings in summary
