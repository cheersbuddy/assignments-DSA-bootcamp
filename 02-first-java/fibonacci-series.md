```
class HelloWorld {
    public static void main(String[] args) {
        int x = 7;
        int n1 = 0;
        int n2 = 1;
        for(int i= 0;i<x;i++){
            System.out.print(n1+" ");
            int n3 = n1+n2;
            n1=n2;
            n2=n3;
        }
        
    }
}
```

```
0 1 1 2 3 5 8
```
