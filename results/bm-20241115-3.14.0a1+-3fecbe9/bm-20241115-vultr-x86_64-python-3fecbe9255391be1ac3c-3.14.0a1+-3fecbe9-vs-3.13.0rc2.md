# Results vs. 3.13.0rc2

- fork: python
- ref: 3fecbe9255391be1ac3c
- machine: linux-x86_64
- commit hash: 3fecbe9
- commit date: 2024-11-15
- overall geometric mean: 1.02x slower
- HPT reliability: 95.40%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                   |
| html5lib       | 67.0 ms                                                      | 66.4 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| coroutines       | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                                  |
| async_generators | 377 ms                                                       | 368 ms: 1.02x faster                                                   |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                 |
| Geometric mean   | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (2): asyncio_tcp, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 78.7 ms: 1.02x slower                                                  |
| pidigits       | 217 ms                                                       | 224 ms: 1.04x slower                                                   |
| nbody          | 85.1 ms                                                      | 95.4 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                       | 183 ms: 1.01x slower                                                   |
| regex_effbot   | 3.08 ms                                                      | 3.13 ms: 1.01x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 24.1 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 24.8 us: 1.09x faster                                                  |
| unpickle             | 14.3 us                                                      | 13.4 us: 1.07x faster                                                  |
| pickle_dict          | 32.5 us                                                      | 31.6 us: 1.03x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 95.6 ms: 1.01x slower                                                  |
| pickle_list          | 4.93 us                                                      | 5.10 us: 1.04x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 220 us: 1.05x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 321 us: 1.09x slower                                                   |
| pickle               | 11.3 us                                                      | 12.4 us: 1.10x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (4): xml_etree_parse, unpickle_list, xml_etree_generate, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.43 ms: 1.00x slower                                                  |
| python_startup         | 11.0 ms                                                      | 11.1 ms: 1.01x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.01x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 49.9 ms: 1.02x slower                                                  |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| django_template | 34.1 ms                                                      | 35.3 ms: 1.03x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 22.3 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                 | 355 us                                                       | 265 us: 1.34x faster                                                   |
| deepcopy_memo            | 39.1 us                                                      | 30.5 us: 1.28x faster                                                  |
| deepcopy_reduce          | 3.11 us                                                      | 2.67 us: 1.16x faster                                                  |
| go                       | 141 ms                                                       | 122 ms: 1.15x faster                                                   |
| unpack_sequence          | 44.8 ns                                                      | 40.8 ns: 1.10x faster                                                  |
| json_loads               | 27.0 us                                                      | 24.8 us: 1.09x faster                                                  |
| unpickle                 | 14.3 us                                                      | 13.4 us: 1.07x faster                                                  |
| telco                    | 7.82 ms                                                      | 7.39 ms: 1.06x faster                                                  |
| json                     | 4.93 ms                                                      | 4.74 ms: 1.04x faster                                                  |
| thrift                   | 778 us                                                       | 749 us: 1.04x faster                                                   |
| pathlib                  | 19.2 ms                                                      | 18.5 ms: 1.04x faster                                                  |
| pprint_safe_repr         | 738 ms                                                       | 713 ms: 1.03x faster                                                   |
| pickle_dict              | 32.5 us                                                      | 31.6 us: 1.03x faster                                                  |
| coroutines               | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                                  |
| async_generators         | 377 ms                                                       | 368 ms: 1.02x faster                                                   |
| bpe_tokeniser            | 4.45 sec                                                     | 4.34 sec: 1.02x faster                                                 |
| 2to3                     | 260 ms                                                       | 254 ms: 1.02x faster                                                   |
| scimark_fft              | 349 ms                                                       | 342 ms: 1.02x faster                                                   |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 4.62 ms: 1.02x faster                                                  |
| coverage                 | 83.0 ms                                                      | 81.7 ms: 1.02x faster                                                  |
| sympy_sum                | 156 ms                                                       | 153 ms: 1.02x faster                                                   |
| generators               | 28.8 ms                                                      | 28.4 ms: 1.01x faster                                                  |
| sqlite_synth             | 2.21 us                                                      | 2.18 us: 1.01x faster                                                  |
| pprint_pformat           | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                 |
| html5lib                 | 67.0 ms                                                      | 66.4 ms: 1.01x faster                                                  |
| sympy_str                | 275 ms                                                       | 272 ms: 1.01x faster                                                   |
| meteor_contest           | 102 ms                                                       | 101 ms: 1.01x faster                                                   |
| crypto_pyaes             | 67.9 ms                                                      | 67.7 ms: 1.00x faster                                                  |
| mdp                      | 2.36 sec                                                     | 2.36 sec: 1.00x slower                                                 |
| python_startup_no_site   | 7.39 ms                                                      | 7.43 ms: 1.00x slower                                                  |
| richards_super           | 51.6 ms                                                      | 51.9 ms: 1.01x slower                                                  |
| scimark_sor              | 134 ms                                                       | 135 ms: 1.01x slower                                                   |
| python_startup           | 11.0 ms                                                      | 11.1 ms: 1.01x slower                                                  |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                 |
| xml_etree_iterparse      | 94.9 ms                                                      | 95.6 ms: 1.01x slower                                                  |
| hexiom                   | 5.99 ms                                                      | 6.03 ms: 1.01x slower                                                  |
| scimark_monte_carlo      | 65.4 ms                                                      | 65.9 ms: 1.01x slower                                                  |
| pyflate                  | 449 ms                                                       | 452 ms: 1.01x slower                                                   |
| dulwich_log              | 74.8 ms                                                      | 75.6 ms: 1.01x slower                                                  |
| logging_simple           | 6.16 us                                                      | 6.23 us: 1.01x slower                                                  |
| typing_runtime_protocols | 155 us                                                       | 156 us: 1.01x slower                                                   |
| create_gc_cycles         | 1.34 ms                                                      | 1.36 ms: 1.01x slower                                                  |
| regex_dna                | 180 ms                                                       | 183 ms: 1.01x slower                                                   |
| regex_effbot             | 3.08 ms                                                      | 3.13 ms: 1.01x slower                                                  |
| logging_format           | 6.84 us                                                      | 6.95 us: 1.02x slower                                                  |
| float                    | 77.5 ms                                                      | 78.7 ms: 1.02x slower                                                  |
| nqueens                  | 78.6 ms                                                      | 79.9 ms: 1.02x slower                                                  |
| scimark_lu               | 113 ms                                                       | 115 ms: 1.02x slower                                                   |
| richards                 | 45.2 ms                                                      | 46.1 ms: 1.02x slower                                                  |
| sqlglot_normalize        | 106 ms                                                       | 108 ms: 1.02x slower                                                   |
| sqlglot_transpile        | 1.56 ms                                                      | 1.60 ms: 1.02x slower                                                  |
| genshi_xml               | 48.8 ms                                                      | 49.9 ms: 1.02x slower                                                  |
| fannkuch                 | 370 ms                                                       | 379 ms: 1.02x slower                                                   |
| logging_silent           | 103 ns                                                       | 105 ns: 1.03x slower                                                   |
| pycparser                | 1.12 sec                                                     | 1.15 sec: 1.03x slower                                                 |
| sqlglot_optimize         | 52.7 ms                                                      | 54.2 ms: 1.03x slower                                                  |
| gc_traversal             | 3.14 ms                                                      | 3.23 ms: 1.03x slower                                                  |
| mako                     | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| django_template          | 34.1 ms                                                      | 35.3 ms: 1.03x slower                                                  |
| pidigits                 | 217 ms                                                       | 224 ms: 1.04x slower                                                   |
| pickle_list              | 4.93 us                                                      | 5.10 us: 1.04x slower                                                  |
| sqlglot_parse            | 1.25 ms                                                      | 1.29 ms: 1.04x slower                                                  |
| genshi_text              | 21.5 ms                                                      | 22.3 ms: 1.04x slower                                                  |
| chaos                    | 57.3 ms                                                      | 59.7 ms: 1.04x slower                                                  |
| raytrace                 | 253 ms                                                       | 263 ms: 1.04x slower                                                   |
| spectral_norm            | 111 ms                                                       | 116 ms: 1.04x slower                                                   |
| deltablue                | 3.12 ms                                                      | 3.27 ms: 1.05x slower                                                  |
| unpickle_pure_python     | 210 us                                                       | 220 us: 1.05x slower                                                   |
| tomli_loads              | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                                 |
| comprehensions           | 16.5 us                                                      | 17.3 us: 1.05x slower                                                  |
| regex_v8                 | 22.7 ms                                                      | 24.1 ms: 1.06x slower                                                  |
| json_dumps               | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                  |
| pickle_pure_python       | 294 us                                                       | 321 us: 1.09x slower                                                   |
| pickle                   | 11.3 us                                                      | 12.4 us: 1.10x slower                                                  |
| bench_thread_pool        | 919 us                                                       | 1.02 ms: 1.11x slower                                                  |
| nbody                    | 85.1 ms                                                      | 95.4 ms: 1.12x slower                                                  |
| bench_mp_pool            | 11.0 ms                                                      | 63.7 ms: 5.79x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (11): regex_compile, xml_etree_parse, docutils, sympy_integrate, asyncio_tcp, unpickle_list, asyncio_websockets, xml_etree_generate, pylint, xml_etree_process, sympy_expand
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 95.40% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x