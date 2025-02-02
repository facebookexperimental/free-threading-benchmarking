# Results vs. 3.13.0rc2

- fork: python
- ref: cf4c4ecc26c7e3b89f2e
- machine: linux-x86_64
- commit hash: cf4c4ec
- commit date: 2025-02-01
- overall geometric mean: 1.065x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 252 ms: 1.03x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.52 sec: 1.04x faster                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 628 ms: 1.46x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 323 ms: 1.43x faster                                                   |
| async_tree_io              | 876 ms                                                       | 620 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 500 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 314 ms: 1.32x faster                                                   |
| async_tree_none            | 354 ms                                                       | 269 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 261 ms: 1.29x faster                                                   |
| async_generators           | 377 ms                                                       | 324 ms: 1.17x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 21.5 ms: 1.10x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                           |

Benchmark hidden because not significant (2): asyncio_tcp, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 197 ms: 1.10x faster                                                   |
| float          | 77.5 ms                                                      | 71.4 ms: 1.09x faster                                                  |
| nbody          | 85.1 ms                                                      | 88.6 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.57 ms: 1.20x faster                                                  |
| regex_dna      | 180 ms                                                       | 170 ms: 1.06x faster                                                   |
| regex_compile  | 132 ms                                                       | 125 ms: 1.06x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 22.8 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle            | 14.3 us                                                      | 13.2 us: 1.09x faster                                                  |
| tomli_loads         | 2.01 sec                                                     | 1.87 sec: 1.07x faster                                                 |
| xml_etree_parse     | 136 ms                                                       | 129 ms: 1.05x faster                                                   |
| xml_etree_iterparse | 94.9 ms                                                      | 91.7 ms: 1.03x faster                                                  |
| xml_etree_generate  | 85.4 ms                                                      | 82.6 ms: 1.03x faster                                                  |
| xml_etree_process   | 59.3 ms                                                      | 57.5 ms: 1.03x faster                                                  |
| pickle_dict         | 32.5 us                                                      | 32.8 us: 1.01x slower                                                  |
| pickle_pure_python  | 294 us                                                       | 307 us: 1.04x slower                                                   |
| json_loads          | 27.0 us                                                      | 28.5 us: 1.05x slower                                                  |
| pickle              | 11.3 us                                                      | 12.1 us: 1.07x slower                                                  |
| json_dumps          | 10.5 ms                                                      | 11.3 ms: 1.08x slower                                                  |
| pickle_list         | 4.93 us                                                      | 5.31 us: 1.08x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (2): unpickle_list, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.44 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.8 ms: 1.04x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 47.9 ms: 1.02x faster                                                  |
| django_template | 34.1 ms                                                      | 33.9 ms: 1.01x faster                                                  |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 628 ms: 1.46x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 323 ms: 1.43x faster                                                   |
| deepcopy                   | 355 us                                                       | 251 us: 1.42x faster                                                   |
| async_tree_io              | 876 ms                                                       | 620 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 500 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 314 ms: 1.32x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 29.7 us: 1.32x faster                                                  |
| async_tree_none            | 354 ms                                                       | 269 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 261 ms: 1.29x faster                                                   |
| go                         | 141 ms                                                       | 112 ms: 1.25x faster                                                   |
| spectral_norm              | 111 ms                                                       | 90.2 ms: 1.23x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.59 us: 1.20x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.57 ms: 1.20x faster                                                  |
| scimark_sor                | 134 ms                                                       | 113 ms: 1.19x faster                                                   |
| async_generators           | 377 ms                                                       | 324 ms: 1.17x faster                                                   |
| pylint                     | 317 ms                                                       | 275 ms: 1.15x faster                                                   |
| scimark_fft                | 349 ms                                                       | 304 ms: 1.15x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.12 ms: 1.14x faster                                                  |
| pyflate                    | 449 ms                                                       | 404 ms: 1.11x faster                                                   |
| pidigits                   | 217 ms                                                       | 197 ms: 1.10x faster                                                   |
| richards                   | 45.2 ms                                                      | 41.1 ms: 1.10x faster                                                  |
| richards_super             | 51.6 ms                                                      | 47.1 ms: 1.10x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.5 ms: 1.10x faster                                                  |
| unpack_sequence            | 44.8 ns                                                      | 41.2 ns: 1.09x faster                                                  |
| unpickle                   | 14.3 us                                                      | 13.2 us: 1.09x faster                                                  |
| float                      | 77.5 ms                                                      | 71.4 ms: 1.09x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.25 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.14 sec: 1.07x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.87 sec: 1.07x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 689 ms: 1.07x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.40 sec: 1.07x faster                                                 |
| thrift                     | 778 us                                                       | 731 us: 1.06x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.4 ms: 1.06x faster                                                  |
| regex_dna                  | 180 ms                                                       | 170 ms: 1.06x faster                                                   |
| regex_compile              | 132 ms                                                       | 125 ms: 1.06x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 107 ms: 1.05x faster                                                   |
| coverage                   | 83.0 ms                                                      | 78.7 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.05x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.69 ms: 1.05x faster                                                  |
| meteor_contest             | 102 ms                                                       | 96.9 ms: 1.05x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.89 us: 1.05x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 64.9 ms: 1.05x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.5 ms: 1.04x faster                                                  |
| chaos                      | 57.3 ms                                                      | 55.2 ms: 1.04x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 20.8 ms: 1.04x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.52 sec: 1.04x faster                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 50.9 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.7 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 82.6 ms: 1.03x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 57.5 ms: 1.03x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.64 us: 1.03x faster                                                  |
| 2to3                       | 260 ms                                                       | 252 ms: 1.03x faster                                                   |
| typing_runtime_protocols   | 155 us                                                       | 150 us: 1.03x faster                                                   |
| sqlglot_normalize          | 106 ms                                                       | 103 ms: 1.03x faster                                                   |
| deltablue                  | 3.12 ms                                                      | 3.04 ms: 1.03x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 152 ms: 1.02x faster                                                   |
| generators                 | 28.8 ms                                                      | 28.2 ms: 1.02x faster                                                  |
| sympy_str                  | 275 ms                                                       | 269 ms: 1.02x faster                                                   |
| comprehensions             | 16.5 us                                                      | 16.1 us: 1.02x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.5 ms: 1.02x faster                                                  |
| genshi_xml                 | 48.8 ms                                                      | 47.9 ms: 1.02x faster                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.54 ms: 1.01x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 77.5 ms: 1.01x faster                                                  |
| logging_silent             | 103 ns                                                       | 101 ns: 1.01x faster                                                   |
| sympy_expand               | 457 ms                                                       | 452 ms: 1.01x faster                                                   |
| fannkuch                   | 370 ms                                                       | 366 ms: 1.01x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| django_template            | 34.1 ms                                                      | 33.9 ms: 1.01x faster                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.24 ms: 1.00x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 75.2 ms: 1.01x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.8 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.44 ms: 1.01x slower                                                  |
| pickle_dict                | 32.5 us                                                      | 32.8 us: 1.01x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.43 sec: 1.03x slower                                                 |
| raytrace                   | 253 ms                                                       | 261 ms: 1.03x slower                                                   |
| json                       | 4.93 ms                                                      | 5.10 ms: 1.04x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                  |
| nbody                      | 85.1 ms                                                      | 88.6 ms: 1.04x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 307 us: 1.04x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.5 us: 1.05x slower                                                  |
| pickle                     | 11.3 us                                                      | 12.1 us: 1.07x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 11.3 ms: 1.08x slower                                                  |
| pickle_list                | 4.93 us                                                      | 5.31 us: 1.08x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.11x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.44 ms: 1.41x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 87.7 ms: 7.98x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (5): asyncio_tcp, sqlite_synth, unpickle_list, asyncio_tcp_ssl, unpickle_pure_python
Ignored benchmarks (7) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, tornado_http
Ignored benchmarks (8) of results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.065x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.10x