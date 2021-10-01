#include <bits/stdc++.h>
using namespace std;
#define nline "\n"
#define int long long

void solve()
{
    int n, m, k;
    cin >> n >> m >> k;
    k--;
    int edge = 0;
    if (m < n - 1 || m > ((n * (n - 1)) / 2))
    {
        cout << "NO";
        return;
    }
    if (m < n)
    {
        edge = n - 1;
    }
    else if (m == ((n * (n - 1)) / 2))
    {
        edge = 1;
    }
    else
    {
        edge = n / 2;
        m -= n;
        if (m >= 2 && n % 2 == 0)
        {
            edge--;
        }
    }
    if (edge < k)
    {
        cout << "YES";
    }
    else
        cout << "NO";
}
int32_t main()
{
    ios_base::sync_with_stdio(false);
#ifndef ONLINE_JUDGE
    freopen("input.txt", "r", stdin);
    freopen("output.txt", "w", stderr);
    freopen("output.txt", "w", stdout);
#endif
    cin.tie(NULL);
    cout.tie(NULL);
    int tt = 1;
    cin >> tt;
    while (tt--)
    {
        solve();
        cout << nline;
    }
    return 0;
}
