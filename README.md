一、	记录与数据处理：
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    double celsius, fahrenheit;
    cout << "请输入摄氏温度: ";
    cin >> celsius;
    fahrenheit = (9.0 / 5.0) * celsius + 32;
    cout << fixed << setprecision(2);
    cout << "对应的华氏温度为: " << fahrenheit << endl;
    return 0;
}
2．
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    double numerator = 2.0;
    double denominator = 1.0;
    double sum = 0.0;
    for (int i = 1; i <= 10; i++) {
        sum += numerator / denominator;
        double next_num = numerator + denominator;
        denominator = numerator;
        numerator = next_num;
    }
    cout << fixed << setprecision(2);
    cout << "数列前10项之和为: " << sum << endl;
    return 0;
}
3. #include <iostream>
#include <cmath>

using namespace std;

// 判断素数的函数
bool isPrime(int n) {
    if (n <= 1) return false;
    for (int i = 2; i <= sqrt(n); i++) {
        if (n % i == 0) return false;
    }
    return true;
}

int main() {
    int num;
    cout << "请输入一个整数: ";
    cin >> num;
    
    if (isPrime(num)) {
        cout << num << " 是素数。" << endl;
    } else {
        cout << num << " 不是素数。" << endl;
    }
    return 0;
}

4．
#include <iostream>
using namespace std;
void bubbleSort(int arr[], int n) {
    for (int i = 0; i < n - 1; i++) {
        bool swapped = false;
        for (int j = 0; j < n - 1 - i; j++) {
            if (arr[j] > arr[j+1]) {
                swap(arr[j], arr[j+1]);
                swapped = true;
            }
        }
        if (!swapped) break;
    }
}

int main() {
    int arr[] = {64, 34, 25, 12, 22, 11, 90};
    int n = sizeof(arr) / sizeof(arr[0]);
    bubbleSort(arr, n);
    cout << "排序后的数组: ";
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    return 0;
}

