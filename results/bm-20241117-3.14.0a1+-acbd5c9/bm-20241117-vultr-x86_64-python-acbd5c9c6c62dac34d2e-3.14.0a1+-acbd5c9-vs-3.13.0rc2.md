# Results vs. 3.13.0rc2

- fork: python
- ref: acbd5c9c6c62dac34d2e
- machine: linux-x86_64
- commit hash: acbd5c9
- commit date: 2024-11-17
- overall geometric mean: 1.02x slower
- HPT reliability: 70.14%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                   |
| html5lib       | 67.0 ms                                                      | 64.9 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| coroutines      | 23.6 ms                                                      | 22.5 ms: 1.05x faster                                                  |
| asyncio_tcp_ssl | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (3): async_generators, asyncio_websockets, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                   |
| float          | 77.5 ms                                                      | 79.0 ms: 1.02x slower                                                  |
| nbody          | 85.1 ms                                                      | 93.3 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 23.0 ms: 1.01x slower                                                  |
| regex_effbot   | 3.08 ms                                                      | 3.27 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 25.0 us: 1.08x faster                                                  |
| unpickle             | 14.3 us                                                      | 13.3 us: 1.07x faster                                                  |
| pickle_dict          | 32.5 us                                                      | 31.2 us: 1.04x faster                                                  |
| unpickle_list        | 4.71 us                                                      | 4.66 us: 1.01x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 95.4 ms: 1.01x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 59.8 ms: 1.01x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 86.6 ms: 1.01x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 215 us: 1.02x slower                                                   |
| pickle_list          | 4.93 us                                                      | 5.10 us: 1.03x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.10 sec: 1.05x slower                                                 |
| pickle               | 11.3 us                                                      | 12.1 us: 1.07x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 319 us: 1.08x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                      | 11.0 ms: 1.01x slower                                                  |
| python_startup_no_site | 7.39 ms                                                      | 7.44 ms: 1.01x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.01x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 22.3 ms: 1.04x slower                                                  |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 50.9 ms: 1.04x slower                                                  |
| django_template | 34.1 ms                                                      | 36.1 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                 | 355 us                                                       | 261 us: 1.36x faster                                                   |
| deepcopy_memo            | 39.1 us                                                      | 29.8 us: 1.31x faster                                                  |
| pidigits                 | 217 ms                                                       | 185 ms: 1.17x faster                                                   |
| go                       | 141 ms                                                       | 121 ms: 1.17x faster                                                   |
| deepcopy_reduce          | 3.11 us                                                      | 2.73 us: 1.14x faster                                                  |
| json_loads               | 27.0 us                                                      | 25.0 us: 1.08x faster                                                  |
| unpickle                 | 14.3 us                                                      | 13.3 us: 1.07x faster                                                  |
| telco                    | 7.82 ms                                                      | 7.30 ms: 1.07x faster                                                  |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 4.39 ms: 1.07x faster                                                  |
| json                     | 4.93 ms                                                      | 4.67 ms: 1.05x faster                                                  |
| coroutines               | 23.6 ms                                                      | 22.5 ms: 1.05x faster                                                  |
| pathlib                  | 19.2 ms                                                      | 18.4 ms: 1.04x faster                                                  |
| pickle_dict              | 32.5 us                                                      | 31.2 us: 1.04x faster                                                  |
| thrift                   | 778 us                                                       | 749 us: 1.04x faster                                                   |
| html5lib                 | 67.0 ms                                                      | 64.9 ms: 1.03x faster                                                  |
| pprint_safe_repr         | 738 ms                                                       | 716 ms: 1.03x faster                                                   |
| bpe_tokeniser            | 4.45 sec                                                     | 4.32 sec: 1.03x faster                                                 |
| scimark_fft              | 349 ms                                                       | 340 ms: 1.03x faster                                                   |
| 2to3                     | 260 ms                                                       | 254 ms: 1.02x faster                                                   |
| coverage                 | 83.0 ms                                                      | 81.2 ms: 1.02x faster                                                  |
| unpack_sequence          | 44.8 ns                                                      | 43.9 ns: 1.02x faster                                                  |
| crypto_pyaes             | 67.9 ms                                                      | 66.6 ms: 1.02x faster                                                  |
| meteor_contest           | 102 ms                                                       | 99.9 ms: 1.02x faster                                                  |
| sympy_sum                | 156 ms                                                       | 153 ms: 1.02x faster                                                   |
| hexiom                   | 5.99 ms                                                      | 5.92 ms: 1.01x faster                                                  |
| pprint_pformat           | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                 |
| unpickle_list            | 4.71 us                                                      | 4.66 us: 1.01x faster                                                  |
| scimark_monte_carlo      | 65.4 ms                                                      | 64.8 ms: 1.01x faster                                                  |
| pyflate                  | 449 ms                                                       | 445 ms: 1.01x faster                                                   |
| sympy_integrate          | 19.8 ms                                                      | 19.9 ms: 1.00x slower                                                  |
| python_startup           | 11.0 ms                                                      | 11.0 ms: 1.01x slower                                                  |
| xml_etree_iterparse      | 94.9 ms                                                      | 95.4 ms: 1.01x slower                                                  |
| scimark_sor              | 134 ms                                                       | 135 ms: 1.01x slower                                                   |
| python_startup_no_site   | 7.39 ms                                                      | 7.44 ms: 1.01x slower                                                  |
| sqlglot_normalize        | 106 ms                                                       | 106 ms: 1.01x slower                                                   |
| xml_etree_process        | 59.3 ms                                                      | 59.8 ms: 1.01x slower                                                  |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                 |
| sqlite_synth             | 2.21 us                                                      | 2.23 us: 1.01x slower                                                  |
| richards                 | 45.2 ms                                                      | 45.7 ms: 1.01x slower                                                  |
| regex_dna                | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| sympy_expand             | 457 ms                                                       | 463 ms: 1.01x slower                                                   |
| scimark_lu               | 113 ms                                                       | 114 ms: 1.01x slower                                                   |
| xml_etree_generate       | 85.4 ms                                                      | 86.6 ms: 1.01x slower                                                  |
| regex_v8                 | 22.7 ms                                                      | 23.0 ms: 1.01x slower                                                  |
| fannkuch                 | 370 ms                                                       | 375 ms: 1.02x slower                                                   |
| dulwich_log              | 74.8 ms                                                      | 76.0 ms: 1.02x slower                                                  |
| create_gc_cycles         | 1.34 ms                                                      | 1.36 ms: 1.02x slower                                                  |
| pycparser                | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                 |
| nqueens                  | 78.6 ms                                                      | 80.0 ms: 1.02x slower                                                  |
| float                    | 77.5 ms                                                      | 79.0 ms: 1.02x slower                                                  |
| sqlglot_optimize         | 52.7 ms                                                      | 53.8 ms: 1.02x slower                                                  |
| unpickle_pure_python     | 210 us                                                       | 215 us: 1.02x slower                                                   |
| deltablue                | 3.12 ms                                                      | 3.20 ms: 1.02x slower                                                  |
| typing_runtime_protocols | 155 us                                                       | 159 us: 1.03x slower                                                   |
| sqlglot_transpile        | 1.56 ms                                                      | 1.60 ms: 1.03x slower                                                  |
| chaos                    | 57.3 ms                                                      | 58.9 ms: 1.03x slower                                                  |
| raytrace                 | 253 ms                                                       | 260 ms: 1.03x slower                                                   |
| comprehensions           | 16.5 us                                                      | 17.0 us: 1.03x slower                                                  |
| pickle_list              | 4.93 us                                                      | 5.10 us: 1.03x slower                                                  |
| genshi_text              | 21.5 ms                                                      | 22.3 ms: 1.04x slower                                                  |
| mako                     | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                  |
| genshi_xml               | 48.8 ms                                                      | 50.9 ms: 1.04x slower                                                  |
| sqlglot_parse            | 1.25 ms                                                      | 1.30 ms: 1.04x slower                                                  |
| tomli_loads              | 2.01 sec                                                     | 2.10 sec: 1.05x slower                                                 |
| django_template          | 34.1 ms                                                      | 36.1 ms: 1.06x slower                                                  |
| regex_effbot             | 3.08 ms                                                      | 3.27 ms: 1.06x slower                                                  |
| pickle                   | 11.3 us                                                      | 12.1 us: 1.07x slower                                                  |
| pickle_pure_python       | 294 us                                                       | 319 us: 1.08x slower                                                   |
| nbody                    | 85.1 ms                                                      | 93.3 ms: 1.10x slower                                                  |
| json_dumps               | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                  |
| bench_thread_pool        | 919 us                                                       | 1.02 ms: 1.11x slower                                                  |
| gc_traversal             | 3.14 ms                                                      | 3.71 ms: 1.18x slower                                                  |
| bench_mp_pool            | 11.0 ms                                                      | 63.7 ms: 5.80x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (15): regex_compile, sympy_str, async_generators, docutils, mdp, generators, xml_etree_parse, spectral_norm, richards_super, asyncio_websockets, logging_silent, pylint, asyncio_tcp, logging_format, logging_simple
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 70.14% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x