//14

        int[] A = { 1, 2, 3, 4, 5, 6, 7, 8 };
        int N = A.Length;

        Console.WriteLine("Четные ");
        for (int i = 1; i < N; i += 2)
        {
            Console.Write(A[i] + " ");
        }

        Console.WriteLine("Нечетные ");
        for (int i = 0; i < N; i += 2)
        {
            Console.Write(A[i] + " ");
        }

//118
        
        Console.WriteLine("Размер массива ");
        int Q = int.Parse(Console.ReadLine());

        int[] E = new int[Q];
        Console.WriteLine("Элементы массива ");
        for (int i = 0; i < Q; i++)
        {
            E[i] = int.Parse(Console.ReadLine());
        }

        List<int> result = new List<int>();

        for (int i = 0; i < E.Length; i++)
        {
            result.Add(E[i]);

            if (i == E.Length - 1 || E[i] != E[i + 1])
            {
                result.Add(0);
            }
        }

        Console.WriteLine("Результат ");
        foreach (int item in result)
        {
            Console.Write(item + " ");
        }







//2

        Console.WriteLine("Количество строк M ");
        int S = int.Parse(Console.ReadLine());

        Console.WriteLine("Количество столбцов N ");
        int W = int.Parse(Console.ReadLine());

        int[,] matrix = new int[S, W];

        for (int i = 0; i < S; i++)
        {
            for (int j = 0; j < W; j++)
            {
                matrix[i, j] = 5 * (j + 1);
            }
        }

        Console.WriteLine("Результат ");
        for (int i = 0; i < S; i++)
        {
            for (int j = 0; j < W; j++)
            {
                Console.Write(matrix[i, j] + " ");
            }
            Console.WriteLine();
        }






//54


    Console.WriteLine("Количество строк M ");
    int T = int.Parse(Console.ReadLine());

    Console.WriteLine("Количество столбцов N ");
    int Y = int.Parse(Console.ReadLine());

    int[,] Matrix = new int[T, Y];

    Console.WriteLine("Элементы матрицы ");
    for (int i = 0; i < T; i++)
    {
        for (int j = 0; j < Y; j++)
        {
            Matrix[i, j] = int.Parse(Console.ReadLine());
        }
    }

    int Otr = -1;
    for (int j = 0; j < Y; j++)
    {
        bool allOtr = true;
        for (int i = 0; i < T; i++)
        {
            if (Matrix[i, j] >= 0)
            {
                allOtr= false;
                break;
            }
        }

        if (allOtr)
        {
            Otr = j;
            break;
        }
    }


    if (Otr != -1)
    {
        for (int i = 0; i < T; i++)
        {
            int temp = Matrix[i, Y - 1];
            Matrix[i, Y - 1] = Matrix[i, Otr];
            Matrix[i, Otr] = temp;
        }
    }

    Console.WriteLine("Результирующая матрица:");
    for (int i = 0; i < T; i++)
    {
        for (int j = 0; j < Y; j++)
        {
            Console.Write(matrix[i, j] + " ");
        }
        Console.WriteLine();
    }
