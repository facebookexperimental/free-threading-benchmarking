# Results vs. 3.13.0rc2

- fork: python
- ref: 2a6b6b33dfe0f3c435ab
- machine: linux-x86_64
- commit hash: 2a6b6b3
- commit date: 2024-11-06
- overall geometric mean: 1.01x slower
- HPT reliability: 76.03%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.75 sec: 1.07x faster                                                 |
| html5lib       | 92.6 ms                                                      | 87.9 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|--------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp        | 948 ms                                                       | 884 ms: 1.07x faster                                                   |
| asyncio_websockets | 766 ms                                                       | 743 ms: 1.03x faster                                                   |
| Geometric mean     | (ref)                                                        | 1.00x faster                                                           |

Benchmark hidden because not significant (3): asyncio_tcp_ssl, async_generators, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 119 ms                                                       | 134 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                        | 1.04x slower                                                           |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 169 ms: 1.07x faster                                                   |
| regex_effbot   | 4.74 ms                                                      | 5.05 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|--------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle_list      | 6.68 us                                                      | 6.91 us: 1.04x slower                                                  |
| json_loads         | 34.3 us                                                      | 37.8 us: 1.10x slower                                                  |
| pickle_pure_python | 416 us                                                       | 463 us: 1.11x slower                                                   |
| json_dumps         | 14.1 ms                                                      | 15.9 ms: 1.12x slower                                                  |
| Geometric mean     | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (10): xml_etree_iterparse, pickle_dict, tomli_loads, unpickle, xml_etree_generate, xml_etree_process, unpickle_pure_python, xml_etree_parse, pickle_list, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 20.1 ms: 1.11x faster                                                  |
| python_startup_no_site | 15.3 ms                                                      | 13.9 ms: 1.10x faster                                                  |
| Geometric mean         | (ref)                                                        | 1.11x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.3 ms                                                      | 48.7 ms: 1.10x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (3): genshi_xml, mako, genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                 | 498 us                                                       | 373 us: 1.33x faster                                                   |
| unpack_sequence          | 74.3 ns                                                      | 61.6 ns: 1.21x faster                                                  |
| deepcopy_memo            | 50.1 us                                                      | 42.9 us: 1.17x faster                                                  |
| go                       | 191 ms                                                       | 165 ms: 1.16x faster                                                   |
| telco                    | 12.2 ms                                                      | 10.7 ms: 1.14x faster                                                  |
| python_startup           | 22.4 ms                                                      | 20.1 ms: 1.11x faster                                                  |
| python_startup_no_site   | 15.3 ms                                                      | 13.9 ms: 1.10x faster                                                  |
| mdp                      | 3.80 sec                                                     | 3.45 sec: 1.10x faster                                                 |
| deepcopy_reduce          | 4.10 us                                                      | 3.77 us: 1.09x faster                                                  |
| bpe_tokeniser            | 6.28 sec                                                     | 5.84 sec: 1.08x faster                                                 |
| regex_compile            | 182 ms                                                       | 169 ms: 1.07x faster                                                   |
| asyncio_tcp              | 948 ms                                                       | 884 ms: 1.07x faster                                                   |
| docutils                 | 4.01 sec                                                     | 3.75 sec: 1.07x faster                                                 |
| typing_runtime_protocols | 226 us                                                       | 212 us: 1.06x faster                                                   |
| logging_simple           | 8.56 us                                                      | 8.09 us: 1.06x faster                                                  |
| html5lib                 | 92.6 ms                                                      | 87.9 ms: 1.05x faster                                                  |
| generators               | 40.0 ms                                                      | 38.5 ms: 1.04x faster                                                  |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 6.51 ms: 1.04x faster                                                  |
| asyncio_websockets       | 766 ms                                                       | 743 ms: 1.03x faster                                                   |
| pyflate                  | 664 ms                                                       | 649 ms: 1.02x faster                                                   |
| unpickle_list            | 6.68 us                                                      | 6.91 us: 1.04x slower                                                  |
| sqlglot_normalize        | 140 ms                                                       | 146 ms: 1.04x slower                                                   |
| hexiom                   | 8.11 ms                                                      | 8.46 ms: 1.04x slower                                                  |
| deltablue                | 4.44 ms                                                      | 4.64 ms: 1.05x slower                                                  |
| scimark_fft              | 473 ms                                                       | 498 ms: 1.05x slower                                                   |
| scimark_lu               | 146 ms                                                       | 156 ms: 1.06x slower                                                   |
| regex_effbot             | 4.74 ms                                                      | 5.05 ms: 1.07x slower                                                  |
| richards                 | 65.5 ms                                                      | 70.1 ms: 1.07x slower                                                  |
| comprehensions           | 22.2 us                                                      | 23.8 us: 1.07x slower                                                  |
| logging_silent           | 130 ns                                                       | 140 ns: 1.08x slower                                                   |
| thrift                   | 1.10 ms                                                      | 1.19 ms: 1.08x slower                                                  |
| django_template          | 44.3 ms                                                      | 48.7 ms: 1.10x slower                                                  |
| sqlglot_transpile        | 2.20 ms                                                      | 2.42 ms: 1.10x slower                                                  |
| json_loads               | 34.3 us                                                      | 37.8 us: 1.10x slower                                                  |
| pickle_pure_python       | 416 us                                                       | 463 us: 1.11x slower                                                   |
| json_dumps               | 14.1 ms                                                      | 15.9 ms: 1.12x slower                                                  |
| nbody                    | 119 ms                                                       | 134 ms: 1.13x slower                                                   |
| logging_format           | 9.24 us                                                      | 10.8 us: 1.17x slower                                                  |
| bench_mp_pool            | 18.7 ms                                                      | 67.7 ms: 3.62x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (49): genshi_xml, pathlib, xml_etree_iterparse, bench_thread_pool, 2to3, scimark_monte_carlo, pickle_dict, sqlite_synth, mako, pidigits, sympy_str, pylint, gc_traversal, sympy_integrate, meteor_contest, regex_v8, fannkuch, sympy_sum, tomli_loads, richards_super, unpickle, genshi_text, sqlglot_optimize, spectral_norm, asyncio_tcp_ssl, pprint_safe_repr, sympy_expand, xml_etree_generate, xml_etree_process, pprint_pformat, float, unpickle_pure_python, xml_etree_parse, pickle_list, pycparser, nqueens, chaos, pickle, dulwich_log, regex_dna, scimark_sor, async_generators, create_gc_cycles, json, raytrace, coverage, crypto_pyaes, coroutines, sqlglot_parse
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 76.03% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x