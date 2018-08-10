# Start-me-up
A place to start my page here
// randc++11
#include <random>
#include <iostream>
  
/* I am aware that I did not originate this code.
it is a starting point for a bigger project. 
If you are the original author of randc++11 or know that person please
contact me! Thanks.  */

namespace
{
    std::random_device rd;
    std::mt19937 mt(rd()); // seed the random number generator once
}

int GetRandomNumber(const int lowBound, const int highBound)
{
    std::uniform_int_distribution<int> dist(lowBound, highBound);
    return dist(mt);
}

int main()
{
    const auto diceResult = GetRandomNumber(1, 6);
    std::cout << diceResult << std::endl;
    return 0;
}
