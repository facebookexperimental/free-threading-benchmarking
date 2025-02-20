# Results vs. 3.13.0rc2

- fork: DinoV
- ref: nolock_loadattr_with
- machine: linux-x86_64
- commit hash: 6a1fe7e
- commit date: 2025-02-19
- overall geometric mean: 1.070x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 300 ms: 1.16x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                                |
| html5lib       | 68.6 ms                                                                | 69.5 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 555 ms: 1.62x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 584 ms: 1.51x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 240 ms: 1.39x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 339 ms: 1.35x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 309 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 488 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 521 ms: 1.28x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 278 ms: 1.27x faster                                                  |
| async_generators           | 375 ms                                                                 | 370 ms: 1.01x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 196 ms: 1.10x faster                                                  |
| float          | 76.7 ms                                                                | 76.1 ms: 1.01x faster                                                 |
| nbody          | 85.3 ms                                                                | 132 ms: 1.55x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.88 ms: 1.11x faster                                                 |
| regex_dna      | 189 ms                                                                 | 176 ms: 1.07x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 23.6 ms: 1.02x slower                                                 |
| regex_compile  | 131 ms                                                                 | 154 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.9 ms: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 95.4 ms: 1.12x slower                                                 |
| json_loads           | 27.3 us                                                                | 31.5 us: 1.15x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.33 sec: 1.16x slower                                                |
| xml_etree_process    | 59.2 ms                                                                | 69.2 ms: 1.17x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 244 us: 1.17x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 355 us: 1.22x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.59 ms: 1.29x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.35x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.0 ms: 1.20x slower                                                 |
| django_template | 34.2 ms                                                                | 41.8 ms: 1.22x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 27.7 ms: 1.27x slower                                                 |
| mako            | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.27x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.72 ms: 1.93x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 555 ms: 1.62x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 584 ms: 1.51x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 240 ms: 1.39x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 339 ms: 1.35x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 309 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 488 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 521 ms: 1.28x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 278 ms: 1.27x faster                                                  |
| deepcopy                   | 357 us                                                                 | 310 us: 1.15x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.88 ms: 1.11x faster                                                 |
| pidigits                   | 216 ms                                                                 | 196 ms: 1.10x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.9 ms: 1.07x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 176 ms: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| go                         | 141 ms                                                                 | 137 ms: 1.02x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 131 ms: 1.02x faster                                                  |
| async_generators           | 375 ms                                                                 | 370 ms: 1.01x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| float                      | 76.7 ms                                                                | 76.1 ms: 1.01x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 109 ms: 1.01x slower                                                  |
| html5lib                   | 68.6 ms                                                                | 69.5 ms: 1.01x slower                                                 |
| regex_v8                   | 23.2 ms                                                                | 23.6 ms: 1.02x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.36 ms: 1.02x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 3.20 us: 1.03x slower                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.67 sec: 1.05x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                                |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.06x slower                                                |
| json                       | 4.98 ms                                                                | 5.34 ms: 1.07x slower                                                 |
| pyflate                    | 449 ms                                                                 | 491 ms: 1.09x slower                                                  |
| logging_silent             | 98.2 ns                                                                | 108 ns: 1.10x slower                                                  |
| generators                 | 28.5 ms                                                                | 31.5 ms: 1.10x slower                                                 |
| dulwich_log                | 74.5 ms                                                                | 82.3 ms: 1.11x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 95.4 ms: 1.12x slower                                                 |
| scimark_fft                | 348 ms                                                                 | 389 ms: 1.12x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.70 ms: 1.12x slower                                                 |
| sqlglot_normalize          | 106 ms                                                                 | 119 ms: 1.13x slower                                                  |
| mdp                        | 2.34 sec                                                               | 2.67 sec: 1.14x slower                                                |
| thrift                     | 772 us                                                                 | 882 us: 1.14x slower                                                  |
| json_loads                 | 27.3 us                                                                | 31.5 us: 1.15x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.98 us: 1.15x slower                                                 |
| logging_simple             | 6.14 us                                                                | 7.10 us: 1.16x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.33 sec: 1.16x slower                                                |
| 2to3                       | 259 ms                                                                 | 300 ms: 1.16x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 832 ms: 1.16x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                                | 61.3 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 69.2 ms: 1.17x slower                                                 |
| regex_compile              | 131 ms                                                                 | 154 ms: 1.17x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 244 us: 1.17x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.72 sec: 1.18x slower                                                |
| coverage                   | 82.5 ms                                                                | 98.2 ms: 1.19x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 542 ms: 1.19x slower                                                  |
| comprehensions             | 16.6 us                                                                | 19.8 us: 1.20x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 59.0 ms: 1.20x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 186 ms: 1.20x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 331 ms: 1.21x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.76 ms: 1.21x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 23.9 ms: 1.21x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 7.23 ms: 1.22x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 94.5 ms: 1.22x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 355 us: 1.22x slower                                                  |
| sqlglot_transpile          | 1.55 ms                                                                | 1.90 ms: 1.22x slower                                                 |
| django_template            | 34.2 ms                                                                | 41.8 ms: 1.22x slower                                                 |
| richards                   | 44.4 ms                                                                | 54.5 ms: 1.23x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.81 ms: 1.23x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 138 ms: 1.23x slower                                                  |
| chaos                      | 56.3 ms                                                                | 70.1 ms: 1.25x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 82.0 ms: 1.25x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                                | 1.58 ms: 1.27x slower                                                 |
| richards_super             | 50.4 ms                                                                | 64.0 ms: 1.27x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 86.9 ms: 1.27x slower                                                 |
| genshi_text                | 21.7 ms                                                                | 27.7 ms: 1.27x slower                                                 |
| raytrace                   | 250 ms                                                                 | 320 ms: 1.28x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 200 us: 1.28x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 131 ms: 1.29x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.59 ms: 1.29x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 489 ms: 1.30x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                                 |
| nbody                      | 85.3 ms                                                                | 132 ms: 1.55x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 3.30 ms: 3.57x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 94.8 ms: 8.62x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.12x slower                                                          |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, deepcopy_memo
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250219-3.14.0a5+-6a1fe7e-NOGIL/bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.070x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.35x