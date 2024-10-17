# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_125608_dict_watch
- machine: linux-x86_64
- commit hash: 28871ed
- commit date: 2024-10-16
- overall geometric mean: 1.01x slower
- HPT reliability: 66.85%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 253 ms: 1.03x faster                                                      |
| docutils       | 2.62 sec                                                     | 2.58 sec: 1.01x faster                                                    |
| html5lib       | 67.0 ms                                                      | 62.6 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                        | 1.03x faster                                                              |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coroutines       | 23.6 ms                                                      | 22.2 ms: 1.06x faster                                                     |
| async_generators | 377 ms                                                       | 374 ms: 1.01x faster                                                      |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                    |
| Geometric mean   | (ref)                                                        | 1.01x faster                                                              |

Benchmark hidden because not significant (2): asyncio_websockets, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                      |
| float          | 77.5 ms                                                      | 78.5 ms: 1.01x slower                                                     |
| nbody          | 85.1 ms                                                      | 93.6 ms: 1.10x slower                                                     |
| Geometric mean | (ref)                                                        | 1.02x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                       | 169 ms: 1.06x faster                                                      |
| regex_compile  | 132 ms                                                       | 129 ms: 1.03x faster                                                      |
| regex_v8       | 22.7 ms                                                      | 23.5 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                        | 1.01x faster                                                              |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| unpickle             | 14.3 us                                                      | 13.5 us: 1.06x faster                                                     |
| json_loads           | 27.0 us                                                      | 26.0 us: 1.04x faster                                                     |
| unpickle_list        | 4.71 us                                                      | 4.65 us: 1.01x faster                                                     |
| pickle               | 11.3 us                                                      | 11.2 us: 1.01x faster                                                     |
| xml_etree_process    | 59.3 ms                                                      | 59.1 ms: 1.00x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 85.2 ms: 1.00x faster                                                     |
| pickle_list          | 4.93 us                                                      | 4.99 us: 1.01x slower                                                     |
| pickle_dict          | 32.5 us                                                      | 33.0 us: 1.01x slower                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 96.8 ms: 1.02x slower                                                     |
| unpickle_pure_python | 210 us                                                       | 216 us: 1.03x slower                                                      |
| tomli_loads          | 2.01 sec                                                     | 2.08 sec: 1.04x slower                                                    |
| pickle_pure_python   | 294 us                                                       | 307 us: 1.04x slower                                                      |
| json_dumps           | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                              |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.40 ms: 1.00x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.00x slower                                                              |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                                     |
| genshi_text     | 21.5 ms                                                      | 22.3 ms: 1.03x slower                                                     |
| django_template | 34.1 ms                                                      | 35.4 ms: 1.04x slower                                                     |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                     |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                              |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1+-28871ed |
|--------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| deepcopy                 | 355 us                                                       | 263 us: 1.35x faster                                                      |
| deepcopy_memo            | 39.1 us                                                      | 30.5 us: 1.28x faster                                                     |
| pidigits                 | 217 ms                                                       | 185 ms: 1.17x faster                                                      |
| deepcopy_reduce          | 3.11 us                                                      | 2.66 us: 1.17x faster                                                     |
| go                       | 141 ms                                                       | 121 ms: 1.17x faster                                                      |
| html5lib                 | 67.0 ms                                                      | 62.6 ms: 1.07x faster                                                     |
| telco                    | 7.82 ms                                                      | 7.34 ms: 1.07x faster                                                     |
| regex_dna                | 180 ms                                                       | 169 ms: 1.06x faster                                                      |
| unpickle                 | 14.3 us                                                      | 13.5 us: 1.06x faster                                                     |
| coroutines               | 23.6 ms                                                      | 22.2 ms: 1.06x faster                                                     |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 4.49 ms: 1.05x faster                                                     |
| scimark_fft              | 349 ms                                                       | 336 ms: 1.04x faster                                                      |
| json_loads               | 27.0 us                                                      | 26.0 us: 1.04x faster                                                     |
| thrift                   | 778 us                                                       | 754 us: 1.03x faster                                                      |
| pprint_safe_repr         | 738 ms                                                       | 714 ms: 1.03x faster                                                      |
| regex_compile            | 132 ms                                                       | 129 ms: 1.03x faster                                                      |
| bpe_tokeniser            | 4.45 sec                                                     | 4.32 sec: 1.03x faster                                                    |
| pathlib                  | 19.2 ms                                                      | 18.7 ms: 1.03x faster                                                     |
| 2to3                     | 260 ms                                                       | 253 ms: 1.03x faster                                                      |
| spectral_norm            | 111 ms                                                       | 108 ms: 1.02x faster                                                      |
| logging_silent           | 103 ns                                                       | 100 ns: 1.02x faster                                                      |
| pprint_pformat           | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                                    |
| logging_simple           | 6.16 us                                                      | 6.05 us: 1.02x faster                                                     |
| logging_format           | 6.84 us                                                      | 6.73 us: 1.02x faster                                                     |
| unpickle_list            | 4.71 us                                                      | 4.65 us: 1.01x faster                                                     |
| pickle                   | 11.3 us                                                      | 11.2 us: 1.01x faster                                                     |
| docutils                 | 2.62 sec                                                     | 2.58 sec: 1.01x faster                                                    |
| json                     | 4.93 ms                                                      | 4.87 ms: 1.01x faster                                                     |
| sympy_sum                | 156 ms                                                       | 154 ms: 1.01x faster                                                      |
| async_generators         | 377 ms                                                       | 374 ms: 1.01x faster                                                      |
| sympy_str                | 275 ms                                                       | 272 ms: 1.01x faster                                                      |
| scimark_lu               | 113 ms                                                       | 112 ms: 1.01x faster                                                      |
| pyflate                  | 449 ms                                                       | 445 ms: 1.01x faster                                                      |
| generators               | 28.8 ms                                                      | 28.6 ms: 1.01x faster                                                     |
| nqueens                  | 78.6 ms                                                      | 78.2 ms: 1.00x faster                                                     |
| xml_etree_process        | 59.3 ms                                                      | 59.1 ms: 1.00x faster                                                     |
| xml_etree_generate       | 85.4 ms                                                      | 85.2 ms: 1.00x faster                                                     |
| python_startup_no_site   | 7.39 ms                                                      | 7.40 ms: 1.00x slower                                                     |
| richards_super           | 51.6 ms                                                      | 51.8 ms: 1.00x slower                                                     |
| sqlglot_normalize        | 106 ms                                                       | 106 ms: 1.01x slower                                                      |
| sympy_integrate          | 19.8 ms                                                      | 20.0 ms: 1.01x slower                                                     |
| crypto_pyaes             | 67.9 ms                                                      | 68.4 ms: 1.01x slower                                                     |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                    |
| scimark_monte_carlo      | 65.4 ms                                                      | 66.0 ms: 1.01x slower                                                     |
| create_gc_cycles         | 1.34 ms                                                      | 1.35 ms: 1.01x slower                                                     |
| richards                 | 45.2 ms                                                      | 45.7 ms: 1.01x slower                                                     |
| pickle_list              | 4.93 us                                                      | 4.99 us: 1.01x slower                                                     |
| float                    | 77.5 ms                                                      | 78.5 ms: 1.01x slower                                                     |
| typing_runtime_protocols | 155 us                                                       | 157 us: 1.01x slower                                                      |
| pickle_dict              | 32.5 us                                                      | 33.0 us: 1.01x slower                                                     |
| pycparser                | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                    |
| genshi_xml               | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                                     |
| fannkuch                 | 370 ms                                                       | 377 ms: 1.02x slower                                                      |
| xml_etree_iterparse      | 94.9 ms                                                      | 96.8 ms: 1.02x slower                                                     |
| sqlglot_optimize         | 52.7 ms                                                      | 53.8 ms: 1.02x slower                                                     |
| chaos                    | 57.3 ms                                                      | 58.8 ms: 1.03x slower                                                     |
| sqlglot_transpile        | 1.56 ms                                                      | 1.60 ms: 1.03x slower                                                     |
| unpickle_pure_python     | 210 us                                                       | 216 us: 1.03x slower                                                      |
| raytrace                 | 253 ms                                                       | 260 ms: 1.03x slower                                                      |
| deltablue                | 3.12 ms                                                      | 3.22 ms: 1.03x slower                                                     |
| genshi_text              | 21.5 ms                                                      | 22.3 ms: 1.03x slower                                                     |
| regex_v8                 | 22.7 ms                                                      | 23.5 ms: 1.03x slower                                                     |
| tomli_loads              | 2.01 sec                                                     | 2.08 sec: 1.04x slower                                                    |
| django_template          | 34.1 ms                                                      | 35.4 ms: 1.04x slower                                                     |
| sqlglot_parse            | 1.25 ms                                                      | 1.30 ms: 1.04x slower                                                     |
| mako                     | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                     |
| comprehensions           | 16.5 us                                                      | 17.1 us: 1.04x slower                                                     |
| pickle_pure_python       | 294 us                                                       | 307 us: 1.04x slower                                                      |
| mdp                      | 2.36 sec                                                     | 2.48 sec: 1.05x slower                                                    |
| nbody                    | 85.1 ms                                                      | 93.6 ms: 1.10x slower                                                     |
| json_dumps               | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                     |
| gc_traversal             | 3.14 ms                                                      | 3.47 ms: 1.10x slower                                                     |
| bench_thread_pool        | 919 us                                                       | 1.02 ms: 1.11x slower                                                     |
| unpack_sequence          | 44.8 ns                                                      | 53.0 ns: 1.18x slower                                                     |
| bench_mp_pool            | 11.0 ms                                                      | 63.4 ms: 5.76x slower                                                     |
| Geometric mean           | (ref)                                                        | 1.01x slower                                                              |

Benchmark hidden because not significant (14): xml_etree_parse, coverage, tornado_http, sympy_expand, dulwich_log, hexiom, sqlite_synth, meteor_contest, python_startup, pylint, asyncio_websockets, regex_effbot, asyncio_tcp, scimark_sor
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 66.85% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x