# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 819f30a
- commit date: 2024-10-18
- overall geometric mean: 1.52x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.37x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 410 ms: 1.58x slower                                                |
| docutils       | 2.62 sec                                                     | 3.28 sec: 1.25x slower                                              |
| html5lib       | 67.0 ms                                                      | 103 ms: 1.54x slower                                                |
| tornado_http   | 114 ms                                                       | 163 ms: 1.43x slower                                                |
| Geometric mean | (ref)                                                        | 1.44x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| asyncio_tcp      | 505 ms                                                       | 582 ms: 1.15x slower                                                |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.82 sec: 1.21x slower                                              |
| coroutines       | 23.6 ms                                                      | 29.2 ms: 1.24x slower                                               |
| async_generators | 377 ms                                                       | 500 ms: 1.32x slower                                                |
| Geometric mean   | (ref)                                                        | 1.18x slower                                                        |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                |
| float          | 77.5 ms                                                      | 146 ms: 1.89x slower                                                |
| nbody          | 85.1 ms                                                      | 186 ms: 2.19x slower                                                |
| Geometric mean | (ref)                                                        | 1.52x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 3.21 ms: 1.04x slower                                               |
| regex_dna      | 180 ms                                                       | 191 ms: 1.06x slower                                                |
| regex_v8       | 22.7 ms                                                      | 25.3 ms: 1.12x slower                                               |
| regex_compile  | 132 ms                                                       | 221 ms: 1.67x slower                                                |
| Geometric mean | (ref)                                                        | 1.20x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 31.1 us: 1.05x faster                                               |
| pickle               | 11.3 us                                                      | 10.8 us: 1.05x faster                                               |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                |
| pickle_list          | 4.93 us                                                      | 4.90 us: 1.01x faster                                               |
| unpickle             | 14.3 us                                                      | 15.0 us: 1.05x slower                                               |
| json_loads           | 27.0 us                                                      | 28.3 us: 1.05x slower                                               |
| unpickle_list        | 4.71 us                                                      | 5.14 us: 1.09x slower                                               |
| xml_etree_iterparse  | 94.9 ms                                                      | 106 ms: 1.12x slower                                                |
| xml_etree_generate   | 85.4 ms                                                      | 109 ms: 1.28x slower                                                |
| json_dumps           | 10.5 ms                                                      | 15.0 ms: 1.42x slower                                               |
| xml_etree_process    | 59.3 ms                                                      | 89.1 ms: 1.50x slower                                               |
| tomli_loads          | 2.01 sec                                                     | 3.21 sec: 1.60x slower                                              |
| unpickle_pure_python | 210 us                                                       | 386 us: 1.84x slower                                                |
| pickle_pure_python   | 294 us                                                       | 584 us: 1.98x slower                                                |
| Geometric mean       | (ref)                                                        | 1.23x slower                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                               |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                               |
| Geometric mean         | (ref)                                                        | 1.41x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 80.6 ms: 1.65x slower                                               |
| mako            | 11.3 ms                                                      | 19.3 ms: 1.70x slower                                               |
| django_template | 34.1 ms                                                      | 62.1 ms: 1.82x slower                                               |
| genshi_text     | 21.5 ms                                                      | 39.2 ms: 1.82x slower                                               |
| Geometric mean  | (ref)                                                        | 1.75x slower                                                        |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|--------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.47 ms: 1.27x faster                                               |
| create_gc_cycles         | 1.34 ms                                                      | 1.13 ms: 1.19x faster                                               |
| pidigits                 | 217 ms                                                       | 184 ms: 1.18x faster                                                |
| pickle_dict              | 32.5 us                                                      | 31.1 us: 1.05x faster                                               |
| pickle                   | 11.3 us                                                      | 10.8 us: 1.05x faster                                               |
| xml_etree_parse          | 136 ms                                                       | 132 ms: 1.03x faster                                                |
| pickle_list              | 4.93 us                                                      | 4.90 us: 1.01x faster                                               |
| regex_effbot             | 3.08 ms                                                      | 3.21 ms: 1.04x slower                                               |
| unpickle                 | 14.3 us                                                      | 15.0 us: 1.05x slower                                               |
| json_loads               | 27.0 us                                                      | 28.3 us: 1.05x slower                                               |
| json                     | 4.93 ms                                                      | 5.20 ms: 1.05x slower                                               |
| regex_dna                | 180 ms                                                       | 191 ms: 1.06x slower                                                |
| unpickle_list            | 4.71 us                                                      | 5.14 us: 1.09x slower                                               |
| sqlite_synth             | 2.21 us                                                      | 2.42 us: 1.10x slower                                               |
| regex_v8                 | 22.7 ms                                                      | 25.3 ms: 1.12x slower                                               |
| xml_etree_iterparse      | 94.9 ms                                                      | 106 ms: 1.12x slower                                                |
| pathlib                  | 19.2 ms                                                      | 21.9 ms: 1.14x slower                                               |
| scimark_fft              | 349 ms                                                       | 401 ms: 1.15x slower                                                |
| asyncio_tcp              | 505 ms                                                       | 582 ms: 1.15x slower                                                |
| deepcopy                 | 355 us                                                       | 414 us: 1.17x slower                                                |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 5.52 ms: 1.17x slower                                               |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.82 sec: 1.21x slower                                              |
| coverage                 | 83.0 ms                                                      | 101 ms: 1.21x slower                                                |
| telco                    | 7.82 ms                                                      | 9.53 ms: 1.22x slower                                               |
| coroutines               | 23.6 ms                                                      | 29.2 ms: 1.24x slower                                               |
| docutils                 | 2.62 sec                                                     | 3.28 sec: 1.25x slower                                              |
| xml_etree_generate       | 85.4 ms                                                      | 109 ms: 1.28x slower                                                |
| deepcopy_memo            | 39.1 us                                                      | 50.3 us: 1.29x slower                                               |
| bpe_tokeniser            | 4.45 sec                                                     | 5.76 sec: 1.30x slower                                              |
| pylint                   | 317 ms                                                       | 414 ms: 1.30x slower                                                |
| async_generators         | 377 ms                                                       | 500 ms: 1.32x slower                                                |
| spectral_norm            | 111 ms                                                       | 147 ms: 1.33x slower                                                |
| mdp                      | 2.36 sec                                                     | 3.13 sec: 1.33x slower                                              |
| meteor_contest           | 102 ms                                                       | 136 ms: 1.34x slower                                                |
| dulwich_log              | 74.8 ms                                                      | 102 ms: 1.36x slower                                                |
| python_startup_no_site   | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                               |
| deepcopy_reduce          | 3.11 us                                                      | 4.34 us: 1.40x slower                                               |
| nqueens                  | 78.6 ms                                                      | 111 ms: 1.41x slower                                                |
| json_dumps               | 10.5 ms                                                      | 15.0 ms: 1.42x slower                                               |
| tornado_http             | 114 ms                                                       | 163 ms: 1.43x slower                                                |
| python_startup           | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                               |
| pycparser                | 1.12 sec                                                     | 1.66 sec: 1.49x slower                                              |
| generators               | 28.8 ms                                                      | 43.1 ms: 1.50x slower                                               |
| fannkuch                 | 370 ms                                                       | 554 ms: 1.50x slower                                                |
| xml_etree_process        | 59.3 ms                                                      | 89.1 ms: 1.50x slower                                               |
| html5lib                 | 67.0 ms                                                      | 103 ms: 1.54x slower                                                |
| typing_runtime_protocols | 155 us                                                       | 241 us: 1.56x slower                                                |
| crypto_pyaes             | 67.9 ms                                                      | 107 ms: 1.58x slower                                                |
| 2to3                     | 260 ms                                                       | 410 ms: 1.58x slower                                                |
| tomli_loads              | 2.01 sec                                                     | 3.21 sec: 1.60x slower                                              |
| sqlglot_normalize        | 106 ms                                                       | 172 ms: 1.62x slower                                                |
| sympy_integrate          | 19.8 ms                                                      | 32.2 ms: 1.63x slower                                               |
| thrift                   | 778 us                                                       | 1.28 ms: 1.64x slower                                               |
| sqlglot_optimize         | 52.7 ms                                                      | 86.6 ms: 1.64x slower                                               |
| genshi_xml               | 48.8 ms                                                      | 80.6 ms: 1.65x slower                                               |
| pyflate                  | 449 ms                                                       | 744 ms: 1.66x slower                                                |
| regex_compile            | 132 ms                                                       | 221 ms: 1.67x slower                                                |
| mako                     | 11.3 ms                                                      | 19.3 ms: 1.70x slower                                               |
| pprint_safe_repr         | 738 ms                                                       | 1.26 sec: 1.71x slower                                              |
| pprint_pformat           | 1.50 sec                                                     | 2.61 sec: 1.75x slower                                              |
| comprehensions           | 16.5 us                                                      | 29.5 us: 1.79x slower                                               |
| django_template          | 34.1 ms                                                      | 62.1 ms: 1.82x slower                                               |
| genshi_text              | 21.5 ms                                                      | 39.2 ms: 1.82x slower                                               |
| unpickle_pure_python     | 210 us                                                       | 386 us: 1.84x slower                                                |
| scimark_monte_carlo      | 65.4 ms                                                      | 123 ms: 1.88x slower                                                |
| float                    | 77.5 ms                                                      | 146 ms: 1.89x slower                                                |
| richards                 | 45.2 ms                                                      | 86.3 ms: 1.91x slower                                               |
| logging_format           | 6.84 us                                                      | 13.2 us: 1.93x slower                                               |
| sympy_str                | 275 ms                                                       | 531 ms: 1.93x slower                                                |
| hexiom                   | 5.99 ms                                                      | 11.7 ms: 1.96x slower                                               |
| scimark_sor              | 134 ms                                                       | 263 ms: 1.96x slower                                                |
| logging_simple           | 6.16 us                                                      | 12.1 us: 1.96x slower                                               |
| pickle_pure_python       | 294 us                                                       | 584 us: 1.98x slower                                                |
| richards_super           | 51.6 ms                                                      | 105 ms: 2.03x slower                                                |
| logging_silent           | 103 ns                                                       | 209 ns: 2.04x slower                                                |
| scimark_lu               | 113 ms                                                       | 233 ms: 2.07x slower                                                |
| chaos                    | 57.3 ms                                                      | 119 ms: 2.07x slower                                                |
| sqlglot_transpile        | 1.56 ms                                                      | 3.26 ms: 2.09x slower                                               |
| go                       | 141 ms                                                       | 296 ms: 2.11x slower                                                |
| nbody                    | 85.1 ms                                                      | 186 ms: 2.19x slower                                                |
| sympy_expand             | 457 ms                                                       | 1.04 sec: 2.27x slower                                              |
| sqlglot_parse            | 1.25 ms                                                      | 2.84 ms: 2.27x slower                                               |
| raytrace                 | 253 ms                                                       | 614 ms: 2.43x slower                                                |
| sympy_sum                | 156 ms                                                       | 379 ms: 2.44x slower                                                |
| deltablue                | 3.12 ms                                                      | 8.76 ms: 2.81x slower                                               |
| unpack_sequence          | 44.8 ns                                                      | 133 ns: 2.96x slower                                                |
| bench_thread_pool        | 919 us                                                       | 3.46 ms: 3.77x slower                                               |
| bench_mp_pool            | 11.0 ms                                                      | 71.9 ms: 6.54x slower                                               |
| Geometric mean           | (ref)                                                        | 1.52x slower                                                        |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.44x
- 95% likely to have a slowdown of 1.42x
- 99% likely to have a slowdown of 1.37x

# Memory
- memory change: 1.20x