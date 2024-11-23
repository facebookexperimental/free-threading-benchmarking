# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 4c7837f
- commit date: 2024-11-21
- overall geometric mean: 1.54x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 411 ms: 1.58x slower                                                 |
| docutils       | 2.62 sec                                                     | 3.32 sec: 1.27x slower                                               |
| html5lib       | 67.0 ms                                                      | 106 ms: 1.59x slower                                                 |
| Geometric mean | (ref)                                                        | 1.47x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 657 ms: 1.03x slower                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 687 ms: 1.03x slower                                                 |
| async_tree_io              | 876 ms                                                       | 941 ms: 1.07x slower                                                 |
| async_tree_memoization     | 461 ms                                                       | 512 ms: 1.11x slower                                                 |
| async_tree_none_tg         | 336 ms                                                       | 382 ms: 1.13x slower                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 481 ms: 1.16x slower                                                 |
| async_tree_none            | 354 ms                                                       | 421 ms: 1.19x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 29.2 ms: 1.24x slower                                                |
| async_generators           | 377 ms                                                       | 481 ms: 1.28x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.11x slower                                                         |

Benchmark hidden because not significant (2): async_tree_io_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 183 ms: 1.18x faster                                                 |
| float          | 77.5 ms                                                      | 148 ms: 1.91x slower                                                 |
| nbody          | 85.1 ms                                                      | 200 ms: 2.36x slower                                                 |
| Geometric mean | (ref)                                                        | 1.56x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.81 ms: 1.10x faster                                                |
| regex_dna      | 180 ms                                                       | 185 ms: 1.03x slower                                                 |
| regex_v8       | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                |
| regex_compile  | 132 ms                                                       | 219 ms: 1.65x slower                                                 |
| Geometric mean | (ref)                                                        | 1.14x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.03x faster                                                 |
| json_loads           | 27.0 us                                                      | 28.3 us: 1.05x slower                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 105 ms: 1.11x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 110 ms: 1.28x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 15.5 ms: 1.47x slower                                                |
| xml_etree_process    | 59.3 ms                                                      | 90.0 ms: 1.52x slower                                                |
| tomli_loads          | 2.01 sec                                                     | 3.16 sec: 1.57x slower                                               |
| unpickle_pure_python | 210 us                                                       | 388 us: 1.85x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 598 us: 2.03x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.39x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                |
| python_startup         | 11.0 ms                                                      | 17.6 ms: 1.60x slower                                                |
| Geometric mean         | (ref)                                                        | 1.49x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 81.0 ms: 1.66x slower                                                |
| mako            | 11.3 ms                                                      | 19.2 ms: 1.69x slower                                                |
| genshi_text     | 21.5 ms                                                      | 39.2 ms: 1.82x slower                                                |
| django_template | 34.1 ms                                                      | 62.3 ms: 1.82x slower                                                |
| Geometric mean  | (ref)                                                        | 1.75x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 183 ms: 1.18x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.81 ms: 1.10x faster                                                |
| xml_etree_parse            | 136 ms                                                       | 133 ms: 1.03x faster                                                 |
| regex_dna                  | 180 ms                                                       | 185 ms: 1.03x slower                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 657 ms: 1.03x slower                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 687 ms: 1.03x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.3 us: 1.05x slower                                                |
| json                       | 4.93 ms                                                      | 5.17 ms: 1.05x slower                                                |
| async_tree_io              | 876 ms                                                       | 941 ms: 1.07x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.42 us: 1.09x slower                                                |
| regex_v8                   | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                |
| async_tree_memoization     | 461 ms                                                       | 512 ms: 1.11x slower                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 105 ms: 1.11x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.50 ms: 1.11x slower                                                |
| pathlib                    | 19.2 ms                                                      | 21.6 ms: 1.13x slower                                                |
| async_tree_none_tg         | 336 ms                                                       | 382 ms: 1.13x slower                                                 |
| deepcopy                   | 355 us                                                       | 413 us: 1.16x slower                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 481 ms: 1.16x slower                                                 |
| async_tree_none            | 354 ms                                                       | 421 ms: 1.19x slower                                                 |
| scimark_fft                | 349 ms                                                       | 417 ms: 1.19x slower                                                 |
| telco                      | 7.82 ms                                                      | 9.46 ms: 1.21x slower                                                |
| coverage                   | 83.0 ms                                                      | 101 ms: 1.21x slower                                                 |
| deepcopy_memo              | 39.1 us                                                      | 48.4 us: 1.24x slower                                                |
| coroutines                 | 23.6 ms                                                      | 29.2 ms: 1.24x slower                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.92 ms: 1.26x slower                                                |
| docutils                   | 2.62 sec                                                     | 3.32 sec: 1.27x slower                                               |
| async_generators           | 377 ms                                                       | 481 ms: 1.28x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 5.69 sec: 1.28x slower                                               |
| xml_etree_generate         | 85.4 ms                                                      | 110 ms: 1.28x slower                                                 |
| mdp                        | 2.36 sec                                                     | 3.03 sec: 1.29x slower                                               |
| pylint                     | 317 ms                                                       | 416 ms: 1.31x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.83 ms: 1.37x slower                                                |
| dulwich_log                | 74.8 ms                                                      | 103 ms: 1.38x slower                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 4.33 us: 1.39x slower                                                |
| python_startup_no_site     | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                |
| meteor_contest             | 102 ms                                                       | 143 ms: 1.40x slower                                                 |
| spectral_norm              | 111 ms                                                       | 158 ms: 1.42x slower                                                 |
| generators                 | 28.8 ms                                                      | 41.1 ms: 1.43x slower                                                |
| nqueens                    | 78.6 ms                                                      | 113 ms: 1.44x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 15.5 ms: 1.47x slower                                                |
| fannkuch                   | 370 ms                                                       | 551 ms: 1.49x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.67 sec: 1.49x slower                                               |
| xml_etree_process          | 59.3 ms                                                      | 90.0 ms: 1.52x slower                                                |
| typing_runtime_protocols   | 155 us                                                       | 243 us: 1.57x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 3.16 sec: 1.57x slower                                               |
| 2to3                       | 260 ms                                                       | 411 ms: 1.58x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 106 ms: 1.59x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 108 ms: 1.59x slower                                                 |
| python_startup             | 11.0 ms                                                      | 17.6 ms: 1.60x slower                                                |
| thrift                     | 778 us                                                       | 1.26 ms: 1.62x slower                                                |
| sqlglot_optimize           | 52.7 ms                                                      | 85.9 ms: 1.63x slower                                                |
| sqlglot_normalize          | 106 ms                                                       | 174 ms: 1.64x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 32.6 ms: 1.64x slower                                                |
| regex_compile              | 132 ms                                                       | 219 ms: 1.65x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 81.0 ms: 1.66x slower                                                |
| pyflate                    | 449 ms                                                       | 752 ms: 1.68x slower                                                 |
| mako                       | 11.3 ms                                                      | 19.2 ms: 1.69x slower                                                |
| pprint_safe_repr           | 738 ms                                                       | 1.25 sec: 1.70x slower                                               |
| pprint_pformat             | 1.50 sec                                                     | 2.60 sec: 1.73x slower                                               |
| comprehensions             | 16.5 us                                                      | 29.5 us: 1.79x slower                                                |
| genshi_text                | 21.5 ms                                                      | 39.2 ms: 1.82x slower                                                |
| django_template            | 34.1 ms                                                      | 62.3 ms: 1.82x slower                                                |
| unpickle_pure_python       | 210 us                                                       | 388 us: 1.85x slower                                                 |
| float                      | 77.5 ms                                                      | 148 ms: 1.91x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 125 ms: 1.91x slower                                                 |
| logging_format             | 6.84 us                                                      | 13.1 us: 1.92x slower                                                |
| logging_simple             | 6.16 us                                                      | 11.9 us: 1.94x slower                                                |
| sympy_str                  | 275 ms                                                       | 533 ms: 1.94x slower                                                 |
| richards                   | 45.2 ms                                                      | 88.1 ms: 1.95x slower                                                |
| hexiom                     | 5.99 ms                                                      | 11.8 ms: 1.97x slower                                                |
| scimark_sor                | 134 ms                                                       | 267 ms: 1.98x slower                                                 |
| logging_silent             | 103 ns                                                       | 208 ns: 2.03x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 598 us: 2.03x slower                                                 |
| chaos                      | 57.3 ms                                                      | 117 ms: 2.05x slower                                                 |
| richards_super             | 51.6 ms                                                      | 106 ms: 2.05x slower                                                 |
| go                         | 141 ms                                                       | 291 ms: 2.07x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 236 ms: 2.09x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 3.30 ms: 2.12x slower                                                |
| sqlglot_parse              | 1.25 ms                                                      | 2.80 ms: 2.24x slower                                                |
| sympy_expand               | 457 ms                                                       | 1.04 sec: 2.28x slower                                               |
| nbody                      | 85.1 ms                                                      | 200 ms: 2.36x slower                                                 |
| raytrace                   | 253 ms                                                       | 602 ms: 2.38x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 379 ms: 2.44x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 8.79 ms: 2.81x slower                                                |
| bench_thread_pool          | 919 us                                                       | 3.50 ms: 3.81x slower                                                |
| bench_mp_pool              | 11.0 ms                                                      | 111 ms: 10.12x slower                                                |
| Geometric mean             | (ref)                                                        | 1.54x slower                                                         |

Benchmark hidden because not significant (2): async_tree_io_tg, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241121-3.14.0a2+-4c7837f-NOGIL/bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.37x
- 95% likely to have a slowdown of 1.33x
- 99% likely to have a slowdown of 1.28x

# Memory
- memory change: 1.31x