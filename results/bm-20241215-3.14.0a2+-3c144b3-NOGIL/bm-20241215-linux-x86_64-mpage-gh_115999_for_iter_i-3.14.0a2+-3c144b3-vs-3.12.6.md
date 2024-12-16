# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_for_iter_i
- machine: linux-x86_64
- commit hash: 3c144b3
- commit date: 2024-12-15
- overall geometric mean: 1.036x slower
- HPT reliability: 99.94%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 526 ms: 1.15x slower                                                  |
| docutils       | 4.00 sec                                               | 4.13 sec: 1.03x slower                                                |
| html5lib       | 88.9 ms                                                | 104 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 742 ms: 2.61x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 837 ms: 2.21x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 321 ms: 2.19x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 447 ms: 2.08x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 514 ms: 1.90x faster                                                  |
| async_tree_none            | 741 ms                                                 | 393 ms: 1.89x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 635 ms: 1.73x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 724 ms: 1.49x faster                                                  |
| async_generators           | 589 ms                                                 | 624 ms: 1.06x slower                                                  |
| coroutines                 | 29.5 ms                                                | 32.4 ms: 1.10x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.63x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 123 ms                                                 | 111 ms: 1.11x faster                                                  |
| pidigits       | 250 ms                                                 | 233 ms: 1.07x faster                                                  |
| nbody          | 119 ms                                                 | 177 ms: 1.48x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.36 ms: 1.18x faster                                                 |
| regex_compile  | 187 ms                                                 | 198 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 131 ms: 1.29x faster                                                  |
| xml_etree_parse      | 241 ms                                                 | 198 ms: 1.21x faster                                                  |
| json_loads           | 37.9 us                                                | 34.6 us: 1.09x faster                                                 |
| tomli_loads          | 2.88 sec                                               | 3.04 sec: 1.05x slower                                                |
| xml_etree_process    | 83.7 ms                                                | 92.1 ms: 1.10x slower                                                 |
| pickle_pure_python   | 436 us                                                 | 482 us: 1.11x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 340 us: 1.13x slower                                                  |
| json_dumps           | 14.3 ms                                                | 17.4 ms: 1.21x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.6 ms: 1.11x slower                                                 |
| python_startup         | 23.7 ms                                                | 31.8 ms: 1.34x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 77.4 ms: 1.15x slower                                                 |
| django_template | 44.9 ms                                                | 51.9 ms: 1.15x slower                                                 |
| genshi_text     | 30.2 ms                                                | 36.6 ms: 1.21x slower                                                 |
| mako            | 15.7 ms                                                | 24.5 ms: 1.55x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 742 ms: 2.61x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 837 ms: 2.21x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 321 ms: 2.19x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 447 ms: 2.08x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 514 ms: 1.90x faster                                                  |
| async_tree_none            | 741 ms                                                 | 393 ms: 1.89x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 635 ms: 1.73x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 724 ms: 1.49x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 131 ms: 1.29x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 198 ms: 1.21x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 4.36 ms: 1.18x faster                                                 |
| pycparser                  | 1.79 sec                                               | 1.58 sec: 1.13x faster                                                |
| float                      | 123 ms                                                 | 111 ms: 1.11x faster                                                  |
| deepcopy                   | 468 us                                                 | 422 us: 1.11x faster                                                  |
| pathlib                    | 31.6 ms                                                | 28.6 ms: 1.11x faster                                                 |
| json_loads                 | 37.9 us                                                | 34.6 us: 1.09x faster                                                 |
| deepcopy_memo              | 52.4 us                                                | 48.5 us: 1.08x faster                                                 |
| comprehensions             | 27.1 us                                                | 25.1 us: 1.08x faster                                                 |
| sqlite_synth               | 3.87 us                                                | 3.61 us: 1.07x faster                                                 |
| pidigits                   | 250 ms                                                 | 233 ms: 1.07x faster                                                  |
| generators                 | 41.1 ms                                                | 42.4 ms: 1.03x slower                                                 |
| docutils                   | 4.00 sec                                               | 4.13 sec: 1.03x slower                                                |
| scimark_fft                | 500 ms                                                 | 520 ms: 1.04x slower                                                  |
| logging_silent             | 139 ns                                                 | 146 ns: 1.05x slower                                                  |
| spectral_norm              | 156 ms                                                 | 163 ms: 1.05x slower                                                  |
| tomli_loads                | 2.88 sec                                               | 3.04 sec: 1.05x slower                                                |
| async_generators           | 589 ms                                                 | 624 ms: 1.06x slower                                                  |
| regex_compile              | 187 ms                                                 | 198 ms: 1.06x slower                                                  |
| deepcopy_reduce            | 4.04 us                                                | 4.28 us: 1.06x slower                                                 |
| nqueens                    | 117 ms                                                 | 125 ms: 1.07x slower                                                  |
| raytrace                   | 408 ms                                                 | 437 ms: 1.07x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 7.11 sec: 1.08x slower                                                |
| sqlalchemy_declarative     | 218 ms                                                 | 238 ms: 1.09x slower                                                  |
| sqlglot_optimize           | 76.0 ms                                                | 83.2 ms: 1.09x slower                                                 |
| coroutines                 | 29.5 ms                                                | 32.4 ms: 1.10x slower                                                 |
| xml_etree_process          | 83.7 ms                                                | 92.1 ms: 1.10x slower                                                 |
| mdp                        | 3.97 sec                                               | 4.39 sec: 1.10x slower                                                |
| pickle_pure_python         | 436 us                                                 | 482 us: 1.11x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 19.6 ms: 1.11x slower                                                 |
| gc_traversal               | 5.86 ms                                                | 6.53 ms: 1.11x slower                                                 |
| logging_format             | 9.59 us                                                | 10.7 us: 1.12x slower                                                 |
| unpickle_pure_python       | 300 us                                                 | 340 us: 1.13x slower                                                  |
| meteor_contest             | 146 ms                                                 | 166 ms: 1.14x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.10 sec: 1.14x slower                                                |
| genshi_xml                 | 67.6 ms                                                | 77.4 ms: 1.15x slower                                                 |
| 2to3                       | 456 ms                                                 | 526 ms: 1.15x slower                                                  |
| django_template            | 44.9 ms                                                | 51.9 ms: 1.15x slower                                                 |
| crypto_pyaes               | 107 ms                                                 | 124 ms: 1.16x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 2.30 sec: 1.16x slower                                                |
| richards_super             | 72.8 ms                                                | 84.6 ms: 1.16x slower                                                 |
| hexiom                     | 8.27 ms                                                | 9.62 ms: 1.16x slower                                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 112 ms: 1.16x slower                                                  |
| html5lib                   | 88.9 ms                                                | 104 ms: 1.17x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 263 us: 1.17x slower                                                  |
| scimark_sor                | 167 ms                                                 | 196 ms: 1.18x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.25 ms: 1.18x slower                                                 |
| sqlglot_transpile          | 2.34 ms                                                | 2.78 ms: 1.19x slower                                                 |
| telco                      | 9.59 ms                                                | 11.5 ms: 1.20x slower                                                 |
| sqlglot_parse              | 1.79 ms                                                | 2.15 ms: 1.20x slower                                                 |
| genshi_text                | 30.2 ms                                                | 36.6 ms: 1.21x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 17.4 ms: 1.21x slower                                                 |
| chaos                      | 84.9 ms                                                | 104 ms: 1.22x slower                                                  |
| fannkuch                   | 540 ms                                                 | 663 ms: 1.23x slower                                                  |
| richards                   | 60.3 ms                                                | 75.5 ms: 1.25x slower                                                 |
| sympy_integrate            | 29.8 ms                                                | 37.4 ms: 1.26x slower                                                 |
| sqlalchemy_imperative      | 24.7 ms                                                | 31.6 ms: 1.28x slower                                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.58 ms: 1.28x slower                                                 |
| scimark_lu                 | 152 ms                                                 | 201 ms: 1.32x slower                                                  |
| python_startup             | 23.7 ms                                                | 31.8 ms: 1.34x slower                                                 |
| deltablue                  | 4.27 ms                                                | 5.91 ms: 1.39x slower                                                 |
| sympy_str                  | 385 ms                                                 | 548 ms: 1.42x slower                                                  |
| coverage                   | 95.4 ms                                                | 136 ms: 1.43x slower                                                  |
| nbody                      | 119 ms                                                 | 177 ms: 1.48x slower                                                  |
| mako                       | 15.7 ms                                                | 24.5 ms: 1.55x slower                                                 |
| create_gc_cycles           | 1.94 ms                                                | 3.42 ms: 1.76x slower                                                 |
| sympy_sum                  | 222 ms                                                 | 392 ms: 1.77x slower                                                  |
| sympy_expand               | 582 ms                                                 | 1.10 sec: 1.89x slower                                                |
| bench_mp_pool              | 20.7 ms                                                | 88.4 ms: 4.27x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                          |

Benchmark hidden because not significant (12): json, sqlglot_normalize, asyncio_websockets, pyflate, logging_simple, bench_thread_pool, dulwich_log, regex_dna, pylint, go, xml_etree_generate, regex_v8
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241215-3.14.0a2+-3c144b3-NOGIL/bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.036x slower

# HPT report

- Reliability score: 99.94% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.35x