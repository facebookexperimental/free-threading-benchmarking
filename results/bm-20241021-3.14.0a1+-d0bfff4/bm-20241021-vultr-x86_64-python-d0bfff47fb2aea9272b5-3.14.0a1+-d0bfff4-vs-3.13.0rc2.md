# Results vs. 3.13.0rc2

- fork: python
- ref: d0bfff47fb2aea9272b5
- machine: linux-x86_64
- commit hash: d0bfff4
- commit date: 2024-10-21
- overall geometric mean: 1.02x slower
- HPT reliability: 99.07%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.63 sec: 1.00x slower                                                 |
| html5lib       | 67.0 ms                                                      | 65.7 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| coroutines       | 23.6 ms                                                      | 22.3 ms: 1.06x faster                                                  |
| async_generators | 377 ms                                                       | 374 ms: 1.01x faster                                                   |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                 |
| Geometric mean   | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (2): asyncio_tcp, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 186 ms: 1.17x faster                                                   |
| float          | 77.5 ms                                                      | 80.8 ms: 1.04x slower                                                  |
| nbody          | 85.1 ms                                                      | 98.0 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                       | 174 ms: 1.04x faster                                                   |
| regex_compile  | 132 ms                                                       | 130 ms: 1.02x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 23.0 ms: 1.01x slower                                                  |
| regex_effbot   | 3.08 ms                                                      | 3.16 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                        | 1.00x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle             | 14.3 us                                                      | 13.6 us: 1.05x faster                                                  |
| json_loads           | 27.0 us                                                      | 26.2 us: 1.03x faster                                                  |
| pickle_list          | 4.93 us                                                      | 4.88 us: 1.01x faster                                                  |
| pickle_dict          | 32.5 us                                                      | 32.3 us: 1.01x faster                                                  |
| unpickle_list        | 4.71 us                                                      | 4.68 us: 1.01x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 96.1 ms: 1.01x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 86.6 ms: 1.01x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 60.6 ms: 1.02x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 221 us: 1.05x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 310 us: 1.05x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.12 sec: 1.06x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 11.7 ms: 1.11x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (2): pickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                      | 11.0 ms: 1.00x slower                                                  |
| python_startup_no_site | 7.39 ms                                                      | 7.42 ms: 1.00x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.00x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 22.5 ms: 1.04x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 51.3 ms: 1.05x slower                                                  |
| django_template | 34.1 ms                                                      | 35.9 ms: 1.05x slower                                                  |
| mako            | 11.3 ms                                                      | 12.1 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.06x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                 | 355 us                                                       | 264 us: 1.35x faster                                                   |
| deepcopy_memo            | 39.1 us                                                      | 31.2 us: 1.25x faster                                                  |
| deepcopy_reduce          | 3.11 us                                                      | 2.66 us: 1.17x faster                                                  |
| pidigits                 | 217 ms                                                       | 186 ms: 1.17x faster                                                   |
| go                       | 141 ms                                                       | 122 ms: 1.16x faster                                                   |
| coroutines               | 23.6 ms                                                      | 22.3 ms: 1.06x faster                                                  |
| telco                    | 7.82 ms                                                      | 7.41 ms: 1.06x faster                                                  |
| unpickle                 | 14.3 us                                                      | 13.6 us: 1.05x faster                                                  |
| pathlib                  | 19.2 ms                                                      | 18.4 ms: 1.04x faster                                                  |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 4.54 ms: 1.04x faster                                                  |
| regex_dna                | 180 ms                                                       | 174 ms: 1.04x faster                                                   |
| json_loads               | 27.0 us                                                      | 26.2 us: 1.03x faster                                                  |
| thrift                   | 778 us                                                       | 759 us: 1.03x faster                                                   |
| pprint_safe_repr         | 738 ms                                                       | 720 ms: 1.03x faster                                                   |
| coverage                 | 83.0 ms                                                      | 81.1 ms: 1.02x faster                                                  |
| 2to3                     | 260 ms                                                       | 254 ms: 1.02x faster                                                   |
| html5lib                 | 67.0 ms                                                      | 65.7 ms: 1.02x faster                                                  |
| json                     | 4.93 ms                                                      | 4.83 ms: 1.02x faster                                                  |
| scimark_fft              | 349 ms                                                       | 344 ms: 1.02x faster                                                   |
| regex_compile            | 132 ms                                                       | 130 ms: 1.02x faster                                                   |
| async_generators         | 377 ms                                                       | 374 ms: 1.01x faster                                                   |
| bpe_tokeniser            | 4.45 sec                                                     | 4.41 sec: 1.01x faster                                                 |
| pickle_list              | 4.93 us                                                      | 4.88 us: 1.01x faster                                                  |
| pickle_dict              | 32.5 us                                                      | 32.3 us: 1.01x faster                                                  |
| unpickle_list            | 4.71 us                                                      | 4.68 us: 1.01x faster                                                  |
| crypto_pyaes             | 67.9 ms                                                      | 67.6 ms: 1.00x faster                                                  |
| pprint_pformat           | 1.50 sec                                                     | 1.49 sec: 1.00x faster                                                 |
| python_startup           | 11.0 ms                                                      | 11.0 ms: 1.00x slower                                                  |
| python_startup_no_site   | 7.39 ms                                                      | 7.42 ms: 1.00x slower                                                  |
| docutils                 | 2.62 sec                                                     | 2.63 sec: 1.00x slower                                                 |
| dulwich_log              | 74.8 ms                                                      | 75.3 ms: 1.01x slower                                                  |
| mdp                      | 2.36 sec                                                     | 2.37 sec: 1.01x slower                                                 |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                 |
| pyflate                  | 449 ms                                                       | 453 ms: 1.01x slower                                                   |
| sqlglot_normalize        | 106 ms                                                       | 107 ms: 1.01x slower                                                   |
| xml_etree_iterparse      | 94.9 ms                                                      | 96.1 ms: 1.01x slower                                                  |
| create_gc_cycles         | 1.34 ms                                                      | 1.35 ms: 1.01x slower                                                  |
| regex_v8                 | 22.7 ms                                                      | 23.0 ms: 1.01x slower                                                  |
| xml_etree_generate       | 85.4 ms                                                      | 86.6 ms: 1.01x slower                                                  |
| pycparser                | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                 |
| sympy_expand             | 457 ms                                                       | 464 ms: 1.01x slower                                                   |
| nqueens                  | 78.6 ms                                                      | 79.9 ms: 1.02x slower                                                  |
| scimark_sor              | 134 ms                                                       | 137 ms: 1.02x slower                                                   |
| hexiom                   | 5.99 ms                                                      | 6.10 ms: 1.02x slower                                                  |
| scimark_lu               | 113 ms                                                       | 115 ms: 1.02x slower                                                   |
| sympy_integrate          | 19.8 ms                                                      | 20.2 ms: 1.02x slower                                                  |
| richards_super           | 51.6 ms                                                      | 52.7 ms: 1.02x slower                                                  |
| generators               | 28.8 ms                                                      | 29.4 ms: 1.02x slower                                                  |
| xml_etree_process        | 59.3 ms                                                      | 60.6 ms: 1.02x slower                                                  |
| typing_runtime_protocols | 155 us                                                       | 158 us: 1.02x slower                                                   |
| sqlglot_optimize         | 52.7 ms                                                      | 54.0 ms: 1.02x slower                                                  |
| meteor_contest           | 102 ms                                                       | 104 ms: 1.02x slower                                                   |
| regex_effbot             | 3.08 ms                                                      | 3.16 ms: 1.03x slower                                                  |
| scimark_monte_carlo      | 65.4 ms                                                      | 67.3 ms: 1.03x slower                                                  |
| sqlglot_transpile        | 1.56 ms                                                      | 1.61 ms: 1.03x slower                                                  |
| gc_traversal             | 3.14 ms                                                      | 3.25 ms: 1.04x slower                                                  |
| comprehensions           | 16.5 us                                                      | 17.0 us: 1.04x slower                                                  |
| float                    | 77.5 ms                                                      | 80.8 ms: 1.04x slower                                                  |
| fannkuch                 | 370 ms                                                       | 386 ms: 1.04x slower                                                   |
| genshi_text              | 21.5 ms                                                      | 22.5 ms: 1.04x slower                                                  |
| unpack_sequence          | 44.8 ns                                                      | 46.8 ns: 1.04x slower                                                  |
| richards                 | 45.2 ms                                                      | 47.2 ms: 1.04x slower                                                  |
| sqlglot_parse            | 1.25 ms                                                      | 1.31 ms: 1.05x slower                                                  |
| chaos                    | 57.3 ms                                                      | 60.1 ms: 1.05x slower                                                  |
| logging_silent           | 103 ns                                                       | 108 ns: 1.05x slower                                                   |
| unpickle_pure_python     | 210 us                                                       | 221 us: 1.05x slower                                                   |
| genshi_xml               | 48.8 ms                                                      | 51.3 ms: 1.05x slower                                                  |
| django_template          | 34.1 ms                                                      | 35.9 ms: 1.05x slower                                                  |
| pickle_pure_python       | 294 us                                                       | 310 us: 1.05x slower                                                   |
| deltablue                | 3.12 ms                                                      | 3.29 ms: 1.05x slower                                                  |
| tomli_loads              | 2.01 sec                                                     | 2.12 sec: 1.06x slower                                                 |
| raytrace                 | 253 ms                                                       | 271 ms: 1.07x slower                                                   |
| mako                     | 11.3 ms                                                      | 12.1 ms: 1.07x slower                                                  |
| bench_thread_pool        | 919 us                                                       | 1.02 ms: 1.11x slower                                                  |
| json_dumps               | 10.5 ms                                                      | 11.7 ms: 1.11x slower                                                  |
| nbody                    | 85.1 ms                                                      | 98.0 ms: 1.15x slower                                                  |
| bench_mp_pool            | 11.0 ms                                                      | 63.1 ms: 5.74x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (12): pickle, logging_simple, tornado_http, spectral_norm, asyncio_tcp, asyncio_websockets, sympy_str, logging_format, sqlite_synth, sympy_sum, pylint, xml_etree_parse
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 99.07% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x