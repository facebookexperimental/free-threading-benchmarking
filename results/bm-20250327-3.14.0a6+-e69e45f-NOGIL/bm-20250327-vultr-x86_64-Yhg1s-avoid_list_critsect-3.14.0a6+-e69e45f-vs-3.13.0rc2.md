# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: avoid_list_critsect
- machine: linux-x86_64
- commit hash: e69e45f
- commit date: 2025-03-27
- overall geometric mean: 1.082x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 299 ms: 1.15x slower                                                 |
| docutils       | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                               |
| html5lib       | 68.6 ms                                                                | 72.2 ms: 1.05x slower                                                |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 553 ms: 1.63x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 585 ms: 1.51x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 239 ms: 1.39x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 333 ms: 1.38x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 301 ms: 1.36x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 495 ms: 1.28x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.28x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 527 ms: 1.26x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 23.7 ms: 1.02x slower                                                |
| async_generators           | 375 ms                                                                 | 383 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 193 ms: 1.12x faster                                                 |
| float          | 76.7 ms                                                                | 79.1 ms: 1.03x slower                                                |
| nbody          | 85.3 ms                                                                | 131 ms: 1.54x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.86 ms: 1.12x faster                                                |
| regex_v8       | 23.2 ms                                                                | 21.5 ms: 1.08x faster                                                |
| regex_dna      | 189 ms                                                                 | 176 ms: 1.07x faster                                                 |
| regex_compile  | 131 ms                                                                 | 159 ms: 1.21x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.4 ms: 1.07x faster                                                |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.06x faster                                                 |
| json_loads           | 27.3 us                                                                | 30.8 us: 1.12x slower                                                |
| xml_etree_generate   | 85.4 ms                                                                | 97.7 ms: 1.14x slower                                                |
| tomli_loads          | 2.01 sec                                                               | 2.40 sec: 1.19x slower                                               |
| xml_etree_process    | 59.2 ms                                                                | 70.9 ms: 1.20x slower                                                |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 258 us: 1.24x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 363 us: 1.25x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.13x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.46x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 61.1 ms: 1.25x slower                                                |
| django_template | 34.2 ms                                                                | 44.3 ms: 1.30x slower                                                |
| genshi_text     | 21.7 ms                                                                | 28.6 ms: 1.32x slower                                                |
| mako            | 11.2 ms                                                                | 16.1 ms: 1.43x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.32x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.82 ms: 1.82x faster                                                |
| async_tree_io_tg           | 901 ms                                                                 | 553 ms: 1.63x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 585 ms: 1.51x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 239 ms: 1.39x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 333 ms: 1.38x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 301 ms: 1.36x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 495 ms: 1.28x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.28x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 527 ms: 1.26x faster                                                 |
| deepcopy                   | 357 us                                                                 | 313 us: 1.14x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 2.86 ms: 1.12x faster                                                |
| pidigits                   | 216 ms                                                                 | 193 ms: 1.12x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.01 us: 1.12x faster                                                |
| regex_v8                   | 23.2 ms                                                                | 21.5 ms: 1.08x faster                                                |
| regex_dna                  | 189 ms                                                                 | 176 ms: 1.07x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.4 ms: 1.07x faster                                                |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.06x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 73.5 ms: 1.01x faster                                                |
| coroutines                 | 23.3 ms                                                                | 23.7 ms: 1.02x slower                                                |
| deepcopy_reduce            | 3.12 us                                                                | 3.19 us: 1.02x slower                                                |
| async_generators           | 375 ms                                                                 | 383 ms: 1.02x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                                |
| float                      | 76.7 ms                                                                | 79.1 ms: 1.03x slower                                                |
| scimark_sor                | 134 ms                                                                 | 138 ms: 1.03x slower                                                 |
| deepcopy_memo              | 38.1 us                                                                | 39.4 us: 1.03x slower                                                |
| create_gc_cycles           | 1.33 ms                                                                | 1.38 ms: 1.04x slower                                                |
| go                         | 141 ms                                                                 | 148 ms: 1.05x slower                                                 |
| html5lib                   | 68.6 ms                                                                | 72.2 ms: 1.05x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                               |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.07x slower                                               |
| json                       | 4.98 ms                                                                | 5.32 ms: 1.07x slower                                                |
| spectral_norm              | 108 ms                                                                 | 115 ms: 1.07x slower                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.85 sec: 1.09x slower                                               |
| generators                 | 28.5 ms                                                                | 31.5 ms: 1.10x slower                                                |
| json_loads                 | 27.3 us                                                                | 30.8 us: 1.12x slower                                                |
| pyflate                    | 449 ms                                                                 | 506 ms: 1.13x slower                                                 |
| thrift                     | 772 us                                                                 | 869 us: 1.13x slower                                                 |
| scimark_fft                | 348 ms                                                                 | 395 ms: 1.13x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 97.7 ms: 1.14x slower                                                |
| 2to3                       | 259 ms                                                                 | 299 ms: 1.15x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 114 ns: 1.16x slower                                                 |
| telco                      | 7.77 ms                                                                | 9.04 ms: 1.16x slower                                                |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.64 ms: 1.19x slower                                                |
| pprint_safe_repr           | 719 ms                                                                 | 855 ms: 1.19x slower                                                 |
| mdp                        | 2.34 sec                                                               | 2.79 sec: 1.19x slower                                               |
| tomli_loads                | 2.01 sec                                                               | 2.40 sec: 1.19x slower                                               |
| logging_simple             | 6.14 us                                                                | 7.32 us: 1.19x slower                                                |
| xml_etree_process          | 59.2 ms                                                                | 70.9 ms: 1.20x slower                                                |
| sympy_integrate            | 19.7 ms                                                                | 23.7 ms: 1.20x slower                                                |
| logging_format             | 6.92 us                                                                | 8.34 us: 1.21x slower                                                |
| sympy_sum                  | 154 ms                                                                 | 186 ms: 1.21x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                |
| regex_compile              | 131 ms                                                                 | 159 ms: 1.21x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 552 ms: 1.22x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.78 sec: 1.22x slower                                               |
| sympy_str                  | 274 ms                                                                 | 335 ms: 1.22x slower                                                 |
| chaos                      | 56.3 ms                                                                | 69.5 ms: 1.23x slower                                                |
| unpickle_pure_python       | 208 us                                                                 | 258 us: 1.24x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 363 us: 1.25x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 61.1 ms: 1.25x slower                                                |
| nqueens                    | 77.7 ms                                                                | 97.6 ms: 1.26x slower                                                |
| typing_runtime_protocols   | 156 us                                                                 | 196 us: 1.26x slower                                                 |
| richards                   | 44.4 ms                                                                | 56.2 ms: 1.27x slower                                                |
| comprehensions             | 16.6 us                                                                | 21.0 us: 1.27x slower                                                |
| deltablue                  | 3.10 ms                                                                | 3.95 ms: 1.28x slower                                                |
| scimark_lu                 | 112 ms                                                                 | 143 ms: 1.28x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 84.6 ms: 1.29x slower                                                |
| crypto_pyaes               | 68.2 ms                                                                | 87.8 ms: 1.29x slower                                                |
| richards_super             | 50.4 ms                                                                | 65.1 ms: 1.29x slower                                                |
| hexiom                     | 5.95 ms                                                                | 7.71 ms: 1.29x slower                                                |
| django_template            | 34.2 ms                                                                | 44.3 ms: 1.30x slower                                                |
| meteor_contest             | 101 ms                                                                 | 132 ms: 1.30x slower                                                 |
| genshi_text                | 21.7 ms                                                                | 28.6 ms: 1.32x slower                                                |
| raytrace                   | 250 ms                                                                 | 329 ms: 1.32x slower                                                 |
| coverage                   | 82.5 ms                                                                | 109 ms: 1.32x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 498 ms: 1.32x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                |
| mako                       | 11.2 ms                                                                | 16.1 ms: 1.43x slower                                                |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                |
| nbody                      | 85.3 ms                                                                | 131 ms: 1.54x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.16 ms: 3.42x slower                                                |
| bench_mp_pool              | 11.0 ms                                                                | 97.1 ms: 8.83x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                         |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250327-3.14.0a6+-e69e45f-NOGIL/bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.082x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.35x