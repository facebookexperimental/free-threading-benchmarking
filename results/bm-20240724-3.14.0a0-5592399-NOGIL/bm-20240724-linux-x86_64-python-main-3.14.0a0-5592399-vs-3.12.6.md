# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5592399
- commit date: 2024-07-24
- overall geometric mean: 1.37x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                                 | 662 ms: 1.45x slower                                  |
| docutils       | 4.00 sec                                               | 4.97 sec: 1.24x slower                                |
| html5lib       | 88.9 ms                                                | 137 ms: 1.54x slower                                  |
| tornado_http   | 266 ms                                                 | 339 ms: 1.27x slower                                  |
| Geometric mean | (ref)                                                  | 1.37x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.17 sec: 1.66x faster                                |
| async_tree_io              | 1.85 sec                                               | 1.27 sec: 1.46x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 652 ms: 1.43x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 514 ms: 1.37x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 850 ms: 1.30x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 759 ms: 1.29x faster                                  |
| async_tree_none            | 741 ms                                                 | 586 ms: 1.27x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 959 ms: 1.12x faster                                  |
| asyncio_websockets         | 748 ms                                                 | 768 ms: 1.03x slower                                  |
| asyncio_tcp                | 923 ms                                                 | 1.08 sec: 1.17x slower                                |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.42 sec: 1.22x slower                                |
| async_generators           | 589 ms                                                 | 721 ms: 1.22x slower                                  |
| coroutines                 | 29.5 ms                                                | 41.7 ms: 1.41x slower                                 |
| Geometric mean             | (ref)                                                  | 1.12x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 250 ms                                                 | 241 ms: 1.04x faster                                  |
| float          | 123 ms                                                 | 211 ms: 1.71x slower                                  |
| nbody          | 119 ms                                                 | 278 ms: 2.33x slower                                  |
| Geometric mean | (ref)                                                  | 1.57x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.76 ms: 1.08x faster                                 |
| regex_v8       | 32.5 ms                                                | 37.6 ms: 1.16x slower                                 |
| regex_compile  | 187 ms                                                 | 307 ms: 1.65x slower                                  |
| Geometric mean | (ref)                                                  | 1.16x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 208 ms: 1.16x faster                                  |
| pickle_dict          | 52.7 us                                                | 45.7 us: 1.15x faster                                 |
| pickle               | 16.4 us                                                | 14.4 us: 1.14x faster                                 |
| pickle_list          | 6.97 us                                                | 6.68 us: 1.04x faster                                 |
| unpickle_list        | 6.83 us                                                | 7.97 us: 1.17x slower                                 |
| json_loads           | 37.9 us                                                | 45.6 us: 1.20x slower                                 |
| xml_etree_generate   | 127 ms                                                 | 164 ms: 1.29x slower                                  |
| json_dumps           | 14.3 ms                                                | 19.0 ms: 1.32x slower                                 |
| tomli_loads          | 2.88 sec                                               | 4.32 sec: 1.50x slower                                |
| xml_etree_process    | 83.7 ms                                                | 127 ms: 1.52x slower                                  |
| unpickle_pure_python | 300 us                                                 | 547 us: 1.82x slower                                  |
| pickle_pure_python   | 436 us                                                 | 801 us: 1.84x slower                                  |
| Geometric mean       | (ref)                                                  | 1.19x slower                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.3 ms: 1.10x slower                                 |
| python_startup         | 23.7 ms                                                | 29.1 ms: 1.23x slower                                 |
| Geometric mean         | (ref)                                                  | 1.16x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 53.7 ms: 1.78x slower                                 |
| genshi_xml      | 67.6 ms                                                | 125 ms: 1.85x slower                                  |
| django_template | 44.9 ms                                                | 86.4 ms: 1.92x slower                                 |
| mako            | 15.7 ms                                                | 31.1 ms: 1.98x slower                                 |
| Geometric mean  | (ref)                                                  | 1.88x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.17 sec: 1.66x faster                                |
| async_tree_io              | 1.85 sec                                               | 1.27 sec: 1.46x faster                                |
| bench_mp_pool              | 20.7 ms                                                | 14.4 ms: 1.43x faster                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 652 ms: 1.43x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 514 ms: 1.37x faster                                  |
| gc_traversal               | 5.86 ms                                                | 4.51 ms: 1.30x faster                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 850 ms: 1.30x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 759 ms: 1.29x faster                                  |
| async_tree_none            | 741 ms                                                 | 586 ms: 1.27x faster                                  |
| xml_etree_parse            | 241 ms                                                 | 208 ms: 1.16x faster                                  |
| pickle_dict                | 52.7 us                                                | 45.7 us: 1.15x faster                                 |
| pickle                     | 16.4 us                                                | 14.4 us: 1.14x faster                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 959 ms: 1.12x faster                                  |
| regex_effbot               | 5.13 ms                                                | 4.76 ms: 1.08x faster                                 |
| pickle_list                | 6.97 us                                                | 6.68 us: 1.04x faster                                 |
| pidigits                   | 250 ms                                                 | 241 ms: 1.04x faster                                  |
| asyncio_websockets         | 748 ms                                                 | 768 ms: 1.03x slower                                  |
| pathlib                    | 31.6 ms                                                | 34.2 ms: 1.08x slower                                 |
| python_startup_no_site     | 17.6 ms                                                | 19.3 ms: 1.10x slower                                 |
| sqlite_synth               | 3.87 us                                                | 4.39 us: 1.13x slower                                 |
| regex_v8                   | 32.5 ms                                                | 37.6 ms: 1.16x slower                                 |
| unpickle_list              | 6.83 us                                                | 7.97 us: 1.17x slower                                 |
| asyncio_tcp                | 923 ms                                                 | 1.08 sec: 1.17x slower                                |
| json                       | 6.85 ms                                                | 8.11 ms: 1.18x slower                                 |
| deepcopy                   | 468 us                                                 | 556 us: 1.19x slower                                  |
| json_loads                 | 37.9 us                                                | 45.6 us: 1.20x slower                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.42 sec: 1.22x slower                                |
| async_generators           | 589 ms                                                 | 721 ms: 1.22x slower                                  |
| bench_thread_pool          | 3.48 ms                                                | 4.26 ms: 1.23x slower                                 |
| python_startup             | 23.7 ms                                                | 29.1 ms: 1.23x slower                                 |
| scimark_fft                | 500 ms                                                 | 616 ms: 1.23x slower                                  |
| docutils                   | 4.00 sec                                               | 4.97 sec: 1.24x slower                                |
| mdp                        | 3.97 sec                                               | 4.96 sec: 1.25x slower                                |
| pycparser                  | 1.79 sec                                               | 2.25 sec: 1.26x slower                                |
| pylint                     | 465 ms                                                 | 592 ms: 1.27x slower                                  |
| tornado_http               | 266 ms                                                 | 339 ms: 1.27x slower                                  |
| xml_etree_generate         | 127 ms                                                 | 164 ms: 1.29x slower                                  |
| generators                 | 41.1 ms                                                | 53.4 ms: 1.30x slower                                 |
| json_dumps                 | 14.3 ms                                                | 19.0 ms: 1.32x slower                                 |
| dulwich_log                | 100 ms                                                 | 134 ms: 1.34x slower                                  |
| deepcopy_memo              | 52.4 us                                                | 70.5 us: 1.35x slower                                 |
| meteor_contest             | 146 ms                                                 | 198 ms: 1.35x slower                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 9.09 ms: 1.36x slower                                 |
| nqueens                    | 117 ms                                                 | 161 ms: 1.38x slower                                  |
| coroutines                 | 29.5 ms                                                | 41.7 ms: 1.41x slower                                 |
| crypto_pyaes               | 107 ms                                                 | 152 ms: 1.42x slower                                  |
| telco                      | 9.59 ms                                                | 13.8 ms: 1.44x slower                                 |
| sqlglot_normalize          | 157 ms                                                 | 227 ms: 1.44x slower                                  |
| 2to3                       | 456 ms                                                 | 662 ms: 1.45x slower                                  |
| fannkuch                   | 540 ms                                                 | 792 ms: 1.47x slower                                  |
| comprehensions             | 27.1 us                                                | 39.9 us: 1.47x slower                                 |
| sympy_integrate            | 29.8 ms                                                | 44.1 ms: 1.48x slower                                 |
| tomli_loads                | 2.88 sec                                               | 4.32 sec: 1.50x slower                                |
| xml_etree_process          | 83.7 ms                                                | 127 ms: 1.52x slower                                  |
| pyflate                    | 727 ms                                                 | 1.12 sec: 1.54x slower                                |
| html5lib                   | 88.9 ms                                                | 137 ms: 1.54x slower                                  |
| coverage                   | 95.4 ms                                                | 148 ms: 1.55x slower                                  |
| bpe_tokeniser              | 6.59 sec                                               | 10.2 sec: 1.55x slower                                |
| typing_runtime_protocols   | 224 us                                                 | 354 us: 1.58x slower                                  |
| spectral_norm              | 156 ms                                                 | 246 ms: 1.58x slower                                  |
| deepcopy_reduce            | 4.04 us                                                | 6.40 us: 1.59x slower                                 |
| sqlglot_optimize           | 76.0 ms                                                | 123 ms: 1.62x slower                                  |
| regex_compile              | 187 ms                                                 | 307 ms: 1.65x slower                                  |
| thrift                     | 1.06 ms                                                | 1.74 ms: 1.65x slower                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 164 ms: 1.71x slower                                  |
| float                      | 123 ms                                                 | 211 ms: 1.71x slower                                  |
| richards_super             | 72.8 ms                                                | 127 ms: 1.75x slower                                  |
| logging_simple             | 9.45 us                                                | 16.5 us: 1.75x slower                                 |
| sympy_str                  | 385 ms                                                 | 679 ms: 1.76x slower                                  |
| richards                   | 60.3 ms                                                | 107 ms: 1.77x slower                                  |
| genshi_text                | 30.2 ms                                                | 53.7 ms: 1.78x slower                                 |
| pprint_pformat             | 1.98 sec                                               | 3.52 sec: 1.78x slower                                |
| pprint_safe_repr           | 967 ms                                                 | 1.75 sec: 1.81x slower                                |
| unpickle_pure_python       | 300 us                                                 | 547 us: 1.82x slower                                  |
| pickle_pure_python         | 436 us                                                 | 801 us: 1.84x slower                                  |
| genshi_xml                 | 67.6 ms                                                | 125 ms: 1.85x slower                                  |
| logging_format             | 9.59 us                                                | 17.9 us: 1.86x slower                                 |
| logging_silent             | 139 ns                                                 | 266 ns: 1.91x slower                                  |
| django_template            | 44.9 ms                                                | 86.4 ms: 1.92x slower                                 |
| sqlglot_transpile          | 2.34 ms                                                | 4.52 ms: 1.94x slower                                 |
| hexiom                     | 8.27 ms                                                | 16.1 ms: 1.95x slower                                 |
| raytrace                   | 408 ms                                                 | 803 ms: 1.97x slower                                  |
| mako                       | 15.7 ms                                                | 31.1 ms: 1.98x slower                                 |
| chaos                      | 84.9 ms                                                | 176 ms: 2.07x slower                                  |
| scimark_lu                 | 152 ms                                                 | 315 ms: 2.07x slower                                  |
| scimark_sor                | 167 ms                                                 | 353 ms: 2.12x slower                                  |
| sympy_expand               | 582 ms                                                 | 1.26 sec: 2.17x slower                                |
| sympy_sum                  | 222 ms                                                 | 483 ms: 2.18x slower                                  |
| sqlglot_parse              | 1.79 ms                                                | 4.03 ms: 2.25x slower                                 |
| nbody                      | 119 ms                                                 | 278 ms: 2.33x slower                                  |
| go                         | 172 ms                                                 | 420 ms: 2.44x slower                                  |
| deltablue                  | 4.27 ms                                                | 11.8 ms: 2.76x slower                                 |
| unpack_sequence            | 60.2 ns                                                | 194 ns: 3.22x slower                                  |
| Geometric mean             | (ref)                                                  | 1.37x slower                                          |

Benchmark hidden because not significant (4): create_gc_cycles, xml_etree_iterparse, regex_dna, unpickle
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.16x