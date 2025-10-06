# Results vs. 3.13.0rc2

- fork: python
- ref: 3195da0b1a5dc8a03faa
- machine: linux-x86_64
- commit hash: 3195da0
- commit date: 2025-10-05
- overall geometric mean: 1.042x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 246 ms: 1.06x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                |
| html5lib       | 67.0 ms                                                      | 61.2 ms: 1.10x faster                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 616 ms: 1.48x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 311 ms: 1.48x faster                                                  |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 490 ms: 1.36x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 251 ms: 1.34x faster                                                  |
| async_tree_none            | 354 ms                                                       | 265 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 313 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 493 ms: 1.29x faster                                                  |
| async_generators           | 377 ms                                                       | 347 ms: 1.09x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                                  |
| float          | 77.5 ms                                                      | 72.0 ms: 1.08x faster                                                 |
| nbody          | 85.1 ms                                                      | 91.1 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.61 ms: 1.18x faster                                                 |
| regex_dna      | 180 ms                                                       | 163 ms: 1.10x faster                                                  |
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.4 ms: 1.06x faster                                                 |
| Geometric mean | (ref)                                                        | 1.10x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.62 ms: 1.10x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 83.6 ms: 1.02x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 206 us: 1.02x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 93.1 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 58.2 ms: 1.02x faster                                                 |
| pickle_pure_python   | 294 us                                                       | 302 us: 1.02x slower                                                  |
| json_loads           | 27.0 us                                                      | 27.8 us: 1.03x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.3 ms: 1.06x faster                                                 |
| genshi_xml      | 48.8 ms                                                      | 48.2 ms: 1.01x faster                                                 |
| django_template | 34.1 ms                                                      | 33.9 ms: 1.01x faster                                                 |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.04x faster                                                |
| deepcopy_memo              | 39.1 us                                                      | 26.1 us: 1.50x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 616 ms: 1.48x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 311 ms: 1.48x faster                                                  |
| deepcopy                   | 355 us                                                       | 241 us: 1.47x faster                                                  |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 490 ms: 1.36x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 251 ms: 1.34x faster                                                  |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                  |
| async_tree_none            | 354 ms                                                       | 265 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 313 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 493 ms: 1.29x faster                                                  |
| scimark_sor                | 134 ms                                                       | 107 ms: 1.25x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.57 us: 1.21x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.61 ms: 1.18x faster                                                 |
| spectral_norm              | 111 ms                                                       | 95.6 ms: 1.16x faster                                                 |
| pylint                     | 317 ms                                                       | 278 ms: 1.14x faster                                                  |
| pyflate                    | 449 ms                                                       | 398 ms: 1.13x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 66.5 ms: 1.13x faster                                                 |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                                  |
| scimark_fft                | 349 ms                                                       | 312 ms: 1.12x faster                                                  |
| richards_super             | 51.6 ms                                                      | 46.5 ms: 1.11x faster                                                 |
| richards                   | 45.2 ms                                                      | 40.8 ms: 1.11x faster                                                 |
| regex_dna                  | 180 ms                                                       | 163 ms: 1.10x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.4 ms: 1.10x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.62 ms: 1.10x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 61.2 ms: 1.10x faster                                                 |
| async_generators           | 377 ms                                                       | 347 ms: 1.09x faster                                                  |
| float                      | 77.5 ms                                                      | 72.0 ms: 1.08x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.74 us: 1.07x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 688 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.40 sec: 1.07x faster                                                |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 20.3 ms: 1.06x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.65 ms: 1.06x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                |
| regex_v8                   | 22.7 ms                                                      | 21.4 ms: 1.06x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.8 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.20 sec: 1.06x faster                                                |
| 2to3                       | 260 ms                                                       | 246 ms: 1.06x faster                                                  |
| generators                 | 28.8 ms                                                      | 27.3 ms: 1.05x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.51 us: 1.05x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 18.9 ms: 1.05x faster                                                 |
| logging_silent             | 103 ns                                                       | 97.9 ns: 1.05x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.7 us: 1.05x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.07 sec: 1.05x faster                                                |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.03x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 150 us: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.6 ms: 1.02x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                 |
| coverage                   | 83.0 ms                                                      | 81.3 ms: 1.02x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 206 us: 1.02x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 93.1 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 58.2 ms: 1.02x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                |
| meteor_contest             | 102 ms                                                       | 99.8 ms: 1.02x faster                                                 |
| thrift                     | 778 us                                                       | 766 us: 1.02x faster                                                  |
| chaos                      | 57.3 ms                                                      | 56.4 ms: 1.02x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 77.6 ms: 1.01x faster                                                 |
| sympy_str                  | 275 ms                                                       | 271 ms: 1.01x faster                                                  |
| genshi_xml                 | 48.8 ms                                                      | 48.2 ms: 1.01x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| django_template            | 34.1 ms                                                      | 33.9 ms: 1.01x faster                                                 |
| json                       | 4.93 ms                                                      | 5.01 ms: 1.02x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.25 us: 1.02x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 69.2 ms: 1.02x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 302 us: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.85 ms: 1.03x slower                                                 |
| json_loads                 | 27.0 us                                                      | 27.8 us: 1.03x slower                                                 |
| fannkuch                   | 370 ms                                                       | 382 ms: 1.03x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.29 ms: 1.05x slower                                                 |
| nbody                      | 85.1 ms                                                      | 91.1 ms: 1.07x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 996 us: 1.08x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.40 ms: 1.40x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.92 ms: 1.44x slower                                                 |
| telco                      | 7.82 ms                                                      | 158 ms: 20.19x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (3): raytrace, scimark_lu, sympy_expand
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251005-3.15.0a0-3195da0/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.042x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x