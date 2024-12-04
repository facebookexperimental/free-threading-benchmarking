# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_load_attr
- machine: linux-x86_64
- commit hash: 3bfbf91
- commit date: 2024-12-03
- overall geometric mean: 1.219x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 365 ms: 1.38x slower                                                 |
| docutils       | 2.64 sec                                               | 3.08 sec: 1.17x slower                                               |
| html5lib       | 63.6 ms                                                | 97.5 ms: 1.53x slower                                                |
| Geometric mean | (ref)                                                  | 1.35x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 800 ms: 1.39x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 821 ms: 1.32x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 438 ms: 1.28x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 352 ms: 1.27x faster                                                 |
| async_tree_none            | 464 ms                                                 | 378 ms: 1.23x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 458 ms: 1.21x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 604 ms: 1.20x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 626 ms: 1.14x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.8 ms: 1.04x slower                                                |
| async_generators           | 384 ms                                                 | 455 ms: 1.18x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.16x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                 |
| nbody          | 89.3 ms                                                | 130 ms: 1.45x slower                                                 |
| float          | 80.8 ms                                                | 139 ms: 1.73x slower                                                 |
| Geometric mean | (ref)                                                  | 1.36x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                 |
| regex_v8       | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                |
| regex_compile  | 142 ms                                                 | 180 ms: 1.26x slower                                                 |
| Geometric mean | (ref)                                                  | 1.11x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 92.1 ms: 1.05x faster                                                |
| json_loads           | 26.5 us                                                | 28.5 us: 1.07x slower                                                |
| xml_etree_generate   | 85.2 ms                                                | 97.7 ms: 1.15x slower                                                |
| tomli_loads          | 2.11 sec                                               | 2.68 sec: 1.27x slower                                               |
| xml_etree_process    | 59.0 ms                                                | 78.4 ms: 1.33x slower                                                |
| json_dumps           | 10.4 ms                                                | 13.9 ms: 1.34x slower                                                |
| unpickle_pure_python | 221 us                                                 | 333 us: 1.51x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 511 us: 1.66x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                |
| python_startup         | 9.93 ms                                                | 17.2 ms: 1.73x slower                                                |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.0 ms: 1.26x slower                                                |
| genshi_text     | 22.8 ms                                                | 30.4 ms: 1.33x slower                                                |
| django_template | 34.7 ms                                                | 50.6 ms: 1.46x slower                                                |
| mako            | 11.0 ms                                                | 17.1 ms: 1.55x slower                                                |
| Geometric mean  | (ref)                                                  | 1.40x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 800 ms: 1.39x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 821 ms: 1.32x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 438 ms: 1.28x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 352 ms: 1.27x faster                                                 |
| async_tree_none            | 464 ms                                                 | 378 ms: 1.23x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 458 ms: 1.21x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 604 ms: 1.20x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 626 ms: 1.14x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                |
| deepcopy                   | 352 us                                                 | 325 us: 1.08x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.9 ms: 1.08x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 3.28 ms: 1.05x faster                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 92.1 ms: 1.05x faster                                                |
| deepcopy_memo              | 40.3 us                                                | 39.9 us: 1.01x faster                                                |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.22 us: 1.01x slower                                                |
| coroutines                 | 23.9 ms                                                | 24.8 ms: 1.04x slower                                                |
| bpe_tokeniser              | 4.74 sec                                               | 5.01 sec: 1.06x slower                                               |
| json_loads                 | 26.5 us                                                | 28.5 us: 1.07x slower                                                |
| spectral_norm              | 110 ms                                                 | 118 ms: 1.07x slower                                                 |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.47 us: 1.13x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 97.7 ms: 1.15x slower                                                |
| docutils                   | 2.64 sec                                               | 3.08 sec: 1.17x slower                                               |
| pylint                     | 319 ms                                                 | 372 ms: 1.17x slower                                                 |
| scimark_fft                | 342 ms                                                 | 400 ms: 1.17x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.86 sec: 1.18x slower                                               |
| crypto_pyaes               | 76.6 ms                                                | 90.6 ms: 1.18x slower                                                |
| async_generators           | 384 ms                                                 | 455 ms: 1.18x slower                                                 |
| nqueens                    | 80.1 ms                                                | 96.0 ms: 1.20x slower                                                |
| dulwich_log                | 78.9 ms                                                | 94.6 ms: 1.20x slower                                                |
| regex_v8                   | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                |
| generators                 | 32.2 ms                                                | 39.0 ms: 1.21x slower                                                |
| genshi_xml                 | 50.2 ms                                                | 63.0 ms: 1.26x slower                                                |
| typing_runtime_protocols   | 163 us                                                 | 206 us: 1.26x slower                                                 |
| regex_compile              | 142 ms                                                 | 180 ms: 1.26x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 67.4 ms: 1.27x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.68 sec: 1.27x slower                                               |
| meteor_contest             | 104 ms                                                 | 133 ms: 1.28x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 137 ms: 1.28x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 963 ms: 1.30x slower                                                 |
| pycparser                  | 1.17 sec                                               | 1.52 sec: 1.30x slower                                               |
| pprint_pformat             | 1.52 sec                                               | 1.99 sec: 1.31x slower                                               |
| fannkuch                   | 372 ms                                                 | 492 ms: 1.32x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 28.9 ms: 1.33x slower                                                |
| xml_etree_process          | 59.0 ms                                                | 78.4 ms: 1.33x slower                                                |
| genshi_text                | 22.8 ms                                                | 30.4 ms: 1.33x slower                                                |
| json_dumps                 | 10.4 ms                                                | 13.9 ms: 1.34x slower                                                |
| telco                      | 6.53 ms                                                | 8.78 ms: 1.35x slower                                                |
| 2to3                       | 264 ms                                                 | 365 ms: 1.38x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 6.08 ms: 1.38x slower                                                |
| comprehensions             | 19.8 us                                                | 27.7 us: 1.40x slower                                                |
| thrift                     | 791 us                                                 | 1.11 ms: 1.40x slower                                                |
| sqlalchemy_declarative     | 143 ms                                                 | 201 ms: 1.41x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                |
| sympy_integrate            | 20.5 ms                                                | 29.6 ms: 1.44x slower                                                |
| nbody                      | 89.3 ms                                                | 130 ms: 1.45x slower                                                 |
| django_template            | 34.7 ms                                                | 50.6 ms: 1.46x slower                                                |
| coverage                   | 71.4 ms                                                | 106 ms: 1.48x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 333 us: 1.51x slower                                                 |
| logging_simple             | 6.63 us                                                | 10.1 us: 1.53x slower                                                |
| html5lib                   | 63.6 ms                                                | 97.5 ms: 1.53x slower                                                |
| logging_format             | 7.35 us                                                | 11.3 us: 1.54x slower                                                |
| pyflate                    | 448 ms                                                 | 694 ms: 1.55x slower                                                 |
| mako                       | 11.0 ms                                                | 17.1 ms: 1.55x slower                                                |
| hexiom                     | 6.17 ms                                                | 9.90 ms: 1.60x slower                                                |
| scimark_lu                 | 114 ms                                                 | 184 ms: 1.61x slower                                                 |
| sympy_str                  | 292 ms                                                 | 477 ms: 1.64x slower                                                 |
| chaos                      | 62.8 ms                                                | 104 ms: 1.65x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.81 ms: 1.66x slower                                                |
| pickle_pure_python         | 308 us                                                 | 511 us: 1.66x slower                                                 |
| richards_super             | 51.9 ms                                                | 86.8 ms: 1.67x slower                                                |
| richards                   | 45.9 ms                                                | 77.6 ms: 1.69x slower                                                |
| logging_silent             | 109 ns                                                 | 188 ns: 1.72x slower                                                 |
| float                      | 80.8 ms                                                | 139 ms: 1.73x slower                                                 |
| python_startup             | 9.93 ms                                                | 17.2 ms: 1.73x slower                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 119 ms: 1.74x slower                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 2.98 ms: 1.78x slower                                                |
| scimark_sor                | 130 ms                                                 | 235 ms: 1.81x slower                                                 |
| raytrace                   | 299 ms                                                 | 556 ms: 1.86x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 2.58 ms: 1.91x slower                                                |
| go                         | 139 ms                                                 | 269 ms: 1.93x slower                                                 |
| sympy_expand               | 468 ms                                                 | 961 ms: 2.05x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 352 ms: 2.12x slower                                                 |
| deltablue                  | 3.45 ms                                                | 8.13 ms: 2.36x slower                                                |
| bench_thread_pool          | 941 us                                                 | 3.34 ms: 3.55x slower                                                |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 9.99x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.33x slower                                                         |

Benchmark hidden because not significant (1): json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241203-3.14.0a2+-3bfbf91-NOGIL/bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.219x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.33x