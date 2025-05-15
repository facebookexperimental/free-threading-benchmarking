# Results vs. 3.12.6

- fork: python
- ref: e123a1d09bcb75aae0c5
- machine: linux-x86_64
- commit hash: e123a1d
- commit date: 2025-05-14
- overall geometric mean: 1.217x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 339 ms: 1.35x faster                                                  |
| docutils       | 4.00 sec                                               | 3.39 sec: 1.18x faster                                                |
| html5lib       | 88.9 ms                                                | 75.2 ms: 1.18x faster                                                 |
| Geometric mean | (ref)                                                  | 1.23x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 977 ms                                                 | 417 ms: 2.34x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 807 ms: 2.29x faster                                                  |
| async_tree_io_tg           | 1.93 sec                                               | 850 ms: 2.28x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 421 ms: 2.21x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 333 ms: 2.11x faster                                                  |
| async_tree_none            | 741 ms                                                 | 351 ms: 2.11x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 625 ms: 1.76x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 623 ms: 1.73x faster                                                  |
| async_generators           | 589 ms                                                 | 506 ms: 1.16x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 649 ms: 1.15x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.75x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 123 ms                                                 | 94.3 ms: 1.30x faster                                                 |
| pidigits       | 250 ms                                                 | 223 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                  | 1.13x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 3.86 ms: 1.33x faster                                                 |
| regex_compile  | 187 ms                                                 | 154 ms: 1.21x faster                                                  |
| regex_dna      | 278 ms                                                 | 246 ms: 1.13x faster                                                  |
| regex_v8       | 32.5 ms                                                | 29.0 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                  | 1.20x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 172 ms: 1.40x faster                                                  |
| xml_etree_iterparse  | 169 ms                                                 | 124 ms: 1.36x faster                                                  |
| xml_etree_generate   | 127 ms                                                 | 109 ms: 1.17x faster                                                  |
| tomli_loads          | 2.88 sec                                               | 2.49 sec: 1.16x faster                                                |
| pickle_pure_python   | 436 us                                                 | 387 us: 1.13x faster                                                  |
| xml_etree_process    | 83.7 ms                                                | 74.9 ms: 1.12x faster                                                 |
| unpickle_pure_python | 300 us                                                 | 270 us: 1.11x faster                                                  |
| json_dumps           | 14.3 ms                                                | 13.7 ms: 1.04x faster                                                 |
| Geometric mean       | (ref)                                                  | 1.16x faster                                                          |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 10.2 ms: 1.72x faster                                                 |
| python_startup         | 23.7 ms                                                | 17.3 ms: 1.37x faster                                                 |
| Geometric mean         | (ref)                                                  | 1.54x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 25.9 ms: 1.17x faster                                                 |
| genshi_xml      | 67.6 ms                                                | 60.9 ms: 1.11x faster                                                 |
| django_template | 44.9 ms                                                | 42.8 ms: 1.05x faster                                                 |
| Geometric mean  | (ref)                                                  | 1.08x faster                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 3.97 sec                                               | 1.61 sec: 2.46x faster                                                |
| async_tree_memoization     | 977 ms                                                 | 417 ms: 2.34x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 807 ms: 2.29x faster                                                  |
| async_tree_io_tg           | 1.93 sec                                               | 850 ms: 2.28x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 421 ms: 2.21x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 333 ms: 2.11x faster                                                  |
| async_tree_none            | 741 ms                                                 | 351 ms: 2.11x faster                                                  |
| bench_thread_pool          | 3.48 ms                                                | 1.77 ms: 1.96x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 625 ms: 1.76x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 623 ms: 1.73x faster                                                  |
| python_startup_no_site     | 17.6 ms                                                | 10.2 ms: 1.72x faster                                                 |
| deepcopy                   | 468 us                                                 | 322 us: 1.45x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 36.8 us: 1.42x faster                                                 |
| xml_etree_parse            | 241 ms                                                 | 172 ms: 1.40x faster                                                  |
| python_startup             | 23.7 ms                                                | 17.3 ms: 1.37x faster                                                 |
| dulwich_log                | 100 ms                                                 | 73.2 ms: 1.37x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 124 ms: 1.36x faster                                                  |
| pathlib                    | 31.6 ms                                                | 23.4 ms: 1.35x faster                                                 |
| 2to3                       | 456 ms                                                 | 339 ms: 1.35x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 3.86 ms: 1.33x faster                                                 |
| float                      | 123 ms                                                 | 94.3 ms: 1.30x faster                                                 |
| pylint                     | 465 ms                                                 | 364 ms: 1.28x faster                                                  |
| sympy_integrate            | 29.8 ms                                                | 23.3 ms: 1.27x faster                                                 |
| comprehensions             | 27.1 us                                                | 21.3 us: 1.27x faster                                                 |
| pycparser                  | 1.79 sec                                               | 1.41 sec: 1.27x faster                                                |
| pyflate                    | 727 ms                                                 | 581 ms: 1.25x faster                                                  |
| go                         | 172 ms                                                 | 141 ms: 1.22x faster                                                  |
| raytrace                   | 408 ms                                                 | 336 ms: 1.22x faster                                                  |
| sympy_sum                  | 222 ms                                                 | 183 ms: 1.21x faster                                                  |
| regex_compile              | 187 ms                                                 | 154 ms: 1.21x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.34 us: 1.21x faster                                                 |
| spectral_norm              | 156 ms                                                 | 129 ms: 1.21x faster                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 5.47 sec: 1.20x faster                                                |
| sqlite_synth               | 3.87 us                                                | 3.24 us: 1.20x faster                                                 |
| sympy_str                  | 385 ms                                                 | 324 ms: 1.19x faster                                                  |
| nqueens                    | 117 ms                                                 | 98.5 ms: 1.19x faster                                                 |
| html5lib                   | 88.9 ms                                                | 75.2 ms: 1.18x faster                                                 |
| richards_super             | 72.8 ms                                                | 61.6 ms: 1.18x faster                                                 |
| docutils                   | 4.00 sec                                               | 3.39 sec: 1.18x faster                                                |
| crypto_pyaes               | 107 ms                                                 | 91.5 ms: 1.17x faster                                                 |
| xml_etree_generate         | 127 ms                                                 | 109 ms: 1.17x faster                                                  |
| genshi_text                | 30.2 ms                                                | 25.9 ms: 1.17x faster                                                 |
| async_generators           | 589 ms                                                 | 506 ms: 1.16x faster                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 83.1 ms: 1.16x faster                                                 |
| tomli_loads                | 2.88 sec                                               | 2.49 sec: 1.16x faster                                                |
| chaos                      | 84.9 ms                                                | 73.4 ms: 1.16x faster                                                 |
| logging_simple             | 9.45 us                                                | 8.18 us: 1.16x faster                                                 |
| asyncio_websockets         | 748 ms                                                 | 649 ms: 1.15x faster                                                  |
| meteor_contest             | 146 ms                                                 | 128 ms: 1.14x faster                                                  |
| scimark_sor                | 167 ms                                                 | 146 ms: 1.14x faster                                                  |
| typing_runtime_protocols   | 224 us                                                 | 197 us: 1.14x faster                                                  |
| regex_dna                  | 278 ms                                                 | 246 ms: 1.13x faster                                                  |
| richards                   | 60.3 ms                                                | 53.6 ms: 1.13x faster                                                 |
| thrift                     | 1.06 ms                                                | 941 us: 1.13x faster                                                  |
| pickle_pure_python         | 436 us                                                 | 387 us: 1.13x faster                                                  |
| regex_v8                   | 32.5 ms                                                | 29.0 ms: 1.12x faster                                                 |
| pidigits                   | 250 ms                                                 | 223 ms: 1.12x faster                                                  |
| xml_etree_process          | 83.7 ms                                                | 74.9 ms: 1.12x faster                                                 |
| genshi_xml                 | 67.6 ms                                                | 60.9 ms: 1.11x faster                                                 |
| unpickle_pure_python       | 300 us                                                 | 270 us: 1.11x faster                                                  |
| hexiom                     | 8.27 ms                                                | 7.55 ms: 1.10x faster                                                 |
| scimark_fft                | 500 ms                                                 | 457 ms: 1.09x faster                                                  |
| logging_format             | 9.59 us                                                | 8.80 us: 1.09x faster                                                 |
| pprint_safe_repr           | 967 ms                                                 | 890 ms: 1.09x faster                                                  |
| pprint_pformat             | 1.98 sec                                               | 1.83 sec: 1.08x faster                                                |
| fannkuch                   | 540 ms                                                 | 502 ms: 1.08x faster                                                  |
| sympy_expand               | 582 ms                                                 | 552 ms: 1.05x faster                                                  |
| django_template            | 44.9 ms                                                | 42.8 ms: 1.05x faster                                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.38 ms: 1.05x faster                                                 |
| generators                 | 41.1 ms                                                | 39.3 ms: 1.05x faster                                                 |
| scimark_lu                 | 152 ms                                                 | 146 ms: 1.04x faster                                                  |
| json_dumps                 | 14.3 ms                                                | 13.7 ms: 1.04x faster                                                 |
| coverage                   | 95.4 ms                                                | 106 ms: 1.11x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.12 ms: 1.61x slower                                                 |
| bench_mp_pool              | 20.7 ms                                                | 81.3 ms: 3.93x slower                                                 |
| logging_silent             | 139 ns                                                 | 609 ns: 4.38x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.19x faster                                                          |

Benchmark hidden because not significant (8): json_loads, telco, mako, json, nbody, deltablue, gc_traversal, coroutines
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.217x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.12x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: 1.17x