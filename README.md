/* BATTLE FOR BAJO DE MASINLOC
 * A text-based RPG/ Strategy game for two players loosely based off on real events.
 * 
 * Submitted by:
 * Miguel Froilan Legata
 * Beatriz Ysabel Reyes
 * Kriz Anne Louise Rodriguez
 * 
 * Submitted to:
 * Mr. Deocaris
 * 
 * 12-Ogilvie, Group MBK
 * 
 */
using System;

namespace _MBK
{
   
    public static class TitleScreen
    {
        public static void TitleASCII()
        {
            Console.BackgroundColor = ConsoleColor.Black;
            Console.ForegroundColor = ConsoleColor.Yellow; // Yellow for any computer-generated text
            Console.Clear();
            Console.Title = "Battle for Bajo de Masinloc";
            Console.WriteLine(@"                       _______  _______  _______  _______  ___      _______                  _______  _______  ______                        
                      |  _    ||   _   ||       ||       ||   |    |       |                |       ||       ||    _ |                       
                      | |_|   ||  |_|  ||_     _||_     _||   |    |    ___|                |    ___||   _   ||   | ||                       
                      |       ||       |  |   |    |   |  |   |    |   |___                 |   |___ |  | |  ||   |_||_                      
                      |  _   | |       |  |   |    |   |  |   |___ |    ___|                |    ___||  |_|  ||    __  |                     
                      | |_|   ||   _   |  |   |    |   |  |       ||   |___                 |   |    |       ||   |  | |                     
                      |_______||__| |__|  |___|    |___|  |_______||_______|                |___|    |_______||___|  |_|                     
 _______  _______      ___  _______            ______   _______          __   __  _______  _______  ___   __    _  ___      _______  _______ 
|  _    ||   _   |    |   ||       |          |      | |       |        |  |_|  ||   _   ||       ||   | |  |  | ||   |    |       ||       |
| |_|   ||  |_|  |    |   ||   _   |          |  _    ||    ___|        |       ||  |_|  ||  _____||   | |   |_| ||   |    |   _   ||       |
|       ||       |    |   ||  | |  |          | | |   ||   |___         |       ||       || |_____ |   | |       ||   |    |  | |  ||       |
|  _   | |       | ___|   ||  |_|  |          | |_|   ||    ___|        |       ||       ||_____  ||   | |  _    ||   |___ |  |_|  ||      _|
| |_|   ||   _   ||       ||       |          |       ||   |___         | ||_|| ||   _   | _____| ||   | | | |   ||       ||       ||     |_ 
|_______||__| |__||_______||_______|          |______| |_______|        |_|   |_||__| |__||_______||___| |_|  |__||_______||_______||_______|");
            Console.ReadLine();
            Console.Clear();
        }

        public static void Introduction()
        {
            Console.ForegroundColor = ConsoleColor.Yellow;
            int PlayerDecision;
            string IntroductionText = @"Welcome to the game BATTLE FOR BAJO DE MASINLOC. 
Two players are required to play this game. 
Please decide which player shall be Player 1 and Player 2. 
..........
Have you decided?
Input the number of your choice:
"; // The text to be displayed which appears as "typing"

            for (int i = 0; i < IntroductionText.Length; i++)
            {
                Console.Write(IntroductionText[i]);
                System.Threading.
                Thread.Sleep(50);
            }

            Console.ForegroundColor = ConsoleColor.Red; // Red for giving choices
            Console.WriteLine("[1. YES/ 2. NO]");
            Console.ForegroundColor = ConsoleColor.White; // White for letting the player choose his/ her own choice
            PlayerDecision = int.Parse(Console.ReadLine()); // will ask for the Player names 

            if (PlayerDecision == 1)
            {
                Console.ForegroundColor = ConsoleColor.Yellow;
                string PlayerOneName = "What is Player 1's name? ";
                for (int i = 0; i < PlayerOneName.Length; i++)
                {
                    Console.Write(PlayerOneName[i]);
                    System.Threading.
                    Thread.Sleep(50);
                }

                Console.ForegroundColor = ConsoleColor.White;
                Console.ReadLine();

                Console.ForegroundColor = ConsoleColor.Yellow;
                string PlayerTwoName = "What is Player 2's name? ";
                for (int i = 0; i < PlayerTwoName.Length; i++)
                {
                    Console.Write(PlayerTwoName[i]);
                    System.Threading.
                    Thread.Sleep(50);
                }

                Console.ForegroundColor = ConsoleColor.White;
                Console.ReadLine();
                Console.WriteLine();

            }

            else
            {
                int PlayerNameFinalDecision;
                Console.ForegroundColor = ConsoleColor.Yellow; // Reverts back to the base game color Yellow
                string PlayerNameDecision = @"Please input 1 to confirm that you are ready. If not, input 2 to reset the title screen.
";
                for (int i = 0; i < PlayerNameDecision.Length; i++)
                {
                    Console.Write(PlayerNameDecision[i]);
                    System.Threading.
                    Thread.Sleep(50);
                }

                Console.ForegroundColor = ConsoleColor.White;
                PlayerNameFinalDecision = int.Parse(Console.ReadLine());
                if (PlayerNameFinalDecision == 1) 
                {
                    Console.ForegroundColor = ConsoleColor.Yellow;
                    string PlayerOneName = "What is Player 1's name? ";
                    for (int i = 0; i < PlayerOneName.Length; i++)
                    {
                        Console.Write(PlayerOneName[i]);
                        System.Threading.
                        Thread.Sleep(50);
                    }

                    Console.ForegroundColor = ConsoleColor.White;
                    Console.ReadLine();

                    Console.ForegroundColor = ConsoleColor.Yellow;
                    string PlayerTwoName = "What is Player 2's name? ";
                    for (int i = 0; i < PlayerTwoName.Length; i++)
                    {
                        Console.Write(PlayerTwoName[i]);
                        System.Threading.
                        Thread.Sleep(50);
                    }
                    Console.ForegroundColor = ConsoleColor.White;
                    Console.ReadLine();
                    Console.WriteLine();

                }
                else 
                {
                    Console.Clear();
                    TitleScreen.Introduction();

                }
            }
           

        }

    }
    class Program
    {
        
        static void Main()
        {
            TitleScreen.TitleASCII();
            TitleScreen.Introduction();
            Console.ReadKey();
        }
    }
}
