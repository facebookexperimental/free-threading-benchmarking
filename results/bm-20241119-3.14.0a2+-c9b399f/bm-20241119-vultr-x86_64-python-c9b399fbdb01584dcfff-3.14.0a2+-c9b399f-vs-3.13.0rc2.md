# Results vs. 3.13.0rc2

- fork: python
- ref: c9b399fbdb01584dcfff
- machine: linux-x86_64
- commit hash: c9b399f
- commit date: 2024-11-19
- overall geometric mean: 1.02x slower
- HPT reliability: 94.59%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 255 ms: 1.02x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.60 sec: 1.01x faster                                                 |
| html5lib       | 67.0 ms                                                      | 64.1 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| coroutines       | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                                  |
| async_generators | 377 ms                                                       | 375 ms: 1.01x faster                                                   |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.53 sec: 1.01x slower                                                 |
| Geometric mean   | (ref)                                                        | 1.00x faster                                                           |

Benchmark hidden because not significant (2): asyncio_tcp, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 79.8 ms: 1.03x slower                                                  |
| nbody          | 85.1 ms                                                      | 96.3 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                  |
| regex_dna      | 180 ms                                                       | 183 ms: 1.01x slower                                                   |
| regex_compile  | 132 ms                                                       | 135 ms: 1.02x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 24.6 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 25.1 us: 1.08x faster                                                  |
| unpickle             | 14.3 us                                                      | 13.7 us: 1.05x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 135 ms: 1.01x faster                                                   |
| xml_etree_process    | 59.3 ms                                                      | 58.8 ms: 1.01x faster                                                  |
| pickle_dict          | 32.5 us                                                      | 32.8 us: 1.01x slower                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 96.1 ms: 1.01x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 215 us: 1.02x slower                                                   |
| unpickle_list        | 4.71 us                                                      | 4.83 us: 1.03x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.13 sec: 1.06x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 317 us: 1.08x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                  |
| pickle_list          | 4.93 us                                                      | 5.32 us: 1.08x slower                                                  |
| pickle               | 11.3 us                                                      | 12.6 us: 1.11x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 11.1 ms: 1.01x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.01x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                                  |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 50.3 ms: 1.03x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 22.4 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                 | 355 us                                                       | 266 us: 1.34x faster                                                   |
| deepcopy_memo            | 39.1 us                                                      | 30.3 us: 1.29x faster                                                  |
| go                       | 141 ms                                                       | 120 ms: 1.17x faster                                                   |
| deepcopy_reduce          | 3.11 us                                                      | 2.69 us: 1.15x faster                                                  |
| json_loads               | 27.0 us                                                      | 25.1 us: 1.08x faster                                                  |
| regex_effbot             | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                  |
| telco                    | 7.82 ms                                                      | 7.35 ms: 1.06x faster                                                  |
| json                     | 4.93 ms                                                      | 4.67 ms: 1.06x faster                                                  |
| pprint_safe_repr         | 738 ms                                                       | 704 ms: 1.05x faster                                                   |
| unpickle                 | 14.3 us                                                      | 13.7 us: 1.05x faster                                                  |
| html5lib                 | 67.0 ms                                                      | 64.1 ms: 1.05x faster                                                  |
| thrift                   | 778 us                                                       | 745 us: 1.05x faster                                                   |
| pathlib                  | 19.2 ms                                                      | 18.4 ms: 1.04x faster                                                  |
| spectral_norm            | 111 ms                                                       | 108 ms: 1.03x faster                                                   |
| coverage                 | 83.0 ms                                                      | 80.6 ms: 1.03x faster                                                  |
| pprint_pformat           | 1.50 sec                                                     | 1.46 sec: 1.03x faster                                                 |
| coroutines               | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                                  |
| bpe_tokeniser            | 4.45 sec                                                     | 4.35 sec: 1.02x faster                                                 |
| 2to3                     | 260 ms                                                       | 255 ms: 1.02x faster                                                   |
| sympy_sum                | 156 ms                                                       | 153 ms: 1.02x faster                                                   |
| xml_etree_parse          | 136 ms                                                       | 135 ms: 1.01x faster                                                   |
| xml_etree_process        | 59.3 ms                                                      | 58.8 ms: 1.01x faster                                                  |
| meteor_contest           | 102 ms                                                       | 101 ms: 1.01x faster                                                   |
| scimark_fft              | 349 ms                                                       | 347 ms: 1.01x faster                                                   |
| async_generators         | 377 ms                                                       | 375 ms: 1.01x faster                                                   |
| docutils                 | 2.62 sec                                                     | 2.60 sec: 1.01x faster                                                 |
| hexiom                   | 5.99 ms                                                      | 5.98 ms: 1.00x faster                                                  |
| sympy_integrate          | 19.8 ms                                                      | 19.9 ms: 1.00x slower                                                  |
| dulwich_log              | 74.8 ms                                                      | 75.2 ms: 1.01x slower                                                  |
| sympy_expand             | 457 ms                                                       | 460 ms: 1.01x slower                                                   |
| crypto_pyaes             | 67.9 ms                                                      | 68.4 ms: 1.01x slower                                                  |
| pyflate                  | 449 ms                                                       | 453 ms: 1.01x slower                                                   |
| pickle_dict              | 32.5 us                                                      | 32.8 us: 1.01x slower                                                  |
| nqueens                  | 78.6 ms                                                      | 79.3 ms: 1.01x slower                                                  |
| richards_super           | 51.6 ms                                                      | 52.1 ms: 1.01x slower                                                  |
| scimark_sor              | 134 ms                                                       | 136 ms: 1.01x slower                                                   |
| python_startup_no_site   | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                  |
| sqlglot_normalize        | 106 ms                                                       | 107 ms: 1.01x slower                                                   |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.53 sec: 1.01x slower                                                 |
| python_startup           | 11.0 ms                                                      | 11.1 ms: 1.01x slower                                                  |
| xml_etree_iterparse      | 94.9 ms                                                      | 96.1 ms: 1.01x slower                                                  |
| logging_silent           | 103 ns                                                       | 104 ns: 1.01x slower                                                   |
| regex_dna                | 180 ms                                                       | 183 ms: 1.01x slower                                                   |
| scimark_monte_carlo      | 65.4 ms                                                      | 66.4 ms: 1.02x slower                                                  |
| typing_runtime_protocols | 155 us                                                       | 157 us: 1.02x slower                                                   |
| fannkuch                 | 370 ms                                                       | 376 ms: 1.02x slower                                                   |
| sqlglot_optimize         | 52.7 ms                                                      | 53.7 ms: 1.02x slower                                                  |
| regex_compile            | 132 ms                                                       | 135 ms: 1.02x slower                                                   |
| unpickle_pure_python     | 210 us                                                       | 215 us: 1.02x slower                                                   |
| sqlglot_transpile        | 1.56 ms                                                      | 1.60 ms: 1.02x slower                                                  |
| pycparser                | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                 |
| logging_format           | 6.84 us                                                      | 7.02 us: 1.03x slower                                                  |
| unpickle_list            | 4.71 us                                                      | 4.83 us: 1.03x slower                                                  |
| django_template          | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                                  |
| create_gc_cycles         | 1.34 ms                                                      | 1.38 ms: 1.03x slower                                                  |
| generators               | 28.8 ms                                                      | 29.7 ms: 1.03x slower                                                  |
| mako                     | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| chaos                    | 57.3 ms                                                      | 59.1 ms: 1.03x slower                                                  |
| float                    | 77.5 ms                                                      | 79.8 ms: 1.03x slower                                                  |
| genshi_xml               | 48.8 ms                                                      | 50.3 ms: 1.03x slower                                                  |
| comprehensions           | 16.5 us                                                      | 17.1 us: 1.04x slower                                                  |
| raytrace                 | 253 ms                                                       | 262 ms: 1.04x slower                                                   |
| sqlglot_parse            | 1.25 ms                                                      | 1.30 ms: 1.04x slower                                                  |
| genshi_text              | 21.5 ms                                                      | 22.4 ms: 1.04x slower                                                  |
| deltablue                | 3.12 ms                                                      | 3.29 ms: 1.05x slower                                                  |
| tomli_loads              | 2.01 sec                                                     | 2.13 sec: 1.06x slower                                                 |
| gc_traversal             | 3.14 ms                                                      | 3.38 ms: 1.07x slower                                                  |
| unpack_sequence          | 44.8 ns                                                      | 48.1 ns: 1.07x slower                                                  |
| pickle_pure_python       | 294 us                                                       | 317 us: 1.08x slower                                                   |
| json_dumps               | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                  |
| pickle_list              | 4.93 us                                                      | 5.32 us: 1.08x slower                                                  |
| regex_v8                 | 22.7 ms                                                      | 24.6 ms: 1.09x slower                                                  |
| bench_thread_pool        | 919 us                                                       | 1.02 ms: 1.10x slower                                                  |
| pickle                   | 11.3 us                                                      | 12.6 us: 1.11x slower                                                  |
| nbody                    | 85.1 ms                                                      | 96.3 ms: 1.13x slower                                                  |
| bench_mp_pool            | 11.0 ms                                                      | 63.8 ms: 5.80x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (12): sqlite_synth, xml_etree_generate, asyncio_tcp, sympy_str, pidigits, asyncio_websockets, logging_simple, scimark_sparse_mat_mult, scimark_lu, mdp, richards, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 94.59% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x