# Results vs. 3.13.0rc2

- fork: python
- ref: de9c32fc34fe2e000de1
- machine: linux-x86_64
- commit hash: de9c32f
- commit date: 2026-05-20
- overall geometric mean: 1.074x slower
- HPT reliability: 98.62%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.62 sec                                                     | 2.98 sec: 1.14x slower                                                |
| html5lib       | 67.0 ms                                                      | 69.9 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 694 ms: 1.32x faster                                                  |
| async_tree_io              | 876 ms                                                       | 713 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 599 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 581 ms: 1.10x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 426 ms: 1.08x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 398 ms: 1.04x faster                                                  |
| async_tree_none            | 354 ms                                                       | 344 ms: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 509 ms: 1.02x faster                                                  |
| async_generators           | 377 ms                                                       | 386 ms: 1.02x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.9 ms: 1.06x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                          |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                  |
| float          | 77.5 ms                                                      | 88.5 ms: 1.14x slower                                                 |
| nbody          | 85.1 ms                                                      | 129 ms: 1.52x slower                                                  |
| Geometric mean | (ref)                                                        | 1.14x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 21.6 ms: 1.05x faster                                                 |
| regex_effbot   | 3.08 ms                                                      | 3.11 ms: 1.01x slower                                                 |
| regex_dna      | 180 ms                                                       | 186 ms: 1.03x slower                                                  |
| regex_compile  | 132 ms                                                       | 144 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.98 sec: 1.01x faster                                                |
| json_dumps           | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 244 us: 1.16x slower                                                  |
| json_loads           | 27.0 us                                                      | 31.5 us: 1.17x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 347 us: 1.18x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 102 ms: 1.20x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 76.0 ms: 1.28x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.11x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 41.0 ms: 1.20x slower                                                 |
| mako            | 11.3 ms                                                      | 16.3 ms: 1.44x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.32x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 133 ms: 2.39x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.33 sec: 1.77x faster                                                |
| gc_traversal               | 3.14 ms                                                      | 1.93 ms: 1.63x faster                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 6.98 ms: 1.58x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 694 ms: 1.32x faster                                                  |
| deepcopy                   | 355 us                                                       | 272 us: 1.31x faster                                                  |
| async_tree_io              | 876 ms                                                       | 713 ms: 1.23x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 31.9 us: 1.23x faster                                                 |
| pidigits                   | 217 ms                                                       | 185 ms: 1.17x faster                                                  |
| go                         | 141 ms                                                       | 124 ms: 1.14x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 1.96 us: 1.13x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 599 ms: 1.11x faster                                                  |
| scimark_sor                | 134 ms                                                       | 122 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 581 ms: 1.10x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 426 ms: 1.08x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 70.1 ms: 1.07x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 145 us: 1.06x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.6 ms: 1.05x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.97 us: 1.05x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 398 ms: 1.04x faster                                                  |
| async_tree_none            | 354 ms                                                       | 344 ms: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 509 ms: 1.02x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.98 sec: 1.01x faster                                                |
| bpe_tokeniser              | 4.45 sec                                                     | 4.40 sec: 1.01x faster                                                |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 3.11 ms: 1.01x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                                 |
| async_generators           | 377 ms                                                       | 386 ms: 1.02x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.15 sec: 1.03x slower                                                |
| logging_silent             | 103 ns                                                       | 106 ns: 1.03x slower                                                  |
| regex_dna                  | 180 ms                                                       | 186 ms: 1.03x slower                                                  |
| pyflate                    | 449 ms                                                       | 467 ms: 1.04x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 69.9 ms: 1.04x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.9 ms: 1.06x slower                                                 |
| comprehensions             | 16.5 us                                                      | 17.7 us: 1.08x slower                                                 |
| regex_compile              | 132 ms                                                       | 144 ms: 1.09x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 6.53 ms: 1.09x slower                                                 |
| json                       | 4.93 ms                                                      | 5.39 ms: 1.09x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.47 ms: 1.10x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 819 ms: 1.11x slower                                                  |
| chaos                      | 57.3 ms                                                      | 63.6 ms: 1.11x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 22.1 ms: 1.12x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 88.3 ms: 1.12x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.95 us: 1.13x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.70 sec: 1.14x slower                                                |
| docutils                   | 2.62 sec                                                     | 2.98 sec: 1.14x slower                                                |
| float                      | 77.5 ms                                                      | 88.5 ms: 1.14x slower                                                 |
| logging_format             | 6.84 us                                                      | 7.83 us: 1.14x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 130 ms: 1.15x slower                                                  |
| sympy_str                  | 275 ms                                                       | 318 ms: 1.16x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.46 ms: 1.16x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 244 us: 1.16x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 181 ms: 1.16x slower                                                  |
| json_loads                 | 27.0 us                                                      | 31.5 us: 1.17x slower                                                 |
| sympy_expand               | 457 ms                                                       | 535 ms: 1.17x slower                                                  |
| richards_super             | 51.6 ms                                                      | 60.5 ms: 1.17x slower                                                 |
| richards                   | 45.2 ms                                                      | 53.1 ms: 1.17x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 347 us: 1.18x slower                                                  |
| generators                 | 28.8 ms                                                      | 34.1 ms: 1.18x slower                                                 |
| thrift                     | 778 us                                                       | 923 us: 1.19x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.73 ms: 1.19x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 102 ms: 1.20x slower                                                  |
| django_template            | 34.1 ms                                                      | 41.0 ms: 1.20x slower                                                 |
| raytrace                   | 253 ms                                                       | 307 ms: 1.21x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 80.3 ms: 1.23x slower                                                 |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                                  |
| fannkuch                   | 370 ms                                                       | 470 ms: 1.27x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 76.0 ms: 1.28x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 89.5 ms: 1.32x slower                                                 |
| coverage                   | 83.0 ms                                                      | 116 ms: 1.39x slower                                                  |
| mako                       | 11.3 ms                                                      | 16.3 ms: 1.44x slower                                                 |
| nbody                      | 85.1 ms                                                      | 129 ms: 1.52x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.48 ms: 1.62x slower                                                 |
| telco                      | 7.82 ms                                                      | 177 ms: 22.67x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                          |

Benchmark hidden because not significant (3): async_tree_none_tg, scimark_fft, xml_etree_iterparse
Ignored benchmarks (23) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260520-3.16.0a0-de9c32f-NOGIL/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.074x slower

# HPT report

- Reliability score: 98.62% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.39x