# Results vs. 3.12.6

- fork: python
- ref: 9ad0c7b0f14c5fcda6bf
- machine: linux-x86_64
- commit hash: 9ad0c7b
- commit date: 2025-05-13
- overall geometric mean: 1.114x faster
- HPT reliability: 93.64%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 378 ms: 1.21x faster                                                  |
| docutils       | 4.00 sec                                               | 3.68 sec: 1.09x faster                                                |
| html5lib       | 88.9 ms                                                | 82.2 ms: 1.08x faster                                                 |
| Geometric mean | (ref)                                                  | 1.12x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 662 ms: 2.92x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 711 ms: 2.60x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 387 ms: 2.40x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 293 ms: 2.40x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 434 ms: 2.25x faster                                                  |
| async_tree_none            | 741 ms                                                 | 340 ms: 2.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 579 ms: 1.90x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 630 ms: 1.71x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 674 ms: 1.11x faster                                                  |
| async_generators           | 589 ms                                                 | 535 ms: 1.10x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.84x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 123 ms                                                 | 91.6 ms: 1.34x faster                                                 |
| pidigits       | 250 ms                                                 | 216 ms: 1.16x faster                                                  |
| nbody          | 119 ms                                                 | 154 ms: 1.29x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 3.97 ms: 1.29x faster                                                 |
| regex_v8       | 32.5 ms                                                | 27.0 ms: 1.20x faster                                                 |
| regex_dna      | 278 ms                                                 | 249 ms: 1.12x faster                                                  |
| regex_compile  | 187 ms                                                 | 179 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                  | 1.16x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|---------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse | 169 ms                                                 | 116 ms: 1.46x faster                                                  |
| xml_etree_parse     | 241 ms                                                 | 172 ms: 1.40x faster                                                  |
| tomli_loads         | 2.88 sec                                               | 2.77 sec: 1.04x faster                                                |
| xml_etree_process   | 83.7 ms                                                | 90.7 ms: 1.08x slower                                                 |
| json_dumps          | 14.3 ms                                                | 15.6 ms: 1.09x slower                                                 |
| json_loads          | 37.9 us                                                | 42.2 us: 1.11x slower                                                 |
| Geometric mean      | (ref)                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (3): pickle_pure_python, unpickle_pure_python, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 13.9 ms: 1.27x faster                                                 |
| python_startup         | 23.7 ms                                                | 22.5 ms: 1.05x faster                                                 |
| Geometric mean         | (ref)                                                  | 1.15x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 73.4 ms: 1.09x slower                                                 |
| django_template | 44.9 ms                                                | 49.2 ms: 1.10x slower                                                 |
| genshi_text     | 30.2 ms                                                | 33.8 ms: 1.12x slower                                                 |
| mako            | 15.7 ms                                                | 20.6 ms: 1.31x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.15x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 662 ms: 2.92x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 711 ms: 2.60x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 387 ms: 2.40x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 293 ms: 2.40x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 434 ms: 2.25x faster                                                  |
| async_tree_none            | 741 ms                                                 | 340 ms: 2.18x faster                                                  |
| gc_traversal               | 5.86 ms                                                | 2.91 ms: 2.01x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 579 ms: 1.90x faster                                                  |
| mdp                        | 3.97 sec                                               | 2.16 sec: 1.84x faster                                                |
| bench_thread_pool          | 3.48 ms                                                | 1.93 ms: 1.80x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 630 ms: 1.71x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 116 ms: 1.46x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 172 ms: 1.40x faster                                                  |
| float                      | 123 ms                                                 | 91.6 ms: 1.34x faster                                                 |
| sqlite_synth               | 3.87 us                                                | 2.99 us: 1.30x faster                                                 |
| regex_effbot               | 5.13 ms                                                | 3.97 ms: 1.29x faster                                                 |
| pathlib                    | 31.6 ms                                                | 24.6 ms: 1.29x faster                                                 |
| dulwich_log                | 100 ms                                                 | 78.1 ms: 1.28x faster                                                 |
| python_startup_no_site     | 17.6 ms                                                | 13.9 ms: 1.27x faster                                                 |
| deepcopy                   | 468 us                                                 | 373 us: 1.25x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.46 sec: 1.23x faster                                                |
| 2to3                       | 456 ms                                                 | 378 ms: 1.21x faster                                                  |
| regex_v8                   | 32.5 ms                                                | 27.0 ms: 1.20x faster                                                 |
| pidigits                   | 250 ms                                                 | 216 ms: 1.16x faster                                                  |
| pylint                     | 465 ms                                                 | 404 ms: 1.15x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 46.0 us: 1.14x faster                                                 |
| regex_dna                  | 278 ms                                                 | 249 ms: 1.12x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 674 ms: 1.11x faster                                                  |
| pyflate                    | 727 ms                                                 | 658 ms: 1.11x faster                                                  |
| spectral_norm              | 156 ms                                                 | 141 ms: 1.10x faster                                                  |
| async_generators           | 589 ms                                                 | 535 ms: 1.10x faster                                                  |
| docutils                   | 4.00 sec                                               | 3.68 sec: 1.09x faster                                                |
| html5lib                   | 88.9 ms                                                | 82.2 ms: 1.08x faster                                                 |
| comprehensions             | 27.1 us                                                | 25.2 us: 1.08x faster                                                 |
| go                         | 172 ms                                                 | 161 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 6.20 sec: 1.06x faster                                                |
| deepcopy_reduce            | 4.04 us                                                | 3.82 us: 1.06x faster                                                 |
| raytrace                   | 408 ms                                                 | 387 ms: 1.05x faster                                                  |
| sympy_integrate            | 29.8 ms                                                | 28.3 ms: 1.05x faster                                                 |
| python_startup             | 23.7 ms                                                | 22.5 ms: 1.05x faster                                                 |
| scimark_sor                | 167 ms                                                 | 160 ms: 1.04x faster                                                  |
| regex_compile              | 187 ms                                                 | 179 ms: 1.04x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.77 sec: 1.04x faster                                                |
| chaos                      | 84.9 ms                                                | 81.6 ms: 1.04x faster                                                 |
| scimark_fft                | 500 ms                                                 | 488 ms: 1.02x faster                                                  |
| richards_super             | 72.8 ms                                                | 75.4 ms: 1.04x slower                                                 |
| pprint_safe_repr           | 967 ms                                                 | 1.00 sec: 1.04x slower                                                |
| generators                 | 41.1 ms                                                | 42.7 ms: 1.04x slower                                                 |
| crypto_pyaes               | 107 ms                                                 | 111 ms: 1.04x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 100 ms: 1.04x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 2.08 sec: 1.05x slower                                                |
| deltablue                  | 4.27 ms                                                | 4.50 ms: 1.05x slower                                                 |
| json                       | 6.85 ms                                                | 7.22 ms: 1.06x slower                                                 |
| hexiom                     | 8.27 ms                                                | 8.83 ms: 1.07x slower                                                 |
| richards                   | 60.3 ms                                                | 64.9 ms: 1.08x slower                                                 |
| xml_etree_process          | 83.7 ms                                                | 90.7 ms: 1.08x slower                                                 |
| meteor_contest             | 146 ms                                                 | 159 ms: 1.08x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 73.4 ms: 1.09x slower                                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.28 ms: 1.09x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 15.6 ms: 1.09x slower                                                 |
| django_template            | 44.9 ms                                                | 49.2 ms: 1.10x slower                                                 |
| logging_format             | 9.59 us                                                | 10.5 us: 1.10x slower                                                 |
| scimark_lu                 | 152 ms                                                 | 167 ms: 1.10x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 248 us: 1.11x slower                                                  |
| sympy_expand               | 582 ms                                                 | 646 ms: 1.11x slower                                                  |
| telco                      | 9.59 ms                                                | 10.7 ms: 1.11x slower                                                 |
| json_loads                 | 37.9 us                                                | 42.2 us: 1.11x slower                                                 |
| genshi_text                | 30.2 ms                                                | 33.8 ms: 1.12x slower                                                 |
| fannkuch                   | 540 ms                                                 | 606 ms: 1.12x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.21 ms: 1.14x slower                                                 |
| nbody                      | 119 ms                                                 | 154 ms: 1.29x slower                                                  |
| mako                       | 15.7 ms                                                | 20.6 ms: 1.31x slower                                                 |
| coverage                   | 95.4 ms                                                | 145 ms: 1.52x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 76.4 ms: 3.69x slower                                                 |
| logging_silent             | 139 ns                                                 | 701 ns: 5.03x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                          |

Benchmark hidden because not significant (9): nqueens, sympy_sum, logging_simple, pickle_pure_python, unpickle_pure_python, sympy_str, xml_etree_generate, thrift, coroutines
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.114x faster

# HPT report

- Reliability score: 93.64% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.42x