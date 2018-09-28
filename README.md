# Factorial
<3
class Recursividad
	{
		
		public void RecFor()
		{
			Random quark = new Random();
			int num = 6;
            int[] Vektor = new int[num];
            for (int k = 0; k < num; k++)
			{
				Console.Write("Numeros: ");
                Vektor[k] = quark.Next(1, 7);
				Console.WriteLine(Vektor[k]);

			}
            for (int r = 0; r < num; r++)
            {
                Vektor[r] = Vektor[r] * r;
                Console.WriteLine("El Resultado del Factorial es: " + Vektor[r]);
            }
		}

		public int Factorial(int n)
		{
            
            if (n== 0)
	        {
				return 1;
			}
			else
			{
                return n + Factorial(n - 1);
			}
		}
        
		static void Main(string[] args)
		{
            Recursividad bit = new Recursividad();

			int op = 0;
			while (op != 3)
			{
				Console.WriteLine("1.-Factorial For. ");
				Console.WriteLine("2.-Factorial Por recursividad.");
                Console.WriteLine("3.- Salir");

      			op = int.Parse(Console.ReadLine());
				Console.WriteLine();
				switch (op)
				{
					case 1:
						TimeSpan stop;
						TimeSpan start = new TimeSpan(DateTime.Now.Ticks);
                        bit.RecFor();
						stop = new TimeSpan(DateTime.Now.Ticks);
						Console.Write(stop.Subtract(start).TotalSeconds); Console.WriteLine(" Segundos ");
						break;
					case 2:
                        
						TimeSpan startp = new TimeSpan(DateTime.Now.Ticks);
                        int v=bit.Factorial(4);
                        Console.WriteLine("El resultado es: " + v);
						stop = new TimeSpan(DateTime.Now.Ticks);
						Console.Write(stop.Subtract(start).TotalSeconds); Console.WriteLine(" Segundos ");
						break;

				}
                Console.ReadKey();
			}
			
		}
	}
