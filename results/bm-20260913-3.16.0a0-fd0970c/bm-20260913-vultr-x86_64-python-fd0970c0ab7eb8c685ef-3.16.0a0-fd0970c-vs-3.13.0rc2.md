# Results vs. 3.13.0rc2

- fork: python
- ref: fd0970c0ab7eb8c685ef
- machine: linux-x86_64
- commit hash: fd0970c
- commit date: 2026-09-13
- overall geometric mean: 1.026x faster
- HPT reliability: 99.91%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 260 ms: 1.00x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.36 sec: 1.11x faster                                                |
| html5lib       | 67.0 ms                                                      | 59.3 ms: 1.13x faster                                                 |
| Geometric mean | (ref)                                                        | 1.08x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 761 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 567 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 556 ms: 1.15x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 366 ms: 1.13x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 409 ms: 1.13x faster                                                  |
| async_tree_io              | 876 ms                                                       | 778 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 302 ms: 1.12x faster                                                  |
| async_generators           | 377 ms                                                       | 346 ms: 1.09x faster                                                  |
| async_tree_none            | 354 ms                                                       | 330 ms: 1.07x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.10x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| float          | 77.5 ms                                                      | 73.0 ms: 1.06x faster                                                 |
| nbody          | 85.1 ms                                                      | 88.4 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 21.0 ms: 1.08x faster                                                 |
| regex_dna      | 180 ms                                                       | 179 ms: 1.01x faster                                                  |
| regex_compile  | 132 ms                                                       | 149 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.32 ms: 1.13x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.82 sec: 1.10x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 92.1 ms: 1.03x faster                                                 |
| json_loads           | 27.0 us                                                      | 27.1 us: 1.00x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.01x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 87.8 ms: 1.03x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 62.2 ms: 1.05x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 309 us: 1.05x slower                                                  |
| xml_etree_parse      | 136 ms                                                       | 145 ms: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.74 ms: 1.05x slower                                                 |
| python_startup         | 11.0 ms                                                      | 13.0 ms: 1.18x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                 |
| django_template | 34.1 ms                                                      | 36.6 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.07x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 114 ms: 2.78x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.13 sec: 2.08x faster                                                |
| deepcopy                   | 355 us                                                       | 235 us: 1.51x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 26.9 us: 1.45x faster                                                 |
| go                         | 141 ms                                                       | 106 ms: 1.32x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 121 us: 1.28x faster                                                  |
| scimark_sor                | 134 ms                                                       | 109 ms: 1.24x faster                                                  |
| spectral_norm              | 111 ms                                                       | 89.8 ms: 1.24x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 761 ms: 1.20x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.61 us: 1.19x faster                                                 |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 567 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 556 ms: 1.15x faster                                                  |
| scimark_fft                | 349 ms                                                       | 305 ms: 1.14x faster                                                  |
| pyflate                    | 449 ms                                                       | 395 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 366 ms: 1.13x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 59.3 ms: 1.13x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.32 ms: 1.13x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 409 ms: 1.13x faster                                                  |
| async_tree_io              | 876 ms                                                       | 778 ms: 1.13x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 66.8 ms: 1.12x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 302 ms: 1.12x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.36 sec: 1.11x faster                                                |
| tomli_loads                | 2.01 sec                                                     | 1.82 sec: 1.10x faster                                                |
| regex_effbot               | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                 |
| async_generators           | 377 ms                                                       | 346 ms: 1.09x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.08x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.0 ms: 1.08x faster                                                 |
| async_tree_none            | 354 ms                                                       | 330 ms: 1.07x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.40 ms: 1.07x faster                                                 |
| chaos                      | 57.3 ms                                                      | 53.6 ms: 1.07x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 73.8 ms: 1.06x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.64 ms: 1.06x faster                                                 |
| float                      | 77.5 ms                                                      | 73.0 ms: 1.06x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.1 ms: 1.05x faster                                                 |
| logging_silent             | 103 ns                                                       | 97.4 ns: 1.05x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.23 sec: 1.05x faster                                                |
| comprehensions             | 16.5 us                                                      | 15.9 us: 1.04x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.1 ms: 1.03x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.4 ms: 1.02x faster                                                 |
| logging_simple             | 6.16 us                                                      | 6.08 us: 1.01x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 729 ms: 1.01x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                |
| raytrace                   | 253 ms                                                       | 251 ms: 1.01x faster                                                  |
| regex_dna                  | 180 ms                                                       | 179 ms: 1.01x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 67.5 ms: 1.01x faster                                                 |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.00x faster                                                  |
| 2to3                       | 260 ms                                                       | 260 ms: 1.00x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.1 us: 1.00x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.01x slower                                                  |
| fannkuch                   | 370 ms                                                       | 376 ms: 1.02x slower                                                  |
| thrift                     | 778 us                                                       | 793 us: 1.02x slower                                                  |
| sympy_str                  | 275 ms                                                       | 281 ms: 1.02x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 87.8 ms: 1.03x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 160 ms: 1.03x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.29 us: 1.04x slower                                                 |
| nbody                      | 85.1 ms                                                      | 88.4 ms: 1.04x slower                                                 |
| sympy_expand               | 457 ms                                                       | 477 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.74 ms: 1.05x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 62.2 ms: 1.05x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 309 us: 1.05x slower                                                  |
| generators                 | 28.8 ms                                                      | 30.4 ms: 1.06x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 119 ms: 1.06x slower                                                  |
| mako                       | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                 |
| xml_etree_parse            | 136 ms                                                       | 145 ms: 1.06x slower                                                  |
| django_template            | 34.1 ms                                                      | 36.6 ms: 1.07x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.37 ms: 1.08x slower                                                 |
| regex_compile              | 132 ms                                                       | 149 ms: 1.12x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.62 ms: 1.15x slower                                                 |
| python_startup             | 11.0 ms                                                      | 13.0 ms: 1.18x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.67 ms: 1.25x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.35 ms: 1.47x slower                                                 |
| telco                      | 7.82 ms                                                      | 161 ms: 20.52x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 275 ms: 24.99x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (6): logging_format, richards_super, pycparser, richards, json, coverage
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260913-3.16.0a0-fd0970c/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.026x faster

# HPT report

- Reliability score: 99.91% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x