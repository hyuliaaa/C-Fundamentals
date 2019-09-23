//program that reads a positive integer number and return its square root. The number will be entered witg "noise" in it, i.g.
//there will be symbols in it which are not digist. These symbols should be ignored. The last symbol of the input will be .(dot)
//  Input   |   Output
//  25.     |   5
// ,,2et5&. |   5
// -9abc.   |   3

#include <iostream>
#include <vector>
#include <cmath>


std::vector <char> readInput()
{
    char symbol;
    std::vector <char> vec;
    while(symbol!='.')
    {
        std::cin>>symbol;
        vec.push_back(symbol);
    }

    return vec;
}

std:: vector <int> extractNumbers( const std::vector <char> &vec)
{
    std::vector<int>numbers;

    for (char symbol: vec)
    {
        if (symbol>='0' && symbol<='9')
        {
            numbers.push_back(symbol-'0');
        }
    }
    return numbers;
}
int calculateNumber( const std::vector <int>& numbers)
{
    int size=numbers.size();
    int multiplier=1;
    int num=0;
    for (int i=size-1; i>=0; i--)
    {
        num+=numbers[i]*multiplier;
        multiplier*=10;
    }
    return num;
}

int main()
{
    const std::vector<char> vec=readInput();
    std::cout<<sqrt(calculateNumber(extractNumbers(vec)));


    return 0;

}
