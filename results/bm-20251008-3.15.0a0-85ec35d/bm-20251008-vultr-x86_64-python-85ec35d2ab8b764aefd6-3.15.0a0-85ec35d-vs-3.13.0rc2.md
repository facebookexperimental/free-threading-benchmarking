# Results vs. 3.13.0rc2

- fork: python
- ref: 85ec35d2ab8b764aefd6
- machine: linux-x86_64
- commit hash: 85ec35d
- commit date: 2025-10-08
- overall geometric mean: 1.040x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 246 ms: 1.06x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                |
| html5lib       | 67.0 ms                                                      | 62.7 ms: 1.07x faster                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 624 ms: 1.46x faster                                                  |
| async_tree_io              | 876 ms                                                       | 605 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 491 ms: 1.36x faster                                                  |
| async_tree_none            | 354 ms                                                       | 263 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 252 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 316 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 494 ms: 1.29x faster                                                  |
| async_generators           | 377 ms                                                       | 341 ms: 1.11x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.5 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 72.3 ms: 1.07x faster                                                 |
| pidigits       | 217 ms                                                       | 213 ms: 1.02x faster                                                  |
| nbody          | 85.1 ms                                                      | 92.1 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                        | 1.00x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.69 ms: 1.14x faster                                                 |
| regex_compile  | 132 ms                                                       | 123 ms: 1.07x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.4 ms: 1.06x faster                                                 |
| regex_dna      | 180 ms                                                       | 179 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.61 ms: 1.10x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.91 sec: 1.05x faster                                                |
| xml_etree_process    | 59.3 ms                                                      | 57.7 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.1 ms: 1.03x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 134 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 206 us: 1.02x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 93.8 ms: 1.01x faster                                                 |
| json_loads           | 27.0 us                                                      | 27.8 us: 1.03x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 306 us: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.4 ms: 1.05x faster                                                 |
| genshi_xml      | 48.8 ms                                                      | 48.1 ms: 1.01x faster                                                 |
| django_template | 34.1 ms                                                      | 34.5 ms: 1.01x slower                                                 |
| mako            | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.07x faster                                                |
| deepcopy_memo              | 39.1 us                                                      | 26.5 us: 1.47x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 624 ms: 1.46x faster                                                  |
| deepcopy                   | 355 us                                                       | 245 us: 1.45x faster                                                  |
| async_tree_io              | 876 ms                                                       | 605 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 491 ms: 1.36x faster                                                  |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                                  |
| async_tree_none            | 354 ms                                                       | 263 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 252 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 316 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 494 ms: 1.29x faster                                                  |
| scimark_sor                | 134 ms                                                       | 107 ms: 1.26x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.63 us: 1.18x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.69 ms: 1.14x faster                                                 |
| pylint                     | 317 ms                                                       | 278 ms: 1.14x faster                                                  |
| spectral_norm              | 111 ms                                                       | 97.8 ms: 1.14x faster                                                 |
| pyflate                    | 449 ms                                                       | 396 ms: 1.13x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 66.8 ms: 1.12x faster                                                 |
| richards                   | 45.2 ms                                                      | 40.7 ms: 1.11x faster                                                 |
| richards_super             | 51.6 ms                                                      | 46.6 ms: 1.11x faster                                                 |
| async_generators           | 377 ms                                                       | 341 ms: 1.11x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.61 ms: 1.10x faster                                                 |
| scimark_fft                | 349 ms                                                       | 320 ms: 1.09x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.6 ms: 1.09x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.67 us: 1.09x faster                                                 |
| logging_silent             | 103 ns                                                       | 95.5 ns: 1.07x faster                                                 |
| regex_compile              | 132 ms                                                       | 123 ms: 1.07x faster                                                  |
| float                      | 77.5 ms                                                      | 72.3 ms: 1.07x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 690 ms: 1.07x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.60 ms: 1.07x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 62.7 ms: 1.07x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.41 us: 1.07x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                                |
| bpe_tokeniser              | 4.45 sec                                                     | 4.19 sec: 1.06x faster                                                |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.7 ms: 1.06x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.4 ms: 1.06x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 18.8 ms: 1.06x faster                                                 |
| 2to3                       | 260 ms                                                       | 246 ms: 1.06x faster                                                  |
| comprehensions             | 16.5 us                                                      | 15.6 us: 1.05x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 20.4 ms: 1.05x faster                                                 |
| thrift                     | 778 us                                                       | 741 us: 1.05x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.91 sec: 1.05x faster                                                |
| pycparser                  | 1.12 sec                                                     | 1.07 sec: 1.05x faster                                                |
| generators                 | 28.8 ms                                                      | 27.6 ms: 1.04x faster                                                 |
| meteor_contest             | 102 ms                                                       | 98.8 ms: 1.03x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 57.7 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 83.1 ms: 1.03x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                |
| nqueens                    | 78.6 ms                                                      | 76.9 ms: 1.02x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                 |
| coverage                   | 83.0 ms                                                      | 81.3 ms: 1.02x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.02x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 134 ms: 1.02x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 152 us: 1.02x faster                                                  |
| pidigits                   | 217 ms                                                       | 213 ms: 1.02x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.02x faster                                                  |
| deltablue                  | 3.12 ms                                                      | 3.07 ms: 1.02x faster                                                 |
| chaos                      | 57.3 ms                                                      | 56.3 ms: 1.02x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 206 us: 1.02x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.64 ms: 1.02x faster                                                 |
| sympy_str                  | 275 ms                                                       | 271 ms: 1.01x faster                                                  |
| genshi_xml                 | 48.8 ms                                                      | 48.1 ms: 1.01x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 93.8 ms: 1.01x faster                                                 |
| regex_dna                  | 180 ms                                                       | 179 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| raytrace                   | 253 ms                                                       | 252 ms: 1.00x faster                                                  |
| django_template            | 34.1 ms                                                      | 34.5 ms: 1.01x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 69.2 ms: 1.02x slower                                                 |
| fannkuch                   | 370 ms                                                       | 377 ms: 1.02x slower                                                  |
| sympy_expand               | 457 ms                                                       | 467 ms: 1.02x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.8 us: 1.03x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 306 us: 1.04x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.30 us: 1.04x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.5 ms: 1.04x slower                                                 |
| nbody                      | 85.1 ms                                                      | 92.1 ms: 1.08x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 996 us: 1.08x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.92 ms: 1.44x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.66 ms: 1.48x slower                                                 |
| telco                      | 7.82 ms                                                      | 156 ms: 19.96x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (1): json
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.040x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x