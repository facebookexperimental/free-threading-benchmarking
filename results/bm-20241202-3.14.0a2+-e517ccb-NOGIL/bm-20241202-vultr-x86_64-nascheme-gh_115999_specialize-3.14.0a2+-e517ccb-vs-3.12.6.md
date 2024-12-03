# Results vs. 3.12.6

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: e517ccb
- commit date: 2024-12-02
- overall geometric mean: 1.265x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 382 ms: 1.45x slower                                                     |
| docutils       | 2.64 sec                                               | 3.22 sec: 1.22x slower                                                   |
| html5lib       | 63.6 ms                                                | 101 ms: 1.58x slower                                                     |
| Geometric mean | (ref)                                                  | 1.41x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 871 ms: 1.27x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 464 ms: 1.21x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 898 ms: 1.21x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 372 ms: 1.20x faster                                                     |
| async_tree_none            | 464 ms                                                 | 403 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 634 ms: 1.14x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 495 ms: 1.12x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 668 ms: 1.07x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                     |
| coroutines                 | 23.9 ms                                                | 28.5 ms: 1.19x slower                                                    |
| async_generators           | 384 ms                                                 | 474 ms: 1.23x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                     |
| nbody          | 89.3 ms                                                | 147 ms: 1.64x slower                                                     |
| float          | 80.8 ms                                                | 143 ms: 1.78x slower                                                     |
| Geometric mean | (ref)                                                  | 1.43x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.97 ms: 1.07x faster                                                    |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                     |
| regex_v8       | 20.6 ms                                                | 26.3 ms: 1.28x slower                                                    |
| regex_compile  | 142 ms                                                 | 195 ms: 1.37x slower                                                     |
| Geometric mean | (ref)                                                  | 1.16x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 95.6 ms: 1.01x faster                                                    |
| json_loads           | 26.5 us                                                | 27.9 us: 1.05x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 103 ms: 1.21x slower                                                     |
| tomli_loads          | 2.11 sec                                               | 2.92 sec: 1.39x slower                                                   |
| json_dumps           | 10.4 ms                                                | 14.4 ms: 1.39x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 83.6 ms: 1.42x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 374 us: 1.70x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 560 us: 1.82x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.29x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                    |
| python_startup         | 9.93 ms                                                | 17.6 ms: 1.77x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 68.1 ms: 1.36x slower                                                    |
| genshi_text     | 22.8 ms                                                | 34.6 ms: 1.52x slower                                                    |
| django_template | 34.7 ms                                                | 55.4 ms: 1.60x slower                                                    |
| mako            | 11.0 ms                                                | 20.2 ms: 1.84x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.57x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 871 ms: 1.27x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 464 ms: 1.21x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 898 ms: 1.21x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 372 ms: 1.20x faster                                                     |
| async_tree_none            | 464 ms                                                 | 403 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 634 ms: 1.14x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 495 ms: 1.12x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 668 ms: 1.07x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.97 ms: 1.07x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                     |
| pathlib                    | 21.5 ms                                                | 20.8 ms: 1.03x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 95.6 ms: 1.01x faster                                                    |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                     |
| deepcopy                   | 352 us                                                 | 357 us: 1.01x slower                                                     |
| gc_traversal               | 3.46 ms                                                | 3.53 ms: 1.02x slower                                                    |
| json_loads                 | 26.5 us                                                | 27.9 us: 1.05x slower                                                    |
| sqlite_synth               | 2.20 us                                                | 2.34 us: 1.06x slower                                                    |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                     |
| deepcopy_memo              | 40.3 us                                                | 44.7 us: 1.11x slower                                                    |
| scimark_fft                | 342 ms                                                 | 389 ms: 1.14x slower                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 5.58 sec: 1.18x slower                                                   |
| spectral_norm              | 110 ms                                                 | 130 ms: 1.18x slower                                                     |
| coroutines                 | 23.9 ms                                                | 28.5 ms: 1.19x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 103 ms: 1.21x slower                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.73 us: 1.21x slower                                                    |
| docutils                   | 2.64 sec                                               | 3.22 sec: 1.22x slower                                                   |
| generators                 | 32.2 ms                                                | 39.5 ms: 1.22x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.39 ms: 1.23x slower                                                    |
| async_generators           | 384 ms                                                 | 474 ms: 1.23x slower                                                     |
| pylint                     | 319 ms                                                 | 396 ms: 1.24x slower                                                     |
| dulwich_log                | 78.9 ms                                                | 99.5 ms: 1.26x slower                                                    |
| mdp                        | 2.42 sec                                               | 3.07 sec: 1.27x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 26.3 ms: 1.28x slower                                                    |
| meteor_contest             | 104 ms                                                 | 137 ms: 1.32x slower                                                     |
| nqueens                    | 80.1 ms                                                | 107 ms: 1.33x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 102 ms: 1.33x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 218 us: 1.33x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 68.1 ms: 1.36x slower                                                    |
| regex_compile              | 142 ms                                                 | 195 ms: 1.37x slower                                                     |
| pycparser                  | 1.17 sec                                               | 1.61 sec: 1.37x slower                                                   |
| telco                      | 6.53 ms                                                | 9.01 ms: 1.38x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.92 sec: 1.39x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 14.4 ms: 1.39x slower                                                    |
| sqlglot_optimize           | 53.3 ms                                                | 75.2 ms: 1.41x slower                                                    |
| coverage                   | 71.4 ms                                                | 101 ms: 1.41x slower                                                     |
| sqlglot_normalize          | 107 ms                                                 | 151 ms: 1.42x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 83.6 ms: 1.42x slower                                                    |
| fannkuch                   | 372 ms                                                 | 535 ms: 1.44x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                    |
| 2to3                       | 264 ms                                                 | 382 ms: 1.45x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 1.08 sec: 1.45x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 2.23 sec: 1.47x slower                                                   |
| comprehensions             | 19.8 us                                                | 29.2 us: 1.47x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 31.0 ms: 1.51x slower                                                    |
| genshi_text                | 22.8 ms                                                | 34.6 ms: 1.52x slower                                                    |
| thrift                     | 791 us                                                 | 1.21 ms: 1.52x slower                                                    |
| html5lib                   | 63.6 ms                                                | 101 ms: 1.58x slower                                                     |
| django_template            | 34.7 ms                                                | 55.4 ms: 1.60x slower                                                    |
| pyflate                    | 448 ms                                                 | 728 ms: 1.63x slower                                                     |
| nbody                      | 89.3 ms                                                | 147 ms: 1.64x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 374 us: 1.70x slower                                                     |
| sympy_str                  | 292 ms                                                 | 497 ms: 1.71x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.71x slower                                                    |
| logging_simple             | 6.63 us                                                | 11.5 us: 1.73x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 199 ms: 1.74x slower                                                     |
| logging_format             | 7.35 us                                                | 12.8 us: 1.74x slower                                                    |
| python_startup             | 9.93 ms                                                | 17.6 ms: 1.77x slower                                                    |
| float                      | 80.8 ms                                                | 143 ms: 1.78x slower                                                     |
| logging_silent             | 109 ns                                                 | 194 ns: 1.78x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 123 ms: 1.79x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 560 us: 1.82x slower                                                     |
| chaos                      | 62.8 ms                                                | 115 ms: 1.82x slower                                                     |
| hexiom                     | 6.17 ms                                                | 11.3 ms: 1.83x slower                                                    |
| mako                       | 11.0 ms                                                | 20.2 ms: 1.84x slower                                                    |
| sqlglot_transpile          | 1.67 ms                                                | 3.10 ms: 1.86x slower                                                    |
| scimark_sor                | 130 ms                                                 | 241 ms: 1.86x slower                                                     |
| richards                   | 45.9 ms                                                | 86.4 ms: 1.88x slower                                                    |
| richards_super             | 51.9 ms                                                | 102 ms: 1.98x slower                                                     |
| sqlglot_parse              | 1.36 ms                                                | 2.70 ms: 1.99x slower                                                    |
| raytrace                   | 299 ms                                                 | 607 ms: 2.03x slower                                                     |
| go                         | 139 ms                                                 | 284 ms: 2.04x slower                                                     |
| sympy_expand               | 468 ms                                                 | 992 ms: 2.12x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 358 ms: 2.15x slower                                                     |
| deltablue                  | 3.45 ms                                                | 8.79 ms: 2.55x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.39 ms: 3.61x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 110 ms: 10.22x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.41x slower                                                             |

Benchmark hidden because not significant (1): json
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241202-3.14.0a2+-e517ccb-NOGIL/bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.265x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.27x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.22x

# Memory
- memory change: 1.33x