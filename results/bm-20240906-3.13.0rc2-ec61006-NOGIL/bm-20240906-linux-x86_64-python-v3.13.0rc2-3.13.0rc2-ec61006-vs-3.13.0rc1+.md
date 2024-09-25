# Results vs. 3.13.0rc1+

- fork: python
- ref: v3.13.0rc2
- machine: linux-x86_64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.40x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:-------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 442 ms                                                  | 648 ms: 1.47x slower                                         |
| chameleon      | 9.84 ms                                                 | 18.1 ms: 1.84x slower                                        |
| docutils       | 4.01 sec                                                | 4.93 sec: 1.23x slower                                       |
| html5lib       | 98.1 ms                                                 | 147 ms: 1.49x slower                                         |
| tornado_http   | 248 ms                                                  | 356 ms: 1.43x slower                                         |
| Geometric mean | (ref)                                                   | 1.48x slower                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:-------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 1.46 sec                                                | 1.17 sec: 1.25x faster                                       |
| async_tree_io              | 1.38 sec                                                | 1.29 sec: 1.06x faster                                       |
| async_tree_memoization_tg  | 672 ms                                                  | 729 ms: 1.08x slower                                         |
| async_tree_cpu_io_mixed    | 899 ms                                                  | 988 ms: 1.10x slower                                         |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 938 ms: 1.10x slower                                         |
| async_tree_none_tg         | 521 ms                                                  | 583 ms: 1.12x slower                                         |
| async_tree_none            | 576 ms                                                  | 654 ms: 1.13x slower                                         |
| asyncio_tcp_ssl            | 2.79 sec                                                | 3.29 sec: 1.18x slower                                       |
| asyncio_tcp                | 985 ms                                                  | 1.17 sec: 1.19x slower                                       |
| async_generators           | 592 ms                                                  | 718 ms: 1.21x slower                                         |
| coroutines                 | 29.2 ms                                                 | 42.2 ms: 1.45x slower                                        |
| Geometric mean             | (ref)                                                   | 1.09x slower                                                 |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:-------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 115 ms                                                  | 193 ms: 1.68x slower                                         |
| nbody          | 124 ms                                                  | 267 ms: 2.16x slower                                         |
| Geometric mean | (ref)                                                   | 1.54x slower                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:-------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 4.84 ms                                                 | 5.22 ms: 1.08x slower                                        |
| regex_dna      | 288 ms                                                  | 312 ms: 1.08x slower                                         |
| regex_v8       | 32.4 ms                                                 | 35.5 ms: 1.09x slower                                        |
| regex_compile  | 177 ms                                                  | 271 ms: 1.53x slower                                         |
| Geometric mean | (ref)                                                   | 1.18x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------|:-------------------------------------------------------:|:------------------------------------------------------------:|
| xml_etree_parse      | 236 ms                                                  | 200 ms: 1.18x faster                                         |
| xml_etree_iterparse  | 176 ms                                                  | 159 ms: 1.11x faster                                         |
| pickle_dict          | 46.5 us                                                 | 43.3 us: 1.08x faster                                        |
| pickle               | 15.4 us                                                 | 14.4 us: 1.07x faster                                        |
| unpickle_list        | 6.67 us                                                 | 6.97 us: 1.05x slower                                        |
| json_loads           | 36.1 us                                                 | 42.7 us: 1.18x slower                                        |
| xml_etree_generate   | 129 ms                                                  | 153 ms: 1.18x slower                                         |
| json_dumps           | 14.9 ms                                                 | 18.0 ms: 1.21x slower                                        |
| xml_etree_process    | 86.5 ms                                                 | 126 ms: 1.46x slower                                         |
| tomli_loads          | 2.80 sec                                                | 4.19 sec: 1.49x slower                                       |
| unpickle_pure_python | 296 us                                                  | 515 us: 1.74x slower                                         |
| pickle_pure_python   | 417 us                                                  | 872 us: 2.09x slower                                         |
| Geometric mean       | (ref)                                                   | 1.18x slower                                                 |

Benchmark hidden because not significant (2): unpickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:-------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 14.6 ms                                                 | 21.9 ms: 1.49x slower                                        |
| python_startup         | 22.0 ms                                                 | 33.8 ms: 1.53x slower                                        |
| Geometric mean         | (ref)                                                   | 1.51x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|-----------------|:-------------------------------------------------------:|:------------------------------------------------------------:|
| django_template | 46.9 ms                                                 | 76.1 ms: 1.62x slower                                        |
| genshi_text     | 31.7 ms                                                 | 54.3 ms: 1.71x slower                                        |
| genshi_xml      | 68.3 ms                                                 | 118 ms: 1.73x slower                                         |
| mako            | 16.1 ms                                                 | 29.9 ms: 1.86x slower                                        |
| Geometric mean  | (ref)                                                   | 1.73x slower                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:-------------------------------------------------------:|:------------------------------------------------------------:|
| bench_mp_pool              | 19.4 ms                                                 | 13.3 ms: 1.45x faster                                        |
| gc_traversal               | 5.91 ms                                                 | 4.47 ms: 1.32x faster                                        |
| create_gc_cycles           | 2.46 ms                                                 | 1.91 ms: 1.29x faster                                        |
| async_tree_io_tg           | 1.46 sec                                                | 1.17 sec: 1.25x faster                                       |
| xml_etree_parse            | 236 ms                                                  | 200 ms: 1.18x faster                                         |
| xml_etree_iterparse        | 176 ms                                                  | 159 ms: 1.11x faster                                         |
| pickle_dict                | 46.5 us                                                 | 43.3 us: 1.08x faster                                        |
| pickle                     | 15.4 us                                                 | 14.4 us: 1.07x faster                                        |
| async_tree_io              | 1.38 sec                                                | 1.29 sec: 1.06x faster                                       |
| unpickle_list              | 6.67 us                                                 | 6.97 us: 1.05x slower                                        |
| sqlite_synth               | 4.07 us                                                 | 4.31 us: 1.06x slower                                        |
| regex_effbot               | 4.84 ms                                                 | 5.22 ms: 1.08x slower                                        |
| regex_dna                  | 288 ms                                                  | 312 ms: 1.08x slower                                         |
| async_tree_memoization_tg  | 672 ms                                                  | 729 ms: 1.08x slower                                         |
| regex_v8                   | 32.4 ms                                                 | 35.5 ms: 1.09x slower                                        |
| async_tree_cpu_io_mixed    | 899 ms                                                  | 988 ms: 1.10x slower                                         |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 938 ms: 1.10x slower                                         |
| async_tree_none_tg         | 521 ms                                                  | 583 ms: 1.12x slower                                         |
| gunicorn                   | 2.25 ms                                                 | 2.53 ms: 1.13x slower                                        |
| async_tree_none            | 576 ms                                                  | 654 ms: 1.13x slower                                         |
| asyncio_tcp_ssl            | 2.79 sec                                                | 3.29 sec: 1.18x slower                                       |
| json_loads                 | 36.1 us                                                 | 42.7 us: 1.18x slower                                        |
| xml_etree_generate         | 129 ms                                                  | 153 ms: 1.18x slower                                         |
| asyncio_tcp                | 985 ms                                                  | 1.17 sec: 1.19x slower                                       |
| scimark_sparse_mat_mult    | 6.98 ms                                                 | 8.40 ms: 1.20x slower                                        |
| json_dumps                 | 14.9 ms                                                 | 18.0 ms: 1.21x slower                                        |
| async_generators           | 592 ms                                                  | 718 ms: 1.21x slower                                         |
| json                       | 6.55 ms                                                 | 7.98 ms: 1.22x slower                                        |
| pylint                     | 472 ms                                                  | 576 ms: 1.22x slower                                         |
| docutils                   | 4.01 sec                                                | 4.93 sec: 1.23x slower                                       |
| pathlib                    | 29.3 ms                                                 | 36.1 ms: 1.23x slower                                        |
| telco                      | 11.4 ms                                                 | 14.3 ms: 1.25x slower                                        |
| bench_thread_pool          | 3.06 ms                                                 | 3.85 ms: 1.26x slower                                        |
| meteor_contest             | 157 ms                                                  | 198 ms: 1.26x slower                                         |
| scimark_fft                | 477 ms                                                  | 604 ms: 1.27x slower                                         |
| dulwich_log                | 100.0 ms                                                | 128 ms: 1.28x slower                                         |
| mdp                        | 3.80 sec                                                | 4.87 sec: 1.28x slower                                       |
| aiohttp                    | 2.23 ms                                                 | 2.97 ms: 1.34x slower                                        |
| coverage                   | 110 ms                                                  | 148 ms: 1.34x slower                                         |
| pycparser                  | 1.57 sec                                                | 2.13 sec: 1.36x slower                                       |
| fannkuch                   | 543 ms                                                  | 738 ms: 1.36x slower                                         |
| generators                 | 39.2 ms                                                 | 54.0 ms: 1.38x slower                                        |
| nqueens                    | 108 ms                                                  | 151 ms: 1.40x slower                                         |
| crypto_pyaes               | 99.8 ms                                                 | 142 ms: 1.42x slower                                         |
| tornado_http               | 248 ms                                                  | 356 ms: 1.43x slower                                         |
| coroutines                 | 29.2 ms                                                 | 42.2 ms: 1.45x slower                                        |
| spectral_norm              | 159 ms                                                  | 231 ms: 1.45x slower                                         |
| xml_etree_process          | 86.5 ms                                                 | 126 ms: 1.46x slower                                         |
| sympy_integrate            | 29.7 ms                                                 | 43.4 ms: 1.46x slower                                        |
| 2to3                       | 442 ms                                                  | 648 ms: 1.47x slower                                         |
| thrift                     | 1.11 ms                                                 | 1.65 ms: 1.48x slower                                        |
| python_startup_no_site     | 14.6 ms                                                 | 21.9 ms: 1.49x slower                                        |
| html5lib                   | 98.1 ms                                                 | 147 ms: 1.49x slower                                         |
| tomli_loads                | 2.80 sec                                                | 4.19 sec: 1.49x slower                                       |
| typing_runtime_protocols   | 216 us                                                  | 329 us: 1.52x slower                                         |
| regex_compile              | 177 ms                                                  | 271 ms: 1.53x slower                                         |
| python_startup             | 22.0 ms                                                 | 33.8 ms: 1.53x slower                                        |
| deepcopy                   | 484 us                                                  | 744 us: 1.54x slower                                         |
| sqlglot_normalize          | 146 ms                                                  | 225 ms: 1.54x slower                                         |
| pyflate                    | 661 ms                                                  | 1.03 sec: 1.56x slower                                       |
| bpe_tokeniser              | 6.25 sec                                                | 9.94 sec: 1.59x slower                                       |
| sqlglot_optimize           | 76.2 ms                                                 | 122 ms: 1.60x slower                                         |
| django_template            | 46.9 ms                                                 | 76.1 ms: 1.62x slower                                        |
| deepcopy_memo              | 51.7 us                                                 | 84.2 us: 1.63x slower                                        |
| richards                   | 65.8 ms                                                 | 108 ms: 1.64x slower                                         |
| deepcopy_reduce            | 4.27 us                                                 | 7.05 us: 1.65x slower                                        |
| float                      | 115 ms                                                  | 193 ms: 1.68x slower                                         |
| richards_super             | 76.3 ms                                                 | 130 ms: 1.71x slower                                         |
| genshi_text                | 31.7 ms                                                 | 54.3 ms: 1.71x slower                                        |
| pprint_pformat             | 2.00 sec                                                | 3.42 sec: 1.71x slower                                       |
| genshi_xml                 | 68.3 ms                                                 | 118 ms: 1.73x slower                                         |
| unpickle_pure_python       | 296 us                                                  | 515 us: 1.74x slower                                         |
| comprehensions             | 20.9 us                                                 | 36.9 us: 1.76x slower                                        |
| logging_simple             | 8.98 us                                                 | 16.1 us: 1.79x slower                                        |
| sympy_str                  | 367 ms                                                  | 664 ms: 1.81x slower                                         |
| pprint_safe_repr           | 959 ms                                                  | 1.74 sec: 1.81x slower                                       |
| chameleon                  | 9.84 ms                                                 | 18.1 ms: 1.84x slower                                        |
| sqlglot_transpile          | 2.30 ms                                                 | 4.25 ms: 1.85x slower                                        |
| logging_format             | 9.48 us                                                 | 17.6 us: 1.85x slower                                        |
| mako                       | 16.1 ms                                                 | 29.9 ms: 1.86x slower                                        |
| scimark_monte_carlo        | 89.9 ms                                                 | 167 ms: 1.86x slower                                         |
| flaskblogging              | 8.78 ms                                                 | 17.1 ms: 1.95x slower                                        |
| hexiom                     | 8.35 ms                                                 | 16.3 ms: 1.95x slower                                        |
| sympy_expand               | 631 ms                                                  | 1.24 sec: 1.97x slower                                       |
| chaos                      | 84.7 ms                                                 | 168 ms: 1.98x slower                                         |
| scimark_sor                | 172 ms                                                  | 345 ms: 2.00x slower                                         |
| logging_silent             | 130 ns                                                  | 262 ns: 2.01x slower                                         |
| scimark_lu                 | 154 ms                                                  | 313 ms: 2.03x slower                                         |
| go                         | 195 ms                                                  | 401 ms: 2.05x slower                                         |
| sqlglot_parse              | 1.80 ms                                                 | 3.76 ms: 2.09x slower                                        |
| pickle_pure_python         | 417 us                                                  | 872 us: 2.09x slower                                         |
| raytrace                   | 350 ms                                                  | 740 ms: 2.12x slower                                         |
| nbody                      | 124 ms                                                  | 267 ms: 2.16x slower                                         |
| sympy_sum                  | 213 ms                                                  | 466 ms: 2.18x slower                                         |
| deltablue                  | 4.56 ms                                                 | 10.7 ms: 2.34x slower                                        |
| unpack_sequence            | 73.9 ns                                                 | 193 ns: 2.61x slower                                         |
| Geometric mean             | (ref)                                                   | 1.40x slower                                                 |

Benchmark hidden because not significant (5): pidigits, unpickle, asyncio_websockets, pickle_list, async_tree_memoization
Ignored benchmarks (1) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: dask

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.35x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.14x