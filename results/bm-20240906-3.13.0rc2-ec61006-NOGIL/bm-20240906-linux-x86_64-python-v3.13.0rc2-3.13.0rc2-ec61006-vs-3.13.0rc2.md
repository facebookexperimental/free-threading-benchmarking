# Results vs. 3.13.0rc2

- fork: python
- ref: v3.13.0rc2
- machine: linux-x86_64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.42x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------|:-------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| 2to3           | 445 ms                                                                                                  | 648 ms: 1.46x slower                                                                                          |
| chameleon      | 9.34 ms                                                                                                 | 18.1 ms: 1.94x slower                                                                                         |
| docutils       | 4.01 sec                                                                                                | 4.93 sec: 1.23x slower                                                                                        |
| html5lib       | 92.6 ms                                                                                                 | 147 ms: 1.58x slower                                                                                          |
| tornado_http   | 251 ms                                                                                                  | 356 ms: 1.42x slower                                                                                          |
| Geometric mean | (ref)                                                                                                   | 1.51x slower                                                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------------------|:-------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                                                                | 1.17 sec: 1.20x faster                                                                                        |
| async_tree_io              | 1.39 sec                                                                                                | 1.29 sec: 1.07x faster                                                                                        |
| async_tree_memoization     | 709 ms                                                                                                  | 766 ms: 1.08x slower                                                                                          |
| async_tree_memoization_tg  | 670 ms                                                                                                  | 729 ms: 1.09x slower                                                                                          |
| async_tree_cpu_io_mixed_tg | 852 ms                                                                                                  | 938 ms: 1.10x slower                                                                                          |
| async_tree_cpu_io_mixed    | 889 ms                                                                                                  | 988 ms: 1.11x slower                                                                                          |
| async_tree_none            | 572 ms                                                                                                  | 654 ms: 1.14x slower                                                                                          |
| async_tree_none_tg         | 504 ms                                                                                                  | 583 ms: 1.16x slower                                                                                          |
| asyncio_tcp_ssl            | 2.77 sec                                                                                                | 3.29 sec: 1.19x slower                                                                                        |
| asyncio_tcp                | 948 ms                                                                                                  | 1.17 sec: 1.23x slower                                                                                        |
| async_generators           | 567 ms                                                                                                  | 718 ms: 1.27x slower                                                                                          |
| coroutines                 | 30.9 ms                                                                                                 | 42.2 ms: 1.37x slower                                                                                         |
| Geometric mean             | (ref)                                                                                                   | 1.11x slower                                                                                                  |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------|:-------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| float          | 116 ms                                                                                                  | 193 ms: 1.66x slower                                                                                          |
| nbody          | 119 ms                                                                                                  | 267 ms: 2.25x slower                                                                                          |
| Geometric mean | (ref)                                                                                                   | 1.55x slower                                                                                                  |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------|:-------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                                                                 | 35.5 ms: 1.08x slower                                                                                         |
| regex_effbot   | 4.74 ms                                                                                                 | 5.22 ms: 1.10x slower                                                                                         |
| regex_dna      | 282 ms                                                                                                  | 312 ms: 1.11x slower                                                                                          |
| regex_compile  | 182 ms                                                                                                  | 271 ms: 1.49x slower                                                                                          |
| Geometric mean | (ref)                                                                                                   | 1.18x slower                                                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------------|:-------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 231 ms                                                                                                  | 200 ms: 1.16x faster                                                                                          |
| xml_etree_iterparse  | 177 ms                                                                                                  | 159 ms: 1.11x faster                                                                                          |
| pickle_dict          | 47.2 us                                                                                                 | 43.3 us: 1.09x faster                                                                                         |
| pickle               | 15.1 us                                                                                                 | 14.4 us: 1.05x faster                                                                                         |
| unpickle_list        | 6.68 us                                                                                                 | 6.97 us: 1.04x slower                                                                                         |
| json_loads           | 34.3 us                                                                                                 | 42.7 us: 1.25x slower                                                                                         |
| xml_etree_generate   | 122 ms                                                                                                  | 153 ms: 1.25x slower                                                                                          |
| json_dumps           | 14.1 ms                                                                                                 | 18.0 ms: 1.27x slower                                                                                         |
| xml_etree_process    | 85.9 ms                                                                                                 | 126 ms: 1.47x slower                                                                                          |
| tomli_loads          | 2.78 sec                                                                                                | 4.19 sec: 1.51x slower                                                                                        |
| unpickle_pure_python | 290 us                                                                                                  | 515 us: 1.77x slower                                                                                          |
| pickle_pure_python   | 416 us                                                                                                  | 872 us: 2.09x slower                                                                                          |
| Geometric mean       | (ref)                                                                                                   | 1.20x slower                                                                                                  |

Benchmark hidden because not significant (2): pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|------------------------|:-------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                                                                 | 21.9 ms: 1.43x slower                                                                                         |
| python_startup         | 22.4 ms                                                                                                 | 33.8 ms: 1.51x slower                                                                                         |
| Geometric mean         | (ref)                                                                                                   | 1.47x slower                                                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|-----------------|:-------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                                                                 | 118 ms: 1.64x slower                                                                                          |
| genshi_text     | 31.7 ms                                                                                                 | 54.3 ms: 1.71x slower                                                                                         |
| django_template | 44.3 ms                                                                                                 | 76.1 ms: 1.72x slower                                                                                         |
| mako            | 15.9 ms                                                                                                 | 29.9 ms: 1.87x slower                                                                                         |
| Geometric mean  | (ref)                                                                                                   | 1.74x slower                                                                                                  |

All benchmarks:
===============

| Benchmark                  | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------------------|:-------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 18.7 ms                                                                                                 | 13.3 ms: 1.40x faster                                                                                         |
| gc_traversal               | 5.70 ms                                                                                                 | 4.47 ms: 1.28x faster                                                                                         |
| create_gc_cycles           | 2.41 ms                                                                                                 | 1.91 ms: 1.26x faster                                                                                         |
| async_tree_io_tg           | 1.40 sec                                                                                                | 1.17 sec: 1.20x faster                                                                                        |
| xml_etree_parse            | 231 ms                                                                                                  | 200 ms: 1.16x faster                                                                                          |
| xml_etree_iterparse        | 177 ms                                                                                                  | 159 ms: 1.11x faster                                                                                          |
| pickle_dict                | 47.2 us                                                                                                 | 43.3 us: 1.09x faster                                                                                         |
| async_tree_io              | 1.39 sec                                                                                                | 1.29 sec: 1.07x faster                                                                                        |
| pickle                     | 15.1 us                                                                                                 | 14.4 us: 1.05x faster                                                                                         |
| unpickle_list              | 6.68 us                                                                                                 | 6.97 us: 1.04x slower                                                                                         |
| async_tree_memoization     | 709 ms                                                                                                  | 766 ms: 1.08x slower                                                                                          |
| sqlite_synth               | 3.99 us                                                                                                 | 4.31 us: 1.08x slower                                                                                         |
| regex_v8                   | 32.8 ms                                                                                                 | 35.5 ms: 1.08x slower                                                                                         |
| async_tree_memoization_tg  | 670 ms                                                                                                  | 729 ms: 1.09x slower                                                                                          |
| regex_effbot               | 4.74 ms                                                                                                 | 5.22 ms: 1.10x slower                                                                                         |
| async_tree_cpu_io_mixed_tg | 852 ms                                                                                                  | 938 ms: 1.10x slower                                                                                          |
| regex_dna                  | 282 ms                                                                                                  | 312 ms: 1.11x slower                                                                                          |
| async_tree_cpu_io_mixed    | 889 ms                                                                                                  | 988 ms: 1.11x slower                                                                                          |
| async_tree_none            | 572 ms                                                                                                  | 654 ms: 1.14x slower                                                                                          |
| async_tree_none_tg         | 504 ms                                                                                                  | 583 ms: 1.16x slower                                                                                          |
| telco                      | 12.2 ms                                                                                                 | 14.3 ms: 1.17x slower                                                                                         |
| asyncio_tcp_ssl            | 2.77 sec                                                                                                | 3.29 sec: 1.19x slower                                                                                        |
| pathlib                    | 29.9 ms                                                                                                 | 36.1 ms: 1.21x slower                                                                                         |
| json                       | 6.51 ms                                                                                                 | 7.98 ms: 1.22x slower                                                                                         |
| pylint                     | 470 ms                                                                                                  | 576 ms: 1.23x slower                                                                                          |
| docutils                   | 4.01 sec                                                                                                | 4.93 sec: 1.23x slower                                                                                        |
| asyncio_tcp                | 948 ms                                                                                                  | 1.17 sec: 1.23x slower                                                                                        |
| scimark_sparse_mat_mult    | 6.76 ms                                                                                                 | 8.40 ms: 1.24x slower                                                                                         |
| json_loads                 | 34.3 us                                                                                                 | 42.7 us: 1.25x slower                                                                                         |
| xml_etree_generate         | 122 ms                                                                                                  | 153 ms: 1.25x slower                                                                                          |
| async_generators           | 567 ms                                                                                                  | 718 ms: 1.27x slower                                                                                          |
| json_dumps                 | 14.1 ms                                                                                                 | 18.0 ms: 1.27x slower                                                                                         |
| scimark_fft                | 473 ms                                                                                                  | 604 ms: 1.28x slower                                                                                          |
| mdp                        | 3.80 sec                                                                                                | 4.87 sec: 1.28x slower                                                                                        |
| meteor_contest             | 150 ms                                                                                                  | 198 ms: 1.32x slower                                                                                          |
| gunicorn                   | 1.91 ms                                                                                                 | 2.53 ms: 1.33x slower                                                                                         |
| bench_thread_pool          | 2.89 ms                                                                                                 | 3.85 ms: 1.33x slower                                                                                         |
| fannkuch                   | 547 ms                                                                                                  | 738 ms: 1.35x slower                                                                                          |
| generators                 | 40.0 ms                                                                                                 | 54.0 ms: 1.35x slower                                                                                         |
| nqueens                    | 112 ms                                                                                                  | 151 ms: 1.35x slower                                                                                          |
| pycparser                  | 1.57 sec                                                                                                | 2.13 sec: 1.36x slower                                                                                        |
| dulwich_log                | 93.7 ms                                                                                                 | 128 ms: 1.37x slower                                                                                          |
| coroutines                 | 30.9 ms                                                                                                 | 42.2 ms: 1.37x slower                                                                                         |
| coverage                   | 107 ms                                                                                                  | 148 ms: 1.38x slower                                                                                          |
| crypto_pyaes               | 100 ms                                                                                                  | 142 ms: 1.41x slower                                                                                          |
| tornado_http               | 251 ms                                                                                                  | 356 ms: 1.42x slower                                                                                          |
| python_startup_no_site     | 15.3 ms                                                                                                 | 21.9 ms: 1.43x slower                                                                                         |
| sympy_integrate            | 30.2 ms                                                                                                 | 43.4 ms: 1.44x slower                                                                                         |
| 2to3                       | 445 ms                                                                                                  | 648 ms: 1.46x slower                                                                                          |
| typing_runtime_protocols   | 226 us                                                                                                  | 329 us: 1.46x slower                                                                                          |
| aiohttp                    | 2.03 ms                                                                                                 | 2.97 ms: 1.46x slower                                                                                         |
| xml_etree_process          | 85.9 ms                                                                                                 | 126 ms: 1.47x slower                                                                                          |
| spectral_norm              | 157 ms                                                                                                  | 231 ms: 1.47x slower                                                                                          |
| regex_compile              | 182 ms                                                                                                  | 271 ms: 1.49x slower                                                                                          |
| deepcopy                   | 498 us                                                                                                  | 744 us: 1.49x slower                                                                                          |
| thrift                     | 1.10 ms                                                                                                 | 1.65 ms: 1.50x slower                                                                                         |
| tomli_loads                | 2.78 sec                                                                                                | 4.19 sec: 1.51x slower                                                                                        |
| python_startup             | 22.4 ms                                                                                                 | 33.8 ms: 1.51x slower                                                                                         |
| pyflate                    | 664 ms                                                                                                  | 1.03 sec: 1.55x slower                                                                                        |
| bpe_tokeniser              | 6.28 sec                                                                                                | 9.94 sec: 1.58x slower                                                                                        |
| html5lib                   | 92.6 ms                                                                                                 | 147 ms: 1.58x slower                                                                                          |
| sqlglot_normalize          | 140 ms                                                                                                  | 225 ms: 1.61x slower                                                                                          |
| sqlglot_optimize           | 74.7 ms                                                                                                 | 122 ms: 1.63x slower                                                                                          |
| genshi_xml                 | 72.1 ms                                                                                                 | 118 ms: 1.64x slower                                                                                          |
| richards                   | 65.5 ms                                                                                                 | 108 ms: 1.65x slower                                                                                          |
| comprehensions             | 22.2 us                                                                                                 | 36.9 us: 1.66x slower                                                                                         |
| float                      | 116 ms                                                                                                  | 193 ms: 1.66x slower                                                                                          |
| deepcopy_memo              | 50.1 us                                                                                                 | 84.2 us: 1.68x slower                                                                                         |
| genshi_text                | 31.7 ms                                                                                                 | 54.3 ms: 1.71x slower                                                                                         |
| django_template            | 44.3 ms                                                                                                 | 76.1 ms: 1.72x slower                                                                                         |
| deepcopy_reduce            | 4.10 us                                                                                                 | 7.05 us: 1.72x slower                                                                                         |
| sympy_str                  | 379 ms                                                                                                  | 664 ms: 1.75x slower                                                                                          |
| pprint_safe_repr           | 987 ms                                                                                                  | 1.74 sec: 1.76x slower                                                                                        |
| pprint_pformat             | 1.94 sec                                                                                                | 3.42 sec: 1.76x slower                                                                                        |
| unpickle_pure_python       | 290 us                                                                                                  | 515 us: 1.77x slower                                                                                          |
| richards_super             | 73.2 ms                                                                                                 | 130 ms: 1.78x slower                                                                                          |
| scimark_monte_carlo        | 90.6 ms                                                                                                 | 167 ms: 1.85x slower                                                                                          |
| mako                       | 15.9 ms                                                                                                 | 29.9 ms: 1.87x slower                                                                                         |
| logging_simple             | 8.56 us                                                                                                 | 16.1 us: 1.88x slower                                                                                         |
| logging_format             | 9.24 us                                                                                                 | 17.6 us: 1.90x slower                                                                                         |
| scimark_sor                | 179 ms                                                                                                  | 345 ms: 1.93x slower                                                                                          |
| sqlglot_transpile          | 2.20 ms                                                                                                 | 4.25 ms: 1.94x slower                                                                                         |
| chameleon                  | 9.34 ms                                                                                                 | 18.1 ms: 1.94x slower                                                                                         |
| chaos                      | 83.6 ms                                                                                                 | 168 ms: 2.01x slower                                                                                          |
| hexiom                     | 8.11 ms                                                                                                 | 16.3 ms: 2.01x slower                                                                                         |
| logging_silent             | 130 ns                                                                                                  | 262 ns: 2.01x slower                                                                                          |
| sympy_expand               | 601 ms                                                                                                  | 1.24 sec: 2.07x slower                                                                                        |
| pickle_pure_python         | 416 us                                                                                                  | 872 us: 2.09x slower                                                                                          |
| go                         | 191 ms                                                                                                  | 401 ms: 2.10x slower                                                                                          |
| scimark_lu                 | 146 ms                                                                                                  | 313 ms: 2.14x slower                                                                                          |
| sqlglot_parse              | 1.76 ms                                                                                                 | 3.76 ms: 2.14x slower                                                                                         |
| raytrace                   | 344 ms                                                                                                  | 740 ms: 2.15x slower                                                                                          |
| sympy_sum                  | 210 ms                                                                                                  | 466 ms: 2.22x slower                                                                                          |
| flaskblogging              | 7.68 ms                                                                                                 | 17.1 ms: 2.23x slower                                                                                         |
| nbody                      | 119 ms                                                                                                  | 267 ms: 2.25x slower                                                                                          |
| deltablue                  | 4.44 ms                                                                                                 | 10.7 ms: 2.41x slower                                                                                         |
| unpack_sequence            | 74.3 ns                                                                                                 | 193 ns: 2.59x slower                                                                                          |
| Geometric mean             | (ref)                                                                                                   | 1.42x slower                                                                                                  |

Benchmark hidden because not significant (4): pidigits, pickle_list, asyncio_websockets, unpickle
Ignored benchmarks (1) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: dask

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.33x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.14x