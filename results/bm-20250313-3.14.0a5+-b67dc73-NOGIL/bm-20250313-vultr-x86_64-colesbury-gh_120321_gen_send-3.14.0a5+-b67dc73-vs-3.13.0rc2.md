# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_120321_gen_send
- machine: linux-x86_64
- commit hash: b67dc73
- commit date: 2025-03-13
- overall geometric mean: 1.083x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5+-b67dc73 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 300 ms: 1.16x slower                                                    |
| docutils       | 2.63 sec                                                               | 2.81 sec: 1.07x slower                                                  |
| html5lib       | 68.6 ms                                                                | 71.7 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5+-b67dc73 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 557 ms: 1.62x faster                                                    |
| async_tree_io              | 881 ms                                                                 | 587 ms: 1.50x faster                                                    |
| async_tree_none_tg         | 333 ms                                                                 | 238 ms: 1.40x faster                                                    |
| async_tree_memoization     | 459 ms                                                                 | 338 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 490 ms: 1.29x faster                                                    |
| async_tree_none            | 353 ms                                                                 | 275 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 523 ms: 1.27x faster                                                    |
| async_generators           | 375 ms                                                                 | 380 ms: 1.01x slower                                                    |
| coroutines                 | 23.3 ms                                                                | 24.3 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5+-b67dc73 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 199 ms: 1.09x faster                                                    |
| float          | 76.7 ms                                                                | 77.8 ms: 1.01x slower                                                   |
| nbody          | 85.3 ms                                                                | 136 ms: 1.59x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5+-b67dc73 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.71 ms: 1.19x faster                                                   |
| regex_dna      | 189 ms                                                                 | 182 ms: 1.04x faster                                                    |
| regex_v8       | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                                   |
| regex_compile  | 131 ms                                                                 | 156 ms: 1.19x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5+-b67dc73 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 89.9 ms: 1.05x faster                                                   |
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.05x faster                                                    |
| json_loads           | 27.3 us                                                                | 29.3 us: 1.07x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                                | 96.9 ms: 1.13x slower                                                   |
| tomli_loads          | 2.01 sec                                                               | 2.34 sec: 1.17x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 70.8 ms: 1.20x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                                   |
| unpickle_pure_python | 208 us                                                                 | 252 us: 1.21x slower                                                    |
| pickle_pure_python   | 292 us                                                                 | 356 us: 1.22x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5+-b67dc73 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                   |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.46x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5+-b67dc73 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 42.5 ms: 1.24x slower                                                   |
| genshi_xml      | 49.1 ms                                                                | 61.8 ms: 1.26x slower                                                   |
| genshi_text     | 21.7 ms                                                                | 29.3 ms: 1.35x slower                                                   |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.31x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5+-b67dc73 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.72 ms: 1.93x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 557 ms: 1.62x faster                                                    |
| async_tree_io              | 881 ms                                                                 | 587 ms: 1.50x faster                                                    |
| async_tree_none_tg         | 333 ms                                                                 | 238 ms: 1.40x faster                                                    |
| async_tree_memoization     | 459 ms                                                                 | 338 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 490 ms: 1.29x faster                                                    |
| async_tree_none            | 353 ms                                                                 | 275 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 523 ms: 1.27x faster                                                    |
| regex_effbot               | 3.21 ms                                                                | 2.71 ms: 1.19x faster                                                   |
| deepcopy                   | 357 us                                                                 | 306 us: 1.17x faster                                                    |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                                   |
| pidigits                   | 216 ms                                                                 | 199 ms: 1.09x faster                                                    |
| xml_etree_iterparse        | 94.4 ms                                                                | 89.9 ms: 1.05x faster                                                   |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.05x faster                                                    |
| regex_dna                  | 189 ms                                                                 | 182 ms: 1.04x faster                                                    |
| create_gc_cycles           | 1.33 ms                                                                | 1.30 ms: 1.02x faster                                                   |
| dulwich_log                | 74.5 ms                                                                | 73.4 ms: 1.01x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 3.14 us: 1.01x slower                                                   |
| go                         | 141 ms                                                                 | 142 ms: 1.01x slower                                                    |
| pathlib                    | 19.3 ms                                                                | 19.5 ms: 1.01x slower                                                   |
| float                      | 76.7 ms                                                                | 77.8 ms: 1.01x slower                                                   |
| async_generators           | 375 ms                                                                 | 380 ms: 1.01x slower                                                    |
| deepcopy_memo              | 38.1 us                                                                | 38.7 us: 1.02x slower                                                   |
| scimark_sor                | 134 ms                                                                 | 136 ms: 1.02x slower                                                    |
| regex_v8                   | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                                   |
| json                       | 4.98 ms                                                                | 5.11 ms: 1.03x slower                                                   |
| coroutines                 | 23.3 ms                                                                | 24.3 ms: 1.04x slower                                                   |
| html5lib                   | 68.6 ms                                                                | 71.7 ms: 1.05x slower                                                   |
| spectral_norm              | 108 ms                                                                 | 113 ms: 1.05x slower                                                    |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.07x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.81 sec: 1.07x slower                                                  |
| json_loads                 | 27.3 us                                                                | 29.3 us: 1.07x slower                                                   |
| bpe_tokeniser              | 4.46 sec                                                               | 4.86 sec: 1.09x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.77 ms: 1.13x slower                                                   |
| pyflate                    | 449 ms                                                                 | 508 ms: 1.13x slower                                                    |
| scimark_fft                | 348 ms                                                                 | 395 ms: 1.13x slower                                                    |
| xml_etree_generate         | 85.4 ms                                                                | 96.9 ms: 1.13x slower                                                   |
| sqlglot_normalize          | 106 ms                                                                 | 121 ms: 1.15x slower                                                    |
| thrift                     | 772 us                                                                 | 886 us: 1.15x slower                                                    |
| logging_silent             | 98.2 ns                                                                | 113 ns: 1.15x slower                                                    |
| 2to3                       | 259 ms                                                                 | 300 ms: 1.16x slower                                                    |
| pprint_safe_repr           | 719 ms                                                                 | 837 ms: 1.16x slower                                                    |
| tomli_loads                | 2.01 sec                                                               | 2.34 sec: 1.17x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                                | 61.7 ms: 1.17x slower                                                   |
| logging_simple             | 6.14 us                                                                | 7.26 us: 1.18x slower                                                   |
| pprint_pformat             | 1.46 sec                                                               | 1.72 sec: 1.18x slower                                                  |
| coverage                   | 82.5 ms                                                                | 97.8 ms: 1.19x slower                                                   |
| regex_compile              | 131 ms                                                                 | 156 ms: 1.19x slower                                                    |
| xml_etree_process          | 59.2 ms                                                                | 70.8 ms: 1.20x slower                                                   |
| mdp                        | 2.34 sec                                                               | 2.80 sec: 1.20x slower                                                  |
| logging_format             | 6.92 us                                                                | 8.28 us: 1.20x slower                                                   |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 252 us: 1.21x slower                                                    |
| sympy_expand               | 454 ms                                                                 | 551 ms: 1.22x slower                                                    |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.79 ms: 1.22x slower                                                   |
| sympy_sum                  | 154 ms                                                                 | 188 ms: 1.22x slower                                                    |
| pickle_pure_python         | 292 us                                                                 | 356 us: 1.22x slower                                                    |
| sympy_integrate            | 19.7 ms                                                                | 24.2 ms: 1.23x slower                                                   |
| sympy_str                  | 274 ms                                                                 | 336 ms: 1.23x slower                                                    |
| chaos                      | 56.3 ms                                                                | 69.2 ms: 1.23x slower                                                   |
| richards                   | 44.4 ms                                                                | 54.9 ms: 1.24x slower                                                   |
| django_template            | 34.2 ms                                                                | 42.5 ms: 1.24x slower                                                   |
| sqlglot_transpile          | 1.55 ms                                                                | 1.94 ms: 1.24x slower                                                   |
| deltablue                  | 3.10 ms                                                                | 3.88 ms: 1.25x slower                                                   |
| genshi_xml                 | 49.1 ms                                                                | 61.8 ms: 1.26x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 142 ms: 1.26x slower                                                    |
| richards_super             | 50.4 ms                                                                | 63.9 ms: 1.27x slower                                                   |
| generators                 | 28.5 ms                                                                | 36.2 ms: 1.27x slower                                                   |
| scimark_monte_carlo        | 65.8 ms                                                                | 83.7 ms: 1.27x slower                                                   |
| comprehensions             | 16.6 us                                                                | 21.1 us: 1.28x slower                                                   |
| typing_runtime_protocols   | 156 us                                                                 | 199 us: 1.28x slower                                                    |
| raytrace                   | 250 ms                                                                 | 321 ms: 1.29x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                                | 1.61 ms: 1.29x slower                                                   |
| crypto_pyaes               | 68.2 ms                                                                | 88.2 ms: 1.29x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 101 ms: 1.30x slower                                                    |
| hexiom                     | 5.95 ms                                                                | 7.82 ms: 1.31x slower                                                   |
| fannkuch                   | 376 ms                                                                 | 495 ms: 1.32x slower                                                    |
| meteor_contest             | 101 ms                                                                 | 134 ms: 1.32x slower                                                    |
| genshi_text                | 21.7 ms                                                                | 29.3 ms: 1.35x slower                                                   |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                   |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                   |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                   |
| nbody                      | 85.3 ms                                                                | 136 ms: 1.59x slower                                                    |
| bench_thread_pool          | 924 us                                                                 | 3.17 ms: 3.43x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                                | 95.5 ms: 8.68x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                            |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250313-3.14.0a5+-b67dc73-NOGIL/bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5+-b67dc73.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.083x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.35x