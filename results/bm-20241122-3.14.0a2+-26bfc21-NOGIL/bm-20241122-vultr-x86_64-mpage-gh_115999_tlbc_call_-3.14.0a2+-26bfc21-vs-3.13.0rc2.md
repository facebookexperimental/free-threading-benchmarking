# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: 26bfc21
- commit date: 2024-11-22
- overall geometric mean: 1.46x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 381 ms: 1.47x slower                                                  |
| docutils       | 2.62 sec                                                     | 3.21 sec: 1.23x slower                                                |
| html5lib       | 67.0 ms                                                      | 99.7 ms: 1.49x slower                                                 |
| Geometric mean | (ref)                                                        | 1.39x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|---------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg          | 913 ms                                                       | 887 ms: 1.03x faster                                                  |
| async_tree_io             | 876 ms                                                       | 912 ms: 1.04x slower                                                  |
| async_tree_memoization    | 461 ms                                                       | 500 ms: 1.08x slower                                                  |
| async_tree_none_tg        | 336 ms                                                       | 377 ms: 1.12x slower                                                  |
| async_tree_memoization_tg | 414 ms                                                       | 472 ms: 1.14x slower                                                  |
| async_tree_none           | 354 ms                                                       | 412 ms: 1.16x slower                                                  |
| coroutines                | 23.6 ms                                                      | 27.5 ms: 1.17x slower                                                 |
| async_generators          | 377 ms                                                       | 473 ms: 1.25x slower                                                  |
| Geometric mean            | (ref)                                                        | 1.08x slower                                                          |

Benchmark hidden because not significant (3): asyncio_websockets, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| nbody          | 85.1 ms                                                      | 158 ms: 1.86x slower                                                  |
| float          | 77.5 ms                                                      | 146 ms: 1.88x slower                                                  |
| Geometric mean | (ref)                                                        | 1.44x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                 |
| regex_dna      | 180 ms                                                       | 181 ms: 1.01x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 25.3 ms: 1.11x slower                                                 |
| regex_compile  | 132 ms                                                       | 196 ms: 1.48x slower                                                  |
| Geometric mean | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 95.6 ms: 1.01x slower                                                 |
| json_loads           | 27.0 us                                                      | 27.9 us: 1.03x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 103 ms: 1.21x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 14.5 ms: 1.38x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 82.6 ms: 1.39x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.88 sec: 1.44x slower                                                |
| unpickle_pure_python | 210 us                                                       | 371 us: 1.77x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 545 us: 1.85x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.30x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                 |
| python_startup         | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.49x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 68.1 ms: 1.40x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 34.2 ms: 1.59x slower                                                 |
| django_template | 34.1 ms                                                      | 55.5 ms: 1.63x slower                                                 |
| mako            | 11.3 ms                                                      | 19.7 ms: 1.74x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.58x slower                                                          |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|---------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                  | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| regex_effbot              | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                 |
| xml_etree_parse           | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| async_tree_io_tg          | 913 ms                                                       | 887 ms: 1.03x faster                                                  |
| regex_dna                 | 180 ms                                                       | 181 ms: 1.01x slower                                                  |
| xml_etree_iterparse       | 94.9 ms                                                      | 95.6 ms: 1.01x slower                                                 |
| json                      | 4.93 ms                                                      | 5.05 ms: 1.03x slower                                                 |
| json_loads                | 27.0 us                                                      | 27.9 us: 1.03x slower                                                 |
| async_tree_io             | 876 ms                                                       | 912 ms: 1.04x slower                                                  |
| sqlite_synth              | 2.21 us                                                      | 2.31 us: 1.05x slower                                                 |
| pathlib                   | 19.2 ms                                                      | 20.7 ms: 1.08x slower                                                 |
| async_tree_memoization    | 461 ms                                                       | 500 ms: 1.08x slower                                                  |
| regex_v8                  | 22.7 ms                                                      | 25.3 ms: 1.11x slower                                                 |
| gc_traversal              | 3.14 ms                                                      | 3.51 ms: 1.12x slower                                                 |
| async_tree_none_tg        | 336 ms                                                       | 377 ms: 1.12x slower                                                  |
| async_tree_memoization_tg | 414 ms                                                       | 472 ms: 1.14x slower                                                  |
| spectral_norm             | 111 ms                                                       | 127 ms: 1.14x slower                                                  |
| scimark_fft               | 349 ms                                                       | 401 ms: 1.15x slower                                                  |
| deepcopy_memo             | 39.1 us                                                      | 45.2 us: 1.16x slower                                                 |
| async_tree_none           | 354 ms                                                       | 412 ms: 1.16x slower                                                  |
| coroutines                | 23.6 ms                                                      | 27.5 ms: 1.17x slower                                                 |
| telco                     | 7.82 ms                                                      | 9.12 ms: 1.17x slower                                                 |
| xml_etree_generate        | 85.4 ms                                                      | 103 ms: 1.21x slower                                                  |
| coverage                  | 83.0 ms                                                      | 101 ms: 1.22x slower                                                  |
| deepcopy_reduce           | 3.11 us                                                      | 3.79 us: 1.22x slower                                                 |
| docutils                  | 2.62 sec                                                     | 3.21 sec: 1.23x slower                                                |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.80 ms: 1.23x slower                                                 |
| pylint                    | 317 ms                                                       | 396 ms: 1.25x slower                                                  |
| async_generators          | 377 ms                                                       | 473 ms: 1.25x slower                                                  |
| bpe_tokeniser             | 4.45 sec                                                     | 5.64 sec: 1.27x slower                                                |
| mdp                       | 2.36 sec                                                     | 3.02 sec: 1.28x slower                                                |
| dulwich_log               | 74.8 ms                                                      | 98.7 ms: 1.32x slower                                                 |
| meteor_contest            | 102 ms                                                       | 136 ms: 1.34x slower                                                  |
| generators                | 28.8 ms                                                      | 39.0 ms: 1.35x slower                                                 |
| typing_runtime_protocols  | 155 us                                                       | 211 us: 1.36x slower                                                  |
| nqueens                   | 78.6 ms                                                      | 108 ms: 1.37x slower                                                  |
| json_dumps                | 10.5 ms                                                      | 14.5 ms: 1.38x slower                                                 |
| create_gc_cycles          | 1.34 ms                                                      | 1.85 ms: 1.38x slower                                                 |
| xml_etree_process         | 59.3 ms                                                      | 82.6 ms: 1.39x slower                                                 |
| python_startup_no_site    | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                 |
| genshi_xml                | 48.8 ms                                                      | 68.1 ms: 1.40x slower                                                 |
| sqlglot_normalize         | 106 ms                                                       | 149 ms: 1.41x slower                                                  |
| sqlglot_optimize          | 52.7 ms                                                      | 75.5 ms: 1.43x slower                                                 |
| tomli_loads               | 2.01 sec                                                     | 2.88 sec: 1.44x slower                                                |
| pycparser                 | 1.12 sec                                                     | 1.61 sec: 1.44x slower                                                |
| pprint_safe_repr          | 738 ms                                                       | 1.07 sec: 1.45x slower                                                |
| 2to3                      | 260 ms                                                       | 381 ms: 1.47x slower                                                  |
| regex_compile             | 132 ms                                                       | 196 ms: 1.48x slower                                                  |
| fannkuch                  | 370 ms                                                       | 550 ms: 1.49x slower                                                  |
| html5lib                  | 67.0 ms                                                      | 99.7 ms: 1.49x slower                                                 |
| pprint_pformat            | 1.50 sec                                                     | 2.23 sec: 1.49x slower                                                |
| crypto_pyaes              | 67.9 ms                                                      | 103 ms: 1.52x slower                                                  |
| thrift                    | 778 us                                                       | 1.21 ms: 1.55x slower                                                 |
| sympy_integrate           | 19.8 ms                                                      | 31.3 ms: 1.58x slower                                                 |
| genshi_text               | 21.5 ms                                                      | 34.2 ms: 1.59x slower                                                 |
| python_startup            | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                 |
| django_template           | 34.1 ms                                                      | 55.5 ms: 1.63x slower                                                 |
| pyflate                   | 449 ms                                                       | 738 ms: 1.65x slower                                                  |
| mako                      | 11.3 ms                                                      | 19.7 ms: 1.74x slower                                                 |
| comprehensions            | 16.5 us                                                      | 28.9 us: 1.75x slower                                                 |
| unpickle_pure_python      | 210 us                                                       | 371 us: 1.77x slower                                                  |
| logging_simple            | 6.16 us                                                      | 11.1 us: 1.80x slower                                                 |
| logging_format            | 6.84 us                                                      | 12.3 us: 1.80x slower                                                 |
| scimark_sor               | 134 ms                                                       | 243 ms: 1.81x slower                                                  |
| sympy_str                 | 275 ms                                                       | 497 ms: 1.81x slower                                                  |
| scimark_lu                | 113 ms                                                       | 205 ms: 1.82x slower                                                  |
| richards                  | 45.2 ms                                                      | 83.6 ms: 1.85x slower                                                 |
| pickle_pure_python        | 294 us                                                       | 545 us: 1.85x slower                                                  |
| scimark_monte_carlo       | 65.4 ms                                                      | 121 ms: 1.86x slower                                                  |
| nbody                     | 85.1 ms                                                      | 158 ms: 1.86x slower                                                  |
| float                     | 77.5 ms                                                      | 146 ms: 1.88x slower                                                  |
| hexiom                    | 5.99 ms                                                      | 11.4 ms: 1.90x slower                                                 |
| logging_silent            | 103 ns                                                       | 195 ns: 1.90x slower                                                  |
| richards_super            | 51.6 ms                                                      | 99.7 ms: 1.93x slower                                                 |
| sqlglot_transpile         | 1.56 ms                                                      | 3.09 ms: 1.98x slower                                                 |
| chaos                     | 57.3 ms                                                      | 115 ms: 2.01x slower                                                  |
| go                        | 141 ms                                                       | 284 ms: 2.02x slower                                                  |
| sqlglot_parse             | 1.25 ms                                                      | 2.68 ms: 2.14x slower                                                 |
| sympy_expand              | 457 ms                                                       | 991 ms: 2.17x slower                                                  |
| sympy_sum                 | 156 ms                                                       | 358 ms: 2.30x slower                                                  |
| raytrace                  | 253 ms                                                       | 601 ms: 2.38x slower                                                  |
| deltablue                 | 3.12 ms                                                      | 8.65 ms: 2.77x slower                                                 |
| bench_thread_pool         | 919 us                                                       | 3.42 ms: 3.72x slower                                                 |
| bench_mp_pool             | 11.0 ms                                                      | 110 ms: 10.00x slower                                                 |
| Geometric mean            | (ref)                                                        | 1.46x slower                                                          |

Benchmark hidden because not significant (4): asyncio_websockets, deepcopy, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241122-3.14.0a2+-26bfc21-NOGIL/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.30x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.31x