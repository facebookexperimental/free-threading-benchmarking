# Results vs. base

- fork: Yhg1s
- ref: optimise_recursive_c
- machine: linux-x86_64
- commit hash: ddb794a
- commit date: 2024-12-20
- overall geometric mean: 1.003x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 360 ms                                                                 | 358 ms: 1.01x faster                                                  |
| html5lib       | 91.4 ms                                                                | 94.1 ms: 1.03x slower                                                 |
| sphinx         | 1.16 sec                                                               | 1.17 sec: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed   | 598 ms                                                                 | 602 ms: 1.01x slower                                                  |
| async_tree_none_tg        | 318 ms                                                                 | 322 ms: 1.01x slower                                                  |
| async_tree_memoization    | 430 ms                                                                 | 436 ms: 1.01x slower                                                  |
| async_tree_memoization_tg | 402 ms                                                                 | 409 ms: 1.02x slower                                                  |
| async_tree_none           | 352 ms                                                                 | 359 ms: 1.02x slower                                                  |
| async_tree_io_tg          | 735 ms                                                                 | 751 ms: 1.02x slower                                                  |
| async_tree_io             | 757 ms                                                                 | 774 ms: 1.02x slower                                                  |
| async_generators          | 445 ms                                                                 | 462 ms: 1.04x slower                                                  |
| coroutines                | 24.0 ms                                                                | 25.5 ms: 1.06x slower                                                 |
| Geometric mean            | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 181 ms                                                                 | 181 ms: 1.00x slower                                                  |
| float          | 113 ms                                                                 | 114 ms: 1.01x slower                                                  |
| nbody          | 127 ms                                                                 | 133 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.89 ms                                                                | 2.91 ms: 1.01x slower                                                 |
| regex_v8       | 24.8 ms                                                                | 25.0 ms: 1.01x slower                                                 |
| regex_compile  | 170 ms                                                                 | 172 ms: 1.01x slower                                                  |
| regex_dna      | 179 ms                                                                 | 188 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_loads           | 28.2 us                                                                | 28.3 us: 1.00x slower                                                 |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| xml_etree_generate   | 97.2 ms                                                                | 98.4 ms: 1.01x slower                                                 |
| xml_etree_iterparse  | 90.4 ms                                                                | 91.7 ms: 1.01x slower                                                 |
| pickle_pure_python   | 500 us                                                                 | 511 us: 1.02x slower                                                  |
| xml_etree_process    | 73.4 ms                                                                | 75.4 ms: 1.03x slower                                                 |
| unpickle_pure_python | 330 us                                                                 | 339 us: 1.03x slower                                                  |
| tomli_loads          | 2.53 sec                                                               | 2.59 sec: 1.03x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.2 ms                                                                | 15.7 ms: 1.09x faster                                                 |
| python_startup_no_site | 10.2 ms                                                                | 9.83 ms: 1.04x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 63.7 ms                                                                | 64.5 ms: 1.01x slower                                                 |
| mako            | 17.1 ms                                                                | 17.5 ms: 1.02x slower                                                 |
| genshi_text     | 30.7 ms                                                                | 31.5 ms: 1.03x slower                                                 |
| django_template | 49.6 ms                                                                | 51.1 ms: 1.03x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                          |

All benchmarks:
===============

| Benchmark                 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-ddb794a |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| sympy_sum                 | 349 ms                                                                 | 200 ms: 1.75x faster                                                  |
| sympy_expand              | 951 ms                                                                 | 595 ms: 1.60x faster                                                  |
| sympy_str                 | 478 ms                                                                 | 365 ms: 1.31x faster                                                  |
| sympy_integrate           | 29.6 ms                                                                | 25.7 ms: 1.15x faster                                                 |
| python_startup            | 17.2 ms                                                                | 15.7 ms: 1.09x faster                                                 |
| bench_mp_pool             | 108 ms                                                                 | 101 ms: 1.07x faster                                                  |
| sqlalchemy_declarative    | 197 ms                                                                 | 186 ms: 1.06x faster                                                  |
| python_startup_no_site    | 10.2 ms                                                                | 9.83 ms: 1.04x faster                                                 |
| meteor_contest            | 131 ms                                                                 | 130 ms: 1.01x faster                                                  |
| coverage                  | 102 ms                                                                 | 101 ms: 1.01x faster                                                  |
| 2to3                      | 360 ms                                                                 | 358 ms: 1.01x faster                                                  |
| scimark_fft               | 388 ms                                                                 | 386 ms: 1.01x faster                                                  |
| scimark_lu                | 158 ms                                                                 | 158 ms: 1.00x faster                                                  |
| pidigits                  | 181 ms                                                                 | 181 ms: 1.00x slower                                                  |
| k_core                    | 2.35 sec                                                               | 2.36 sec: 1.00x slower                                                |
| json_loads                | 28.2 us                                                                | 28.3 us: 1.00x slower                                                 |
| scimark_sor               | 219 ms                                                                 | 220 ms: 1.00x slower                                                  |
| sqlglot_parse             | 2.38 ms                                                                | 2.39 ms: 1.01x slower                                                 |
| async_tree_cpu_io_mixed   | 598 ms                                                                 | 602 ms: 1.01x slower                                                  |
| scimark_monte_carlo       | 107 ms                                                                 | 107 ms: 1.01x slower                                                  |
| regex_effbot              | 2.89 ms                                                                | 2.91 ms: 1.01x slower                                                 |
| bench_thread_pool         | 3.38 ms                                                                | 3.40 ms: 1.01x slower                                                 |
| deltablue                 | 7.67 ms                                                                | 7.73 ms: 1.01x slower                                                 |
| regex_v8                  | 24.8 ms                                                                | 25.0 ms: 1.01x slower                                                 |
| sphinx                    | 1.16 sec                                                               | 1.17 sec: 1.01x slower                                                |
| sqlglot_transpile         | 2.73 ms                                                                | 2.75 ms: 1.01x slower                                                 |
| pycparser                 | 1.38 sec                                                               | 1.39 sec: 1.01x slower                                                |
| xml_etree_parse           | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| richards                  | 69.1 ms                                                                | 69.8 ms: 1.01x slower                                                 |
| subparsers                | 28.9 ms                                                                | 29.1 ms: 1.01x slower                                                 |
| float                     | 113 ms                                                                 | 114 ms: 1.01x slower                                                  |
| comprehensions            | 27.9 us                                                                | 28.2 us: 1.01x slower                                                 |
| async_tree_none_tg        | 318 ms                                                                 | 322 ms: 1.01x slower                                                  |
| regex_compile             | 170 ms                                                                 | 172 ms: 1.01x slower                                                  |
| many_optionals            | 1.25 ms                                                                | 1.26 ms: 1.01x slower                                                 |
| chaos                     | 96.1 ms                                                                | 97.2 ms: 1.01x slower                                                 |
| xml_etree_generate        | 97.2 ms                                                                | 98.4 ms: 1.01x slower                                                 |
| raytrace                  | 497 ms                                                                 | 503 ms: 1.01x slower                                                  |
| go                        | 244 ms                                                                 | 247 ms: 1.01x slower                                                  |
| genshi_xml                | 63.7 ms                                                                | 64.5 ms: 1.01x slower                                                 |
| xml_etree_iterparse       | 90.4 ms                                                                | 91.7 ms: 1.01x slower                                                 |
| async_tree_memoization    | 430 ms                                                                 | 436 ms: 1.01x slower                                                  |
| fannkuch                  | 490 ms                                                                 | 497 ms: 1.01x slower                                                  |
| bpe_tokeniser             | 4.99 sec                                                               | 5.07 sec: 1.02x slower                                                |
| deepcopy_reduce           | 3.40 us                                                                | 3.46 us: 1.02x slower                                                 |
| deepcopy                  | 323 us                                                                 | 329 us: 1.02x slower                                                  |
| typing_runtime_protocols  | 206 us                                                                 | 209 us: 1.02x slower                                                  |
| async_tree_memoization_tg | 402 ms                                                                 | 409 ms: 1.02x slower                                                  |
| pprint_pformat            | 1.99 sec                                                               | 2.03 sec: 1.02x slower                                                |
| connected_components      | 501 ms                                                                 | 510 ms: 1.02x slower                                                  |
| logging_format            | 10.3 us                                                                | 10.4 us: 1.02x slower                                                 |
| dulwich_log               | 90.1 ms                                                                | 91.8 ms: 1.02x slower                                                 |
| shortest_path             | 549 ms                                                                 | 559 ms: 1.02x slower                                                  |
| pprint_safe_repr          | 956 ms                                                                 | 975 ms: 1.02x slower                                                  |
| hexiom                    | 9.66 ms                                                                | 9.85 ms: 1.02x slower                                                 |
| sqlglot_optimize          | 65.9 ms                                                                | 67.1 ms: 1.02x slower                                                 |
| scimark_sparse_mat_mult   | 5.47 ms                                                                | 5.58 ms: 1.02x slower                                                 |
| async_tree_none           | 352 ms                                                                 | 359 ms: 1.02x slower                                                  |
| pickle_pure_python        | 500 us                                                                 | 511 us: 1.02x slower                                                  |
| mako                      | 17.1 ms                                                                | 17.5 ms: 1.02x slower                                                 |
| async_tree_io_tg          | 735 ms                                                                 | 751 ms: 1.02x slower                                                  |
| async_tree_io             | 757 ms                                                                 | 774 ms: 1.02x slower                                                  |
| create_gc_cycles          | 1.79 ms                                                                | 1.83 ms: 1.02x slower                                                 |
| genshi_text               | 30.7 ms                                                                | 31.5 ms: 1.03x slower                                                 |
| xml_etree_process         | 73.4 ms                                                                | 75.4 ms: 1.03x slower                                                 |
| unpickle_pure_python      | 330 us                                                                 | 339 us: 1.03x slower                                                  |
| tomli_loads               | 2.53 sec                                                               | 2.59 sec: 1.03x slower                                                |
| richards_super            | 76.4 ms                                                                | 78.5 ms: 1.03x slower                                                 |
| logging_silent            | 184 ns                                                                 | 189 ns: 1.03x slower                                                  |
| html5lib                  | 91.4 ms                                                                | 94.1 ms: 1.03x slower                                                 |
| nqueens                   | 98.0 ms                                                                | 101 ms: 1.03x slower                                                  |
| crypto_pyaes              | 89.7 ms                                                                | 92.4 ms: 1.03x slower                                                 |
| mdp                       | 2.81 sec                                                               | 2.90 sec: 1.03x slower                                                |
| django_template           | 49.6 ms                                                                | 51.1 ms: 1.03x slower                                                 |
| deepcopy_memo             | 39.9 us                                                                | 41.2 us: 1.03x slower                                                 |
| sqlglot_normalize         | 133 ms                                                                 | 137 ms: 1.03x slower                                                  |
| async_generators          | 445 ms                                                                 | 462 ms: 1.04x slower                                                  |
| regex_dna                 | 179 ms                                                                 | 188 ms: 1.05x slower                                                  |
| nbody                     | 127 ms                                                                 | 133 ms: 1.05x slower                                                  |
| coroutines                | 24.0 ms                                                                | 25.5 ms: 1.06x slower                                                 |
| gc_traversal              | 3.26 ms                                                                | 3.51 ms: 1.08x slower                                                 |
| spectral_norm             | 111 ms                                                                 | 122 ms: 1.10x slower                                                  |
| generators                | 38.4 ms                                                                | 42.3 ms: 1.10x slower                                                 |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (13): pylint, thrift, telco, json, logging_simple, pyflate, asyncio_websockets, docutils, async_tree_cpu_io_mixed_tg, pathlib, json_dumps, sqlalchemy_imperative, sqlite_synth

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x