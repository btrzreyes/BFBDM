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
        public static string PlayerOne, PlayerTwo; // allows the user input for Player 1 and Player 2 be read in other classes
        public static void TitleASCII()
        {
            Console.BackgroundColor = ConsoleColor.Black;
            Console.ForegroundColor = ConsoleColor.Yellow; // Yellow for any computer-generated text
            Console.Clear();
            Console.Title = "BATTLE FOR BAJO DE MASINLOC"; // The title at the top part of the dialog box when the application runs
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
            Console.Title = "Introduction and Player Creation";
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
                PlayerOne = Console.ReadLine();

                Console.ForegroundColor = ConsoleColor.Yellow;
                string PlayerTwoName = "What is Player 2's name? ";
                for (int i = 0; i < PlayerTwoName.Length; i++)
                {
                    Console.Write(PlayerTwoName[i]);
                    System.Threading.
                    Thread.Sleep(50);
                }

                Console.ForegroundColor = ConsoleColor.White;
                PlayerTwo = Console.ReadLine();
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
                    PlayerOne = Console.ReadLine();

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

    public static class MainStory
    {
        public static void MeetTheLeaders()
        {
            int PlayerDecision;
            Console.Clear();
            Console.Title = "Meet the Leaders";
            Console.ForegroundColor = ConsoleColor.Yellow; // Reverts back to the base game color Yellow

            string MeetLeadersIntro = "Welcome to the game, " + TitleScreen.PlayerOne + " and " + TitleScreen.PlayerTwo + "! \nThese two characters that you must choose are as follows.";
            for (int i = 0; i < MeetLeadersIntro.Length; i++)
            {
                Console.Write(MeetLeadersIntro[i]);
                System.Threading.
                Thread.Sleep(50);
            }

            Console.ReadLine();
            Console.Clear();

            Console.Title = "Meet Ogirdor";
            Console.WriteLine(@"                                                                                              
        _____          _____     ____      _____        _____           _____         _____   
   ____|\    \     ___|\    \   |    | ___|\    \   ___|\    \     ____|\    \    ___|\    \  
  /     /\    \   /    /\    \  |    ||    |\    \ |    |\    \   /     /\    \  |    |\    \ 
 /     /  \    \ |    |  |____| |    ||    | |    ||    | |    | /     /  \    \ |    | |    |
|     |    |    ||    |    ____ |    ||    |/____/ |    | |    ||     |    |    ||    |/____/ 
|     |    |    ||    |   |    ||    ||    |\    \ |    | |    ||     |    |    ||    |\    \ 
|\     \  /    /||    |   |_,  ||    ||    | |    ||    | |    ||\     \  /    /||    | |    |
| \_____\/____/ ||\ ___\___/  /||____||____| |____||____|/____/|| \_____\/____/ ||____| |____|
 \ |    ||    | /| |   /____ / ||    ||    | |    ||    /    | | \ |    ||    | /|    | |    |
  \|____||____|/  \|___|    | / |____||____| |____||____|____|/   \|____||____|/ |____| |____|
     \(    )/       \( |____|/    \(    \(     )/    \(    )/        \(    )/      \(     )/  
      '    '         '   )/        '     '     '      '    '          '    '        '     ' ");

            string OgirdorIntro = "insert text of Ogirdor here, based on the Story Flow";
            for (int i = 0; i < OgirdorIntro.Length; i++)
            {
                Console.Write(OgirdorIntro[i]);
                System.Threading.
                Thread.Sleep(50);
            }

            Console.WriteLine();
            Console.WriteLine("Press enter to view the next character.");
            Console.ReadLine();
            Console.Clear();

            Console.Title = "Meet Chinping";
            Console.WriteLine(@"                                                                               ______                                                         
        _____         __     __         ____________  _____    _____     _____|\     \   ____________  _____    _____            _____        
   _____\    \_      /  \   /  \       /            \|\    \   \    \   /     / |     | /            \|\    \   \    \      _____\    \_      
  /     /|     |    /   /| |\   \     |\___/\  \\___/|\\    \   |    | |      |/     /||\___/\  \\___/|\\    \   |    |    /     /|     |     
 /     / /____/|   /   //   \\   \     \|____\  \___|/ \\    \  |    | |      |\____/ | \|____\  \___|/ \\    \  |    |   /     / /____/|     
|     | |____|/   /    \_____/    \          |  |       \|    \ |    | |\     \    | /        |  |       \|    \ |    |  |     | |_____|/     
|     |  _____   /    /\_____/\    \    __  /   / __     |     \|    | | \     \___|/    __  /   / __     |     \|    |  |     | |_________   
|\     \|\    \ /    //\_____/\\    \  /  \/   /_/  |   /     /\      \|  \     \       /  \/   /_/  |   /     /\      \ |\     \|\        \  
| \_____\|    |/____/ |       | \____\|____________/|  /_____/ /______/|\  \_____\     |____________/|  /_____/ /______/|| \_____\|    |\__/| 
| |     /____/||    | |       | |    ||           | / |      | |     | | \ |     |     |           | / |      | |     | || |     /____/| | || 
 \|_____|    |||____|/         \|____||___________|/  |______|/|_____|/   \|_____|     |___________|/  |______|/|_____|/  \|_____|     |\|_|/ 
        |____|/                                                                                                                  |____/       ");
            
            string ChinpingIntro = "insert text of Chinping here, based on the Story Flow";
            for (int i = 0; i < ChinpingIntro.Length; i++)
            {
                Console.Write(ChinpingIntro[i]);
                System.Threading.
                Thread.Sleep(50);
            }

            Console.WriteLine();
            Console.WriteLine("Press enter to continue to the story.");
            Console.ReadLine();
            Console.Clear();

            string NumericalValuesPrompt = "Would you like to see the numerical values of the attacks and items?";
            for (int i = 0; i < NumericalValuesPrompt.Length; i++)
            {
                Console.Write(NumericalValuesPrompt[i]);
                System.Threading.
                Thread.Sleep(50);
            }

            Console.WriteLine();
            Console.ForegroundColor = ConsoleColor.Red; // Red for giving choices
            Console.WriteLine("[1. YES/ 2. NO]");
            Console.ForegroundColor = ConsoleColor.White; // White for letting the player choose his/ her own choice

            PlayerDecision = int.Parse(Console.ReadLine()); // will ask for the Player choice

            if (PlayerDecision == 1 )
            {
                MainStory.LeaderStats();
            }
            else if (PlayerDecision == 2)
            {
                MainStory.PlayerChoose();
            }

        }

        public static void LeaderStats()
        {
            Console.Clear();
            Console.WriteLine("Leader Stats");
        }

        public static void PlayerChoose()
        {
            Console.Clear();
            Console.WriteLine("Player Choose");
        }

        class Program
        {

            static void Main()
            {
                TitleScreen.TitleASCII();
                TitleScreen.Introduction();
                MainStory.MeetTheLeaders();
                Console.ReadKey();
            }
        }
    }
}
