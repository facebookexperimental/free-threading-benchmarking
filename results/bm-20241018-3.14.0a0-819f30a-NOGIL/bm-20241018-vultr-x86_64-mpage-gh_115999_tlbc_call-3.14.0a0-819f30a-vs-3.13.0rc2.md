# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 819f30a
- commit date: 2024-10-18
- overall geometric mean: 1.53x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.38x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 411 ms: 1.58x slower                                                |
| docutils       | 2.62 sec                                                     | 3.28 sec: 1.25x slower                                              |
| html5lib       | 67.0 ms                                                      | 103 ms: 1.54x slower                                                |
| tornado_http   | 114 ms                                                       | 162 ms: 1.42x slower                                                |
| Geometric mean | (ref)                                                        | 1.44x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| asyncio_tcp      | 505 ms                                                       | 581 ms: 1.15x slower                                                |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.81 sec: 1.20x slower                                              |
| coroutines       | 23.6 ms                                                      | 29.3 ms: 1.24x slower                                               |
| async_generators | 377 ms                                                       | 525 ms: 1.39x slower                                                |
| Geometric mean   | (ref)                                                        | 1.19x slower                                                        |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 186 ms: 1.16x faster                                                |
| float          | 77.5 ms                                                      | 146 ms: 1.88x slower                                                |
| nbody          | 85.1 ms                                                      | 185 ms: 2.18x slower                                                |
| Geometric mean | (ref)                                                        | 1.52x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 3.10 ms: 1.01x slower                                               |
| regex_dna      | 180 ms                                                       | 190 ms: 1.05x slower                                                |
| regex_v8       | 22.7 ms                                                      | 26.1 ms: 1.15x slower                                               |
| regex_compile  | 132 ms                                                       | 221 ms: 1.67x slower                                                |
| Geometric mean | (ref)                                                        | 1.19x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle               | 11.3 us                                                      | 10.9 us: 1.04x faster                                               |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                |
| pickle_dict          | 32.5 us                                                      | 31.6 us: 1.03x faster                                               |
| pickle_list          | 4.93 us                                                      | 4.84 us: 1.02x faster                                               |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.04x slower                                               |
| unpickle_list        | 4.71 us                                                      | 5.18 us: 1.10x slower                                               |
| xml_etree_iterparse  | 94.9 ms                                                      | 105 ms: 1.11x slower                                                |
| xml_etree_generate   | 85.4 ms                                                      | 110 ms: 1.29x slower                                                |
| json_dumps           | 10.5 ms                                                      | 15.1 ms: 1.44x slower                                               |
| xml_etree_process    | 59.3 ms                                                      | 89.8 ms: 1.51x slower                                               |
| tomli_loads          | 2.01 sec                                                     | 3.22 sec: 1.61x slower                                              |
| unpickle_pure_python | 210 us                                                       | 393 us: 1.87x slower                                                |
| pickle_pure_python   | 294 us                                                       | 586 us: 1.99x slower                                                |
| Geometric mean       | (ref)                                                        | 1.24x slower                                                        |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                               |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                               |
| Geometric mean         | (ref)                                                        | 1.41x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 81.0 ms: 1.66x slower                                               |
| mako            | 11.3 ms                                                      | 19.1 ms: 1.69x slower                                               |
| django_template | 34.1 ms                                                      | 62.5 ms: 1.83x slower                                               |
| genshi_text     | 21.5 ms                                                      | 40.3 ms: 1.87x slower                                               |
| Geometric mean  | (ref)                                                        | 1.76x slower                                                        |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|--------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.55 ms: 1.23x faster                                               |
| create_gc_cycles         | 1.34 ms                                                      | 1.10 ms: 1.22x faster                                               |
| pidigits                 | 217 ms                                                       | 186 ms: 1.16x faster                                                |
| pickle                   | 11.3 us                                                      | 10.9 us: 1.04x faster                                               |
| xml_etree_parse          | 136 ms                                                       | 132 ms: 1.03x faster                                                |
| pickle_dict              | 32.5 us                                                      | 31.6 us: 1.03x faster                                               |
| pickle_list              | 4.93 us                                                      | 4.84 us: 1.02x faster                                               |
| regex_effbot             | 3.08 ms                                                      | 3.10 ms: 1.01x slower                                               |
| json_loads               | 27.0 us                                                      | 28.2 us: 1.04x slower                                               |
| regex_dna                | 180 ms                                                       | 190 ms: 1.05x slower                                                |
| json                     | 4.93 ms                                                      | 5.20 ms: 1.06x slower                                               |
| sqlite_synth             | 2.21 us                                                      | 2.38 us: 1.08x slower                                               |
| unpickle_list            | 4.71 us                                                      | 5.18 us: 1.10x slower                                               |
| xml_etree_iterparse      | 94.9 ms                                                      | 105 ms: 1.11x slower                                                |
| scimark_fft              | 349 ms                                                       | 391 ms: 1.12x slower                                                |
| pathlib                  | 19.2 ms                                                      | 21.9 ms: 1.14x slower                                               |
| asyncio_tcp              | 505 ms                                                       | 581 ms: 1.15x slower                                                |
| regex_v8                 | 22.7 ms                                                      | 26.1 ms: 1.15x slower                                               |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 5.46 ms: 1.16x slower                                               |
| deepcopy                 | 355 us                                                       | 420 us: 1.18x slower                                                |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.81 sec: 1.20x slower                                              |
| telco                    | 7.82 ms                                                      | 9.53 ms: 1.22x slower                                               |
| coverage                 | 83.0 ms                                                      | 101 ms: 1.22x slower                                                |
| coroutines               | 23.6 ms                                                      | 29.3 ms: 1.24x slower                                               |
| docutils                 | 2.62 sec                                                     | 3.28 sec: 1.25x slower                                              |
| deepcopy_memo            | 39.1 us                                                      | 49.8 us: 1.28x slower                                               |
| bpe_tokeniser            | 4.45 sec                                                     | 5.70 sec: 1.28x slower                                              |
| xml_etree_generate       | 85.4 ms                                                      | 110 ms: 1.29x slower                                                |
| pylint                   | 317 ms                                                       | 413 ms: 1.30x slower                                                |
| spectral_norm            | 111 ms                                                       | 148 ms: 1.34x slower                                                |
| mdp                      | 2.36 sec                                                     | 3.21 sec: 1.36x slower                                              |
| meteor_contest           | 102 ms                                                       | 139 ms: 1.37x slower                                                |
| dulwich_log              | 74.8 ms                                                      | 103 ms: 1.37x slower                                                |
| python_startup_no_site   | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                               |
| async_generators         | 377 ms                                                       | 525 ms: 1.39x slower                                                |
| tornado_http             | 114 ms                                                       | 162 ms: 1.42x slower                                                |
| deepcopy_reduce          | 3.11 us                                                      | 4.43 us: 1.42x slower                                               |
| nqueens                  | 78.6 ms                                                      | 112 ms: 1.42x slower                                                |
| python_startup           | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                               |
| json_dumps               | 10.5 ms                                                      | 15.1 ms: 1.44x slower                                               |
| generators               | 28.8 ms                                                      | 43.0 ms: 1.49x slower                                               |
| pycparser                | 1.12 sec                                                     | 1.67 sec: 1.50x slower                                              |
| fannkuch                 | 370 ms                                                       | 553 ms: 1.50x slower                                                |
| xml_etree_process        | 59.3 ms                                                      | 89.8 ms: 1.51x slower                                               |
| html5lib                 | 67.0 ms                                                      | 103 ms: 1.54x slower                                                |
| typing_runtime_protocols | 155 us                                                       | 243 us: 1.57x slower                                                |
| crypto_pyaes             | 67.9 ms                                                      | 107 ms: 1.58x slower                                                |
| 2to3                     | 260 ms                                                       | 411 ms: 1.58x slower                                                |
| tomli_loads              | 2.01 sec                                                     | 3.22 sec: 1.61x slower                                              |
| sympy_integrate          | 19.8 ms                                                      | 32.3 ms: 1.63x slower                                               |
| sqlglot_normalize        | 106 ms                                                       | 173 ms: 1.64x slower                                                |
| thrift                   | 778 us                                                       | 1.28 ms: 1.65x slower                                               |
| sqlglot_optimize         | 52.7 ms                                                      | 87.3 ms: 1.66x slower                                               |
| genshi_xml               | 48.8 ms                                                      | 81.0 ms: 1.66x slower                                               |
| pyflate                  | 449 ms                                                       | 747 ms: 1.66x slower                                                |
| regex_compile            | 132 ms                                                       | 221 ms: 1.67x slower                                                |
| mako                     | 11.3 ms                                                      | 19.1 ms: 1.69x slower                                               |
| pprint_safe_repr         | 738 ms                                                       | 1.26 sec: 1.71x slower                                              |
| pprint_pformat           | 1.50 sec                                                     | 2.63 sec: 1.76x slower                                              |
| comprehensions           | 16.5 us                                                      | 29.5 us: 1.79x slower                                               |
| django_template          | 34.1 ms                                                      | 62.5 ms: 1.83x slower                                               |
| scimark_monte_carlo      | 65.4 ms                                                      | 122 ms: 1.86x slower                                                |
| genshi_text              | 21.5 ms                                                      | 40.3 ms: 1.87x slower                                               |
| unpickle_pure_python     | 210 us                                                       | 393 us: 1.87x slower                                                |
| float                    | 77.5 ms                                                      | 146 ms: 1.88x slower                                                |
| richards                 | 45.2 ms                                                      | 86.0 ms: 1.90x slower                                               |
| hexiom                   | 5.99 ms                                                      | 11.6 ms: 1.94x slower                                               |
| sympy_str                | 275 ms                                                       | 533 ms: 1.94x slower                                                |
| scimark_sor              | 134 ms                                                       | 262 ms: 1.95x slower                                                |
| logging_format           | 6.84 us                                                      | 13.5 us: 1.97x slower                                               |
| pickle_pure_python       | 294 us                                                       | 586 us: 1.99x slower                                                |
| logging_simple           | 6.16 us                                                      | 12.3 us: 1.99x slower                                               |
| richards_super           | 51.6 ms                                                      | 104 ms: 2.02x slower                                                |
| logging_silent           | 103 ns                                                       | 209 ns: 2.04x slower                                                |
| chaos                    | 57.3 ms                                                      | 117 ms: 2.05x slower                                                |
| scimark_lu               | 113 ms                                                       | 233 ms: 2.07x slower                                                |
| go                       | 141 ms                                                       | 296 ms: 2.11x slower                                                |
| sqlglot_transpile        | 1.56 ms                                                      | 3.29 ms: 2.11x slower                                               |
| nbody                    | 85.1 ms                                                      | 185 ms: 2.18x slower                                                |
| sqlglot_parse            | 1.25 ms                                                      | 2.84 ms: 2.28x slower                                               |
| sympy_expand             | 457 ms                                                       | 1.04 sec: 2.28x slower                                              |
| raytrace                 | 253 ms                                                       | 611 ms: 2.42x slower                                                |
| sympy_sum                | 156 ms                                                       | 379 ms: 2.44x slower                                                |
| deltablue                | 3.12 ms                                                      | 8.71 ms: 2.79x slower                                               |
| unpack_sequence          | 44.8 ns                                                      | 140 ns: 3.11x slower                                                |
| bench_thread_pool        | 919 us                                                       | 3.48 ms: 3.78x slower                                               |
| bench_mp_pool            | 11.0 ms                                                      | 71.7 ms: 6.53x slower                                               |
| Geometric mean           | (ref)                                                        | 1.53x slower                                                        |

Benchmark hidden because not significant (2): asyncio_websockets, unpickle
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.44x
- 95% likely to have a slowdown of 1.42x
- 99% likely to have a slowdown of 1.38x

# Memory
- memory change: 1.20x