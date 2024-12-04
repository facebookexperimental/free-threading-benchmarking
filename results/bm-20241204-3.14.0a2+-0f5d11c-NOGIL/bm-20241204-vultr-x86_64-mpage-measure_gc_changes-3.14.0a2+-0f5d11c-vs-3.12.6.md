# Results vs. 3.12.6

- fork: mpage
- ref: measure_gc_changes
- machine: linux-x86_64
- commit hash: 0f5d11c
- commit date: 2024-12-04
- overall geometric mean: 1.255x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 376 ms: 1.43x slower                                                |
| docutils       | 2.64 sec                                               | 3.19 sec: 1.21x slower                                              |
| html5lib       | 63.6 ms                                                | 98.9 ms: 1.56x slower                                               |
| Geometric mean | (ref)                                                  | 1.39x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 865 ms: 1.28x faster                                                |
| async_tree_none_tg         | 446 ms                                                 | 366 ms: 1.22x faster                                                |
| async_tree_io              | 1.08 sec                                               | 891 ms: 1.22x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 461 ms: 1.21x faster                                                |
| async_tree_none            | 464 ms                                                 | 400 ms: 1.16x faster                                                |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 624 ms: 1.16x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 493 ms: 1.13x faster                                                |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 659 ms: 1.09x faster                                                |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                |
| coroutines                 | 23.9 ms                                                | 28.4 ms: 1.19x slower                                               |
| async_generators           | 384 ms                                                 | 467 ms: 1.22x slower                                                |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x slower                                                |
| nbody          | 89.3 ms                                                | 128 ms: 1.43x slower                                                |
| float          | 80.8 ms                                                | 143 ms: 1.77x slower                                                |
| Geometric mean | (ref)                                                  | 1.36x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.67 ms: 1.19x faster                                               |
| regex_dna      | 168 ms                                                 | 175 ms: 1.04x slower                                                |
| regex_v8       | 20.6 ms                                                | 23.8 ms: 1.15x slower                                               |
| regex_compile  | 142 ms                                                 | 191 ms: 1.34x slower                                                |
| Geometric mean | (ref)                                                  | 1.08x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 94.9 ms: 1.02x faster                                               |
| json_loads           | 26.5 us                                                | 28.1 us: 1.06x slower                                               |
| xml_etree_generate   | 85.2 ms                                                | 103 ms: 1.20x slower                                                |
| tomli_loads          | 2.11 sec                                               | 2.81 sec: 1.33x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 82.3 ms: 1.40x slower                                               |
| json_dumps           | 10.4 ms                                                | 14.5 ms: 1.40x slower                                               |
| unpickle_pure_python | 221 us                                                 | 379 us: 1.72x slower                                                |
| pickle_pure_python   | 308 us                                                 | 556 us: 1.81x slower                                                |
| Geometric mean       | (ref)                                                  | 1.28x slower                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                               |
| python_startup         | 9.93 ms                                                | 17.4 ms: 1.76x slower                                               |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 66.7 ms: 1.33x slower                                               |
| genshi_text     | 22.8 ms                                                | 33.5 ms: 1.47x slower                                               |
| django_template | 34.7 ms                                                | 55.2 ms: 1.59x slower                                               |
| mako            | 11.0 ms                                                | 19.6 ms: 1.78x slower                                               |
| Geometric mean  | (ref)                                                  | 1.53x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 865 ms: 1.28x faster                                                |
| async_tree_none_tg         | 446 ms                                                 | 366 ms: 1.22x faster                                                |
| async_tree_io              | 1.08 sec                                               | 891 ms: 1.22x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 461 ms: 1.21x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.67 ms: 1.19x faster                                               |
| async_tree_none            | 464 ms                                                 | 400 ms: 1.16x faster                                                |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 624 ms: 1.16x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 493 ms: 1.13x faster                                                |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 659 ms: 1.09x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                |
| gc_traversal               | 3.46 ms                                                | 3.30 ms: 1.05x faster                                               |
| pathlib                    | 21.5 ms                                                | 20.7 ms: 1.04x faster                                               |
| xml_etree_iterparse        | 96.7 ms                                                | 94.9 ms: 1.02x faster                                               |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x slower                                                |
| deepcopy                   | 352 us                                                 | 353 us: 1.00x slower                                                |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                |
| json                       | 5.02 ms                                                | 5.06 ms: 1.01x slower                                               |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.04x slower                                                |
| sqlite_synth               | 2.20 us                                                | 2.30 us: 1.04x slower                                               |
| json_loads                 | 26.5 us                                                | 28.1 us: 1.06x slower                                               |
| deepcopy_memo              | 40.3 us                                                | 44.9 us: 1.12x slower                                               |
| regex_v8                   | 20.6 ms                                                | 23.8 ms: 1.15x slower                                               |
| bpe_tokeniser              | 4.74 sec                                               | 5.47 sec: 1.15x slower                                              |
| scimark_fft                | 342 ms                                                 | 401 ms: 1.17x slower                                                |
| coroutines                 | 23.9 ms                                                | 28.4 ms: 1.19x slower                                               |
| generators                 | 32.2 ms                                                | 38.4 ms: 1.19x slower                                               |
| xml_etree_generate         | 85.2 ms                                                | 103 ms: 1.20x slower                                                |
| docutils                   | 2.64 sec                                               | 3.19 sec: 1.21x slower                                              |
| spectral_norm              | 110 ms                                                 | 134 ms: 1.21x slower                                                |
| deepcopy_reduce            | 3.08 us                                                | 3.74 us: 1.21x slower                                               |
| async_generators           | 384 ms                                                 | 467 ms: 1.22x slower                                                |
| pylint                     | 319 ms                                                 | 393 ms: 1.23x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 95.4 ms: 1.24x slower                                               |
| mdp                        | 2.42 sec                                               | 3.03 sec: 1.25x slower                                              |
| dulwich_log                | 78.9 ms                                                | 98.9 ms: 1.25x slower                                               |
| nqueens                    | 80.1 ms                                                | 103 ms: 1.29x slower                                                |
| typing_runtime_protocols   | 163 us                                                 | 212 us: 1.30x slower                                                |
| meteor_contest             | 104 ms                                                 | 135 ms: 1.31x slower                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.82 ms: 1.33x slower                                               |
| genshi_xml                 | 50.2 ms                                                | 66.7 ms: 1.33x slower                                               |
| tomli_loads                | 2.11 sec                                               | 2.81 sec: 1.33x slower                                              |
| regex_compile              | 142 ms                                                 | 191 ms: 1.34x slower                                                |
| telco                      | 6.53 ms                                                | 8.79 ms: 1.35x slower                                               |
| fannkuch                   | 372 ms                                                 | 511 ms: 1.37x slower                                                |
| pycparser                  | 1.17 sec                                               | 1.61 sec: 1.38x slower                                              |
| sqlalchemy_imperative      | 21.8 ms                                                | 30.2 ms: 1.38x slower                                               |
| coverage                   | 71.4 ms                                                | 99.7 ms: 1.40x slower                                               |
| xml_etree_process          | 59.0 ms                                                | 82.3 ms: 1.40x slower                                               |
| json_dumps                 | 10.4 ms                                                | 14.5 ms: 1.40x slower                                               |
| sqlglot_optimize           | 53.3 ms                                                | 75.4 ms: 1.42x slower                                               |
| sqlglot_normalize          | 107 ms                                                 | 151 ms: 1.42x slower                                                |
| 2to3                       | 264 ms                                                 | 376 ms: 1.43x slower                                                |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                               |
| nbody                      | 89.3 ms                                                | 128 ms: 1.43x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 1.07 sec: 1.44x slower                                              |
| sqlalchemy_declarative     | 143 ms                                                 | 207 ms: 1.45x slower                                                |
| comprehensions             | 19.8 us                                                | 28.9 us: 1.46x slower                                               |
| genshi_text                | 22.8 ms                                                | 33.5 ms: 1.47x slower                                               |
| pprint_pformat             | 1.52 sec                                               | 2.24 sec: 1.47x slower                                              |
| sympy_integrate            | 20.5 ms                                                | 30.8 ms: 1.50x slower                                               |
| thrift                     | 791 us                                                 | 1.22 ms: 1.54x slower                                               |
| html5lib                   | 63.6 ms                                                | 98.9 ms: 1.56x slower                                               |
| django_template            | 34.7 ms                                                | 55.2 ms: 1.59x slower                                               |
| pyflate                    | 448 ms                                                 | 726 ms: 1.62x slower                                                |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.67x slower                                               |
| scimark_lu                 | 114 ms                                                 | 194 ms: 1.70x slower                                                |
| sympy_str                  | 292 ms                                                 | 495 ms: 1.70x slower                                                |
| logging_simple             | 6.63 us                                                | 11.3 us: 1.70x slower                                               |
| logging_format             | 7.35 us                                                | 12.6 us: 1.71x slower                                               |
| unpickle_pure_python       | 221 us                                                 | 379 us: 1.72x slower                                                |
| hexiom                     | 6.17 ms                                                | 10.8 ms: 1.75x slower                                               |
| python_startup             | 9.93 ms                                                | 17.4 ms: 1.76x slower                                               |
| float                      | 80.8 ms                                                | 143 ms: 1.77x slower                                                |
| chaos                      | 62.8 ms                                                | 112 ms: 1.77x slower                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 122 ms: 1.78x slower                                                |
| mako                       | 11.0 ms                                                | 19.6 ms: 1.78x slower                                               |
| richards                   | 45.9 ms                                                | 82.6 ms: 1.80x slower                                               |
| pickle_pure_python         | 308 us                                                 | 556 us: 1.81x slower                                                |
| logging_silent             | 109 ns                                                 | 197 ns: 1.81x slower                                                |
| sqlglot_transpile          | 1.67 ms                                                | 3.08 ms: 1.84x slower                                               |
| scimark_sor                | 130 ms                                                 | 245 ms: 1.89x slower                                                |
| richards_super             | 51.9 ms                                                | 99.1 ms: 1.91x slower                                               |
| sqlglot_parse              | 1.36 ms                                                | 2.66 ms: 1.97x slower                                               |
| raytrace                   | 299 ms                                                 | 602 ms: 2.01x slower                                                |
| go                         | 139 ms                                                 | 281 ms: 2.02x slower                                                |
| sympy_expand               | 468 ms                                                 | 987 ms: 2.11x slower                                                |
| sympy_sum                  | 166 ms                                                 | 359 ms: 2.16x slower                                                |
| deltablue                  | 3.45 ms                                                | 8.76 ms: 2.54x slower                                               |
| bench_thread_pool          | 941 us                                                 | 3.38 ms: 3.60x slower                                               |
| bench_mp_pool              | 10.8 ms                                                | 110 ms: 10.15x slower                                               |
| Geometric mean             | (ref)                                                  | 1.39x slower                                                        |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241204-3.14.0a2+-0f5d11c-NOGIL/bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.255x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.25x
- 99% likely to have a slowdown of 1.21x

# Memory
- memory change: 1.33x