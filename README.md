int[] A = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21 };
int[,] B = new int[6, 6];
int index = 0;
for (int b = 0; b < 6; b++)
{
    int count = b + 1;
    for (int a = 0; a < count; a++)
    {
        B[b, a] = A[index];
        index++;
    }
}
Console.WriteLine("Исходная матрица B:");
for (int b = 0; b < 6; b++)
{
    for (int a = 0; a < 6; a++)
    {
        Console.Write(B[b, a] + "\t");
    }
    Console.WriteLine();
}
for (int b = 0; b < 6; b++)
{
    for (int a = 0; a < 3; a++)
    {
        int c = 5 - a;
        int temp = B[b, a];
        B[b, a] = B[b, c];
        B[b, c] = temp;
    }
}
Console.WriteLine("\nОтзеркаленная матрица B:");
for (int b = 0; b < 6; b++)
{
    for (int a = 0; a < 6; a++)
    {
        Console.Write(B[b, a] + "\t");
    }
    Console.WriteLine();
}
