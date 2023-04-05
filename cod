List<int> mussort = new List<int>();
bool boole = true;
int n = 0;
Console.Write("введите длину массва:  ");
while (boole == true)
{
    try
    {
        n = Convert.ToInt32(Console.ReadLine());
        boole = false;
    }
    catch
    {
        Console.WriteLine("ошибка, введите число");
        boole = true;
    }

}

int[] nums = new int[n];
Console.WriteLine("введите элементы массива");
for (int i = 0; i < n; i++)
{
    try
    {
        if (i != n - 1)
            nums[i] = Convert.ToInt32(Console.ReadLine());
        else
        {
            Console.WriteLine("введите последний элемент массива: ");
            nums[i] = Convert.ToInt32(Console.ReadLine());
        }
    }
    catch
    {
        Console.WriteLine("введен неверный символ, введите число!");
        i = i - 1;
    }

}

Console.WriteLine("массив до сортировки");
Console.WriteLine(String.Join(" ", nums));
Console.WriteLine("\nдля проверки <<<");
grup(nums, mussort);
Console.WriteLine(">>> \n");
Console.WriteLine("массив после сортировки");
Console.WriteLine(String.Join(" ", mussort));


static void grup(int[] num, List<int> mus1)
{
    int n = 5, j = 0, g = 0;
    int[] nums = new int[n];
    int b = num.Length / 5;
    for (int i = 0; i < num.Length; i++)
    {
        if (g != b)
        {
            while (j < nums.Length)
            {
                nums[j] = num[i];
                j++;
                i++;
            }
            if (i % 5 == 0 && i != 0)
            {
                sort(nums, mus1);
                j = 0;
                i = i - 1;
                g++;
            }
        }
        else
        {
            n = num.Length % 5;
            nums = new int[n];
            while (j < nums.Length)
            {
                nums[j] = num[i];
                j++;
                i++;
            }
            sort(nums, mus1);
            j = 0;
            i = i - 1;
        }
    }

}


static void sort(int[] num, List<int> mus)
{
    int temp, n = num.Length;
    if (n == 2 || n == 3)
    {
        Console.Write("до   ");
        Console.WriteLine(String.Join(" ", num));
        for (int i = 0; i < num.Length - 1; i++)
        {
            for (int j = i + 1; j < num.Length; j++)
            {
                if (num[i] > num[j])
                {
                    temp = num[i];
                    num[i] = num[j];
                    num[j] = temp;
                }
            }
        }
        foreach (int i in num)
        {
            mus.Add(i);
        }
        Console.Write("после    ");
        Console.WriteLine(String.Join(" ", num));
    }
    else if (n == 4)
    {
        Console.Write("до   ");
        Console.WriteLine(String.Join(" ", num));
        int[] num1 = new int[3];
        int j = 0;
        for (int i = 0; i < num.Length - 1; i++)
        {

            while (j < num1.Length)
            {
                num1[j] = num[i];
                j++;
                i++;
            }
        }
        for (int i = 0; i < num1.Length - 1; i++)
        {
            for (j = i + 1; j < num1.Length; j++)
            {
                if (num1[i] > num1[j])
                {
                    temp = num1[i];
                    num1[i] = num1[j];
                    num1[j] = temp;
                }
            }
        }

        for (int i = 0; i < num.Length - 1; i++)
        {
            num[i] = num1[i];
        }

        if (num[1] > num[3])
        {
            if (num[3] < num[0])
            {
                temp = num[0];
                num[0] = num[3];
                num[3] = num[2];
                num[2] = num[1];
                num[1] = temp;
            }
            else
            {
                temp = num[1];
                num[1] = num[3];
                num[3] = num[2];
                num[2] = temp;
            }

        }
        else
        {
            if (num[3] < num[2])
            {
                temp = num[2];
                num[2] = num[3];
                num[3] = temp;
            }
        }
        foreach (int i in num)
        {
            mus.Add(i);
        }
        Console.Write("после    ");
        Console.WriteLine(String.Join(" ", num));
    }
    else if (n == 5)
    {
        Console.Write("до   ");
        Console.WriteLine(String.Join(" ", num));
        if (num[4] < num[0])
        {
            temp = num[4];
            num[4] = num[0];
            num[0] = temp;
        }
        if (num[3] < num[1])
        {
            temp = num[3];
            num[3] = num[1];
            num[1] = temp;
        }
        if (num[1] < num[0])
        {
            temp = num[1];
            num[1] = num[0];
            num[0] = temp;
            temp = num[4];
            num[4] = num[3];
            num[3] = temp;
        }
        if (num[2] < num[1])
        {
            temp = num[2];
            num[2] = num[1];
            if (temp < num[0])
            {
                num[1] = num[0];
                num[0] = temp;
            }
            else num[1] = temp;
        }
        else if (num[3] < num[2])
        {
            temp = num[2];
            num[2] = num[3];
            num[3] = temp;
        }
        if (num[4] < num[2])
        {
            temp = num[4];
            num[4] = num[3];
            num[3] = num[2];
            if (temp < num[1])
            {
                num[2] = num[1];
                num[1] = temp;
            }
            else num[2] = temp;
        }
        else if (num[4] < num[3])
        {
            temp = num[4];
            num[4] = num[3];
            num[3] = temp;
        }

        foreach (int i in num)
        {
            mus.Add(i);
        }
        Console.Write("после    ");
        Console.WriteLine(String.Join(" ", num));
    }
    else
    {
        Console.Write("до   ");
        Console.WriteLine(String.Join(" ", num));
        Console.Write("символ один, сортировка не требуется");
        foreach (int i in num)
        {
            mus.Add(i);
        }
    }
}
