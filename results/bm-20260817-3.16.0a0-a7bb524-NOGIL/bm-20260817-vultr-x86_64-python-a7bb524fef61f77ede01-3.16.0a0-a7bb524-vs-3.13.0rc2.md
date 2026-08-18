# Results vs. 3.13.0rc2

- fork: python
- ref: a7bb524fef61f77ede01
- machine: linux-x86_64
- commit hash: a7bb524
- commit date: 2026-08-17
- overall geometric mean: 1.077x slower
- HPT reliability: 99.62%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 298 ms: 1.15x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.94 sec: 1.12x slower                                                |
| html5lib       | 67.0 ms                                                      | 66.2 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                        | 1.08x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 700 ms: 1.31x faster                                                  |
| async_tree_io              | 876 ms                                                       | 712 ms: 1.23x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 425 ms: 1.09x faster                                                  |
| async_tree_none            | 354 ms                                                       | 343 ms: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.6 ms: 1.04x slower                                                 |
| async_generators           | 377 ms                                                       | 396 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 701 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 681 ms: 1.07x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 215 ms: 1.01x faster                                                  |
| float          | 77.5 ms                                                      | 84.3 ms: 1.09x slower                                                 |
| nbody          | 85.1 ms                                                      | 120 ms: 1.41x slower                                                  |
| Geometric mean | (ref)                                                        | 1.15x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 20.9 ms: 1.08x faster                                                 |
| regex_effbot   | 3.08 ms                                                      | 2.95 ms: 1.05x faster                                                 |
| regex_compile  | 132 ms                                                       | 171 ms: 1.29x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 10.1 ms: 1.04x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.96 sec: 1.02x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 139 ms: 1.02x slower                                                  |
| json_loads           | 27.0 us                                                      | 30.5 us: 1.13x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 240 us: 1.14x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 337 us: 1.14x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 101 ms: 1.18x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 75.0 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.27 ms: 1.25x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 41.7 ms: 1.22x slower                                                 |
| mako            | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 131 ms: 2.42x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.31 sec: 1.80x faster                                                |
| gc_traversal               | 3.14 ms                                                      | 1.79 ms: 1.76x faster                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 6.78 ms: 1.62x faster                                                 |
| deepcopy                   | 355 us                                                       | 272 us: 1.31x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 700 ms: 1.31x faster                                                  |
| async_tree_io              | 876 ms                                                       | 712 ms: 1.23x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 31.9 us: 1.22x faster                                                 |
| go                         | 141 ms                                                       | 120 ms: 1.18x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 1.95 us: 1.13x faster                                                 |
| scimark_sor                | 134 ms                                                       | 121 ms: 1.11x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 425 ms: 1.09x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 20.9 ms: 1.08x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 17.9 ms: 1.07x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 70.7 ms: 1.06x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.95 ms: 1.05x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 10.1 ms: 1.04x faster                                                 |
| spectral_norm              | 111 ms                                                       | 106 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.99 us: 1.04x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 149 us: 1.04x faster                                                  |
| async_tree_none            | 354 ms                                                       | 343 ms: 1.03x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.96 sec: 1.02x faster                                                |
| scimark_fft                | 349 ms                                                       | 342 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.38 sec: 1.01x faster                                                |
| html5lib                   | 67.0 ms                                                      | 66.2 ms: 1.01x faster                                                 |
| pidigits                   | 217 ms                                                       | 215 ms: 1.01x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 139 ms: 1.02x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.38 ms: 1.03x slower                                                 |
| pyflate                    | 449 ms                                                       | 464 ms: 1.04x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.6 ms: 1.04x slower                                                 |
| logging_silent             | 103 ns                                                       | 107 ns: 1.04x slower                                                  |
| async_generators           | 377 ms                                                       | 396 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 701 ms: 1.05x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.18 sec: 1.06x slower                                                |
| chaos                      | 57.3 ms                                                      | 60.7 ms: 1.06x slower                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 681 ms: 1.07x slower                                                  |
| comprehensions             | 16.5 us                                                      | 17.9 us: 1.08x slower                                                 |
| float                      | 77.5 ms                                                      | 84.3 ms: 1.09x slower                                                 |
| json                       | 4.93 ms                                                      | 5.38 ms: 1.09x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.55 ms: 1.09x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.19 ms: 1.10x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 22.0 ms: 1.11x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.94 sec: 1.12x slower                                                |
| pprint_safe_repr           | 738 ms                                                       | 832 ms: 1.13x slower                                                  |
| json_loads                 | 27.0 us                                                      | 30.5 us: 1.13x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 88.8 ms: 1.13x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.98 us: 1.13x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 240 us: 1.14x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 129 ms: 1.14x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 337 us: 1.14x slower                                                  |
| 2to3                       | 260 ms                                                       | 298 ms: 1.15x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.72 sec: 1.15x slower                                                |
| richards                   | 45.2 ms                                                      | 52.4 ms: 1.16x slower                                                 |
| raytrace                   | 253 ms                                                       | 293 ms: 1.16x slower                                                  |
| richards_super             | 51.6 ms                                                      | 60.0 ms: 1.16x slower                                                 |
| generators                 | 28.8 ms                                                      | 33.5 ms: 1.16x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 182 ms: 1.17x slower                                                  |
| sympy_str                  | 275 ms                                                       | 321 ms: 1.17x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 101 ms: 1.18x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.07 us: 1.18x slower                                                 |
| sympy_expand               | 457 ms                                                       | 540 ms: 1.18x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.70 ms: 1.19x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 78.1 ms: 1.19x slower                                                 |
| thrift                     | 778 us                                                       | 935 us: 1.20x slower                                                  |
| django_template            | 34.1 ms                                                      | 41.7 ms: 1.22x slower                                                 |
| meteor_contest             | 102 ms                                                       | 125 ms: 1.23x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.27 ms: 1.25x slower                                                 |
| fannkuch                   | 370 ms                                                       | 464 ms: 1.26x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 75.0 ms: 1.26x slower                                                 |
| regex_compile              | 132 ms                                                       | 171 ms: 1.29x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 89.3 ms: 1.31x slower                                                 |
| coverage                   | 83.0 ms                                                      | 115 ms: 1.38x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                 |
| nbody                      | 85.1 ms                                                      | 120 ms: 1.41x slower                                                  |
| python_startup             | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.49 ms: 1.62x slower                                                 |
| telco                      | 7.82 ms                                                      | 178 ms: 22.70x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                          |

Benchmark hidden because not significant (4): async_tree_memoization_tg, async_tree_none_tg, xml_etree_iterparse, regex_dna
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.077x slower

# HPT report

- Reliability score: 99.62% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x