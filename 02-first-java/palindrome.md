```
// Online Java Compiler
// Use this editor to write, compile and run your Java code online

class HelloWorld {
    public static void main(String[] args) {
        int x = 12321;
        int n1 = 0;
        int x1 = x;
        while(x1>0){
           
            n1 = n1*10 + x1%10;
            x1 = x1/10;
        }
        System.out.println(n1);
        if(n1 == x){
             System.out.println("Palindrome ");
        }
        else{
            System.out.println("Not Palindrome ");
        }
        
    }
}
```

```
12321
Palindrome 
```
