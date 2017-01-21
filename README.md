# Benchmarks

The following setups provide some performance overview of different technologies
for web developers.

## Apache Benchmark Tool

For measuring performance the Apache Benchmark tool is used with the following
configuration:

```bash
ab -c 200 -n 200000 -k -r http://localhost/
```

## Results

| Setup                           | Benchmark 1 | Benchmark 2 | Benchmark 3 | Average |
|---------------------------------|-------------|-------------|-------------|---------|
| Apache                          | 21581.97    | 21027.88    | 21523.00    |         |
| Nginx                           | 31753.23    | 32329.99    | 31013.53    |         |
| OpenLiteSpeed                   | 35055.21    | 34897.56    | 36317.55    |         |
| OpenLiteSpeed + PHP             | 17378.13    | 17919.59    | 16342.48    |         |
| OpenLiteSpeed + Swoole (TCP/IP) | 23332.65    | 23080.37    | 23532.65    |         |
| Apache + PHP                    | 8428.64     | 9418.61     | 9337.44     |         |
| Nginx PHP-FPM (TCP/IP socket)   | 4220.03     | 3891.33     | 4006.04     |         |
| Nginx PHP-FPM (UNIX socket)     | 13992.15    | 14458.09    | 13663.37    |         |
| Swoole                          | 43139.84    | 42701.30    | 42474.30    |         |
| Nginx + Swoole (TCP/IP) socket  | 12225.28    | 10430.24    | 10443.99    |         |
| Nginx + Swoole (UNIX Socket)    | 13522.05    | 14737.56    | 16314.50    |         |

## Disclaimer

The following benchmarks are intended to provide an overview how different setups
behave and to learn how to optimize certain technology for performance.

Running the benchmarks on different hardware also gets different results. Better
workstation/server might have different results because of CPU and network, but
the relative comparison shouldn't be much different from one hardware to another.

## License

This repository is released under the [MIT License](LICENSE).
