# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: dc12237
- commit date: 2024-09-28
- overall geometric mean: 1.46x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.31x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 264 ms                                                 | 408 ms: 1.55x slower                                  |
| docutils       | 2.64 sec                                               | 3.29 sec: 1.24x slower                                |
| html5lib       | 63.6 ms                                                | 102 ms: 1.60x slower                                  |
| tornado_http   | 119 ms                                                 | 161 ms: 1.35x slower                                  |
| Geometric mean | (ref)                                                  | 1.43x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 906 ms: 1.23x faster                                  |
| async_tree_none_tg         | 446 ms                                                 | 376 ms: 1.19x faster                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 472 ms: 1.19x faster                                  |
| async_tree_io              | 1.08 sec                                               | 949 ms: 1.14x faster                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 635 ms: 1.14x faster                                  |
| async_tree_none            | 464 ms                                                 | 421 ms: 1.10x faster                                  |
| async_tree_memoization     | 555 ms                                                 | 506 ms: 1.10x faster                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 670 ms: 1.07x faster                                  |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                  |
| asyncio_tcp                | 519 ms                                                 | 574 ms: 1.11x slower                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.74 sec: 1.15x slower                                |
| async_generators           | 384 ms                                                 | 497 ms: 1.29x slower                                  |
| coroutines                 | 23.9 ms                                                | 31.4 ms: 1.31x slower                                 |
| Geometric mean             | (ref)                                                  | 1.02x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 184 ms                                                 | 188 ms: 1.02x slower                                  |
| float          | 80.8 ms                                                | 153 ms: 1.89x slower                                  |
| nbody          | 89.3 ms                                                | 223 ms: 2.50x slower                                  |
| Geometric mean | (ref)                                                  | 1.69x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.13 ms: 1.01x faster                                 |
| regex_dna      | 168 ms                                                 | 192 ms: 1.14x slower                                  |
| regex_v8       | 20.6 ms                                                | 26.3 ms: 1.28x slower                                 |
| regex_compile  | 142 ms                                                 | 228 ms: 1.60x slower                                  |
| Geometric mean | (ref)                                                  | 1.23x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 134 ms: 1.03x faster                                  |
| unpickle             | 14.1 us                                                | 15.3 us: 1.09x slower                                 |
| unpickle_list        | 4.67 us                                                | 5.10 us: 1.09x slower                                 |
| json_loads           | 26.5 us                                                | 29.2 us: 1.10x slower                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 109 ms: 1.12x slower                                  |
| xml_etree_generate   | 85.2 ms                                                | 112 ms: 1.31x slower                                  |
| json_dumps           | 10.4 ms                                                | 13.7 ms: 1.32x slower                                 |
| tomli_loads          | 2.11 sec                                               | 3.24 sec: 1.54x slower                                |
| xml_etree_process    | 59.0 ms                                                | 92.0 ms: 1.56x slower                                 |
| unpickle_pure_python | 221 us                                                 | 408 us: 1.85x slower                                  |
| pickle_pure_python   | 308 us                                                 | 592 us: 1.92x slower                                  |
| Geometric mean       | (ref)                                                  | 1.24x slower                                          |

Benchmark hidden because not significant (3): pickle, pickle_list, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.1 ms: 1.40x slower                                 |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                 |
| Geometric mean         | (ref)                                                  | 1.48x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 80.7 ms: 1.61x slower                                 |
| genshi_text     | 22.8 ms                                                | 39.5 ms: 1.73x slower                                 |
| django_template | 34.7 ms                                                | 64.1 ms: 1.85x slower                                 |
| mako            | 11.0 ms                                                | 20.4 ms: 1.85x slower                                 |
| Geometric mean  | (ref)                                                  | 1.76x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 2.44 ms: 1.41x faster                                 |
| async_tree_io_tg           | 1.11 sec                                               | 906 ms: 1.23x faster                                  |
| async_tree_none_tg         | 446 ms                                                 | 376 ms: 1.19x faster                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 472 ms: 1.19x faster                                  |
| async_tree_io              | 1.08 sec                                               | 949 ms: 1.14x faster                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 635 ms: 1.14x faster                                  |
| async_tree_none            | 464 ms                                                 | 421 ms: 1.10x faster                                  |
| async_tree_memoization     | 555 ms                                                 | 506 ms: 1.10x faster                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 670 ms: 1.07x faster                                  |
| xml_etree_parse            | 139 ms                                                 | 134 ms: 1.03x faster                                  |
| regex_effbot               | 3.17 ms                                                | 3.13 ms: 1.01x faster                                 |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.11 ms: 1.01x slower                                 |
| pidigits                   | 184 ms                                                 | 188 ms: 1.02x slower                                  |
| pathlib                    | 21.5 ms                                                | 22.0 ms: 1.02x slower                                 |
| json                       | 5.02 ms                                                | 5.33 ms: 1.06x slower                                 |
| sqlite_synth               | 2.20 us                                                | 2.39 us: 1.09x slower                                 |
| unpickle                   | 14.1 us                                                | 15.3 us: 1.09x slower                                 |
| unpickle_list              | 4.67 us                                                | 5.10 us: 1.09x slower                                 |
| json_loads                 | 26.5 us                                                | 29.2 us: 1.10x slower                                 |
| asyncio_tcp                | 519 ms                                                 | 574 ms: 1.11x slower                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 109 ms: 1.12x slower                                  |
| regex_dna                  | 168 ms                                                 | 192 ms: 1.14x slower                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.74 sec: 1.15x slower                                |
| deepcopy                   | 352 us                                                 | 430 us: 1.22x slower                                  |
| docutils                   | 2.64 sec                                               | 3.29 sec: 1.24x slower                                |
| mdp                        | 2.42 sec                                               | 3.04 sec: 1.26x slower                                |
| generators                 | 32.2 ms                                                | 40.6 ms: 1.26x slower                                 |
| regex_v8                   | 20.6 ms                                                | 26.3 ms: 1.28x slower                                 |
| async_generators           | 384 ms                                                 | 497 ms: 1.29x slower                                  |
| pylint                     | 319 ms                                                 | 415 ms: 1.30x slower                                  |
| dulwich_log                | 78.9 ms                                                | 103 ms: 1.31x slower                                  |
| xml_etree_generate         | 85.2 ms                                                | 112 ms: 1.31x slower                                  |
| coroutines                 | 23.9 ms                                                | 31.4 ms: 1.31x slower                                 |
| deepcopy_memo              | 40.3 us                                                | 53.0 us: 1.31x slower                                 |
| json_dumps                 | 10.4 ms                                                | 13.7 ms: 1.32x slower                                 |
| meteor_contest             | 104 ms                                                 | 138 ms: 1.34x slower                                  |
| scimark_fft                | 342 ms                                                 | 458 ms: 1.34x slower                                  |
| bpe_tokeniser              | 4.74 sec                                               | 6.37 sec: 1.35x slower                                |
| tornado_http               | 119 ms                                                 | 161 ms: 1.35x slower                                  |
| python_startup_no_site     | 7.16 ms                                                | 10.1 ms: 1.40x slower                                 |
| crypto_pyaes               | 76.6 ms                                                | 109 ms: 1.42x slower                                  |
| pycparser                  | 1.17 sec                                               | 1.67 sec: 1.43x slower                                |
| telco                      | 6.53 ms                                                | 9.32 ms: 1.43x slower                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 6.36 ms: 1.45x slower                                 |
| coverage                   | 71.4 ms                                                | 104 ms: 1.45x slower                                  |
| deepcopy_reduce            | 3.08 us                                                | 4.52 us: 1.47x slower                                 |
| nqueens                    | 80.1 ms                                                | 119 ms: 1.48x slower                                  |
| typing_runtime_protocols   | 163 us                                                 | 245 us: 1.50x slower                                  |
| comprehensions             | 19.8 us                                                | 30.1 us: 1.52x slower                                 |
| tomli_loads                | 2.11 sec                                               | 3.24 sec: 1.54x slower                                |
| 2to3                       | 264 ms                                                 | 408 ms: 1.55x slower                                  |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.55x slower                                 |
| fannkuch                   | 372 ms                                                 | 577 ms: 1.55x slower                                  |
| xml_etree_process          | 59.0 ms                                                | 92.0 ms: 1.56x slower                                 |
| sympy_integrate            | 20.5 ms                                                | 32.4 ms: 1.58x slower                                 |
| regex_compile              | 142 ms                                                 | 228 ms: 1.60x slower                                  |
| html5lib                   | 63.6 ms                                                | 102 ms: 1.60x slower                                  |
| spectral_norm              | 110 ms                                                 | 177 ms: 1.60x slower                                  |
| thrift                     | 791 us                                                 | 1.27 ms: 1.61x slower                                 |
| genshi_xml                 | 50.2 ms                                                | 80.7 ms: 1.61x slower                                 |
| sqlglot_normalize          | 107 ms                                                 | 177 ms: 1.66x slower                                  |
| sqlglot_optimize           | 53.3 ms                                                | 89.6 ms: 1.68x slower                                 |
| pyflate                    | 448 ms                                                 | 775 ms: 1.73x slower                                  |
| genshi_text                | 22.8 ms                                                | 39.5 ms: 1.73x slower                                 |
| pprint_safe_repr           | 743 ms                                                 | 1.31 sec: 1.77x slower                                |
| logging_format             | 7.35 us                                                | 13.1 us: 1.78x slower                                 |
| pprint_pformat             | 1.52 sec                                               | 2.72 sec: 1.79x slower                                |
| logging_simple             | 6.63 us                                                | 11.9 us: 1.80x slower                                 |
| sympy_str                  | 292 ms                                                 | 535 ms: 1.84x slower                                  |
| django_template            | 34.7 ms                                                | 64.1 ms: 1.85x slower                                 |
| mako                       | 11.0 ms                                                | 20.4 ms: 1.85x slower                                 |
| unpickle_pure_python       | 221 us                                                 | 408 us: 1.85x slower                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 129 ms: 1.88x slower                                  |
| float                      | 80.8 ms                                                | 153 ms: 1.89x slower                                  |
| richards                   | 45.9 ms                                                | 88.2 ms: 1.92x slower                                 |
| pickle_pure_python         | 308 us                                                 | 592 us: 1.92x slower                                  |
| logging_silent             | 109 ns                                                 | 210 ns: 1.93x slower                                  |
| sqlglot_transpile          | 1.67 ms                                                | 3.33 ms: 1.99x slower                                 |
| hexiom                     | 6.17 ms                                                | 12.3 ms: 1.99x slower                                 |
| chaos                      | 62.8 ms                                                | 127 ms: 2.02x slower                                  |
| richards_super             | 51.9 ms                                                | 107 ms: 2.06x slower                                  |
| scimark_sor                | 130 ms                                                 | 269 ms: 2.07x slower                                  |
| sqlglot_parse              | 1.36 ms                                                | 2.86 ms: 2.11x slower                                 |
| raytrace                   | 299 ms                                                 | 634 ms: 2.12x slower                                  |
| scimark_lu                 | 114 ms                                                 | 244 ms: 2.14x slower                                  |
| go                         | 139 ms                                                 | 301 ms: 2.17x slower                                  |
| sympy_expand               | 468 ms                                                 | 1.05 sec: 2.25x slower                                |
| sympy_sum                  | 166 ms                                                 | 379 ms: 2.29x slower                                  |
| nbody                      | 89.3 ms                                                | 223 ms: 2.50x slower                                  |
| deltablue                  | 3.45 ms                                                | 8.89 ms: 2.58x slower                                 |
| unpack_sequence            | 52.1 ns                                                | 149 ns: 2.87x slower                                  |
| bench_thread_pool          | 941 us                                                 | 3.14 ms: 3.34x slower                                 |
| bench_mp_pool              | 10.8 ms                                                | 70.7 ms: 6.55x slower                                 |
| Geometric mean             | (ref)                                                  | 1.46x slower                                          |

Benchmark hidden because not significant (3): pickle, pickle_list, pickle_dict
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.33x
- 99% likely to have a slowdown of 1.31x

# Memory
- memory change: 1.18x