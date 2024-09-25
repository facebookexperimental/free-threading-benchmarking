# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_thread_loc
- machine: linux-x86_64
- commit hash: d8a840b
- commit date: 2024-09-03
- overall geometric mean: 1.38x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 698 ms: 1.53x slower                                                 |
| docutils       | 4.00 sec                                               | 4.84 sec: 1.21x slower                                               |
| html5lib       | 88.9 ms                                                | 142 ms: 1.60x slower                                                 |
| tornado_http   | 266 ms                                                 | 399 ms: 1.50x slower                                                 |
| Geometric mean | (ref)                                                  | 1.45x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.15 sec: 1.68x faster                                               |
| async_tree_io              | 1.85 sec                                               | 1.30 sec: 1.42x faster                                               |
| async_tree_none_tg         | 704 ms                                                 | 505 ms: 1.39x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 676 ms: 1.38x faster                                                 |
| async_tree_memoization     | 977 ms                                                 | 727 ms: 1.34x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 851 ms: 1.29x faster                                                 |
| async_tree_none            | 741 ms                                                 | 581 ms: 1.28x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 974 ms: 1.11x faster                                                 |
| async_generators           | 589 ms                                                 | 712 ms: 1.21x slower                                                 |
| asyncio_tcp                | 923 ms                                                 | 1.12 sec: 1.21x slower                                               |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.41 sec: 1.21x slower                                               |
| coroutines                 | 29.5 ms                                                | 41.6 ms: 1.41x slower                                                |
| Geometric mean             | (ref)                                                  | 1.12x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 123 ms                                                 | 192 ms: 1.56x slower                                                 |
| nbody          | 119 ms                                                 | 271 ms: 2.28x slower                                                 |
| Geometric mean | (ref)                                                  | 1.52x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.57 ms: 1.12x faster                                                |
| regex_dna      | 278 ms                                                 | 297 ms: 1.07x slower                                                 |
| regex_v8       | 32.5 ms                                                | 35.5 ms: 1.09x slower                                                |
| regex_compile  | 187 ms                                                 | 312 ms: 1.67x slower                                                 |
| Geometric mean | (ref)                                                  | 1.15x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle               | 16.4 us                                                | 13.8 us: 1.18x faster                                                |
| pickle_dict          | 52.7 us                                                | 44.6 us: 1.18x faster                                                |
| unpickle             | 21.2 us                                                | 22.9 us: 1.08x slower                                                |
| json_loads           | 37.9 us                                                | 43.5 us: 1.15x slower                                                |
| unpickle_list        | 6.83 us                                                | 8.26 us: 1.21x slower                                                |
| json_dumps           | 14.3 ms                                                | 17.3 ms: 1.21x slower                                                |
| xml_etree_generate   | 127 ms                                                 | 166 ms: 1.31x slower                                                 |
| tomli_loads          | 2.88 sec                                               | 4.40 sec: 1.53x slower                                               |
| xml_etree_process    | 83.7 ms                                                | 131 ms: 1.57x slower                                                 |
| pickle_pure_python   | 436 us                                                 | 812 us: 1.86x slower                                                 |
| unpickle_pure_python | 300 us                                                 | 597 us: 1.99x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.22x slower                                                         |

Benchmark hidden because not significant (3): xml_etree_parse, pickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 21.7 ms: 1.24x slower                                                |
| python_startup         | 23.7 ms                                                | 35.2 ms: 1.49x slower                                                |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 120 ms: 1.77x slower                                                 |
| genshi_text     | 30.2 ms                                                | 55.2 ms: 1.83x slower                                                |
| django_template | 44.9 ms                                                | 82.3 ms: 1.83x slower                                                |
| mako            | 15.7 ms                                                | 32.1 ms: 2.04x slower                                                |
| Geometric mean  | (ref)                                                  | 1.86x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.15 sec: 1.68x faster                                               |
| async_tree_io              | 1.85 sec                                               | 1.30 sec: 1.42x faster                                               |
| async_tree_none_tg         | 704 ms                                                 | 505 ms: 1.39x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 676 ms: 1.38x faster                                                 |
| async_tree_memoization     | 977 ms                                                 | 727 ms: 1.34x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 851 ms: 1.29x faster                                                 |
| async_tree_none            | 741 ms                                                 | 581 ms: 1.28x faster                                                 |
| pickle                     | 16.4 us                                                | 13.8 us: 1.18x faster                                                |
| pickle_dict                | 52.7 us                                                | 44.6 us: 1.18x faster                                                |
| gc_traversal               | 5.86 ms                                                | 5.05 ms: 1.16x faster                                                |
| regex_effbot               | 5.13 ms                                                | 4.57 ms: 1.12x faster                                                |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 974 ms: 1.11x faster                                                 |
| create_gc_cycles           | 1.94 ms                                                | 1.85 ms: 1.05x faster                                                |
| regex_dna                  | 278 ms                                                 | 297 ms: 1.07x slower                                                 |
| scimark_fft                | 500 ms                                                 | 539 ms: 1.08x slower                                                 |
| unpickle                   | 21.2 us                                                | 22.9 us: 1.08x slower                                                |
| regex_v8                   | 32.5 ms                                                | 35.5 ms: 1.09x slower                                                |
| json_loads                 | 37.9 us                                                | 43.5 us: 1.15x slower                                                |
| pathlib                    | 31.6 ms                                                | 36.3 ms: 1.15x slower                                                |
| sqlite_synth               | 3.87 us                                                | 4.64 us: 1.20x slower                                                |
| deepcopy                   | 468 us                                                 | 564 us: 1.21x slower                                                 |
| unpickle_list              | 6.83 us                                                | 8.26 us: 1.21x slower                                                |
| json_dumps                 | 14.3 ms                                                | 17.3 ms: 1.21x slower                                                |
| async_generators           | 589 ms                                                 | 712 ms: 1.21x slower                                                 |
| docutils                   | 4.00 sec                                               | 4.84 sec: 1.21x slower                                               |
| asyncio_tcp                | 923 ms                                                 | 1.12 sec: 1.21x slower                                               |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.41 sec: 1.21x slower                                               |
| pycparser                  | 1.79 sec                                               | 2.20 sec: 1.23x slower                                               |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.22 ms: 1.23x slower                                                |
| mdp                        | 3.97 sec                                               | 4.90 sec: 1.23x slower                                               |
| python_startup_no_site     | 17.6 ms                                                | 21.7 ms: 1.24x slower                                                |
| json                       | 6.85 ms                                                | 8.56 ms: 1.25x slower                                                |
| bench_thread_pool          | 3.48 ms                                                | 4.51 ms: 1.30x slower                                                |
| generators                 | 41.1 ms                                                | 53.5 ms: 1.30x slower                                                |
| xml_etree_generate         | 127 ms                                                 | 166 ms: 1.31x slower                                                 |
| pylint                     | 465 ms                                                 | 609 ms: 1.31x slower                                                 |
| meteor_contest             | 146 ms                                                 | 195 ms: 1.33x slower                                                 |
| nqueens                    | 117 ms                                                 | 160 ms: 1.37x slower                                                 |
| deepcopy_memo              | 52.4 us                                                | 72.1 us: 1.37x slower                                                |
| coroutines                 | 29.5 ms                                                | 41.6 ms: 1.41x slower                                                |
| fannkuch                   | 540 ms                                                 | 761 ms: 1.41x slower                                                 |
| comprehensions             | 27.1 us                                                | 38.6 us: 1.42x slower                                                |
| pyflate                    | 727 ms                                                 | 1.04 sec: 1.43x slower                                               |
| spectral_norm              | 156 ms                                                 | 224 ms: 1.44x slower                                                 |
| crypto_pyaes               | 107 ms                                                 | 156 ms: 1.46x slower                                                 |
| telco                      | 9.59 ms                                                | 14.0 ms: 1.46x slower                                                |
| python_startup             | 23.7 ms                                                | 35.2 ms: 1.49x slower                                                |
| bpe_tokeniser              | 6.59 sec                                               | 9.87 sec: 1.50x slower                                               |
| tornado_http               | 266 ms                                                 | 399 ms: 1.50x slower                                                 |
| coverage                   | 95.4 ms                                                | 144 ms: 1.52x slower                                                 |
| tomli_loads                | 2.88 sec                                               | 4.40 sec: 1.53x slower                                               |
| 2to3                       | 456 ms                                                 | 698 ms: 1.53x slower                                                 |
| deepcopy_reduce            | 4.04 us                                                | 6.24 us: 1.55x slower                                                |
| float                      | 123 ms                                                 | 192 ms: 1.56x slower                                                 |
| sqlglot_optimize           | 76.0 ms                                                | 119 ms: 1.57x slower                                                 |
| xml_etree_process          | 83.7 ms                                                | 131 ms: 1.57x slower                                                 |
| sqlglot_normalize          | 157 ms                                                 | 249 ms: 1.58x slower                                                 |
| html5lib                   | 88.9 ms                                                | 142 ms: 1.60x slower                                                 |
| thrift                     | 1.06 ms                                                | 1.73 ms: 1.64x slower                                                |
| scimark_monte_carlo        | 96.4 ms                                                | 160 ms: 1.66x slower                                                 |
| regex_compile              | 187 ms                                                 | 312 ms: 1.67x slower                                                 |
| typing_runtime_protocols   | 224 us                                                 | 381 us: 1.70x slower                                                 |
| sympy_integrate            | 29.8 ms                                                | 51.4 ms: 1.73x slower                                                |
| pprint_pformat             | 1.98 sec                                               | 3.47 sec: 1.75x slower                                               |
| logging_simple             | 9.45 us                                                | 16.6 us: 1.76x slower                                                |
| genshi_xml                 | 67.6 ms                                                | 120 ms: 1.77x slower                                                 |
| richards                   | 60.3 ms                                                | 107 ms: 1.77x slower                                                 |
| sympy_str                  | 385 ms                                                 | 698 ms: 1.81x slower                                                 |
| chaos                      | 84.9 ms                                                | 154 ms: 1.82x slower                                                 |
| pprint_safe_repr           | 967 ms                                                 | 1.77 sec: 1.83x slower                                               |
| genshi_text                | 30.2 ms                                                | 55.2 ms: 1.83x slower                                                |
| django_template            | 44.9 ms                                                | 82.3 ms: 1.83x slower                                                |
| pickle_pure_python         | 436 us                                                 | 812 us: 1.86x slower                                                 |
| richards_super             | 72.8 ms                                                | 137 ms: 1.88x slower                                                 |
| logging_silent             | 139 ns                                                 | 262 ns: 1.88x slower                                                 |
| hexiom                     | 8.27 ms                                                | 15.8 ms: 1.91x slower                                                |
| raytrace                   | 408 ms                                                 | 788 ms: 1.93x slower                                                 |
| scimark_sor                | 167 ms                                                 | 331 ms: 1.99x slower                                                 |
| logging_format             | 9.59 us                                                | 19.1 us: 1.99x slower                                                |
| unpickle_pure_python       | 300 us                                                 | 597 us: 1.99x slower                                                 |
| sqlglot_transpile          | 2.34 ms                                                | 4.66 ms: 1.99x slower                                                |
| mako                       | 15.7 ms                                                | 32.1 ms: 2.04x slower                                                |
| scimark_lu                 | 152 ms                                                 | 317 ms: 2.09x slower                                                 |
| go                         | 172 ms                                                 | 370 ms: 2.15x slower                                                 |
| sqlglot_parse              | 1.79 ms                                                | 4.06 ms: 2.27x slower                                                |
| nbody                      | 119 ms                                                 | 271 ms: 2.28x slower                                                 |
| sympy_sum                  | 222 ms                                                 | 512 ms: 2.31x slower                                                 |
| sympy_expand               | 582 ms                                                 | 1.35 sec: 2.31x slower                                               |
| deltablue                  | 4.27 ms                                                | 11.5 ms: 2.69x slower                                                |
| unpack_sequence            | 60.2 ns                                                | 191 ns: 3.18x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.38x slower                                                         |

Benchmark hidden because not significant (6): bench_mp_pool, pidigits, asyncio_websockets, xml_etree_parse, pickle_list, xml_etree_iterparse
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.22x

# Memory
- memory change: 1.18x