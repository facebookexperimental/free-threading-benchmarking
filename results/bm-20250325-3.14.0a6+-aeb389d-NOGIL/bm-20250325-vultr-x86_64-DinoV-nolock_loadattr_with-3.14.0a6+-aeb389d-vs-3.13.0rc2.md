# Results vs. 3.13.0rc2

- fork: DinoV
- ref: nolock_loadattr_with
- machine: linux-x86_64
- commit hash: aeb389d
- commit date: 2025-03-25
- overall geometric mean: 1.076x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 298 ms: 1.15x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                                |
| html5lib       | 68.6 ms                                                                | 71.7 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 557 ms: 1.62x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 588 ms: 1.50x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 237 ms: 1.40x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 337 ms: 1.36x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 302 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 485 ms: 1.31x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 524 ms: 1.27x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.4 ms: 1.00x slower                                                 |
| async_generators           | 375 ms                                                                 | 387 ms: 1.03x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 208 ms: 1.04x faster                                                  |
| float          | 76.7 ms                                                                | 76.5 ms: 1.00x faster                                                 |
| nbody          | 85.3 ms                                                                | 132 ms: 1.55x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.64 ms: 1.21x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.6 ms: 1.08x faster                                                 |
| regex_dna      | 189 ms                                                                 | 180 ms: 1.05x faster                                                  |
| regex_compile  | 131 ms                                                                 | 158 ms: 1.21x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.4 ms: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                  |
| json_loads           | 27.3 us                                                                | 29.4 us: 1.07x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 97.3 ms: 1.14x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.35 sec: 1.17x slower                                                |
| xml_etree_process    | 59.2 ms                                                                | 71.1 ms: 1.20x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 252 us: 1.21x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 13.0 ms: 1.23x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 364 us: 1.25x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                 |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.5 ms: 1.21x slower                                                 |
| django_template | 34.2 ms                                                                | 42.4 ms: 1.24x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 28.3 ms: 1.30x slower                                                 |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.80 ms: 1.85x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 557 ms: 1.62x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 588 ms: 1.50x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 237 ms: 1.40x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 337 ms: 1.36x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 302 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 485 ms: 1.31x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 524 ms: 1.27x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.64 ms: 1.21x faster                                                 |
| deepcopy                   | 357 us                                                                 | 313 us: 1.14x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.6 ms: 1.08x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.4 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 180 ms: 1.05x faster                                                  |
| pidigits                   | 216 ms                                                                 | 208 ms: 1.04x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 73.7 ms: 1.01x faster                                                 |
| float                      | 76.7 ms                                                                | 76.5 ms: 1.00x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 23.4 ms: 1.00x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.35 ms: 1.01x slower                                                 |
| json                       | 4.98 ms                                                                | 5.07 ms: 1.02x slower                                                 |
| scimark_sor                | 134 ms                                                                 | 136 ms: 1.02x slower                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.19 us: 1.02x slower                                                 |
| go                         | 141 ms                                                                 | 144 ms: 1.03x slower                                                  |
| async_generators           | 375 ms                                                                 | 387 ms: 1.03x slower                                                  |
| deepcopy_memo              | 38.1 us                                                                | 39.3 us: 1.03x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 20.1 ms: 1.04x slower                                                 |
| spectral_norm              | 108 ms                                                                 | 112 ms: 1.04x slower                                                  |
| html5lib                   | 68.6 ms                                                                | 71.7 ms: 1.05x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.77 sec: 1.05x slower                                                |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.07x slower                                                |
| json_loads                 | 27.3 us                                                                | 29.4 us: 1.07x slower                                                 |
| generators                 | 28.5 ms                                                                | 31.0 ms: 1.09x slower                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.88 sec: 1.09x slower                                                |
| pyflate                    | 449 ms                                                                 | 506 ms: 1.13x slower                                                  |
| thrift                     | 772 us                                                                 | 876 us: 1.14x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 397 ms: 1.14x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 97.3 ms: 1.14x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 112 ns: 1.15x slower                                                  |
| 2to3                       | 259 ms                                                                 | 298 ms: 1.15x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 838 ms: 1.17x slower                                                  |
| mdp                        | 2.34 sec                                                               | 2.73 sec: 1.17x slower                                                |
| tomli_loads                | 2.01 sec                                                               | 2.35 sec: 1.17x slower                                                |
| telco                      | 7.77 ms                                                                | 9.09 ms: 1.17x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.73 sec: 1.19x slower                                                |
| logging_simple             | 6.14 us                                                                | 7.34 us: 1.19x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 23.7 ms: 1.20x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 71.1 ms: 1.20x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 186 ms: 1.20x slower                                                  |
| regex_compile              | 131 ms                                                                 | 158 ms: 1.21x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 252 us: 1.21x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 59.5 ms: 1.21x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.78 ms: 1.22x slower                                                 |
| chaos                      | 56.3 ms                                                                | 68.4 ms: 1.22x slower                                                 |
| logging_format             | 6.92 us                                                                | 8.41 us: 1.22x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 553 ms: 1.22x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 13.0 ms: 1.23x slower                                                 |
| richards                   | 44.4 ms                                                                | 54.7 ms: 1.23x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 338 ms: 1.23x slower                                                  |
| django_template            | 34.2 ms                                                                | 42.4 ms: 1.24x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 364 us: 1.25x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.86 ms: 1.25x slower                                                 |
| comprehensions             | 16.6 us                                                                | 20.7 us: 1.25x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 97.6 ms: 1.26x slower                                                 |
| richards_super             | 50.4 ms                                                                | 63.4 ms: 1.26x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 83.4 ms: 1.27x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 143 ms: 1.27x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 7.63 ms: 1.28x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.28x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 87.9 ms: 1.29x slower                                                 |
| raytrace                   | 250 ms                                                                 | 322 ms: 1.29x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 28.3 ms: 1.30x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 203 us: 1.30x slower                                                  |
| coverage                   | 82.5 ms                                                                | 109 ms: 1.32x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 497 ms: 1.32x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                 |
| nbody                      | 85.3 ms                                                                | 132 ms: 1.55x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 3.16 ms: 3.42x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 97.4 ms: 8.85x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.12x slower                                                          |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250325-3.14.0a6+-aeb389d-NOGIL/bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.076x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.35x