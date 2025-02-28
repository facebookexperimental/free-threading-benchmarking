# Results vs. 3.13.0rc2

- fork: mpage
- ref: all_blocks
- machine: linux-x86_64
- commit hash: 9ad230b
- commit date: 2025-02-27
- overall geometric mean: 1.061x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 296 ms: 1.14x slower                                        |
| docutils       | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                      |
| html5lib       | 68.6 ms                                                                | 68.9 ms: 1.00x slower                                       |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 532 ms: 1.69x faster                                        |
| async_tree_io              | 881 ms                                                                 | 563 ms: 1.57x faster                                        |
| async_tree_none_tg         | 333 ms                                                                 | 231 ms: 1.44x faster                                        |
| async_tree_memoization     | 459 ms                                                                 | 330 ms: 1.39x faster                                        |
| async_tree_memoization_tg  | 410 ms                                                                 | 297 ms: 1.38x faster                                        |
| async_tree_none            | 353 ms                                                                 | 270 ms: 1.31x faster                                        |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 530 ms: 1.20x faster                                        |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 562 ms: 1.19x faster                                        |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                        |
| coroutines                 | 23.3 ms                                                                | 24.1 ms: 1.03x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 76.7 ms                                                                | 70.7 ms: 1.09x faster                                       |
| pidigits       | 216 ms                                                                 | 216 ms: 1.00x faster                                        |
| nbody          | 85.3 ms                                                                | 120 ms: 1.41x slower                                        |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.74 ms: 1.17x faster                                       |
| regex_dna      | 189 ms                                                                 | 183 ms: 1.03x faster                                        |
| regex_v8       | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                       |
| regex_compile  | 131 ms                                                                 | 151 ms: 1.15x slower                                        |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.1 ms: 1.07x faster                                       |
| xml_etree_parse      | 136 ms                                                                 | 127 ms: 1.07x faster                                        |
| json_loads           | 27.3 us                                                                | 29.6 us: 1.08x slower                                       |
| tomli_loads          | 2.01 sec                                                               | 2.20 sec: 1.09x slower                                      |
| xml_etree_generate   | 85.4 ms                                                                | 95.7 ms: 1.12x slower                                       |
| unpickle_pure_python | 208 us                                                                 | 236 us: 1.13x slower                                        |
| pickle_pure_python   | 292 us                                                                 | 342 us: 1.17x slower                                        |
| xml_etree_process    | 59.2 ms                                                                | 69.5 ms: 1.17x slower                                       |
| json_dumps           | 10.6 ms                                                                | 12.6 ms: 1.19x slower                                       |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.64 ms: 1.30x slower                                       |
| python_startup         | 11.0 ms                                                                | 15.6 ms: 1.42x slower                                       |
| Geometric mean         | (ref)                                                                  | 1.36x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 57.8 ms: 1.18x slower                                       |
| genshi_text     | 21.7 ms                                                                | 26.5 ms: 1.22x slower                                       |
| django_template | 34.2 ms                                                                | 42.1 ms: 1.23x slower                                       |
| mako            | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                       |
| Geometric mean  | (ref)                                                                  | 1.25x slower                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.71 ms: 1.94x faster                                       |
| async_tree_io_tg           | 901 ms                                                                 | 532 ms: 1.69x faster                                        |
| async_tree_io              | 881 ms                                                                 | 563 ms: 1.57x faster                                        |
| async_tree_none_tg         | 333 ms                                                                 | 231 ms: 1.44x faster                                        |
| async_tree_memoization     | 459 ms                                                                 | 330 ms: 1.39x faster                                        |
| async_tree_memoization_tg  | 410 ms                                                                 | 297 ms: 1.38x faster                                        |
| async_tree_none            | 353 ms                                                                 | 270 ms: 1.31x faster                                        |
| deepcopy                   | 357 us                                                                 | 294 us: 1.22x faster                                        |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 530 ms: 1.20x faster                                        |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 562 ms: 1.19x faster                                        |
| regex_effbot               | 3.21 ms                                                                | 2.74 ms: 1.17x faster                                       |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                       |
| go                         | 141 ms                                                                 | 129 ms: 1.09x faster                                        |
| float                      | 76.7 ms                                                                | 70.7 ms: 1.09x faster                                       |
| deepcopy_memo              | 38.1 us                                                                | 35.3 us: 1.08x faster                                       |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.1 ms: 1.07x faster                                       |
| xml_etree_parse            | 136 ms                                                                 | 127 ms: 1.07x faster                                        |
| create_gc_cycles           | 1.33 ms                                                                | 1.30 ms: 1.03x faster                                       |
| deepcopy_reduce            | 3.12 us                                                                | 3.03 us: 1.03x faster                                       |
| regex_dna                  | 189 ms                                                                 | 183 ms: 1.03x faster                                        |
| pidigits                   | 216 ms                                                                 | 216 ms: 1.00x faster                                        |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                        |
| html5lib                   | 68.6 ms                                                                | 68.9 ms: 1.00x slower                                       |
| pathlib                    | 19.3 ms                                                                | 19.5 ms: 1.01x slower                                       |
| json                       | 4.98 ms                                                                | 5.06 ms: 1.01x slower                                       |
| scimark_sor                | 134 ms                                                                 | 136 ms: 1.02x slower                                        |
| regex_v8                   | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                       |
| coroutines                 | 23.3 ms                                                                | 24.1 ms: 1.03x slower                                       |
| bpe_tokeniser              | 4.46 sec                                                               | 4.62 sec: 1.04x slower                                      |
| pycparser                  | 1.12 sec                                                               | 1.17 sec: 1.05x slower                                      |
| docutils                   | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                      |
| pyflate                    | 449 ms                                                                 | 478 ms: 1.06x slower                                        |
| logging_silent             | 98.2 ns                                                                | 106 ns: 1.08x slower                                        |
| json_loads                 | 27.3 us                                                                | 29.6 us: 1.08x slower                                       |
| tomli_loads                | 2.01 sec                                                               | 2.20 sec: 1.09x slower                                      |
| mdp                        | 2.34 sec                                                               | 2.57 sec: 1.10x slower                                      |
| dulwich_log                | 74.5 ms                                                                | 82.1 ms: 1.10x slower                                       |
| pprint_safe_repr           | 719 ms                                                                 | 793 ms: 1.10x slower                                        |
| telco                      | 7.77 ms                                                                | 8.60 ms: 1.11x slower                                       |
| xml_etree_generate         | 85.4 ms                                                                | 95.7 ms: 1.12x slower                                       |
| pprint_pformat             | 1.46 sec                                                               | 1.63 sec: 1.12x slower                                      |
| sqlglot_normalize          | 106 ms                                                                 | 119 ms: 1.13x slower                                        |
| thrift                     | 772 us                                                                 | 872 us: 1.13x slower                                        |
| unpickle_pure_python       | 208 us                                                                 | 236 us: 1.13x slower                                        |
| 2to3                       | 259 ms                                                                 | 296 ms: 1.14x slower                                        |
| sqlglot_optimize           | 52.7 ms                                                                | 60.3 ms: 1.15x slower                                       |
| regex_compile              | 131 ms                                                                 | 151 ms: 1.15x slower                                        |
| generators                 | 28.5 ms                                                                | 33.0 ms: 1.16x slower                                       |
| sqlglot_transpile          | 1.55 ms                                                                | 1.81 ms: 1.17x slower                                       |
| logging_simple             | 6.14 us                                                                | 7.16 us: 1.17x slower                                       |
| comprehensions             | 16.6 us                                                                | 19.4 us: 1.17x slower                                       |
| deltablue                  | 3.10 ms                                                                | 3.62 ms: 1.17x slower                                       |
| coverage                   | 82.5 ms                                                                | 96.5 ms: 1.17x slower                                       |
| pickle_pure_python         | 292 us                                                                 | 342 us: 1.17x slower                                        |
| xml_etree_process          | 59.2 ms                                                                | 69.5 ms: 1.17x slower                                       |
| chaos                      | 56.3 ms                                                                | 66.1 ms: 1.17x slower                                       |
| genshi_xml                 | 49.1 ms                                                                | 57.8 ms: 1.18x slower                                       |
| logging_format             | 6.92 us                                                                | 8.19 us: 1.18x slower                                       |
| richards                   | 44.4 ms                                                                | 52.6 ms: 1.18x slower                                       |
| json_dumps                 | 10.6 ms                                                                | 12.6 ms: 1.19x slower                                       |
| sqlglot_parse              | 1.25 ms                                                                | 1.49 ms: 1.20x slower                                       |
| sympy_integrate            | 19.7 ms                                                                | 23.6 ms: 1.20x slower                                       |
| sympy_expand               | 454 ms                                                                 | 545 ms: 1.20x slower                                        |
| raytrace                   | 250 ms                                                                 | 300 ms: 1.20x slower                                        |
| sympy_sum                  | 154 ms                                                                 | 185 ms: 1.20x slower                                        |
| hexiom                     | 5.95 ms                                                                | 7.15 ms: 1.20x slower                                       |
| sympy_str                  | 274 ms                                                                 | 331 ms: 1.21x slower                                        |
| richards_super             | 50.4 ms                                                                | 61.1 ms: 1.21x slower                                       |
| genshi_text                | 21.7 ms                                                                | 26.5 ms: 1.22x slower                                       |
| nqueens                    | 77.7 ms                                                                | 94.7 ms: 1.22x slower                                       |
| django_template            | 34.2 ms                                                                | 42.1 ms: 1.23x slower                                       |
| meteor_contest             | 101 ms                                                                 | 125 ms: 1.24x slower                                        |
| crypto_pyaes               | 68.2 ms                                                                | 84.9 ms: 1.24x slower                                       |
| fannkuch                   | 376 ms                                                                 | 471 ms: 1.25x slower                                        |
| typing_runtime_protocols   | 156 us                                                                 | 196 us: 1.26x slower                                        |
| python_startup_no_site     | 7.41 ms                                                                | 9.64 ms: 1.30x slower                                       |
| scimark_fft                | 348 ms                                                                 | 454 ms: 1.30x slower                                        |
| scimark_monte_carlo        | 65.8 ms                                                                | 89.1 ms: 1.35x slower                                       |
| scimark_lu                 | 112 ms                                                                 | 153 ms: 1.36x slower                                        |
| mako                       | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                       |
| nbody                      | 85.3 ms                                                                | 120 ms: 1.41x slower                                        |
| python_startup             | 11.0 ms                                                                | 15.6 ms: 1.42x slower                                       |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 7.38 ms: 1.55x slower                                       |
| bench_thread_pool          | 924 us                                                                 | 3.27 ms: 3.53x slower                                       |
| bench_mp_pool              | 11.0 ms                                                                | 95.3 ms: 8.66x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.11x slower                                                |

Benchmark hidden because not significant (3): pylint, async_generators, spectral_norm
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250227-3.14.0a5+-9ad230b-NOGIL/bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.061x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.34x