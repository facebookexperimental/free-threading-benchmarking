# Results vs. 3.13.0rc2

- fork: python
- ref: 2a6b6b33dfe0f3c435ab
- machine: linux-x86_64
- commit hash: 2a6b6b3
- commit date: 2024-11-06
- overall geometric mean: 1.02x slower
- HPT reliability: 99.77%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                   |
| html5lib       | 67.0 ms                                                      | 66.5 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_generators | 377 ms                                                       | 373 ms: 1.01x faster                                                   |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                 |
| Geometric mean   | (ref)                                                        | 1.00x faster                                                           |

Benchmark hidden because not significant (3): coroutines, asyncio_websockets, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 222 ms: 1.02x slower                                                   |
| float          | 77.5 ms                                                      | 79.7 ms: 1.03x slower                                                  |
| nbody          | 85.1 ms                                                      | 95.6 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                       | 184 ms: 1.02x slower                                                   |
| regex_effbot   | 3.08 ms                                                      | 3.18 ms: 1.03x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 24.6 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle             | 14.3 us                                                      | 13.3 us: 1.08x faster                                                  |
| json_loads           | 27.0 us                                                      | 25.7 us: 1.05x faster                                                  |
| unpickle_list        | 4.71 us                                                      | 4.68 us: 1.01x faster                                                  |
| pickle               | 11.3 us                                                      | 11.3 us: 1.01x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 135 ms: 1.01x faster                                                   |
| pickle_list          | 4.93 us                                                      | 4.90 us: 1.01x faster                                                  |
| pickle_dict          | 32.5 us                                                      | 32.8 us: 1.01x slower                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 95.9 ms: 1.01x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 217 us: 1.03x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.10 sec: 1.05x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 317 us: 1.08x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_generate, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                      | 11.0 ms: 1.00x slower                                                  |
| python_startup_no_site | 7.39 ms                                                      | 7.41 ms: 1.00x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.00x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 35.2 ms: 1.03x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 50.9 ms: 1.04x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 22.6 ms: 1.05x slower                                                  |
| mako            | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.05x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                 | 355 us                                                       | 265 us: 1.34x faster                                                   |
| deepcopy_memo            | 39.1 us                                                      | 30.0 us: 1.30x faster                                                  |
| go                       | 141 ms                                                       | 122 ms: 1.15x faster                                                   |
| deepcopy_reduce          | 3.11 us                                                      | 2.72 us: 1.15x faster                                                  |
| unpickle                 | 14.3 us                                                      | 13.3 us: 1.08x faster                                                  |
| pathlib                  | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                  |
| telco                    | 7.82 ms                                                      | 7.44 ms: 1.05x faster                                                  |
| json_loads               | 27.0 us                                                      | 25.7 us: 1.05x faster                                                  |
| thrift                   | 778 us                                                       | 750 us: 1.04x faster                                                   |
| pprint_safe_repr         | 738 ms                                                       | 717 ms: 1.03x faster                                                   |
| 2to3                     | 260 ms                                                       | 254 ms: 1.02x faster                                                   |
| coverage                 | 83.0 ms                                                      | 81.1 ms: 1.02x faster                                                  |
| bpe_tokeniser            | 4.45 sec                                                     | 4.35 sec: 1.02x faster                                                 |
| sympy_sum                | 156 ms                                                       | 153 ms: 1.02x faster                                                   |
| pprint_pformat           | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                 |
| async_generators         | 377 ms                                                       | 373 ms: 1.01x faster                                                   |
| scimark_fft              | 349 ms                                                       | 345 ms: 1.01x faster                                                   |
| meteor_contest           | 102 ms                                                       | 100 ms: 1.01x faster                                                   |
| json                     | 4.93 ms                                                      | 4.88 ms: 1.01x faster                                                  |
| html5lib                 | 67.0 ms                                                      | 66.5 ms: 1.01x faster                                                  |
| sqlite_synth             | 2.21 us                                                      | 2.19 us: 1.01x faster                                                  |
| unpickle_list            | 4.71 us                                                      | 4.68 us: 1.01x faster                                                  |
| pickle                   | 11.3 us                                                      | 11.3 us: 1.01x faster                                                  |
| xml_etree_parse          | 136 ms                                                       | 135 ms: 1.01x faster                                                   |
| pickle_list              | 4.93 us                                                      | 4.90 us: 1.01x faster                                                  |
| python_startup           | 11.0 ms                                                      | 11.0 ms: 1.00x slower                                                  |
| python_startup_no_site   | 7.39 ms                                                      | 7.41 ms: 1.00x slower                                                  |
| mdp                      | 2.36 sec                                                     | 2.37 sec: 1.01x slower                                                 |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                 |
| pickle_dict              | 32.5 us                                                      | 32.8 us: 1.01x slower                                                  |
| nqueens                  | 78.6 ms                                                      | 79.3 ms: 1.01x slower                                                  |
| sympy_integrate          | 19.8 ms                                                      | 20.0 ms: 1.01x slower                                                  |
| logging_format           | 6.84 us                                                      | 6.91 us: 1.01x slower                                                  |
| sympy_expand             | 457 ms                                                       | 461 ms: 1.01x slower                                                   |
| logging_simple           | 6.16 us                                                      | 6.22 us: 1.01x slower                                                  |
| xml_etree_iterparse      | 94.9 ms                                                      | 95.9 ms: 1.01x slower                                                  |
| hexiom                   | 5.99 ms                                                      | 6.07 ms: 1.01x slower                                                  |
| create_gc_cycles         | 1.34 ms                                                      | 1.35 ms: 1.01x slower                                                  |
| dulwich_log              | 74.8 ms                                                      | 75.8 ms: 1.01x slower                                                  |
| richards_super           | 51.6 ms                                                      | 52.3 ms: 1.01x slower                                                  |
| sqlglot_normalize        | 106 ms                                                       | 107 ms: 1.01x slower                                                   |
| scimark_sor              | 134 ms                                                       | 136 ms: 1.01x slower                                                   |
| fannkuch                 | 370 ms                                                       | 377 ms: 1.02x slower                                                   |
| pycparser                | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                 |
| sqlglot_optimize         | 52.7 ms                                                      | 53.8 ms: 1.02x slower                                                  |
| regex_dna                | 180 ms                                                       | 184 ms: 1.02x slower                                                   |
| pidigits                 | 217 ms                                                       | 222 ms: 1.02x slower                                                   |
| spectral_norm            | 111 ms                                                       | 114 ms: 1.03x slower                                                   |
| float                    | 77.5 ms                                                      | 79.7 ms: 1.03x slower                                                  |
| scimark_lu               | 113 ms                                                       | 116 ms: 1.03x slower                                                   |
| django_template          | 34.1 ms                                                      | 35.2 ms: 1.03x slower                                                  |
| sqlglot_transpile        | 1.56 ms                                                      | 1.61 ms: 1.03x slower                                                  |
| typing_runtime_protocols | 155 us                                                       | 159 us: 1.03x slower                                                   |
| regex_effbot             | 3.08 ms                                                      | 3.18 ms: 1.03x slower                                                  |
| gc_traversal             | 3.14 ms                                                      | 3.24 ms: 1.03x slower                                                  |
| logging_silent           | 103 ns                                                       | 106 ns: 1.03x slower                                                   |
| unpickle_pure_python     | 210 us                                                       | 217 us: 1.03x slower                                                   |
| chaos                    | 57.3 ms                                                      | 59.3 ms: 1.04x slower                                                  |
| richards                 | 45.2 ms                                                      | 47.0 ms: 1.04x slower                                                  |
| genshi_xml               | 48.8 ms                                                      | 50.9 ms: 1.04x slower                                                  |
| comprehensions           | 16.5 us                                                      | 17.2 us: 1.05x slower                                                  |
| tomli_loads              | 2.01 sec                                                     | 2.10 sec: 1.05x slower                                                 |
| genshi_text              | 21.5 ms                                                      | 22.6 ms: 1.05x slower                                                  |
| sqlglot_parse            | 1.25 ms                                                      | 1.31 ms: 1.05x slower                                                  |
| deltablue                | 3.12 ms                                                      | 3.28 ms: 1.05x slower                                                  |
| raytrace                 | 253 ms                                                       | 266 ms: 1.05x slower                                                   |
| mako                     | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                  |
| pickle_pure_python       | 294 us                                                       | 317 us: 1.08x slower                                                   |
| regex_v8                 | 22.7 ms                                                      | 24.6 ms: 1.08x slower                                                  |
| bench_thread_pool        | 919 us                                                       | 1.01 ms: 1.10x slower                                                  |
| json_dumps               | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                  |
| nbody                    | 85.1 ms                                                      | 95.6 ms: 1.12x slower                                                  |
| unpack_sequence          | 44.8 ns                                                      | 51.6 ns: 1.15x slower                                                  |
| bench_mp_pool            | 11.0 ms                                                      | 63.5 ms: 5.77x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (14): regex_compile, sympy_str, generators, docutils, crypto_pyaes, coroutines, xml_etree_generate, asyncio_websockets, scimark_monte_carlo, pylint, asyncio_tcp, pyflate, xml_etree_process, scimark_sparse_mat_mult
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 99.77% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x