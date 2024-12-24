# Results vs. 3.12.6

- fork: python
- ref: 30efede33ca1fe32debb
- machine: linux-x86_64
- commit hash: 30efede
- commit date: 2024-12-24
- overall geometric mean: 1.140x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 612 ms: 1.34x slower                                                   |
| docutils       | 4.00 sec                                               | 4.40 sec: 1.10x slower                                                 |
| html5lib       | 88.9 ms                                                | 131 ms: 1.47x slower                                                   |
| Geometric mean | (ref)                                                  | 1.30x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 964 ms: 2.01x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 1.06 sec: 1.75x faster                                                 |
| async_tree_none_tg         | 704 ms                                                 | 421 ms: 1.67x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 571 ms: 1.63x faster                                                   |
| async_tree_none            | 741 ms                                                 | 504 ms: 1.47x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 671 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 776 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 857 ms: 1.26x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 770 ms: 1.03x slower                                                   |
| async_generators           | 589 ms                                                 | 658 ms: 1.12x slower                                                   |
| coroutines                 | 29.5 ms                                                | 35.0 ms: 1.19x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 240 ms: 1.04x faster                                                   |
| float          | 123 ms                                                 | 147 ms: 1.19x slower                                                   |
| nbody          | 119 ms                                                 | 177 ms: 1.48x slower                                                   |
| Geometric mean | (ref)                                                  | 1.19x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.76 ms: 1.08x faster                                                  |
| regex_dna      | 278 ms                                                 | 300 ms: 1.08x slower                                                   |
| regex_v8       | 32.5 ms                                                | 35.7 ms: 1.10x slower                                                  |
| regex_compile  | 187 ms                                                 | 219 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 148 ms: 1.14x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 222 ms: 1.08x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 3.25 sec: 1.13x slower                                                 |
| xml_etree_generate   | 127 ms                                                 | 147 ms: 1.15x slower                                                   |
| xml_etree_process    | 83.7 ms                                                | 101 ms: 1.21x slower                                                   |
| json_dumps           | 14.3 ms                                                | 17.6 ms: 1.23x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 418 us: 1.39x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 654 us: 1.50x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.14x slower                                                           |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 20.4 ms: 1.16x slower                                                  |
| python_startup         | 23.7 ms                                                | 31.0 ms: 1.31x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.23x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 87.7 ms: 1.30x slower                                                  |
| django_template | 44.9 ms                                                | 59.3 ms: 1.32x slower                                                  |
| genshi_text     | 30.2 ms                                                | 40.0 ms: 1.32x slower                                                  |
| mako            | 15.7 ms                                                | 26.8 ms: 1.70x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.40x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 964 ms: 2.01x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 1.06 sec: 1.75x faster                                                 |
| async_tree_none_tg         | 704 ms                                                 | 421 ms: 1.67x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 571 ms: 1.63x faster                                                   |
| async_tree_none            | 741 ms                                                 | 504 ms: 1.47x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 671 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 776 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 857 ms: 1.26x faster                                                   |
| deepcopy                   | 468 us                                                 | 408 us: 1.15x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 148 ms: 1.14x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 222 ms: 1.08x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.76 ms: 1.08x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.68 us: 1.05x faster                                                  |
| pidigits                   | 250 ms                                                 | 240 ms: 1.04x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 770 ms: 1.03x slower                                                   |
| pycparser                  | 1.79 sec                                               | 1.87 sec: 1.04x slower                                                 |
| spectral_norm              | 156 ms                                                 | 165 ms: 1.06x slower                                                   |
| regex_dna                  | 278 ms                                                 | 300 ms: 1.08x slower                                                   |
| pylint                     | 465 ms                                                 | 509 ms: 1.10x slower                                                   |
| regex_v8                   | 32.5 ms                                                | 35.7 ms: 1.10x slower                                                  |
| docutils                   | 4.00 sec                                               | 4.40 sec: 1.10x slower                                                 |
| scimark_fft                | 500 ms                                                 | 551 ms: 1.10x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.39 sec: 1.11x slower                                                 |
| sqlalchemy_declarative     | 218 ms                                                 | 242 ms: 1.11x slower                                                   |
| nqueens                    | 117 ms                                                 | 130 ms: 1.11x slower                                                   |
| async_generators           | 589 ms                                                 | 658 ms: 1.12x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.25 sec: 1.13x slower                                                 |
| deepcopy_reduce            | 4.04 us                                                | 4.57 us: 1.13x slower                                                  |
| sqlglot_normalize          | 157 ms                                                 | 179 ms: 1.14x slower                                                   |
| dulwich_log                | 100 ms                                                 | 115 ms: 1.15x slower                                                   |
| xml_etree_generate         | 127 ms                                                 | 147 ms: 1.15x slower                                                   |
| python_startup_no_site     | 17.6 ms                                                | 20.4 ms: 1.16x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 6.85 ms: 1.17x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 260 ms: 1.17x slower                                                   |
| regex_compile              | 187 ms                                                 | 219 ms: 1.17x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 126 ms: 1.18x slower                                                   |
| coroutines                 | 29.5 ms                                                | 35.0 ms: 1.19x slower                                                  |
| float                      | 123 ms                                                 | 147 ms: 1.19x slower                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 91.1 ms: 1.20x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 35.8 ms: 1.20x slower                                                  |
| sympy_str                  | 385 ms                                                 | 464 ms: 1.21x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 101 ms: 1.21x slower                                                   |
| logging_simple             | 9.45 us                                                | 11.5 us: 1.21x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.29 ms: 1.22x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.18 ms: 1.22x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 17.6 ms: 1.23x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 8.12 sec: 1.23x slower                                                 |
| sympy_expand               | 582 ms                                                 | 718 ms: 1.23x slower                                                   |
| meteor_contest             | 146 ms                                                 | 181 ms: 1.24x slower                                                   |
| bench_thread_pool          | 3.48 ms                                                | 4.32 ms: 1.24x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 278 us: 1.24x slower                                                   |
| pyflate                    | 727 ms                                                 | 930 ms: 1.28x slower                                                   |
| comprehensions             | 27.1 us                                                | 34.7 us: 1.28x slower                                                  |
| fannkuch                   | 540 ms                                                 | 697 ms: 1.29x slower                                                   |
| generators                 | 41.1 ms                                                | 53.2 ms: 1.29x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 87.7 ms: 1.30x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 198 ms: 1.30x slower                                                   |
| python_startup             | 23.7 ms                                                | 31.0 ms: 1.31x slower                                                  |
| django_template            | 44.9 ms                                                | 59.3 ms: 1.32x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 2.62 sec: 1.32x slower                                                 |
| genshi_text                | 30.2 ms                                                | 40.0 ms: 1.32x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.28 sec: 1.33x slower                                                 |
| richards_super             | 72.8 ms                                                | 96.8 ms: 1.33x slower                                                  |
| 2to3                       | 456 ms                                                 | 612 ms: 1.34x slower                                                   |
| logging_format             | 9.59 us                                                | 12.9 us: 1.35x slower                                                  |
| telco                      | 9.59 ms                                                | 13.0 ms: 1.36x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 418 us: 1.39x slower                                                   |
| coverage                   | 95.4 ms                                                | 136 ms: 1.43x slower                                                   |
| richards                   | 60.3 ms                                                | 87.7 ms: 1.45x slower                                                  |
| html5lib                   | 88.9 ms                                                | 131 ms: 1.47x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 142 ms: 1.48x slower                                                   |
| nbody                      | 119 ms                                                 | 177 ms: 1.48x slower                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 36.7 ms: 1.49x slower                                                  |
| raytrace                   | 408 ms                                                 | 607 ms: 1.49x slower                                                   |
| pickle_pure_python         | 436 us                                                 | 654 us: 1.50x slower                                                   |
| chaos                      | 84.9 ms                                                | 129 ms: 1.53x slower                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 3.60 ms: 1.54x slower                                                  |
| hexiom                     | 8.27 ms                                                | 13.0 ms: 1.57x slower                                                  |
| logging_silent             | 139 ns                                                 | 222 ns: 1.60x slower                                                   |
| scimark_sor                | 167 ms                                                 | 272 ms: 1.63x slower                                                   |
| sqlglot_parse              | 1.79 ms                                                | 2.94 ms: 1.65x slower                                                  |
| go                         | 172 ms                                                 | 289 ms: 1.68x slower                                                   |
| mako                       | 15.7 ms                                                | 26.8 ms: 1.70x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.38 ms: 1.74x slower                                                  |
| deltablue                  | 4.27 ms                                                | 11.0 ms: 2.57x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 95.6 ms: 4.62x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.19x slower                                                           |

Benchmark hidden because not significant (4): pathlib, json_loads, deepcopy_memo, json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.140x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.34x