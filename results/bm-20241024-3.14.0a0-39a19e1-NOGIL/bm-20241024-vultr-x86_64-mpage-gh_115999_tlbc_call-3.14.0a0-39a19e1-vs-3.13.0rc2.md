# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 39a19e1
- commit date: 2024-10-24
- overall geometric mean: 1.51x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.36x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 408 ms: 1.57x slower                                                |
| docutils       | 2.62 sec                                                     | 3.25 sec: 1.24x slower                                              |
| html5lib       | 67.0 ms                                                      | 102 ms: 1.52x slower                                                |
| tornado_http   | 114 ms                                                       | 161 ms: 1.41x slower                                                |
| Geometric mean | (ref)                                                        | 1.43x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| asyncio_tcp      | 505 ms                                                       | 581 ms: 1.15x slower                                                |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.83 sec: 1.21x slower                                              |
| coroutines       | 23.6 ms                                                      | 28.7 ms: 1.22x slower                                               |
| async_generators | 377 ms                                                       | 487 ms: 1.29x slower                                                |
| Geometric mean   | (ref)                                                        | 1.17x slower                                                        |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 223 ms: 1.03x slower                                                |
| float          | 77.5 ms                                                      | 146 ms: 1.88x slower                                                |
| nbody          | 85.1 ms                                                      | 187 ms: 2.20x slower                                                |
| Geometric mean | (ref)                                                        | 1.62x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 3.05 ms: 1.01x faster                                               |
| regex_dna      | 180 ms                                                       | 191 ms: 1.06x slower                                                |
| regex_v8       | 22.7 ms                                                      | 25.8 ms: 1.14x slower                                               |
| regex_compile  | 132 ms                                                       | 215 ms: 1.63x slower                                                |
| Geometric mean | (ref)                                                        | 1.18x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 29.7 us: 1.09x faster                                               |
| pickle_list          | 4.93 us                                                      | 4.74 us: 1.04x faster                                               |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.05x slower                                               |
| unpickle_list        | 4.71 us                                                      | 5.07 us: 1.08x slower                                               |
| xml_etree_iterparse  | 94.9 ms                                                      | 106 ms: 1.11x slower                                                |
| xml_etree_generate   | 85.4 ms                                                      | 108 ms: 1.27x slower                                                |
| json_dumps           | 10.5 ms                                                      | 15.1 ms: 1.43x slower                                               |
| xml_etree_process    | 59.3 ms                                                      | 88.1 ms: 1.49x slower                                               |
| tomli_loads          | 2.01 sec                                                     | 3.18 sec: 1.59x slower                                              |
| unpickle_pure_python | 210 us                                                       | 389 us: 1.85x slower                                                |
| pickle_pure_python   | 294 us                                                       | 572 us: 1.94x slower                                                |
| Geometric mean       | (ref)                                                        | 1.22x slower                                                        |

Benchmark hidden because not significant (2): pickle, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                               |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                               |
| Geometric mean         | (ref)                                                        | 1.41x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 78.9 ms: 1.62x slower                                               |
| mako            | 11.3 ms                                                      | 19.2 ms: 1.69x slower                                               |
| genshi_text     | 21.5 ms                                                      | 38.8 ms: 1.80x slower                                               |
| django_template | 34.1 ms                                                      | 62.3 ms: 1.83x slower                                               |
| Geometric mean  | (ref)                                                        | 1.73x slower                                                        |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241024-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-39a19e1 |
|--------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.48 ms: 1.27x faster                                               |
| create_gc_cycles         | 1.34 ms                                                      | 1.13 ms: 1.18x faster                                               |
| pickle_dict              | 32.5 us                                                      | 29.7 us: 1.09x faster                                               |
| pickle_list              | 4.93 us                                                      | 4.74 us: 1.04x faster                                               |
| xml_etree_parse          | 136 ms                                                       | 131 ms: 1.04x faster                                                |
| regex_effbot             | 3.08 ms                                                      | 3.05 ms: 1.01x faster                                               |
| pidigits                 | 217 ms                                                       | 223 ms: 1.03x slower                                                |
| json_loads               | 27.0 us                                                      | 28.2 us: 1.05x slower                                               |
| json                     | 4.93 ms                                                      | 5.20 ms: 1.06x slower                                               |
| regex_dna                | 180 ms                                                       | 191 ms: 1.06x slower                                                |
| unpickle_list            | 4.71 us                                                      | 5.07 us: 1.08x slower                                               |
| sqlite_synth             | 2.21 us                                                      | 2.44 us: 1.10x slower                                               |
| scimark_fft              | 349 ms                                                       | 387 ms: 1.11x slower                                                |
| xml_etree_iterparse      | 94.9 ms                                                      | 106 ms: 1.11x slower                                                |
| pathlib                  | 19.2 ms                                                      | 21.6 ms: 1.13x slower                                               |
| regex_v8                 | 22.7 ms                                                      | 25.8 ms: 1.14x slower                                               |
| asyncio_tcp              | 505 ms                                                       | 581 ms: 1.15x slower                                                |
| deepcopy                 | 355 us                                                       | 411 us: 1.16x slower                                                |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 5.61 ms: 1.19x slower                                               |
| telco                    | 7.82 ms                                                      | 9.43 ms: 1.21x slower                                               |
| coverage                 | 83.0 ms                                                      | 100 ms: 1.21x slower                                                |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.83 sec: 1.21x slower                                              |
| coroutines               | 23.6 ms                                                      | 28.7 ms: 1.22x slower                                               |
| docutils                 | 2.62 sec                                                     | 3.25 sec: 1.24x slower                                              |
| deepcopy_memo            | 39.1 us                                                      | 49.1 us: 1.26x slower                                               |
| xml_etree_generate       | 85.4 ms                                                      | 108 ms: 1.27x slower                                                |
| async_generators         | 377 ms                                                       | 487 ms: 1.29x slower                                                |
| pylint                   | 317 ms                                                       | 411 ms: 1.30x slower                                                |
| bpe_tokeniser            | 4.45 sec                                                     | 5.79 sec: 1.30x slower                                              |
| spectral_norm            | 111 ms                                                       | 147 ms: 1.33x slower                                                |
| meteor_contest           | 102 ms                                                       | 137 ms: 1.34x slower                                                |
| dulwich_log              | 74.8 ms                                                      | 101 ms: 1.35x slower                                                |
| mdp                      | 2.36 sec                                                     | 3.21 sec: 1.36x slower                                              |
| deepcopy_reduce          | 3.11 us                                                      | 4.29 us: 1.38x slower                                               |
| python_startup_no_site   | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                               |
| tornado_http             | 114 ms                                                       | 161 ms: 1.41x slower                                                |
| python_startup           | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                               |
| nqueens                  | 78.6 ms                                                      | 112 ms: 1.43x slower                                                |
| json_dumps               | 10.5 ms                                                      | 15.1 ms: 1.43x slower                                               |
| generators               | 28.8 ms                                                      | 42.0 ms: 1.46x slower                                               |
| pycparser                | 1.12 sec                                                     | 1.64 sec: 1.47x slower                                              |
| xml_etree_process        | 59.3 ms                                                      | 88.1 ms: 1.49x slower                                               |
| fannkuch                 | 370 ms                                                       | 554 ms: 1.50x slower                                                |
| html5lib                 | 67.0 ms                                                      | 102 ms: 1.52x slower                                                |
| typing_runtime_protocols | 155 us                                                       | 240 us: 1.55x slower                                                |
| 2to3                     | 260 ms                                                       | 408 ms: 1.57x slower                                                |
| crypto_pyaes             | 67.9 ms                                                      | 107 ms: 1.58x slower                                                |
| thrift                   | 778 us                                                       | 1.23 ms: 1.58x slower                                               |
| tomli_loads              | 2.01 sec                                                     | 3.18 sec: 1.59x slower                                              |
| sqlglot_normalize        | 106 ms                                                       | 171 ms: 1.62x slower                                                |
| genshi_xml               | 48.8 ms                                                      | 78.9 ms: 1.62x slower                                               |
| sqlglot_optimize         | 52.7 ms                                                      | 85.5 ms: 1.62x slower                                               |
| sympy_integrate          | 19.8 ms                                                      | 32.2 ms: 1.62x slower                                               |
| regex_compile            | 132 ms                                                       | 215 ms: 1.63x slower                                                |
| pyflate                  | 449 ms                                                       | 735 ms: 1.64x slower                                                |
| mako                     | 11.3 ms                                                      | 19.2 ms: 1.69x slower                                               |
| pprint_safe_repr         | 738 ms                                                       | 1.25 sec: 1.69x slower                                              |
| pprint_pformat           | 1.50 sec                                                     | 2.60 sec: 1.74x slower                                              |
| comprehensions           | 16.5 us                                                      | 29.2 us: 1.78x slower                                               |
| genshi_text              | 21.5 ms                                                      | 38.8 ms: 1.80x slower                                               |
| django_template          | 34.1 ms                                                      | 62.3 ms: 1.83x slower                                               |
| unpickle_pure_python     | 210 us                                                       | 389 us: 1.85x slower                                                |
| scimark_monte_carlo      | 65.4 ms                                                      | 122 ms: 1.87x slower                                                |
| float                    | 77.5 ms                                                      | 146 ms: 1.88x slower                                                |
| richards                 | 45.2 ms                                                      | 85.4 ms: 1.89x slower                                               |
| sympy_str                | 275 ms                                                       | 526 ms: 1.92x slower                                                |
| logging_format           | 6.84 us                                                      | 13.2 us: 1.93x slower                                               |
| logging_simple           | 6.16 us                                                      | 11.9 us: 1.93x slower                                               |
| scimark_sor              | 134 ms                                                       | 261 ms: 1.94x slower                                                |
| pickle_pure_python       | 294 us                                                       | 572 us: 1.94x slower                                                |
| chaos                    | 57.3 ms                                                      | 112 ms: 1.96x slower                                                |
| hexiom                   | 5.99 ms                                                      | 11.8 ms: 1.97x slower                                               |
| richards_super           | 51.6 ms                                                      | 103 ms: 1.99x slower                                                |
| logging_silent           | 103 ns                                                       | 210 ns: 2.05x slower                                                |
| go                       | 141 ms                                                       | 290 ms: 2.06x slower                                                |
| scimark_lu               | 113 ms                                                       | 233 ms: 2.06x slower                                                |
| sqlglot_transpile        | 1.56 ms                                                      | 3.26 ms: 2.09x slower                                               |
| nbody                    | 85.1 ms                                                      | 187 ms: 2.20x slower                                                |
| sqlglot_parse            | 1.25 ms                                                      | 2.82 ms: 2.26x slower                                               |
| sympy_expand             | 457 ms                                                       | 1.03 sec: 2.26x slower                                              |
| raytrace                 | 253 ms                                                       | 580 ms: 2.30x slower                                                |
| sympy_sum                | 156 ms                                                       | 376 ms: 2.42x slower                                                |
| deltablue                | 3.12 ms                                                      | 8.61 ms: 2.76x slower                                               |
| unpack_sequence          | 44.8 ns                                                      | 137 ns: 3.05x slower                                                |
| bench_thread_pool        | 919 us                                                       | 3.45 ms: 3.76x slower                                               |
| bench_mp_pool            | 11.0 ms                                                      | 71.7 ms: 6.52x slower                                               |
| Geometric mean           | (ref)                                                        | 1.51x slower                                                        |

Benchmark hidden because not significant (3): asyncio_websockets, pickle, unpickle
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.43x
- 95% likely to have a slowdown of 1.42x
- 99% likely to have a slowdown of 1.36x

# Memory
- memory change: 1.21x