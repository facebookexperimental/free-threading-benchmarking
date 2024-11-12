# Results vs. 3.13.0rc2

- fork: Eclips4
- ref: ft_specialize_unpack
- machine: linux-x86_64
- commit hash: d49e9e6
- commit date: 2024-11-08
- overall geometric mean: 1.02x slower
- HPT reliability: 77.18%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                    |
| html5lib       | 67.0 ms                                                      | 66.2 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                            |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_generators | 377 ms                                                       | 366 ms: 1.03x faster                                                    |
| coroutines       | 23.6 ms                                                      | 23.3 ms: 1.01x faster                                                   |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                  |
| Geometric mean   | (ref)                                                        | 1.01x faster                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 78.1 ms: 1.01x slower                                                   |
| pidigits       | 217 ms                                                       | 224 ms: 1.03x slower                                                    |
| nbody          | 85.1 ms                                                      | 93.8 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                        | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 129 ms: 1.03x faster                                                    |
| regex_dna      | 180 ms                                                       | 183 ms: 1.02x slower                                                    |
| regex_v8       | 22.7 ms                                                      | 23.6 ms: 1.04x slower                                                   |
| regex_effbot   | 3.08 ms                                                      | 3.35 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                        | 1.03x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 26.0 us: 1.04x faster                                                   |
| unpickle             | 14.3 us                                                      | 14.0 us: 1.02x faster                                                   |
| pickle_dict          | 32.5 us                                                      | 32.2 us: 1.01x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 85.9 ms: 1.01x slower                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 95.9 ms: 1.01x slower                                                   |
| unpickle_pure_python | 210 us                                                       | 214 us: 1.02x slower                                                    |
| pickle_list          | 4.93 us                                                      | 5.08 us: 1.03x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                                  |
| unpickle_list        | 4.71 us                                                      | 4.99 us: 1.06x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 317 us: 1.08x slower                                                    |
| json_dumps           | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                   |
| pickle               | 11.3 us                                                      | 12.6 us: 1.11x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.03x slower                                                            |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                      | 11.1 ms: 1.01x slower                                                   |
| python_startup_no_site | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 34.9 ms: 1.02x slower                                                   |
| genshi_xml      | 48.8 ms                                                      | 50.2 ms: 1.03x slower                                                   |
| genshi_text     | 21.5 ms                                                      | 22.3 ms: 1.03x slower                                                   |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                            |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|--------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| deepcopy                 | 355 us                                                       | 262 us: 1.36x faster                                                    |
| deepcopy_memo            | 39.1 us                                                      | 29.9 us: 1.31x faster                                                   |
| deepcopy_reduce          | 3.11 us                                                      | 2.61 us: 1.19x faster                                                   |
| go                       | 141 ms                                                       | 121 ms: 1.16x faster                                                    |
| pathlib                  | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                   |
| telco                    | 7.82 ms                                                      | 7.43 ms: 1.05x faster                                                   |
| pprint_safe_repr         | 738 ms                                                       | 704 ms: 1.05x faster                                                    |
| thrift                   | 778 us                                                       | 747 us: 1.04x faster                                                    |
| json_loads               | 27.0 us                                                      | 26.0 us: 1.04x faster                                                   |
| scimark_fft              | 349 ms                                                       | 338 ms: 1.03x faster                                                    |
| async_generators         | 377 ms                                                       | 366 ms: 1.03x faster                                                    |
| pprint_pformat           | 1.50 sec                                                     | 1.46 sec: 1.03x faster                                                  |
| regex_compile            | 132 ms                                                       | 129 ms: 1.03x faster                                                    |
| 2to3                     | 260 ms                                                       | 254 ms: 1.02x faster                                                    |
| bpe_tokeniser            | 4.45 sec                                                     | 4.35 sec: 1.02x faster                                                  |
| unpickle                 | 14.3 us                                                      | 14.0 us: 1.02x faster                                                   |
| coverage                 | 83.0 ms                                                      | 81.3 ms: 1.02x faster                                                   |
| logging_simple           | 6.16 us                                                      | 6.04 us: 1.02x faster                                                   |
| crypto_pyaes             | 67.9 ms                                                      | 66.9 ms: 1.01x faster                                                   |
| html5lib                 | 67.0 ms                                                      | 66.2 ms: 1.01x faster                                                   |
| scimark_sor              | 134 ms                                                       | 133 ms: 1.01x faster                                                    |
| logging_format           | 6.84 us                                                      | 6.77 us: 1.01x faster                                                   |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 4.66 ms: 1.01x faster                                                   |
| sympy_sum                | 156 ms                                                       | 154 ms: 1.01x faster                                                    |
| meteor_contest           | 102 ms                                                       | 101 ms: 1.01x faster                                                    |
| coroutines               | 23.6 ms                                                      | 23.3 ms: 1.01x faster                                                   |
| pickle_dict              | 32.5 us                                                      | 32.2 us: 1.01x faster                                                   |
| sympy_str                | 275 ms                                                       | 272 ms: 1.01x faster                                                    |
| pyflate                  | 449 ms                                                       | 445 ms: 1.01x faster                                                    |
| scimark_monte_carlo      | 65.4 ms                                                      | 65.0 ms: 1.01x faster                                                   |
| hexiom                   | 5.99 ms                                                      | 5.97 ms: 1.00x faster                                                   |
| sympy_integrate          | 19.8 ms                                                      | 19.9 ms: 1.00x slower                                                   |
| xml_etree_generate       | 85.4 ms                                                      | 85.9 ms: 1.01x slower                                                   |
| sqlglot_normalize        | 106 ms                                                       | 106 ms: 1.01x slower                                                    |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                  |
| richards                 | 45.2 ms                                                      | 45.6 ms: 1.01x slower                                                   |
| float                    | 77.5 ms                                                      | 78.1 ms: 1.01x slower                                                   |
| dulwich_log              | 74.8 ms                                                      | 75.5 ms: 1.01x slower                                                   |
| xml_etree_iterparse      | 94.9 ms                                                      | 95.9 ms: 1.01x slower                                                   |
| python_startup           | 11.0 ms                                                      | 11.1 ms: 1.01x slower                                                   |
| python_startup_no_site   | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                                   |
| sqlglot_transpile        | 1.56 ms                                                      | 1.58 ms: 1.01x slower                                                   |
| pycparser                | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                  |
| sqlite_synth             | 2.21 us                                                      | 2.24 us: 1.01x slower                                                   |
| spectral_norm            | 111 ms                                                       | 113 ms: 1.02x slower                                                    |
| regex_dna                | 180 ms                                                       | 183 ms: 1.02x slower                                                    |
| unpack_sequence          | 44.8 ns                                                      | 45.5 ns: 1.02x slower                                                   |
| chaos                    | 57.3 ms                                                      | 58.3 ms: 1.02x slower                                                   |
| typing_runtime_protocols | 155 us                                                       | 157 us: 1.02x slower                                                    |
| generators               | 28.8 ms                                                      | 29.3 ms: 1.02x slower                                                   |
| unpickle_pure_python     | 210 us                                                       | 214 us: 1.02x slower                                                    |
| sqlglot_optimize         | 52.7 ms                                                      | 53.7 ms: 1.02x slower                                                   |
| create_gc_cycles         | 1.34 ms                                                      | 1.36 ms: 1.02x slower                                                   |
| scimark_lu               | 113 ms                                                       | 115 ms: 1.02x slower                                                    |
| fannkuch                 | 370 ms                                                       | 377 ms: 1.02x slower                                                    |
| raytrace                 | 253 ms                                                       | 259 ms: 1.02x slower                                                    |
| django_template          | 34.1 ms                                                      | 34.9 ms: 1.02x slower                                                   |
| sqlglot_parse            | 1.25 ms                                                      | 1.28 ms: 1.03x slower                                                   |
| deltablue                | 3.12 ms                                                      | 3.21 ms: 1.03x slower                                                   |
| genshi_xml               | 48.8 ms                                                      | 50.2 ms: 1.03x slower                                                   |
| pickle_list              | 4.93 us                                                      | 5.08 us: 1.03x slower                                                   |
| pidigits                 | 217 ms                                                       | 224 ms: 1.03x slower                                                    |
| genshi_text              | 21.5 ms                                                      | 22.3 ms: 1.03x slower                                                   |
| gc_traversal             | 3.14 ms                                                      | 3.25 ms: 1.03x slower                                                   |
| mako                     | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                   |
| regex_v8                 | 22.7 ms                                                      | 23.6 ms: 1.04x slower                                                   |
| comprehensions           | 16.5 us                                                      | 17.2 us: 1.04x slower                                                   |
| tomli_loads              | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                                  |
| unpickle_list            | 4.71 us                                                      | 4.99 us: 1.06x slower                                                   |
| pickle_pure_python       | 294 us                                                       | 317 us: 1.08x slower                                                    |
| regex_effbot             | 3.08 ms                                                      | 3.35 ms: 1.09x slower                                                   |
| json_dumps               | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                   |
| nbody                    | 85.1 ms                                                      | 93.8 ms: 1.10x slower                                                   |
| bench_thread_pool        | 919 us                                                       | 1.02 ms: 1.11x slower                                                   |
| pickle                   | 11.3 us                                                      | 12.6 us: 1.11x slower                                                   |
| bench_mp_pool            | 11.0 ms                                                      | 64.2 ms: 5.84x slower                                                   |
| Geometric mean           | (ref)                                                        | 1.02x slower                                                            |

Benchmark hidden because not significant (12): json, richards_super, docutils, mdp, pylint, nqueens, asyncio_websockets, asyncio_tcp, xml_etree_parse, xml_etree_process, sympy_expand, logging_silent
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 77.18% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x