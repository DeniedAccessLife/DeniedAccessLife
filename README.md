```csharp
using System;

class DeniedAccessLife
{
    public static void Inject()
    {
        Console.WriteLine("Initiating driver injection into kernel...");

        string encoded = Decrypt("AxoWYRkmdw4GLwlpOg1Pe0Q=");
        Console.WriteLine($"Driver payload injected: {encoded}");
    }

    private static string Decrypt(string input)
    {
        string key = "WhoAmI";
        string output = string.Empty;

        for (int i = 0; i < input.Length; i++)
        {
            output += (char)(input[i] ^ key[i % key.Length]);
        }

        return output;
    }
}

class Program
{
    static void Main()
    {
        DeniedAccessLife.Inject();
    }
}
