//Задайте двумерный массив из целых чисел. Найдите среднее арифметическое элементов в каждом столбце.

//Например, задан массив:
//1 4 7 2
//5 9 2 3
//8 4 2 4
//Среднее арифметическое каждого столбца: 4,6; 5,6; 3,6; 3.

Console.WriteLine("Введите количество строк: ");

int m = Convert.ToInt32(Console.ReadLine());

Console.WriteLine("Введите количество столбцов: ");

int n = Convert.ToInt32(Console.ReadLine());

int[,] a = new int[m,n];

for (int i = 0; i < m;i++)

{

    for (int j =0; j<n; j++)
    
    {
    
        a[i,j] = new Random().Next(0,100);
        
        Console.Write(string.Format("{0} ", a[i, j]));
        
    }
    
    Console.Write(Environment.NewLine + Environment.NewLine);
    
}

for (int j = 0; j < n;j++)

{

    double s = 0;
    
    int t =0;
    
    for (int i =0; i<m; i++)
    
    {
    
        s = s+a[i,j];
        
        t++;
        
    }
    
    Console.Write($"Срарфим элементов {j} столбца - {s/t} ");
    
}

