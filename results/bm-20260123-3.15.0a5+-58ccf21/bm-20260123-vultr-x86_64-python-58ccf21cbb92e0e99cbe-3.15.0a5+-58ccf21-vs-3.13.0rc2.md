# Results vs. 3.13.0rc2

- fork: python
- ref: 58ccf21cbb92e0e99cbe
- machine: linux-x86_64
- commit hash: 58ccf21
- commit date: 2026-01-23
- overall geometric mean: 1.044x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                 |
| html5lib       | 67.0 ms                                                      | 59.0 ms: 1.14x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 559 ms: 1.64x faster                                                   |
| async_tree_io              | 876 ms                                                       | 546 ms: 1.60x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 304 ms: 1.52x faster                                                   |
| async_tree_none            | 354 ms                                                       | 242 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 295 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 491 ms: 1.36x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 249 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 495 ms: 1.29x faster                                                   |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                                   |
| float          | 77.5 ms                                                      | 70.6 ms: 1.10x faster                                                  |
| nbody          | 85.1 ms                                                      | 90.9 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                  |
| regex_compile  | 132 ms                                                       | 122 ms: 1.08x faster                                                   |
| regex_dna      | 180 ms                                                       | 173 ms: 1.04x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 22.3 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 85.1 ms: 1.12x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 9.54 ms: 1.10x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.83 sec: 1.09x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 82.0 ms: 1.04x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| xml_etree_process    | 59.3 ms                                                      | 57.5 ms: 1.03x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 212 us: 1.01x slower                                                   |
| json_loads           | 27.0 us                                                      | 27.7 us: 1.03x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 304 us: 1.03x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.27 ms: 1.02x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                  |
| django_template | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                  |
| mako            | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.05x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 559 ms: 1.64x faster                                                   |
| async_tree_io              | 876 ms                                                       | 546 ms: 1.60x faster                                                   |
| deepcopy                   | 355 us                                                       | 230 us: 1.54x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 304 ms: 1.52x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.4 us: 1.48x faster                                                  |
| async_tree_none            | 354 ms                                                       | 242 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 295 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 491 ms: 1.36x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 249 ms: 1.35x faster                                                   |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                   |
| scimark_sor                | 134 ms                                                       | 104 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 495 ms: 1.29x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.54 us: 1.23x faster                                                  |
| spectral_norm              | 111 ms                                                       | 92.8 ms: 1.20x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 59.0 ms: 1.14x faster                                                  |
| scimark_fft                | 349 ms                                                       | 308 ms: 1.13x faster                                                   |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 66.7 ms: 1.12x faster                                                  |
| pylint                     | 317 ms                                                       | 283 ms: 1.12x faster                                                   |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 85.1 ms: 1.12x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.3 ms: 1.11x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.54 ms: 1.10x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                  |
| float                      | 77.5 ms                                                      | 70.6 ms: 1.10x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.83 sec: 1.09x faster                                                 |
| pyflate                    | 449 ms                                                       | 411 ms: 1.09x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.33 ms: 1.09x faster                                                  |
| regex_compile              | 132 ms                                                       | 122 ms: 1.08x faster                                                   |
| richards                   | 45.2 ms                                                      | 42.1 ms: 1.07x faster                                                  |
| richards_super             | 51.6 ms                                                      | 48.4 ms: 1.07x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.62 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.20 sec: 1.06x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 107 ms: 1.05x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 18.9 ms: 1.05x faster                                                  |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| regex_dna                  | 180 ms                                                       | 173 ms: 1.04x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 82.0 ms: 1.04x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 709 ms: 1.04x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.1 ms: 1.04x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.08 sec: 1.04x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.96 us: 1.03x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 57.5 ms: 1.03x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.45 sec: 1.03x faster                                                 |
| thrift                     | 778 us                                                       | 757 us: 1.03x faster                                                   |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                 |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                  |
| coverage                   | 83.0 ms                                                      | 81.0 ms: 1.02x faster                                                  |
| chaos                      | 57.3 ms                                                      | 56.1 ms: 1.02x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.3 ms: 1.02x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.27 ms: 1.02x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.75 us: 1.01x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                  |
| raytrace                   | 253 ms                                                       | 252 ms: 1.00x faster                                                   |
| meteor_contest             | 102 ms                                                       | 102 ms: 1.00x slower                                                   |
| json                       | 4.93 ms                                                      | 4.98 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 212 us: 1.01x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 79.7 ms: 1.01x slower                                                  |
| django_template            | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                  |
| generators                 | 28.8 ms                                                      | 29.4 ms: 1.02x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.26 us: 1.02x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.7 us: 1.03x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                  |
| fannkuch                   | 370 ms                                                       | 381 ms: 1.03x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 304 us: 1.03x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.28 ms: 1.05x slower                                                  |
| mako                       | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                  |
| nbody                      | 85.1 ms                                                      | 90.9 ms: 1.07x slower                                                  |
| sympy_expand               | 457 ms                                                       | 491 ms: 1.07x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.29 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.30 ms: 1.42x slower                                                  |
| telco                      | 7.82 ms                                                      | 156 ms: 19.95x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 255 ms: 23.17x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.00x faster                                                           |

Benchmark hidden because not significant (4): crypto_pyaes, genshi_xml, logging_silent, sympy_str
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260123-3.15.0a5+-58ccf21/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.044x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.16x