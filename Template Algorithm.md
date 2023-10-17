# <center> Templates
by Hyr1sky_He

## Bit Algorithm

#### About XOR
blog [here](https://www.ruanyifeng.com/blog/2021/01/_xor.html#:~:text=%E5%BC%82%E6%88%96%E8%BF%90%E7%AE%97%E5%8F%AF%E4%BB%A5%E7%94%A8%E4%BA%8E%E6%95%B0%E6%8D%AE%E5%A4%87%E4%BB%BD%E3%80%82%20%E6%96%87%E4%BB%B6%20x%20%E5%92%8C%E6%96%87%E4%BB%B6%20y%20%E8%BF%9B%E8%A1%8C%E5%BC%82%E6%88%96%E8%BF%90%E7%AE%97%EF%BC%8C%E4%BA%A7%E7%94%9F%E4%B8%80%E4%B8%AA%E5%A4%87%E4%BB%BD%E6%96%87%E4%BB%B6%20z%E3%80%82%20x,%5E%20y%20%3D%200%20%5E%20y%20%3D%20y)


## Quick Power

#### Normal Version
```c++
long long int quik_power(int base, int power)
{
	long long int result = 1;
	while (power > 0)           //指数大于0进行指数折半，底数变其平方的操作
	{
		if (power & 1)			//指数为奇数，power & 1这相当于power % 2 == 1
			result *= base;     //分离出当前项并累乘后保存
		power >>= 1;			//指数折半,power >>= 1这相当于power /= 2;
		base *= base;           //底数变其平方
	}
	return result;              //返回最终结果
}

```