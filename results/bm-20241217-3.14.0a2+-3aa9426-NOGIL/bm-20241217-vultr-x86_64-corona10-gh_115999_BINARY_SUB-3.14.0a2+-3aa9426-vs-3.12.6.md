# Results vs. 3.12.6

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 3aa9426
- commit date: 2024-12-17
- overall geometric mean: 1.226x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 368 ms: 1.39x slower                                                     |
| docutils       | 2.64 sec                                               | 3.11 sec: 1.18x slower                                                   |
| html5lib       | 63.6 ms                                                | 98.4 ms: 1.55x slower                                                    |
| Geometric mean | (ref)                                                  | 1.37x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 827 ms: 1.34x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 849 ms: 1.28x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 445 ms: 1.26x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 358 ms: 1.25x faster                                                     |
| async_tree_none            | 464 ms                                                 | 389 ms: 1.20x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 472 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 622 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 651 ms: 1.10x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                     |
| coroutines                 | 23.9 ms                                                | 25.2 ms: 1.05x slower                                                    |
| async_generators           | 384 ms                                                 | 461 ms: 1.20x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.13x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                     |
| nbody          | 89.3 ms                                                | 132 ms: 1.48x slower                                                     |
| float          | 80.8 ms                                                | 141 ms: 1.74x slower                                                     |
| Geometric mean | (ref)                                                  | 1.36x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.90 ms: 1.09x faster                                                    |
| regex_dna      | 168 ms                                                 | 177 ms: 1.06x slower                                                     |
| regex_v8       | 20.6 ms                                                | 24.8 ms: 1.20x slower                                                    |
| regex_compile  | 142 ms                                                 | 179 ms: 1.25x slower                                                     |
| Geometric mean | (ref)                                                  | 1.10x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 91.9 ms: 1.05x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                     |
| json_loads           | 26.5 us                                                | 28.7 us: 1.08x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 98.0 ms: 1.15x slower                                                    |
| tomli_loads          | 2.11 sec                                               | 2.69 sec: 1.28x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 78.2 ms: 1.33x slower                                                    |
| json_dumps           | 10.4 ms                                                | 14.2 ms: 1.37x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 333 us: 1.51x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 517 us: 1.68x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                    |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 64.7 ms: 1.29x slower                                                    |
| genshi_text     | 22.8 ms                                                | 32.2 ms: 1.41x slower                                                    |
| django_template | 34.7 ms                                                | 51.4 ms: 1.48x slower                                                    |
| mako            | 11.0 ms                                                | 17.8 ms: 1.62x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.44x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 827 ms: 1.34x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 849 ms: 1.28x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 445 ms: 1.26x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 358 ms: 1.25x faster                                                     |
| async_tree_none            | 464 ms                                                 | 389 ms: 1.20x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 472 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 622 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 651 ms: 1.10x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.90 ms: 1.09x faster                                                    |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.09x faster                                                    |
| deepcopy                   | 352 us                                                 | 331 us: 1.06x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 91.9 ms: 1.05x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                     |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 39.9 us: 1.01x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                     |
| json                       | 5.02 ms                                                | 5.09 ms: 1.01x slower                                                    |
| gc_traversal               | 3.46 ms                                                | 3.52 ms: 1.02x slower                                                    |
| sqlite_synth               | 2.20 us                                                | 2.27 us: 1.03x slower                                                    |
| coroutines                 | 23.9 ms                                                | 25.2 ms: 1.05x slower                                                    |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.06x slower                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 5.02 sec: 1.06x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.7 us: 1.08x slower                                                    |
| spectral_norm              | 110 ms                                                 | 126 ms: 1.14x slower                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.53 us: 1.15x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 98.0 ms: 1.15x slower                                                    |
| mdp                        | 2.42 sec                                               | 2.84 sec: 1.17x slower                                                   |
| docutils                   | 2.64 sec                                               | 3.11 sec: 1.18x slower                                                   |
| async_generators           | 384 ms                                                 | 461 ms: 1.20x slower                                                     |
| pylint                     | 319 ms                                                 | 382 ms: 1.20x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 24.8 ms: 1.20x slower                                                    |
| generators                 | 32.2 ms                                                | 38.8 ms: 1.20x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 92.6 ms: 1.21x slower                                                    |
| scimark_fft                | 342 ms                                                 | 414 ms: 1.21x slower                                                     |
| dulwich_log                | 78.9 ms                                                | 95.7 ms: 1.21x slower                                                    |
| nqueens                    | 80.1 ms                                                | 98.0 ms: 1.22x slower                                                    |
| regex_compile              | 142 ms                                                 | 179 ms: 1.25x slower                                                     |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 207 us: 1.27x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 2.69 sec: 1.28x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 64.7 ms: 1.29x slower                                                    |
| sqlglot_normalize          | 107 ms                                                 | 138 ms: 1.29x slower                                                     |
| sqlglot_optimize           | 53.3 ms                                                | 69.2 ms: 1.30x slower                                                    |
| pycparser                  | 1.17 sec                                               | 1.53 sec: 1.31x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 981 ms: 1.32x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 78.2 ms: 1.33x slower                                                    |
| telco                      | 6.53 ms                                                | 8.67 ms: 1.33x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 2.04 sec: 1.34x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 29.5 ms: 1.35x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 155 ms: 1.36x slower                                                     |
| comprehensions             | 19.8 us                                                | 27.2 us: 1.37x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 14.2 ms: 1.37x slower                                                    |
| fannkuch                   | 372 ms                                                 | 512 ms: 1.37x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 6.10 ms: 1.39x slower                                                    |
| 2to3                       | 264 ms                                                 | 368 ms: 1.39x slower                                                     |
| genshi_text                | 22.8 ms                                                | 32.2 ms: 1.41x slower                                                    |
| sqlalchemy_declarative     | 143 ms                                                 | 204 ms: 1.43x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 29.5 ms: 1.44x slower                                                    |
| coverage                   | 71.4 ms                                                | 103 ms: 1.45x slower                                                     |
| thrift                     | 791 us                                                 | 1.15 ms: 1.46x slower                                                    |
| django_template            | 34.7 ms                                                | 51.4 ms: 1.48x slower                                                    |
| nbody                      | 89.3 ms                                                | 132 ms: 1.48x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 333 us: 1.51x slower                                                     |
| html5lib                   | 63.6 ms                                                | 98.4 ms: 1.55x slower                                                    |
| pyflate                    | 448 ms                                                 | 696 ms: 1.55x slower                                                     |
| hexiom                     | 6.17 ms                                                | 9.71 ms: 1.57x slower                                                    |
| logging_simple             | 6.63 us                                                | 10.7 us: 1.62x slower                                                    |
| mako                       | 11.0 ms                                                | 17.8 ms: 1.62x slower                                                    |
| logging_format             | 7.35 us                                                | 12.0 us: 1.63x slower                                                    |
| sympy_str                  | 292 ms                                                 | 477 ms: 1.64x slower                                                     |
| richards                   | 45.9 ms                                                | 76.4 ms: 1.66x slower                                                    |
| chaos                      | 62.8 ms                                                | 104 ms: 1.66x slower                                                     |
| richards_super             | 51.9 ms                                                | 86.3 ms: 1.66x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 517 us: 1.68x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                    |
| logging_silent             | 109 ns                                                 | 184 ns: 1.69x slower                                                     |
| scimark_sor                | 130 ms                                                 | 224 ms: 1.73x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 118 ms: 1.73x slower                                                     |
| float                      | 80.8 ms                                                | 141 ms: 1.74x slower                                                     |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                    |
| sqlglot_transpile          | 1.67 ms                                                | 3.02 ms: 1.80x slower                                                    |
| raytrace                   | 299 ms                                                 | 548 ms: 1.83x slower                                                     |
| sqlglot_parse              | 1.36 ms                                                | 2.60 ms: 1.92x slower                                                    |
| go                         | 139 ms                                                 | 269 ms: 1.93x slower                                                     |
| sympy_expand               | 468 ms                                                 | 956 ms: 2.04x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 350 ms: 2.11x slower                                                     |
| deltablue                  | 3.45 ms                                                | 7.94 ms: 2.30x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.43 ms: 3.64x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 109 ms: 10.07x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.34x slower                                                             |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241217-3.14.0a2+-3aa9426-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.226x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.22x
- 95% likely to have a slowdown of 1.21x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.33x