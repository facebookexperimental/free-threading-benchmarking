# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_129068_rangeiter_
- machine: linux-x86_64
- commit hash: afd3eff
- commit date: 2025-12-16
- overall geometric mean: 1.009x slower
- HPT reliability: 55.53%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.44x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 269 ms: 1.04x slower                                                      |
| docutils       | 2.62 sec                                                     | 2.65 sec: 1.01x slower                                                    |
| html5lib       | 67.0 ms                                                      | 65.3 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                        | 1.01x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 573 ms: 1.60x faster                                                      |
| async_tree_io              | 876 ms                                                       | 597 ms: 1.47x faster                                                      |
| async_tree_memoization     | 461 ms                                                       | 334 ms: 1.38x faster                                                      |
| async_tree_none_tg         | 336 ms                                                       | 250 ms: 1.34x faster                                                      |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                      |
| async_tree_none            | 354 ms                                                       | 269 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 486 ms: 1.31x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 514 ms: 1.30x faster                                                      |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                      |
| coroutines                 | 23.6 ms                                                      | 21.9 ms: 1.08x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                      |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 192 ms: 1.13x faster                                                      |
| float          | 77.5 ms                                                      | 69.8 ms: 1.11x faster                                                     |
| nbody          | 85.1 ms                                                      | 117 ms: 1.38x slower                                                      |
| Geometric mean | (ref)                                                        | 1.03x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 134 ms: 1.01x slower                                                      |
| regex_v8       | 22.7 ms                                                      | 24.1 ms: 1.06x slower                                                     |
| regex_effbot   | 3.08 ms                                                      | 3.39 ms: 1.10x slower                                                     |
| regex_dna      | 180 ms                                                       | 206 ms: 1.14x slower                                                      |
| Geometric mean | (ref)                                                        | 1.08x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.1 ms: 1.13x faster                                                     |
| json_dumps           | 10.5 ms                                                      | 9.54 ms: 1.10x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 87.3 ms: 1.02x slower                                                     |
| xml_etree_process    | 59.3 ms                                                      | 62.2 ms: 1.05x slower                                                     |
| xml_etree_parse      | 136 ms                                                       | 143 ms: 1.05x slower                                                      |
| unpickle_pure_python | 210 us                                                       | 221 us: 1.05x slower                                                      |
| json_loads           | 27.0 us                                                      | 28.4 us: 1.05x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 313 us: 1.06x slower                                                      |
| tomli_loads          | 2.01 sec                                                     | 2.16 sec: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.59 ms: 1.30x slower                                                     |
| python_startup         | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.36x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 50.4 ms: 1.03x slower                                                     |
| django_template | 34.1 ms                                                      | 36.0 ms: 1.05x slower                                                     |
| genshi_text     | 21.5 ms                                                      | 22.9 ms: 1.06x slower                                                     |
| mako            | 11.3 ms                                                      | 15.1 ms: 1.33x slower                                                     |
| Geometric mean  | (ref)                                                        | 1.11x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.26 sec: 1.88x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 573 ms: 1.60x faster                                                      |
| bench_mp_pool              | 11.0 ms                                                      | 7.14 ms: 1.54x faster                                                     |
| async_tree_io              | 876 ms                                                       | 597 ms: 1.47x faster                                                      |
| deepcopy                   | 355 us                                                       | 247 us: 1.44x faster                                                      |
| gc_traversal               | 3.14 ms                                                      | 2.19 ms: 1.44x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 334 ms: 1.38x faster                                                      |
| deepcopy_memo              | 39.1 us                                                      | 28.5 us: 1.37x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 250 ms: 1.34x faster                                                      |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                      |
| async_tree_none            | 354 ms                                                       | 269 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 486 ms: 1.31x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 514 ms: 1.30x faster                                                      |
| go                         | 141 ms                                                       | 115 ms: 1.23x faster                                                      |
| scimark_sor                | 134 ms                                                       | 112 ms: 1.20x faster                                                      |
| deepcopy_reduce            | 3.11 us                                                      | 2.62 us: 1.19x faster                                                     |
| logging_silent             | 103 ns                                                       | 86.5 ns: 1.19x faster                                                     |
| scimark_fft                | 349 ms                                                       | 299 ms: 1.17x faster                                                      |
| pylint                     | 317 ms                                                       | 277 ms: 1.15x faster                                                      |
| spectral_norm              | 111 ms                                                       | 97.6 ms: 1.14x faster                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.1 ms: 1.13x faster                                                     |
| pidigits                   | 217 ms                                                       | 192 ms: 1.13x faster                                                      |
| pathlib                    | 19.2 ms                                                      | 17.1 ms: 1.12x faster                                                     |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                      |
| float                      | 77.5 ms                                                      | 69.8 ms: 1.11x faster                                                     |
| json_dumps                 | 10.5 ms                                                      | 9.54 ms: 1.10x faster                                                     |
| sqlite_synth               | 2.21 us                                                      | 2.03 us: 1.09x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 21.9 ms: 1.08x faster                                                     |
| pyflate                    | 449 ms                                                       | 425 ms: 1.06x faster                                                      |
| bpe_tokeniser              | 4.45 sec                                                     | 4.23 sec: 1.05x faster                                                    |
| scimark_lu                 | 113 ms                                                       | 108 ms: 1.04x faster                                                      |
| html5lib                   | 67.0 ms                                                      | 65.3 ms: 1.03x faster                                                     |
| generators                 | 28.8 ms                                                      | 28.1 ms: 1.03x faster                                                     |
| pprint_safe_repr           | 738 ms                                                       | 720 ms: 1.02x faster                                                      |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                      |
| dulwich_log                | 74.8 ms                                                      | 73.6 ms: 1.02x faster                                                     |
| comprehensions             | 16.5 us                                                      | 16.3 us: 1.01x faster                                                     |
| pprint_pformat             | 1.50 sec                                                     | 1.49 sec: 1.00x faster                                                    |
| regex_compile              | 132 ms                                                       | 134 ms: 1.01x slower                                                      |
| hexiom                     | 5.99 ms                                                      | 6.07 ms: 1.01x slower                                                     |
| docutils                   | 2.62 sec                                                     | 2.65 sec: 1.01x slower                                                    |
| chaos                      | 57.3 ms                                                      | 58.2 ms: 1.02x slower                                                     |
| richards                   | 45.2 ms                                                      | 45.9 ms: 1.02x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 87.3 ms: 1.02x slower                                                     |
| genshi_xml                 | 48.8 ms                                                      | 50.4 ms: 1.03x slower                                                     |
| richards_super             | 51.6 ms                                                      | 53.4 ms: 1.03x slower                                                     |
| 2to3                       | 260 ms                                                       | 269 ms: 1.04x slower                                                      |
| sympy_integrate            | 19.8 ms                                                      | 20.6 ms: 1.04x slower                                                     |
| json                       | 4.93 ms                                                      | 5.14 ms: 1.04x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 3.27 ms: 1.05x slower                                                     |
| xml_etree_process          | 59.3 ms                                                      | 62.2 ms: 1.05x slower                                                     |
| xml_etree_parse            | 136 ms                                                       | 143 ms: 1.05x slower                                                      |
| unpickle_pure_python       | 210 us                                                       | 221 us: 1.05x slower                                                      |
| json_loads                 | 27.0 us                                                      | 28.4 us: 1.05x slower                                                     |
| logging_simple             | 6.16 us                                                      | 6.48 us: 1.05x slower                                                     |
| django_template            | 34.1 ms                                                      | 36.0 ms: 1.05x slower                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.97 ms: 1.06x slower                                                     |
| nqueens                    | 78.6 ms                                                      | 83.2 ms: 1.06x slower                                                     |
| scimark_monte_carlo        | 65.4 ms                                                      | 69.4 ms: 1.06x slower                                                     |
| genshi_text                | 21.5 ms                                                      | 22.9 ms: 1.06x slower                                                     |
| pickle_pure_python         | 294 us                                                       | 313 us: 1.06x slower                                                      |
| regex_v8                   | 22.7 ms                                                      | 24.1 ms: 1.06x slower                                                     |
| sympy_sum                  | 156 ms                                                       | 166 ms: 1.07x slower                                                      |
| tomli_loads                | 2.01 sec                                                     | 2.16 sec: 1.08x slower                                                    |
| sympy_str                  | 275 ms                                                       | 297 ms: 1.08x slower                                                      |
| logging_format             | 6.84 us                                                      | 7.46 us: 1.09x slower                                                     |
| regex_effbot               | 3.08 ms                                                      | 3.39 ms: 1.10x slower                                                     |
| raytrace                   | 253 ms                                                       | 278 ms: 1.10x slower                                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.47 ms: 1.10x slower                                                     |
| sympy_expand               | 457 ms                                                       | 505 ms: 1.10x slower                                                      |
| thrift                     | 778 us                                                       | 860 us: 1.11x slower                                                      |
| typing_runtime_protocols   | 155 us                                                       | 172 us: 1.11x slower                                                      |
| fannkuch                   | 370 ms                                                       | 412 ms: 1.12x slower                                                      |
| regex_dna                  | 180 ms                                                       | 206 ms: 1.14x slower                                                      |
| coverage                   | 83.0 ms                                                      | 95.7 ms: 1.15x slower                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 80.6 ms: 1.19x slower                                                     |
| meteor_contest             | 102 ms                                                       | 121 ms: 1.19x slower                                                      |
| python_startup_no_site     | 7.39 ms                                                      | 9.59 ms: 1.30x slower                                                     |
| mako                       | 11.3 ms                                                      | 15.1 ms: 1.33x slower                                                     |
| nbody                      | 85.1 ms                                                      | 117 ms: 1.38x slower                                                      |
| python_startup             | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                     |
| bench_thread_pool          | 919 us                                                       | 1.46 ms: 1.58x slower                                                     |
| telco                      | 7.82 ms                                                      | 168 ms: 21.41x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                              |

Benchmark hidden because not significant (1): pycparser
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251216-3.15.0a3+-afd3eff-CLANG,NOGIL/bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.009x slower

# HPT report

- Reliability score: 55.53% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.44x