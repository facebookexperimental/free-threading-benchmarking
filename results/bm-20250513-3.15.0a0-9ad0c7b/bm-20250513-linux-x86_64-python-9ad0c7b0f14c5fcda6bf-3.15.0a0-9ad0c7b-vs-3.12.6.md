# Results vs. 3.12.6

- fork: python
- ref: 9ad0c7b0f14c5fcda6bf
- machine: linux-x86_64
- commit hash: 9ad0c7b
- commit date: 2025-05-13
- overall geometric mean: 1.209x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 338 ms: 1.35x faster                                                  |
| docutils       | 4.00 sec                                               | 3.39 sec: 1.18x faster                                                |
| html5lib       | 88.9 ms                                                | 76.2 ms: 1.17x faster                                                 |
| Geometric mean | (ref)                                                  | 1.23x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 977 ms                                                 | 412 ms: 2.37x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 801 ms: 2.31x faster                                                  |
| async_tree_io_tg           | 1.93 sec                                               | 841 ms: 2.30x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 416 ms: 2.24x faster                                                  |
| async_tree_none            | 741 ms                                                 | 347 ms: 2.14x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 331 ms: 2.13x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 620 ms: 1.78x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 618 ms: 1.74x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 649 ms: 1.15x faster                                                  |
| async_generators           | 589 ms                                                 | 512 ms: 1.15x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.77x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 123 ms                                                 | 97.2 ms: 1.27x faster                                                 |
| pidigits       | 250 ms                                                 | 232 ms: 1.08x faster                                                  |
| nbody          | 119 ms                                                 | 123 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 3.74 ms: 1.37x faster                                                 |
| regex_compile  | 187 ms                                                 | 153 ms: 1.22x faster                                                  |
| regex_v8       | 32.5 ms                                                | 27.7 ms: 1.17x faster                                                 |
| regex_dna      | 278 ms                                                 | 237 ms: 1.17x faster                                                  |
| Geometric mean | (ref)                                                  | 1.23x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 175 ms: 1.38x faster                                                  |
| xml_etree_iterparse  | 169 ms                                                 | 125 ms: 1.35x faster                                                  |
| xml_etree_generate   | 127 ms                                                 | 110 ms: 1.16x faster                                                  |
| tomli_loads          | 2.88 sec                                               | 2.50 sec: 1.15x faster                                                |
| pickle_pure_python   | 436 us                                                 | 390 us: 1.12x faster                                                  |
| unpickle_pure_python | 300 us                                                 | 269 us: 1.11x faster                                                  |
| xml_etree_process    | 83.7 ms                                                | 75.2 ms: 1.11x faster                                                 |
| json_dumps           | 14.3 ms                                                | 13.8 ms: 1.04x faster                                                 |
| Geometric mean       | (ref)                                                  | 1.15x faster                                                          |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 10.4 ms: 1.69x faster                                                 |
| python_startup         | 23.7 ms                                                | 17.6 ms: 1.35x faster                                                 |
| Geometric mean         | (ref)                                                  | 1.51x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 26.4 ms: 1.14x faster                                                 |
| genshi_xml      | 67.6 ms                                                | 62.0 ms: 1.09x faster                                                 |
| django_template | 44.9 ms                                                | 43.2 ms: 1.04x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 977 ms                                                 | 412 ms: 2.37x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 801 ms: 2.31x faster                                                  |
| async_tree_io_tg           | 1.93 sec                                               | 841 ms: 2.30x faster                                                  |
| mdp                        | 3.97 sec                                               | 1.74 sec: 2.28x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 416 ms: 2.24x faster                                                  |
| async_tree_none            | 741 ms                                                 | 347 ms: 2.14x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 331 ms: 2.13x faster                                                  |
| bench_thread_pool          | 3.48 ms                                                | 1.79 ms: 1.95x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 620 ms: 1.78x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 618 ms: 1.74x faster                                                  |
| python_startup_no_site     | 17.6 ms                                                | 10.4 ms: 1.69x faster                                                 |
| deepcopy                   | 468 us                                                 | 326 us: 1.44x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 37.4 us: 1.40x faster                                                 |
| xml_etree_parse            | 241 ms                                                 | 175 ms: 1.38x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 3.74 ms: 1.37x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 125 ms: 1.35x faster                                                  |
| 2to3                       | 456 ms                                                 | 338 ms: 1.35x faster                                                  |
| dulwich_log                | 100 ms                                                 | 74.3 ms: 1.35x faster                                                 |
| python_startup             | 23.7 ms                                                | 17.6 ms: 1.35x faster                                                 |
| pathlib                    | 31.6 ms                                                | 24.0 ms: 1.31x faster                                                 |
| pyflate                    | 727 ms                                                 | 559 ms: 1.30x faster                                                  |
| sympy_integrate            | 29.8 ms                                                | 23.4 ms: 1.27x faster                                                 |
| pylint                     | 465 ms                                                 | 365 ms: 1.27x faster                                                  |
| comprehensions             | 27.1 us                                                | 21.4 us: 1.27x faster                                                 |
| float                      | 123 ms                                                 | 97.2 ms: 1.27x faster                                                 |
| pycparser                  | 1.79 sec                                               | 1.45 sec: 1.23x faster                                                |
| regex_compile              | 187 ms                                                 | 153 ms: 1.22x faster                                                  |
| raytrace                   | 408 ms                                                 | 336 ms: 1.22x faster                                                  |
| sympy_sum                  | 222 ms                                                 | 183 ms: 1.21x faster                                                  |
| go                         | 172 ms                                                 | 142 ms: 1.21x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.22 us: 1.20x faster                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 5.52 sec: 1.19x faster                                                |
| deepcopy_reduce            | 4.04 us                                                | 3.40 us: 1.19x faster                                                 |
| spectral_norm              | 156 ms                                                 | 131 ms: 1.19x faster                                                  |
| sympy_str                  | 385 ms                                                 | 325 ms: 1.18x faster                                                  |
| docutils                   | 4.00 sec                                               | 3.39 sec: 1.18x faster                                                |
| nqueens                    | 117 ms                                                 | 99.3 ms: 1.18x faster                                                 |
| regex_v8                   | 32.5 ms                                                | 27.7 ms: 1.17x faster                                                 |
| regex_dna                  | 278 ms                                                 | 237 ms: 1.17x faster                                                  |
| richards_super             | 72.8 ms                                                | 62.3 ms: 1.17x faster                                                 |
| html5lib                   | 88.9 ms                                                | 76.2 ms: 1.17x faster                                                 |
| crypto_pyaes               | 107 ms                                                 | 92.3 ms: 1.16x faster                                                 |
| xml_etree_generate         | 127 ms                                                 | 110 ms: 1.16x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.50 sec: 1.15x faster                                                |
| asyncio_websockets         | 748 ms                                                 | 649 ms: 1.15x faster                                                  |
| logging_simple             | 9.45 us                                                | 8.20 us: 1.15x faster                                                 |
| async_generators           | 589 ms                                                 | 512 ms: 1.15x faster                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 83.9 ms: 1.15x faster                                                 |
| genshi_text                | 30.2 ms                                                | 26.4 ms: 1.14x faster                                                 |
| chaos                      | 84.9 ms                                                | 74.2 ms: 1.14x faster                                                 |
| typing_runtime_protocols   | 224 us                                                 | 197 us: 1.14x faster                                                  |
| meteor_contest             | 146 ms                                                 | 129 ms: 1.13x faster                                                  |
| scimark_sor                | 167 ms                                                 | 149 ms: 1.12x faster                                                  |
| thrift                     | 1.06 ms                                                | 946 us: 1.12x faster                                                  |
| pickle_pure_python         | 436 us                                                 | 390 us: 1.12x faster                                                  |
| richards                   | 60.3 ms                                                | 54.0 ms: 1.12x faster                                                 |
| unpickle_pure_python       | 300 us                                                 | 269 us: 1.11x faster                                                  |
| xml_etree_process          | 83.7 ms                                                | 75.2 ms: 1.11x faster                                                 |
| scimark_fft                | 500 ms                                                 | 456 ms: 1.10x faster                                                  |
| hexiom                     | 8.27 ms                                                | 7.59 ms: 1.09x faster                                                 |
| genshi_xml                 | 67.6 ms                                                | 62.0 ms: 1.09x faster                                                 |
| pidigits                   | 250 ms                                                 | 232 ms: 1.08x faster                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.25 ms: 1.07x faster                                                 |
| logging_format             | 9.59 us                                                | 8.97 us: 1.07x faster                                                 |
| pprint_pformat             | 1.98 sec                                               | 1.85 sec: 1.07x faster                                                |
| pprint_safe_repr           | 967 ms                                                 | 909 ms: 1.06x faster                                                  |
| sympy_expand               | 582 ms                                                 | 550 ms: 1.06x faster                                                  |
| fannkuch                   | 540 ms                                                 | 512 ms: 1.05x faster                                                  |
| django_template            | 44.9 ms                                                | 43.2 ms: 1.04x faster                                                 |
| scimark_lu                 | 152 ms                                                 | 146 ms: 1.04x faster                                                  |
| json_dumps                 | 14.3 ms                                                | 13.8 ms: 1.04x faster                                                 |
| generators                 | 41.1 ms                                                | 39.7 ms: 1.04x faster                                                 |
| nbody                      | 119 ms                                                 | 123 ms: 1.03x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 6.39 ms: 1.09x slower                                                 |
| coverage                   | 95.4 ms                                                | 105 ms: 1.10x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.16 ms: 1.63x slower                                                 |
| bench_mp_pool              | 20.7 ms                                                | 80.3 ms: 3.88x slower                                                 |
| logging_silent             | 139 ns                                                 | 615 ns: 4.42x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.19x faster                                                          |

Benchmark hidden because not significant (6): telco, json_loads, deltablue, coroutines, json, mako
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.209x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.12x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.17x