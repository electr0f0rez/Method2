# Method2
```

    internal class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello, World!");
            Tervitus();
            string kasutajaNimi = "";
            Tervitus();
            kasutajaNimi = KasutajanimeKüsimine(kasutajaNimi);
            float eelarve = KasutajanimeKüsimine(ref kasutajaNimi);
            bool kasKasutajaNõustab = false;
            Tervitus();
            kasKasutajaNõustab = NõusolekuKüsimine(kasutajaNimi, eelarve, kasKasutajaNõustab);

        }

        private static string kasutajaNimi(string kasutajaNimi)
        {
            return kasutajaNimi;
        }

        private static void Tervitus()
        {
            Tervitus();
        }

        private static bool NõusolekuKüsimine(string kasutajaNimi, float eelarve, bool kasKasutajaNõustab)
        {
            while (kasKasutajaNõustab == false)
            {
                Console.WriteLine($"{kasutajaNimi}, kas see on sinu õige eelarve: {eelarve}");
                Console.WriteLine("Vasta kas jah või ei");
                string vastus = Console.ReadLine();
                if (vastus == "jah")
                {
                    kasKasutajaNõustab = true;
                }
                else
                {
                    kasKasutajaNõustab = false;
                }
            }

            return kasKasutajaNõustab;
        }

        private static float KasutajanimeKüsimine(ref string kasutajaNimi)
        {
            while (kasutajaNimi == "")
            {
                Console.WriteLine("TERRE, palun sisesta oma kasutajanimi");
                kasutajaNimi = Console.ReadLine();
            }
            Console.WriteLine("Mis on sinu nädalane eelarve?");
            float eelarve = 0.00f;
            return kasutajaNimi;
        }
    }
}
