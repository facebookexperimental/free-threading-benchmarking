# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5a4fb7e
- commit date: 2024-09-06
- overall geometric mean: 1.48x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.36x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 445 ms                                                       | 682 ms: 1.53x slower                                  |
| docutils       | 4.01 sec                                                     | 5.10 sec: 1.27x slower                                |
| html5lib       | 92.6 ms                                                      | 147 ms: 1.59x slower                                  |
| tornado_http   | 251 ms                                                       | 420 ms: 1.67x slower                                  |
| Geometric mean | (ref)                                                        | 1.51x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.24 sec: 1.13x faster                                |
| async_tree_io              | 1.39 sec                                                     | 1.32 sec: 1.05x faster                                |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 885 ms: 1.04x slower                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 937 ms: 1.05x slower                                  |
| async_tree_none            | 572 ms                                                       | 607 ms: 1.06x slower                                  |
| asyncio_websockets         | 766 ms                                                       | 818 ms: 1.07x slower                                  |
| async_tree_none_tg         | 504 ms                                                       | 540 ms: 1.07x slower                                  |
| async_tree_memoization     | 709 ms                                                       | 770 ms: 1.09x slower                                  |
| async_generators           | 567 ms                                                       | 723 ms: 1.27x slower                                  |
| asyncio_tcp                | 948 ms                                                       | 1.22 sec: 1.29x slower                                |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.67 sec: 1.32x slower                                |
| coroutines                 | 30.9 ms                                                      | 42.2 ms: 1.37x slower                                 |
| Geometric mean             | (ref)                                                        | 1.10x slower                                          |

Benchmark hidden because not significant (1): async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 116 ms                                                       | 203 ms: 1.75x slower                                  |
| nbody          | 119 ms                                                       | 315 ms: 2.66x slower                                  |
| Geometric mean | (ref)                                                        | 1.68x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 299 ms: 1.06x slower                                  |
| regex_effbot   | 4.74 ms                                                      | 5.21 ms: 1.10x slower                                 |
| regex_v8       | 32.8 ms                                                      | 37.6 ms: 1.15x slower                                 |
| regex_compile  | 182 ms                                                       | 305 ms: 1.68x slower                                  |
| Geometric mean | (ref)                                                        | 1.22x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle               | 15.1 us                                                      | 13.8 us: 1.10x faster                                 |
| xml_etree_iterparse  | 177 ms                                                       | 168 ms: 1.06x faster                                  |
| pickle_list          | 6.86 us                                                      | 6.51 us: 1.05x faster                                 |
| unpickle_list        | 6.68 us                                                      | 7.45 us: 1.12x slower                                 |
| unpickle             | 20.5 us                                                      | 23.1 us: 1.13x slower                                 |
| json_dumps           | 14.1 ms                                                      | 18.0 ms: 1.28x slower                                 |
| json_loads           | 34.3 us                                                      | 47.7 us: 1.39x slower                                 |
| xml_etree_generate   | 122 ms                                                       | 179 ms: 1.47x slower                                  |
| tomli_loads          | 2.78 sec                                                     | 4.37 sec: 1.57x slower                                |
| xml_etree_process    | 85.9 ms                                                      | 136 ms: 1.58x slower                                  |
| pickle_pure_python   | 416 us                                                       | 762 us: 1.83x slower                                  |
| unpickle_pure_python | 290 us                                                       | 563 us: 1.94x slower                                  |
| Geometric mean       | (ref)                                                        | 1.25x slower                                          |

Benchmark hidden because not significant (2): pickle_dict, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 24.3 ms: 1.59x slower                                 |
| python_startup         | 22.4 ms                                                      | 37.1 ms: 1.65x slower                                 |
| Geometric mean         | (ref)                                                        | 1.62x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 57.6 ms: 1.82x slower                                 |
| django_template | 44.3 ms                                                      | 83.6 ms: 1.89x slower                                 |
| genshi_xml      | 72.1 ms                                                      | 141 ms: 1.95x slower                                  |
| mako            | 15.9 ms                                                      | 31.9 ms: 2.00x slower                                 |
| Geometric mean  | (ref)                                                        | 1.91x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| create_gc_cycles           | 2.41 ms                                                      | 1.96 ms: 1.23x faster                                 |
| gc_traversal               | 5.70 ms                                                      | 4.74 ms: 1.20x faster                                 |
| async_tree_io_tg           | 1.40 sec                                                     | 1.24 sec: 1.13x faster                                |
| pickle                     | 15.1 us                                                      | 13.8 us: 1.10x faster                                 |
| xml_etree_iterparse        | 177 ms                                                       | 168 ms: 1.06x faster                                  |
| pickle_list                | 6.86 us                                                      | 6.51 us: 1.05x faster                                 |
| async_tree_io              | 1.39 sec                                                     | 1.32 sec: 1.05x faster                                |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 885 ms: 1.04x slower                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 937 ms: 1.05x slower                                  |
| regex_dna                  | 282 ms                                                       | 299 ms: 1.06x slower                                  |
| async_tree_none            | 572 ms                                                       | 607 ms: 1.06x slower                                  |
| sqlite_synth               | 3.99 us                                                      | 4.25 us: 1.07x slower                                 |
| asyncio_websockets         | 766 ms                                                       | 818 ms: 1.07x slower                                  |
| async_tree_none_tg         | 504 ms                                                       | 540 ms: 1.07x slower                                  |
| async_tree_memoization     | 709 ms                                                       | 770 ms: 1.09x slower                                  |
| regex_effbot               | 4.74 ms                                                      | 5.21 ms: 1.10x slower                                 |
| unpickle_list              | 6.68 us                                                      | 7.45 us: 1.12x slower                                 |
| unpickle                   | 20.5 us                                                      | 23.1 us: 1.13x slower                                 |
| regex_v8                   | 32.8 ms                                                      | 37.6 ms: 1.15x slower                                 |
| pathlib                    | 29.9 ms                                                      | 36.2 ms: 1.21x slower                                 |
| telco                      | 12.2 ms                                                      | 14.9 ms: 1.22x slower                                 |
| deepcopy                   | 498 us                                                       | 617 us: 1.24x slower                                  |
| docutils                   | 4.01 sec                                                     | 5.10 sec: 1.27x slower                                |
| async_generators           | 567 ms                                                       | 723 ms: 1.27x slower                                  |
| json_dumps                 | 14.1 ms                                                      | 18.0 ms: 1.28x slower                                 |
| asyncio_tcp                | 948 ms                                                       | 1.22 sec: 1.29x slower                                |
| meteor_contest             | 150 ms                                                       | 196 ms: 1.30x slower                                  |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.67 sec: 1.32x slower                                |
| mdp                        | 3.80 sec                                                     | 5.07 sec: 1.33x slower                                |
| coverage                   | 107 ms                                                       | 144 ms: 1.35x slower                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 9.21 ms: 1.36x slower                                 |
| pylint                     | 470 ms                                                       | 641 ms: 1.36x slower                                  |
| coroutines                 | 30.9 ms                                                      | 42.2 ms: 1.37x slower                                 |
| json                       | 6.51 ms                                                      | 9.01 ms: 1.38x slower                                 |
| json_loads                 | 34.3 us                                                      | 47.7 us: 1.39x slower                                 |
| scimark_fft                | 473 ms                                                       | 659 ms: 1.39x slower                                  |
| generators                 | 40.0 ms                                                      | 56.6 ms: 1.41x slower                                 |
| deepcopy_memo              | 50.1 us                                                      | 71.0 us: 1.42x slower                                 |
| deepcopy_reduce            | 4.10 us                                                      | 5.81 us: 1.42x slower                                 |
| pycparser                  | 1.57 sec                                                     | 2.29 sec: 1.46x slower                                |
| xml_etree_generate         | 122 ms                                                       | 179 ms: 1.47x slower                                  |
| fannkuch                   | 547 ms                                                       | 807 ms: 1.48x slower                                  |
| nqueens                    | 112 ms                                                       | 170 ms: 1.52x slower                                  |
| thrift                     | 1.10 ms                                                      | 1.68 ms: 1.53x slower                                 |
| dulwich_log                | 93.7 ms                                                      | 143 ms: 1.53x slower                                  |
| 2to3                       | 445 ms                                                       | 682 ms: 1.53x slower                                  |
| tomli_loads                | 2.78 sec                                                     | 4.37 sec: 1.57x slower                                |
| crypto_pyaes               | 100 ms                                                       | 158 ms: 1.57x slower                                  |
| xml_etree_process          | 85.9 ms                                                      | 136 ms: 1.58x slower                                  |
| typing_runtime_protocols   | 226 us                                                       | 357 us: 1.58x slower                                  |
| python_startup_no_site     | 15.3 ms                                                      | 24.3 ms: 1.59x slower                                 |
| html5lib                   | 92.6 ms                                                      | 147 ms: 1.59x slower                                  |
| spectral_norm              | 157 ms                                                       | 253 ms: 1.62x slower                                  |
| richards                   | 65.5 ms                                                      | 107 ms: 1.63x slower                                  |
| sympy_integrate            | 30.2 ms                                                      | 49.3 ms: 1.63x slower                                 |
| python_startup             | 22.4 ms                                                      | 37.1 ms: 1.65x slower                                 |
| sqlglot_optimize           | 74.7 ms                                                      | 125 ms: 1.67x slower                                  |
| pyflate                    | 664 ms                                                       | 1.11 sec: 1.67x slower                                |
| tornado_http               | 251 ms                                                       | 420 ms: 1.67x slower                                  |
| regex_compile              | 182 ms                                                       | 305 ms: 1.68x slower                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.66 sec: 1.68x slower                                |
| bpe_tokeniser              | 6.28 sec                                                     | 10.8 sec: 1.71x slower                                |
| richards_super             | 73.2 ms                                                      | 126 ms: 1.72x slower                                  |
| float                      | 116 ms                                                       | 203 ms: 1.75x slower                                  |
| sqlglot_normalize          | 140 ms                                                       | 248 ms: 1.77x slower                                  |
| genshi_text                | 31.7 ms                                                      | 57.6 ms: 1.82x slower                                 |
| pprint_pformat             | 1.94 sec                                                     | 3.55 sec: 1.83x slower                                |
| pickle_pure_python         | 416 us                                                       | 762 us: 1.83x slower                                  |
| bench_thread_pool          | 2.89 ms                                                      | 5.33 ms: 1.85x slower                                 |
| comprehensions             | 22.2 us                                                      | 41.3 us: 1.86x slower                                 |
| logging_simple             | 8.56 us                                                      | 16.0 us: 1.87x slower                                 |
| sympy_str                  | 379 ms                                                       | 708 ms: 1.87x slower                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 171 ms: 1.88x slower                                  |
| django_template            | 44.3 ms                                                      | 83.6 ms: 1.89x slower                                 |
| logging_format             | 9.24 us                                                      | 17.5 us: 1.89x slower                                 |
| go                         | 191 ms                                                       | 370 ms: 1.94x slower                                  |
| unpickle_pure_python       | 290 us                                                       | 563 us: 1.94x slower                                  |
| chaos                      | 83.6 ms                                                      | 163 ms: 1.94x slower                                  |
| genshi_xml                 | 72.1 ms                                                      | 141 ms: 1.95x slower                                  |
| mako                       | 15.9 ms                                                      | 31.9 ms: 2.00x slower                                 |
| scimark_sor                | 179 ms                                                       | 360 ms: 2.02x slower                                  |
| logging_silent             | 130 ns                                                       | 266 ns: 2.04x slower                                  |
| hexiom                     | 8.11 ms                                                      | 17.1 ms: 2.11x slower                                 |
| sqlglot_parse              | 1.76 ms                                                      | 3.76 ms: 2.14x slower                                 |
| sqlglot_transpile          | 2.20 ms                                                      | 4.73 ms: 2.15x slower                                 |
| sympy_expand               | 601 ms                                                       | 1.32 sec: 2.19x slower                                |
| scimark_lu                 | 146 ms                                                       | 328 ms: 2.24x slower                                  |
| sympy_sum                  | 210 ms                                                       | 472 ms: 2.24x slower                                  |
| raytrace                   | 344 ms                                                       | 798 ms: 2.32x slower                                  |
| nbody                      | 119 ms                                                       | 315 ms: 2.66x slower                                  |
| deltablue                  | 4.44 ms                                                      | 12.2 ms: 2.74x slower                                 |
| unpack_sequence            | 74.3 ns                                                      | 207 ns: 2.79x slower                                  |
| Geometric mean             | (ref)                                                        | 1.48x slower                                          |

Benchmark hidden because not significant (5): pickle_dict, xml_etree_parse, async_tree_memoization_tg, pidigits, bench_mp_pool
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.40x
- 95% likely to have a slowdown of 1.39x
- 99% likely to have a slowdown of 1.36x

# Memory
- memory change: 1.15x