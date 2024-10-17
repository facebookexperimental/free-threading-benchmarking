# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_125610_STORE_ATTR
- machine: linux-x86_64
- commit hash: 3a126a8
- commit date: 2024-10-16
- overall geometric mean: 1.02x slower
- HPT reliability: 96.88%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 255 ms: 1.02x faster                                                      |
| html5lib       | 67.0 ms                                                      | 63.1 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                        | 1.02x faster                                                              |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coroutines       | 23.6 ms                                                      | 22.3 ms: 1.05x faster                                                     |
| async_generators | 377 ms                                                       | 371 ms: 1.02x faster                                                      |
| asyncio_tcp      | 505 ms                                                       | 501 ms: 1.01x faster                                                      |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                    |
| Geometric mean   | (ref)                                                        | 1.01x faster                                                              |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 186 ms: 1.16x faster                                                      |
| float          | 77.5 ms                                                      | 79.8 ms: 1.03x slower                                                     |
| nbody          | 85.1 ms                                                      | 93.8 ms: 1.10x slower                                                     |
| Geometric mean | (ref)                                                        | 1.01x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 3.01 ms: 1.02x faster                                                     |
| regex_compile  | 132 ms                                                       | 129 ms: 1.02x faster                                                      |
| regex_dna      | 180 ms                                                       | 179 ms: 1.01x faster                                                      |
| regex_v8       | 22.7 ms                                                      | 24.5 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                        | 1.01x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| unpickle             | 14.3 us                                                      | 13.8 us: 1.04x faster                                                     |
| json_loads           | 27.0 us                                                      | 26.2 us: 1.03x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 85.0 ms: 1.00x faster                                                     |
| xml_etree_parse      | 136 ms                                                       | 138 ms: 1.01x slower                                                      |
| xml_etree_iterparse  | 94.9 ms                                                      | 96.4 ms: 1.02x slower                                                     |
| pickle               | 11.3 us                                                      | 11.5 us: 1.02x slower                                                     |
| pickle_list          | 4.93 us                                                      | 5.03 us: 1.02x slower                                                     |
| unpickle_list        | 4.71 us                                                      | 4.89 us: 1.04x slower                                                     |
| unpickle_pure_python | 210 us                                                       | 218 us: 1.04x slower                                                      |
| pickle_pure_python   | 294 us                                                       | 307 us: 1.04x slower                                                      |
| pickle_dict          | 32.5 us                                                      | 34.0 us: 1.04x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.10 sec: 1.05x slower                                                    |
| json_dumps           | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                              |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                     |
| python_startup         | 11.0 ms                                                      | 11.1 ms: 1.01x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.01x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                     |
| genshi_xml      | 48.8 ms                                                      | 50.3 ms: 1.03x slower                                                     |
| genshi_text     | 21.5 ms                                                      | 22.3 ms: 1.04x slower                                                     |
| django_template | 34.1 ms                                                      | 35.4 ms: 1.04x slower                                                     |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                              |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|--------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| deepcopy                 | 355 us                                                       | 263 us: 1.35x faster                                                      |
| deepcopy_memo            | 39.1 us                                                      | 30.0 us: 1.30x faster                                                     |
| deepcopy_reduce          | 3.11 us                                                      | 2.66 us: 1.17x faster                                                     |
| pidigits                 | 217 ms                                                       | 186 ms: 1.16x faster                                                      |
| go                       | 141 ms                                                       | 122 ms: 1.15x faster                                                      |
| html5lib                 | 67.0 ms                                                      | 63.1 ms: 1.06x faster                                                     |
| coroutines               | 23.6 ms                                                      | 22.3 ms: 1.05x faster                                                     |
| telco                    | 7.82 ms                                                      | 7.43 ms: 1.05x faster                                                     |
| unpickle                 | 14.3 us                                                      | 13.8 us: 1.04x faster                                                     |
| pprint_safe_repr         | 738 ms                                                       | 712 ms: 1.04x faster                                                      |
| json_loads               | 27.0 us                                                      | 26.2 us: 1.03x faster                                                     |
| pathlib                  | 19.2 ms                                                      | 18.6 ms: 1.03x faster                                                     |
| regex_effbot             | 3.08 ms                                                      | 3.01 ms: 1.02x faster                                                     |
| regex_compile            | 132 ms                                                       | 129 ms: 1.02x faster                                                      |
| coverage                 | 83.0 ms                                                      | 81.1 ms: 1.02x faster                                                     |
| thrift                   | 778 us                                                       | 762 us: 1.02x faster                                                      |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 4.62 ms: 1.02x faster                                                     |
| pprint_pformat           | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                                    |
| 2to3                     | 260 ms                                                       | 255 ms: 1.02x faster                                                      |
| async_generators         | 377 ms                                                       | 371 ms: 1.02x faster                                                      |
| scimark_fft              | 349 ms                                                       | 346 ms: 1.01x faster                                                      |
| logging_simple           | 6.16 us                                                      | 6.10 us: 1.01x faster                                                     |
| asyncio_tcp              | 505 ms                                                       | 501 ms: 1.01x faster                                                      |
| bpe_tokeniser            | 4.45 sec                                                     | 4.41 sec: 1.01x faster                                                    |
| regex_dna                | 180 ms                                                       | 179 ms: 1.01x faster                                                      |
| xml_etree_generate       | 85.4 ms                                                      | 85.0 ms: 1.00x faster                                                     |
| sympy_expand             | 457 ms                                                       | 460 ms: 1.01x slower                                                      |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                    |
| generators               | 28.8 ms                                                      | 29.0 ms: 1.01x slower                                                     |
| typing_runtime_protocols | 155 us                                                       | 156 us: 1.01x slower                                                      |
| hexiom                   | 5.99 ms                                                      | 6.05 ms: 1.01x slower                                                     |
| python_startup_no_site   | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                     |
| xml_etree_parse          | 136 ms                                                       | 138 ms: 1.01x slower                                                      |
| python_startup           | 11.0 ms                                                      | 11.1 ms: 1.01x slower                                                     |
| sympy_integrate          | 19.8 ms                                                      | 20.1 ms: 1.01x slower                                                     |
| richards_super           | 51.6 ms                                                      | 52.4 ms: 1.02x slower                                                     |
| sqlglot_optimize         | 52.7 ms                                                      | 53.5 ms: 1.02x slower                                                     |
| xml_etree_iterparse      | 94.9 ms                                                      | 96.4 ms: 1.02x slower                                                     |
| scimark_sor              | 134 ms                                                       | 137 ms: 1.02x slower                                                      |
| pickle                   | 11.3 us                                                      | 11.5 us: 1.02x slower                                                     |
| fannkuch                 | 370 ms                                                       | 376 ms: 1.02x slower                                                      |
| scimark_monte_carlo      | 65.4 ms                                                      | 66.5 ms: 1.02x slower                                                     |
| crypto_pyaes             | 67.9 ms                                                      | 69.1 ms: 1.02x slower                                                     |
| spectral_norm            | 111 ms                                                       | 113 ms: 1.02x slower                                                      |
| pickle_list              | 4.93 us                                                      | 5.03 us: 1.02x slower                                                     |
| pyflate                  | 449 ms                                                       | 458 ms: 1.02x slower                                                      |
| sqlglot_transpile        | 1.56 ms                                                      | 1.59 ms: 1.02x slower                                                     |
| meteor_contest           | 102 ms                                                       | 104 ms: 1.02x slower                                                      |
| mako                     | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                     |
| create_gc_cycles         | 1.34 ms                                                      | 1.38 ms: 1.03x slower                                                     |
| genshi_xml               | 48.8 ms                                                      | 50.3 ms: 1.03x slower                                                     |
| float                    | 77.5 ms                                                      | 79.8 ms: 1.03x slower                                                     |
| richards                 | 45.2 ms                                                      | 46.7 ms: 1.03x slower                                                     |
| sqlglot_parse            | 1.25 ms                                                      | 1.29 ms: 1.03x slower                                                     |
| logging_silent           | 103 ns                                                       | 106 ns: 1.04x slower                                                      |
| genshi_text              | 21.5 ms                                                      | 22.3 ms: 1.04x slower                                                     |
| unpickle_list            | 4.71 us                                                      | 4.89 us: 1.04x slower                                                     |
| django_template          | 34.1 ms                                                      | 35.4 ms: 1.04x slower                                                     |
| unpickle_pure_python     | 210 us                                                       | 218 us: 1.04x slower                                                      |
| chaos                    | 57.3 ms                                                      | 59.6 ms: 1.04x slower                                                     |
| pickle_pure_python       | 294 us                                                       | 307 us: 1.04x slower                                                      |
| pickle_dict              | 32.5 us                                                      | 34.0 us: 1.04x slower                                                     |
| tomli_loads              | 2.01 sec                                                     | 2.10 sec: 1.05x slower                                                    |
| comprehensions           | 16.5 us                                                      | 17.2 us: 1.05x slower                                                     |
| gc_traversal             | 3.14 ms                                                      | 3.30 ms: 1.05x slower                                                     |
| deltablue                | 3.12 ms                                                      | 3.28 ms: 1.05x slower                                                     |
| raytrace                 | 253 ms                                                       | 266 ms: 1.05x slower                                                      |
| regex_v8                 | 22.7 ms                                                      | 24.5 ms: 1.08x slower                                                     |
| pycparser                | 1.12 sec                                                     | 1.21 sec: 1.09x slower                                                    |
| nbody                    | 85.1 ms                                                      | 93.8 ms: 1.10x slower                                                     |
| json_dumps               | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                     |
| bench_thread_pool        | 919 us                                                       | 1.01 ms: 1.10x slower                                                     |
| unpack_sequence          | 44.8 ns                                                      | 51.0 ns: 1.14x slower                                                     |
| bench_mp_pool            | 11.0 ms                                                      | 64.0 ms: 5.82x slower                                                     |
| Geometric mean           | (ref)                                                        | 1.02x slower                                                              |

Benchmark hidden because not significant (15): sqlite_synth, sympy_str, docutils, sympy_sum, logging_format, nqueens, asyncio_websockets, scimark_lu, json, xml_etree_process, mdp, dulwich_log, sqlglot_normalize, tornado_http, pylint
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 96.88% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x