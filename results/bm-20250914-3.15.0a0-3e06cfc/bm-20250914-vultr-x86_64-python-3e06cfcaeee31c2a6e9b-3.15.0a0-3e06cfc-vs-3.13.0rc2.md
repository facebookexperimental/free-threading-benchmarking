# Results vs. 3.13.0rc2

- fork: python
- ref: 3e06cfcaeee31c2a6e9b
- machine: linux-x86_64
- commit hash: 3e06cfc
- commit date: 2025-09-14
- overall geometric mean: 1.041x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 251 ms: 1.04x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.53 sec: 1.03x faster                                                |
| html5lib       | 67.0 ms                                                      | 61.3 ms: 1.09x faster                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 621 ms: 1.47x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 314 ms: 1.47x faster                                                  |
| async_tree_io              | 876 ms                                                       | 605 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 493 ms: 1.35x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 253 ms: 1.33x faster                                                  |
| async_tree_none            | 354 ms                                                       | 267 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 316 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 494 ms: 1.29x faster                                                  |
| async_generators           | 377 ms                                                       | 347 ms: 1.09x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.02x faster                                                 |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                                  |
| float          | 77.5 ms                                                      | 71.5 ms: 1.08x faster                                                 |
| nbody          | 85.1 ms                                                      | 89.3 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.56 ms: 1.21x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 20.7 ms: 1.10x faster                                                 |
| regex_dna      | 180 ms                                                       | 166 ms: 1.08x faster                                                  |
| regex_compile  | 132 ms                                                       | 123 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                        | 1.11x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.57 ms: 1.10x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 92.8 ms: 1.02x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.7 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 58.2 ms: 1.02x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 208 us: 1.01x faster                                                  |
| pickle_pure_python   | 294 us                                                       | 301 us: 1.02x slower                                                  |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 21.5 ms                                                      | 20.6 ms: 1.04x faster                                                 |
| genshi_xml     | 48.8 ms                                                      | 48.4 ms: 1.01x faster                                                 |
| mako           | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.04x faster                                                |
| deepcopy_memo              | 39.1 us                                                      | 26.1 us: 1.50x faster                                                 |
| deepcopy                   | 355 us                                                       | 240 us: 1.48x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 621 ms: 1.47x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 314 ms: 1.47x faster                                                  |
| async_tree_io              | 876 ms                                                       | 605 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 493 ms: 1.35x faster                                                  |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 253 ms: 1.33x faster                                                  |
| async_tree_none            | 354 ms                                                       | 267 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 316 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 494 ms: 1.29x faster                                                  |
| scimark_sor                | 134 ms                                                       | 109 ms: 1.24x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.57 us: 1.21x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.56 ms: 1.21x faster                                                 |
| spectral_norm              | 111 ms                                                       | 94.5 ms: 1.18x faster                                                 |
| pylint                     | 317 ms                                                       | 279 ms: 1.14x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 66.5 ms: 1.13x faster                                                 |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                                  |
| pyflate                    | 449 ms                                                       | 404 ms: 1.11x faster                                                  |
| richards_super             | 51.6 ms                                                      | 46.9 ms: 1.10x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.57 ms: 1.10x faster                                                 |
| richards                   | 45.2 ms                                                      | 41.1 ms: 1.10x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 20.7 ms: 1.10x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 61.3 ms: 1.09x faster                                                 |
| async_generators           | 377 ms                                                       | 347 ms: 1.09x faster                                                  |
| float                      | 77.5 ms                                                      | 71.5 ms: 1.08x faster                                                 |
| regex_dna                  | 180 ms                                                       | 166 ms: 1.08x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.54 ms: 1.08x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 684 ms: 1.08x faster                                                  |
| regex_compile              | 132 ms                                                       | 123 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.40 sec: 1.07x faster                                                |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.07x faster                                                 |
| logging_silent             | 103 ns                                                       | 96.1 ns: 1.07x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.18 sec: 1.06x faster                                                |
| sympy_integrate            | 19.8 ms                                                      | 18.7 ms: 1.06x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                |
| comprehensions             | 16.5 us                                                      | 15.5 us: 1.06x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.2 ms: 1.05x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.88 us: 1.05x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.54 us: 1.05x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 20.6 ms: 1.04x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.7 ms: 1.04x faster                                                 |
| 2to3                       | 260 ms                                                       | 251 ms: 1.04x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 109 ms: 1.04x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 149 us: 1.03x faster                                                  |
| sympy_str                  | 275 ms                                                       | 265 ms: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.53 sec: 1.03x faster                                                |
| scimark_fft                | 349 ms                                                       | 339 ms: 1.03x faster                                                  |
| meteor_contest             | 102 ms                                                       | 98.5 ms: 1.03x faster                                                 |
| thrift                     | 778 us                                                       | 756 us: 1.03x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 152 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.8 ms: 1.02x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 83.7 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 58.2 ms: 1.02x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.10 sec: 1.02x faster                                                |
| sympy_expand               | 457 ms                                                       | 450 ms: 1.02x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.02x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 77.7 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 208 us: 1.01x faster                                                  |
| genshi_xml                 | 48.8 ms                                                      | 48.4 ms: 1.01x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 68.1 ms: 1.00x slower                                                 |
| raytrace                   | 253 ms                                                       | 255 ms: 1.01x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 301 us: 1.02x slower                                                  |
| json                       | 4.93 ms                                                      | 5.06 ms: 1.03x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.24 ms: 1.04x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                                 |
| fannkuch                   | 370 ms                                                       | 384 ms: 1.04x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.31 us: 1.05x slower                                                 |
| nbody                      | 85.1 ms                                                      | 89.3 ms: 1.05x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.00 ms: 1.09x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.92 ms: 1.44x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.68 ms: 1.49x slower                                                 |
| telco                      | 7.82 ms                                                      | 157 ms: 20.10x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (5): coverage, scimark_sparse_mat_mult, chaos, asyncio_websockets, django_template
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250914-3.15.0a0-3e06cfc/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.041x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x