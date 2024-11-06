# Results vs. 3.13.0rc2

- fork: python
- ref: 83ba8c2bba834c0b92de
- machine: linux-x86_64
- commit hash: 83ba8c2
- commit date: 2024-11-05
- overall geometric mean: 1.01x slower
- HPT reliability: 94.86%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 252 ms: 1.03x faster                                                   |
| html5lib       | 67.0 ms                                                      | 66.3 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_generators | 377 ms                                                       | 373 ms: 1.01x faster                                                   |
| coroutines       | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                  |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                 |
| Geometric mean   | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                   |
| float          | 77.5 ms                                                      | 79.2 ms: 1.02x slower                                                  |
| nbody          | 85.1 ms                                                      | 94.3 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 129 ms: 1.03x faster                                                   |
| regex_dna      | 180 ms                                                       | 183 ms: 1.01x slower                                                   |
| regex_effbot   | 3.08 ms                                                      | 3.12 ms: 1.01x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 24.3 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 30.4 us: 1.07x faster                                                  |
| unpickle             | 14.3 us                                                      | 13.5 us: 1.06x faster                                                  |
| pickle_list          | 4.93 us                                                      | 4.64 us: 1.06x faster                                                  |
| json_loads           | 27.0 us                                                      | 26.4 us: 1.02x faster                                                  |
| pickle               | 11.3 us                                                      | 11.1 us: 1.02x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 84.7 ms: 1.01x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.9 ms: 1.01x faster                                                  |
| unpickle_list        | 4.71 us                                                      | 4.69 us: 1.00x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 96.0 ms: 1.01x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 217 us: 1.03x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.10 sec: 1.05x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 313 us: 1.06x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                      | 11.0 ms: 1.00x slower                                                  |
| python_startup_no_site | 7.39 ms                                                      | 7.43 ms: 1.00x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.00x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.5 ms: 1.02x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                                  |
| django_template | 34.1 ms                                                      | 34.9 ms: 1.02x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 22.5 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                 | 355 us                                                       | 263 us: 1.35x faster                                                   |
| deepcopy_memo            | 39.1 us                                                      | 29.8 us: 1.31x faster                                                  |
| deepcopy_reduce          | 3.11 us                                                      | 2.65 us: 1.17x faster                                                  |
| pidigits                 | 217 ms                                                       | 185 ms: 1.17x faster                                                   |
| go                       | 141 ms                                                       | 120 ms: 1.17x faster                                                   |
| unpack_sequence          | 44.8 ns                                                      | 41.6 ns: 1.08x faster                                                  |
| pickle_dict              | 32.5 us                                                      | 30.4 us: 1.07x faster                                                  |
| unpickle                 | 14.3 us                                                      | 13.5 us: 1.06x faster                                                  |
| pickle_list              | 4.93 us                                                      | 4.64 us: 1.06x faster                                                  |
| pathlib                  | 19.2 ms                                                      | 18.3 ms: 1.05x faster                                                  |
| telco                    | 7.82 ms                                                      | 7.45 ms: 1.05x faster                                                  |
| pprint_safe_repr         | 738 ms                                                       | 708 ms: 1.04x faster                                                   |
| thrift                   | 778 us                                                       | 749 us: 1.04x faster                                                   |
| 2to3                     | 260 ms                                                       | 252 ms: 1.03x faster                                                   |
| scimark_fft              | 349 ms                                                       | 340 ms: 1.03x faster                                                   |
| regex_compile            | 132 ms                                                       | 129 ms: 1.03x faster                                                   |
| logging_simple           | 6.16 us                                                      | 6.01 us: 1.02x faster                                                  |
| coverage                 | 83.0 ms                                                      | 81.1 ms: 1.02x faster                                                  |
| json_loads               | 27.0 us                                                      | 26.4 us: 1.02x faster                                                  |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 4.61 ms: 1.02x faster                                                  |
| pprint_pformat           | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                                 |
| sympy_sum                | 156 ms                                                       | 153 ms: 1.02x faster                                                   |
| logging_format           | 6.84 us                                                      | 6.71 us: 1.02x faster                                                  |
| pickle                   | 11.3 us                                                      | 11.1 us: 1.02x faster                                                  |
| bpe_tokeniser            | 4.45 sec                                                     | 4.37 sec: 1.02x faster                                                 |
| json                     | 4.93 ms                                                      | 4.86 ms: 1.01x faster                                                  |
| meteor_contest           | 102 ms                                                       | 100 ms: 1.01x faster                                                   |
| hexiom                   | 5.99 ms                                                      | 5.92 ms: 1.01x faster                                                  |
| sqlite_synth             | 2.21 us                                                      | 2.18 us: 1.01x faster                                                  |
| async_generators         | 377 ms                                                       | 373 ms: 1.01x faster                                                   |
| html5lib                 | 67.0 ms                                                      | 66.3 ms: 1.01x faster                                                  |
| xml_etree_generate       | 85.4 ms                                                      | 84.7 ms: 1.01x faster                                                  |
| xml_etree_process        | 59.3 ms                                                      | 58.9 ms: 1.01x faster                                                  |
| pyflate                  | 449 ms                                                       | 446 ms: 1.00x faster                                                   |
| unpickle_list            | 4.71 us                                                      | 4.69 us: 1.00x faster                                                  |
| python_startup           | 11.0 ms                                                      | 11.0 ms: 1.00x slower                                                  |
| sympy_integrate          | 19.8 ms                                                      | 19.9 ms: 1.00x slower                                                  |
| python_startup_no_site   | 7.39 ms                                                      | 7.43 ms: 1.00x slower                                                  |
| scimark_monte_carlo      | 65.4 ms                                                      | 65.7 ms: 1.01x slower                                                  |
| sqlglot_normalize        | 106 ms                                                       | 106 ms: 1.01x slower                                                   |
| coroutines               | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                  |
| nqueens                  | 78.6 ms                                                      | 79.2 ms: 1.01x slower                                                  |
| scimark_sor              | 134 ms                                                       | 136 ms: 1.01x slower                                                   |
| richards                 | 45.2 ms                                                      | 45.6 ms: 1.01x slower                                                  |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                 |
| xml_etree_iterparse      | 94.9 ms                                                      | 96.0 ms: 1.01x slower                                                  |
| crypto_pyaes             | 67.9 ms                                                      | 68.8 ms: 1.01x slower                                                  |
| regex_dna                | 180 ms                                                       | 183 ms: 1.01x slower                                                   |
| regex_effbot             | 3.08 ms                                                      | 3.12 ms: 1.01x slower                                                  |
| sqlglot_optimize         | 52.7 ms                                                      | 53.4 ms: 1.01x slower                                                  |
| scimark_lu               | 113 ms                                                       | 114 ms: 1.01x slower                                                   |
| typing_runtime_protocols | 155 us                                                       | 157 us: 1.01x slower                                                   |
| pycparser                | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                 |
| create_gc_cycles         | 1.34 ms                                                      | 1.36 ms: 1.02x slower                                                  |
| fannkuch                 | 370 ms                                                       | 376 ms: 1.02x slower                                                   |
| mako                     | 11.3 ms                                                      | 11.5 ms: 1.02x slower                                                  |
| generators               | 28.8 ms                                                      | 29.3 ms: 1.02x slower                                                  |
| genshi_xml               | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                                  |
| float                    | 77.5 ms                                                      | 79.2 ms: 1.02x slower                                                  |
| django_template          | 34.1 ms                                                      | 34.9 ms: 1.02x slower                                                  |
| spectral_norm            | 111 ms                                                       | 114 ms: 1.02x slower                                                   |
| sqlglot_transpile        | 1.56 ms                                                      | 1.60 ms: 1.02x slower                                                  |
| chaos                    | 57.3 ms                                                      | 59.0 ms: 1.03x slower                                                  |
| unpickle_pure_python     | 210 us                                                       | 217 us: 1.03x slower                                                   |
| deltablue                | 3.12 ms                                                      | 3.24 ms: 1.04x slower                                                  |
| logging_silent           | 103 ns                                                       | 106 ns: 1.04x slower                                                   |
| raytrace                 | 253 ms                                                       | 263 ms: 1.04x slower                                                   |
| sqlglot_parse            | 1.25 ms                                                      | 1.30 ms: 1.04x slower                                                  |
| genshi_text              | 21.5 ms                                                      | 22.5 ms: 1.04x slower                                                  |
| tomli_loads              | 2.01 sec                                                     | 2.10 sec: 1.05x slower                                                 |
| mdp                      | 2.36 sec                                                     | 2.50 sec: 1.06x slower                                                 |
| pickle_pure_python       | 294 us                                                       | 313 us: 1.06x slower                                                   |
| comprehensions           | 16.5 us                                                      | 17.5 us: 1.06x slower                                                  |
| regex_v8                 | 22.7 ms                                                      | 24.3 ms: 1.07x slower                                                  |
| bench_thread_pool        | 919 us                                                       | 1.01 ms: 1.10x slower                                                  |
| json_dumps               | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                  |
| nbody                    | 85.1 ms                                                      | 94.3 ms: 1.11x slower                                                  |
| gc_traversal             | 3.14 ms                                                      | 3.70 ms: 1.18x slower                                                  |
| bench_mp_pool            | 11.0 ms                                                      | 63.2 ms: 5.75x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (9): sympy_str, dulwich_log, docutils, richards_super, asyncio_websockets, xml_etree_parse, asyncio_tcp, sympy_expand, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 94.86% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x