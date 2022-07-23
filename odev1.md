// SORU 1: Bir konsol uygulamasında kullanıcıdan pozitif bir sayı girmesini isteyin(n). 
// Sonrasında kullanıcıdan n adet pozitif sayı girmesini isteyin. 
// Kullanıcının girmiş olduğu sayılardan çift olanlar console'a yazdırın.
```
using System;

public class HelloWorld
{
    public static void Main(string[] args)
    {   
        Console.WriteLine("Pozitif Sayi:");
        string n = Console.ReadLine();
        bool success = int.TryParse(n, out int number);
        if (!success)
            Console.WriteLine("Lütfen Sayı giriniz");
        else if(number <= 0)
            Console.WriteLine("Lutfen Pozitif Sayi giriniz");
        
        
        int[] dizi = new int[number];
        Console.WriteLine(n + " tane pozitif sayi: ");
        for(int i = 1; i <= number; i++){
            Console.Write("Sayi " + i + " ");
            int s = Convert.ToInt32(Console.ReadLine());
            dizi[i - 1] = s;
            
        }
        foreach(int item in dizi) {
            if (item % 2 == 0)
                Console.WriteLine(item);
        }
        
        
    }
}
```

// SORU 2: Bir konsol uygulamasında kullanıcıdan pozitif iki sayı girmesini isteyin (n, m). 
// Sonrasında kullanıcıdan n adet pozitif sayı girmesini isteyin. 
// Kullanıcının girmiş olduğu sayılardan m'e eşit yada tam bölünenleri console'a yazdırın.
```
using System;
using System.Collections.Generic;

public class HelloWorld
{
    public static void Main(string[] args)
    {
 		int n;
		int m;
		input:
		try {	
			Console.WriteLine("Iki Pozitif Sayi: ");
			Console.WriteLine("1. Sayi: ");
			n = Convert.ToInt32(Console.ReadLine());
			Console.Write("2. Sayi: ");
			m = Convert.ToInt32(Console.ReadLine());
		}	
		catch (System.Exception ex) {
			Console.WriteLine("Sadece Pozitif Sayi Girebilirsiniz. Error:" + ex.Message);
			goto input;
		}
		List<int> liste = new List<int>();
		for(int i = 0; i < n; i++) {
			Console.WriteLine("Dizinin " + (i+1) + ". sayisi");
			int a = Convert.ToInt32(Console.ReadLine());
			liste.Add(a);
		}
		foreach(int elem in liste) {
			if(elem % m == 0)
				Console.WriteLine(elem);
		}
	} 
}
```

// SORU 3: Bir konsol uygulamasında kullanıcıdan pozitif bir sayı girmesini isteyin (n). 
Sonrasında kullanıcıdan n adet kelime girmesi isteyin. 
Kullanıcının girişini yaptığı kelimeleri sondan başa doğru console'a yazdırın.
```
using System;
using System.Collections.Generic;

public class HelloWorld
{
    public static void Main(string[] args)
    {
		int n;
		input:
		try {	
			Console.WriteLine("Pozitif Sayi: ");			
			n = Convert.ToInt32(Console.ReadLine());			
		}	
		catch (System.Exception ex) {
			Console.WriteLine("Sadece Pozitif Sayi Girebilirsiniz. Error:" + ex.Message);
			goto input;
		}
		if(n > 0) {
			List<string> liste = new List<string>();
			for(int i = 0; i < n; i++) {
				Console.WriteLine("Dizinin " + (i+1) + ". kelimesi");
				string a = (Console.ReadLine());
				liste.Add(a);
			}
			for(int i = n - 1; i >= 0; i--) {
					Console.WriteLine(liste[i]);
			}
		}
		
		else{
			Console.WriteLine("Sadece Pozitif Sayi");
			goto input;
		}
	}
    
}
```

// SORU 4: Bir konsol uygulamasında kullanıcıdan bir cümle yazması isteyin. 
Cümledeki toplam kelime ve harf sayısını console'a yazdırın.
```
using System;

public class HelloWorld
{
    public static void Main(string[] args)
    {
		Console.WriteLine("Bir cumle giriniz");
		string input = Console.ReadLine();
		input = input.TrimEnd();
		
		string[] kelime = input.Split(" ");
		int harf;
		foreach(string ch in kelime){
			harf += ch.Length;
		}
		Console.WriteLine("harf sayisi: " + harf);
		Console.WriteLine("kelime sayisi: " + kelime.Length);
    }	
}
```
