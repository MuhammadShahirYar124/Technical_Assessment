# Technical_Assessment

#include <iostream>
using namespace std;
void maxMeeting(int start[], int end[], int n) {
	int max_start = start[0];
	int max_end = end[0];
	int count = 0;

	for (int i = 0; i<n; i++)
	{
		for (int j = 0; j<n; j++)
		{
			if (max_start <= start[i])
			{
				max_start = start[i];
				if (max_end <= end[j])
				{
					max_end = end[j];


					if (start[i] <= end[j])
					{

						/*cout << a[i] << " | " << b[j] << endl;*/
						count++;

						i++;
					}
				}

			}

			else
			{
				i++;
			}


		}
		cout << count << endl;
	}

}
int main()
{
	int start[] = { 1, 3, 2, 5 };
	int end[] = { 2, 4, 3, 6 };

	int n = sizeof(start) / sizeof(start[0]);
	maxMeeting(start, end, n);
	system("pause");
	return 0;
}
