# 1260---Sales


#include <iostream>

using namespace std;

int  A[1001];

int main()
{

	int T, n;

	int i, j;
	cin >> T;

	while (T--) {
		
		cin >> n;

		int res = 0, tmp;

		for (i = 0; i < n; i++)
		{
			cin >> tmp;

			for (j = i - 1; j >= 0; j--)
				if (tmp < A[j])
					A[j + 1] = A[j];
				else
					break;
			
			A[j + 1] = tmp;
			res += j + 1;
		}
		cout << res << endl;
	}
	return 0;
}
