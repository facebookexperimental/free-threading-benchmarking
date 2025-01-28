# Results vs. 3.13.0rc2

- fork: python
- ref: 1c3bb200da77f9df30af
- machine: linux-x86_64
- commit hash: 1c3bb20
- commit date: 2025-01-28
- overall geometric mean: 1.051x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 619 ms: 1.48x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 325 ms: 1.42x faster                                                   |
| async_tree_io              | 876 ms                                                       | 626 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 494 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 316 ms: 1.31x faster                                                   |
| async_tree_none            | 354 ms                                                       | 272 ms: 1.30x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 264 ms: 1.27x faster                                                   |
| async_generators           | 377 ms                                                       | 320 ms: 1.18x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 21.8 ms: 1.08x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 194 ms: 1.11x faster                                                   |
| float          | 77.5 ms                                                      | 72.0 ms: 1.08x faster                                                  |
| nbody          | 85.1 ms                                                      | 89.3 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                  |
| regex_compile  | 132 ms                                                       | 126 ms: 1.05x faster                                                   |
| regex_dna      | 180 ms                                                       | 172 ms: 1.05x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.5 ms: 1.05x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.94 sec: 1.04x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.6 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 212 us: 1.01x slower                                                   |
| json_loads           | 27.0 us                                                      | 28.4 us: 1.05x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 312 us: 1.06x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.3 ms: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.42 ms: 1.00x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.15x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 48.4 ms: 1.01x faster                                                  |
| django_template | 34.1 ms                                                      | 34.9 ms: 1.02x slower                                                  |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 619 ms: 1.48x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 325 ms: 1.42x faster                                                   |
| async_tree_io              | 876 ms                                                       | 626 ms: 1.40x faster                                                   |
| deepcopy                   | 355 us                                                       | 256 us: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 494 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 316 ms: 1.31x faster                                                   |
| async_tree_none            | 354 ms                                                       | 272 ms: 1.30x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 30.1 us: 1.30x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 264 ms: 1.27x faster                                                   |
| spectral_norm              | 111 ms                                                       | 90.5 ms: 1.23x faster                                                  |
| go                         | 141 ms                                                       | 115 ms: 1.22x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.60 us: 1.19x faster                                                  |
| async_generators           | 377 ms                                                       | 320 ms: 1.18x faster                                                   |
| scimark_sor                | 134 ms                                                       | 116 ms: 1.16x faster                                                   |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                   |
| pidigits                   | 217 ms                                                       | 194 ms: 1.11x faster                                                   |
| scimark_fft                | 349 ms                                                       | 317 ms: 1.10x faster                                                   |
| telco                      | 7.82 ms                                                      | 7.21 ms: 1.08x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.8 ms: 1.08x faster                                                  |
| pyflate                    | 449 ms                                                       | 415 ms: 1.08x faster                                                   |
| float                      | 77.5 ms                                                      | 72.0 ms: 1.08x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                  |
| richards                   | 45.2 ms                                                      | 42.5 ms: 1.06x faster                                                  |
| richards_super             | 51.6 ms                                                      | 48.6 ms: 1.06x faster                                                  |
| thrift                     | 778 us                                                       | 732 us: 1.06x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.44 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.21 sec: 1.06x faster                                                 |
| regex_compile              | 132 ms                                                       | 126 ms: 1.05x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 703 ms: 1.05x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.5 ms: 1.05x faster                                                  |
| regex_dna                  | 180 ms                                                       | 172 ms: 1.05x faster                                                   |
| coverage                   | 83.0 ms                                                      | 79.5 ms: 1.04x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.44 sec: 1.04x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 18.5 ms: 1.04x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.94 sec: 1.04x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.80 ms: 1.03x faster                                                  |
| chaos                      | 57.3 ms                                                      | 55.5 ms: 1.03x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 152 ms: 1.02x faster                                                   |
| docutils                   | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                 |
| meteor_contest             | 102 ms                                                       | 99.4 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.6 ms: 1.02x faster                                                  |
| 2to3                       | 260 ms                                                       | 254 ms: 1.02x faster                                                   |
| logging_simple             | 6.16 us                                                      | 6.04 us: 1.02x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 51.8 ms: 1.02x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 77.2 ms: 1.02x faster                                                  |
| generators                 | 28.8 ms                                                      | 28.3 ms: 1.02x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.73 us: 1.02x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 64.3 ms: 1.02x faster                                                  |
| sqlglot_normalize          | 106 ms                                                       | 104 ms: 1.02x faster                                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 1.54 ms: 1.01x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                  |
| sympy_str                  | 275 ms                                                       | 271 ms: 1.01x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.01x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 19.7 ms: 1.01x faster                                                  |
| genshi_xml                 | 48.8 ms                                                      | 48.4 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| sqlglot_parse              | 1.25 ms                                                      | 1.24 ms: 1.01x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.42 ms: 1.00x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 212 us: 1.01x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.18 ms: 1.02x slower                                                  |
| fannkuch                   | 370 ms                                                       | 377 ms: 1.02x slower                                                   |
| comprehensions             | 16.5 us                                                      | 16.8 us: 1.02x slower                                                  |
| django_template            | 34.1 ms                                                      | 34.9 ms: 1.02x slower                                                  |
| json                       | 4.93 ms                                                      | 5.05 ms: 1.03x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.44 sec: 1.03x slower                                                 |
| logging_silent             | 103 ns                                                       | 106 ns: 1.03x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                                  |
| nbody                      | 85.1 ms                                                      | 89.3 ms: 1.05x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.4 us: 1.05x slower                                                  |
| raytrace                   | 253 ms                                                       | 268 ms: 1.06x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 312 us: 1.06x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 11.3 ms: 1.07x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.21 ms: 1.34x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 87.8 ms: 7.98x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (7): dulwich_log, xml_etree_process, sqlite_synth, sympy_expand, pycparser, crypto_pyaes, typing_runtime_protocols
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.051x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.10x