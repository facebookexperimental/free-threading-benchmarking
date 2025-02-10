# Results vs. 3.13.0rc2

- fork: python
- ref: 7e6ee50b6b8c760bcefb
- machine: linux-x86_64
- commit hash: 7e6ee50
- commit date: 2025-02-10
- overall geometric mean: 1.058x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 253 ms: 1.03x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 626 ms: 1.46x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 321 ms: 1.44x faster                                                   |
| async_tree_io              | 876 ms                                                       | 619 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 498 ms: 1.34x faster                                                   |
| async_tree_none            | 354 ms                                                       | 269 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 489 ms: 1.30x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 319 ms: 1.30x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 261 ms: 1.29x faster                                                   |
| async_generators           | 377 ms                                                       | 322 ms: 1.17x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 22.6 ms: 1.04x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 186 ms: 1.16x faster                                                   |
| float          | 77.5 ms                                                      | 71.6 ms: 1.08x faster                                                  |
| nbody          | 85.1 ms                                                      | 95.8 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                  |
| regex_dna      | 180 ms                                                       | 164 ms: 1.10x faster                                                   |
| regex_compile  | 132 ms                                                       | 127 ms: 1.04x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 23.3 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.88 sec: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.8 ms: 1.05x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 83.4 ms: 1.02x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.1 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 212 us: 1.01x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 308 us: 1.05x slower                                                   |
| json_loads           | 27.0 us                                                      | 28.4 us: 1.05x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.51 ms: 1.02x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.8 ms: 1.34x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.8 ms: 1.03x faster                                                  |
| django_template | 34.1 ms                                                      | 34.5 ms: 1.01x slower                                                  |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 626 ms: 1.46x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 321 ms: 1.44x faster                                                   |
| async_tree_io              | 876 ms                                                       | 619 ms: 1.41x faster                                                   |
| deepcopy                   | 355 us                                                       | 253 us: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 498 ms: 1.34x faster                                                   |
| async_tree_none            | 354 ms                                                       | 269 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 489 ms: 1.30x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 30.0 us: 1.30x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 319 ms: 1.30x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 261 ms: 1.29x faster                                                   |
| go                         | 141 ms                                                       | 115 ms: 1.22x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.55 us: 1.22x faster                                                  |
| spectral_norm              | 111 ms                                                       | 91.4 ms: 1.21x faster                                                  |
| scimark_sor                | 134 ms                                                       | 113 ms: 1.19x faster                                                   |
| async_generators           | 377 ms                                                       | 322 ms: 1.17x faster                                                   |
| pidigits                   | 217 ms                                                       | 186 ms: 1.16x faster                                                   |
| pylint                     | 317 ms                                                       | 278 ms: 1.14x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.14 ms: 1.14x faster                                                  |
| scimark_fft                | 349 ms                                                       | 310 ms: 1.13x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                  |
| regex_dna                  | 180 ms                                                       | 164 ms: 1.10x faster                                                   |
| telco                      | 7.82 ms                                                      | 7.16 ms: 1.09x faster                                                  |
| float                      | 77.5 ms                                                      | 71.6 ms: 1.08x faster                                                  |
| pyflate                    | 449 ms                                                       | 415 ms: 1.08x faster                                                   |
| richards_super             | 51.6 ms                                                      | 48.0 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.13 sec: 1.08x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 687 ms: 1.07x faster                                                   |
| richards                   | 45.2 ms                                                      | 42.1 ms: 1.07x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.88 sec: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                                 |
| thrift                     | 778 us                                                       | 735 us: 1.06x faster                                                   |
| coverage                   | 83.0 ms                                                      | 79.0 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.8 ms: 1.05x faster                                                  |
| regex_compile              | 132 ms                                                       | 127 ms: 1.04x faster                                                   |
| sqlglot_normalize          | 106 ms                                                       | 101 ms: 1.04x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 22.6 ms: 1.04x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 65.6 ms: 1.04x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 20.8 ms: 1.03x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.96 us: 1.03x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 51.1 ms: 1.03x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.65 us: 1.03x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 151 ms: 1.03x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.83 ms: 1.03x faster                                                  |
| sympy_str                  | 275 ms                                                       | 267 ms: 1.03x faster                                                   |
| 2to3                       | 260 ms                                                       | 253 ms: 1.03x faster                                                   |
| meteor_contest             | 102 ms                                                       | 99.1 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.4 ms: 1.02x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.9 ms: 1.02x faster                                                  |
| mdp                        | 2.36 sec                                                     | 2.30 sec: 1.02x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 58.1 ms: 1.02x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 152 us: 1.02x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 18.8 ms: 1.02x faster                                                  |
| sympy_expand               | 457 ms                                                       | 450 ms: 1.02x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 19.5 ms: 1.02x faster                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.54 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.19 us: 1.01x faster                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.24 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| fannkuch                   | 370 ms                                                       | 368 ms: 1.01x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 112 ms: 1.01x faster                                                   |
| comprehensions             | 16.5 us                                                      | 16.4 us: 1.00x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 75.6 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 212 us: 1.01x slower                                                   |
| generators                 | 28.8 ms                                                      | 29.1 ms: 1.01x slower                                                  |
| django_template            | 34.1 ms                                                      | 34.5 ms: 1.01x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 79.6 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.51 ms: 1.02x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 23.3 ms: 1.02x slower                                                  |
| json                       | 4.93 ms                                                      | 5.06 ms: 1.03x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| raytrace                   | 253 ms                                                       | 262 ms: 1.04x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 308 us: 1.05x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.4 us: 1.05x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 11.4 ms: 1.09x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                  |
| nbody                      | 85.1 ms                                                      | 95.8 ms: 1.13x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.8 ms: 1.34x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.24 ms: 1.35x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 89.2 ms: 8.11x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (5): genshi_xml, chaos, logging_silent, pycparser, deltablue
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.058x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.10x