
#include <iostream>
#include <queue>
#include <ctime>
using namespace std;
int main() 
{
    srand((unsigned)time(0));

    const int arraySize = 10;
    const int upperBounds = 500;

    int orderedRandArray[arraySize] = {0};
    
    //
    // Generate and sort the random numbers
    priority_queue<int> orderedRand;
    for (int i = 0; i < arraySize; ++i)
    {
        orderedRand.push( rand() % upperBounds);
    }
    
    //
    // Get the numbers out of the queue and store them.
    for(int i =0; i < arraySize; ++i)
    {
        orderedRandArray[i] = orderedRand.top();
        orderedRand.pop();
        //
        // Show number on screen.
        cout << orderedRandArray[i] << endl;
    }

    return 0;

}
