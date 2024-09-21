# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: e001027
- commit date: 2024-08-15
- overall geometric mean: 1.41x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                                 | 698 ms: 1.53x slower                                  |
| docutils       | 4.00 sec                                               | 5.02 sec: 1.26x slower                                |
| html5lib       | 88.9 ms                                                | 149 ms: 1.68x slower                                  |
| tornado_http   | 266 ms                                                 | 429 ms: 1.61x slower                                  |
| Geometric mean | (ref)                                                  | 1.51x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.19 sec: 1.63x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 647 ms: 1.44x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 510 ms: 1.38x faster                                  |
| async_tree_io              | 1.85 sec                                               | 1.34 sec: 1.38x faster                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 846 ms: 1.30x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 759 ms: 1.29x faster                                  |
| async_tree_none            | 741 ms                                                 | 614 ms: 1.21x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 974 ms: 1.11x faster                                  |
| asyncio_websockets         | 748 ms                                                 | 795 ms: 1.06x slower                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.41 sec: 1.21x slower                                |
| asyncio_tcp                | 923 ms                                                 | 1.12 sec: 1.22x slower                                |
| async_generators           | 589 ms                                                 | 763 ms: 1.30x slower                                  |
| coroutines                 | 29.5 ms                                                | 43.6 ms: 1.48x slower                                 |
| Geometric mean             | (ref)                                                  | 1.10x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 250 ms                                                 | 275 ms: 1.10x slower                                  |
| float          | 123 ms                                                 | 191 ms: 1.55x slower                                  |
| nbody          | 119 ms                                                 | 317 ms: 2.66x slower                                  |
| Geometric mean | (ref)                                                  | 1.65x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.79 ms: 1.07x faster                                 |
| regex_dna      | 278 ms                                                 | 297 ms: 1.07x slower                                  |
| regex_v8       | 32.5 ms                                                | 36.7 ms: 1.13x slower                                 |
| regex_compile  | 187 ms                                                 | 303 ms: 1.62x slower                                  |
| Geometric mean | (ref)                                                  | 1.16x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 46.3 us: 1.14x faster                                 |
| unpickle             | 21.2 us                                                | 23.1 us: 1.09x slower                                 |
| unpickle_list        | 6.83 us                                                | 7.97 us: 1.17x slower                                 |
| json_dumps           | 14.3 ms                                                | 17.9 ms: 1.25x slower                                 |
| json_loads           | 37.9 us                                                | 48.4 us: 1.28x slower                                 |
| xml_etree_generate   | 127 ms                                                 | 180 ms: 1.41x slower                                  |
| tomli_loads          | 2.88 sec                                               | 4.36 sec: 1.51x slower                                |
| xml_etree_process    | 83.7 ms                                                | 133 ms: 1.59x slower                                  |
| unpickle_pure_python | 300 us                                                 | 574 us: 1.92x slower                                  |
| pickle_pure_python   | 436 us                                                 | 910 us: 2.09x slower                                  |
| Geometric mean       | (ref)                                                  | 1.25x slower                                          |

Benchmark hidden because not significant (4): pickle_list, pickle, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 22.7 ms: 1.29x slower                                 |
| python_startup         | 23.7 ms                                                | 31.2 ms: 1.32x slower                                 |
| Geometric mean         | (ref)                                                  | 1.30x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 118 ms: 1.75x slower                                  |
| django_template | 44.9 ms                                                | 80.8 ms: 1.80x slower                                 |
| mako            | 15.7 ms                                                | 30.6 ms: 1.94x slower                                 |
| genshi_text     | 30.2 ms                                                | 59.2 ms: 1.96x slower                                 |
| Geometric mean  | (ref)                                                  | 1.86x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.19 sec: 1.63x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 647 ms: 1.44x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 510 ms: 1.38x faster                                  |
| async_tree_io              | 1.85 sec                                               | 1.34 sec: 1.38x faster                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 846 ms: 1.30x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 759 ms: 1.29x faster                                  |
| bench_mp_pool              | 20.7 ms                                                | 17.0 ms: 1.21x faster                                 |
| async_tree_none            | 741 ms                                                 | 614 ms: 1.21x faster                                  |
| pickle_dict                | 52.7 us                                                | 46.3 us: 1.14x faster                                 |
| gc_traversal               | 5.86 ms                                                | 5.18 ms: 1.13x faster                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 974 ms: 1.11x faster                                  |
| regex_effbot               | 5.13 ms                                                | 4.79 ms: 1.07x faster                                 |
| asyncio_websockets         | 748 ms                                                 | 795 ms: 1.06x slower                                  |
| regex_dna                  | 278 ms                                                 | 297 ms: 1.07x slower                                  |
| unpickle                   | 21.2 us                                                | 23.1 us: 1.09x slower                                 |
| pidigits                   | 250 ms                                                 | 275 ms: 1.10x slower                                  |
| sqlite_synth               | 3.87 us                                                | 4.35 us: 1.12x slower                                 |
| regex_v8                   | 32.5 ms                                                | 36.7 ms: 1.13x slower                                 |
| unpickle_list              | 6.83 us                                                | 7.97 us: 1.17x slower                                 |
| pathlib                    | 31.6 ms                                                | 37.5 ms: 1.19x slower                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.41 sec: 1.21x slower                                |
| asyncio_tcp                | 923 ms                                                 | 1.12 sec: 1.22x slower                                |
| pycparser                  | 1.79 sec                                               | 2.21 sec: 1.23x slower                                |
| json_dumps                 | 14.3 ms                                                | 17.9 ms: 1.25x slower                                 |
| docutils                   | 4.00 sec                                               | 5.02 sec: 1.26x slower                                |
| pylint                     | 465 ms                                                 | 586 ms: 1.26x slower                                  |
| deepcopy                   | 468 us                                                 | 596 us: 1.27x slower                                  |
| json_loads                 | 37.9 us                                                | 48.4 us: 1.28x slower                                 |
| json                       | 6.85 ms                                                | 8.77 ms: 1.28x slower                                 |
| scimark_fft                | 500 ms                                                 | 642 ms: 1.28x slower                                  |
| generators                 | 41.1 ms                                                | 53.0 ms: 1.29x slower                                 |
| python_startup_no_site     | 17.6 ms                                                | 22.7 ms: 1.29x slower                                 |
| async_generators           | 589 ms                                                 | 763 ms: 1.30x slower                                  |
| python_startup             | 23.7 ms                                                | 31.2 ms: 1.32x slower                                 |
| mdp                        | 3.97 sec                                               | 5.29 sec: 1.33x slower                                |
| bench_thread_pool          | 3.48 ms                                                | 4.67 ms: 1.34x slower                                 |
| deepcopy_memo              | 52.4 us                                                | 70.9 us: 1.35x slower                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 9.11 ms: 1.36x slower                                 |
| deepcopy_reduce            | 4.04 us                                                | 5.58 us: 1.38x slower                                 |
| meteor_contest             | 146 ms                                                 | 203 ms: 1.39x slower                                  |
| crypto_pyaes               | 107 ms                                                 | 150 ms: 1.40x slower                                  |
| xml_etree_generate         | 127 ms                                                 | 180 ms: 1.41x slower                                  |
| fannkuch                   | 540 ms                                                 | 786 ms: 1.46x slower                                  |
| comprehensions             | 27.1 us                                                | 39.5 us: 1.46x slower                                 |
| telco                      | 9.59 ms                                                | 14.1 ms: 1.47x slower                                 |
| coroutines                 | 29.5 ms                                                | 43.6 ms: 1.48x slower                                 |
| nqueens                    | 117 ms                                                 | 175 ms: 1.50x slower                                  |
| tomli_loads                | 2.88 sec                                               | 4.36 sec: 1.51x slower                                |
| 2to3                       | 456 ms                                                 | 698 ms: 1.53x slower                                  |
| sqlglot_normalize          | 157 ms                                                 | 240 ms: 1.53x slower                                  |
| float                      | 123 ms                                                 | 191 ms: 1.55x slower                                  |
| pyflate                    | 727 ms                                                 | 1.13 sec: 1.56x slower                                |
| bpe_tokeniser              | 6.59 sec                                               | 10.3 sec: 1.57x slower                                |
| spectral_norm              | 156 ms                                                 | 245 ms: 1.57x slower                                  |
| logging_simple             | 9.45 us                                                | 14.9 us: 1.58x slower                                 |
| typing_runtime_protocols   | 224 us                                                 | 355 us: 1.58x slower                                  |
| xml_etree_process          | 83.7 ms                                                | 133 ms: 1.59x slower                                  |
| coverage                   | 95.4 ms                                                | 152 ms: 1.59x slower                                  |
| thrift                     | 1.06 ms                                                | 1.70 ms: 1.60x slower                                 |
| tornado_http               | 266 ms                                                 | 429 ms: 1.61x slower                                  |
| regex_compile              | 187 ms                                                 | 303 ms: 1.62x slower                                  |
| sympy_integrate            | 29.8 ms                                                | 48.4 ms: 1.63x slower                                 |
| html5lib                   | 88.9 ms                                                | 149 ms: 1.68x slower                                  |
| sqlglot_optimize           | 76.0 ms                                                | 128 ms: 1.68x slower                                  |
| genshi_xml                 | 67.6 ms                                                | 118 ms: 1.75x slower                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 170 ms: 1.77x slower                                  |
| richards                   | 60.3 ms                                                | 107 ms: 1.78x slower                                  |
| django_template            | 44.9 ms                                                | 80.8 ms: 1.80x slower                                 |
| pprint_pformat             | 1.98 sec                                               | 3.57 sec: 1.81x slower                                |
| pprint_safe_repr           | 967 ms                                                 | 1.77 sec: 1.83x slower                                |
| logging_format             | 9.59 us                                                | 17.9 us: 1.86x slower                                 |
| richards_super             | 72.8 ms                                                | 137 ms: 1.88x slower                                  |
| sympy_str                  | 385 ms                                                 | 730 ms: 1.90x slower                                  |
| logging_silent             | 139 ns                                                 | 267 ns: 1.91x slower                                  |
| unpickle_pure_python       | 300 us                                                 | 574 us: 1.92x slower                                  |
| sqlglot_transpile          | 2.34 ms                                                | 4.53 ms: 1.94x slower                                 |
| mako                       | 15.7 ms                                                | 30.6 ms: 1.94x slower                                 |
| genshi_text                | 30.2 ms                                                | 59.2 ms: 1.96x slower                                 |
| hexiom                     | 8.27 ms                                                | 16.3 ms: 1.97x slower                                 |
| raytrace                   | 408 ms                                                 | 816 ms: 2.00x slower                                  |
| chaos                      | 84.9 ms                                                | 175 ms: 2.07x slower                                  |
| pickle_pure_python         | 436 us                                                 | 910 us: 2.09x slower                                  |
| scimark_sor                | 167 ms                                                 | 354 ms: 2.13x slower                                  |
| sqlglot_parse              | 1.79 ms                                                | 3.81 ms: 2.13x slower                                 |
| scimark_lu                 | 152 ms                                                 | 330 ms: 2.17x slower                                  |
| sympy_expand               | 582 ms                                                 | 1.31 sec: 2.25x slower                                |
| sympy_sum                  | 222 ms                                                 | 509 ms: 2.29x slower                                  |
| go                         | 172 ms                                                 | 452 ms: 2.62x slower                                  |
| deltablue                  | 4.27 ms                                                | 11.3 ms: 2.65x slower                                 |
| nbody                      | 119 ms                                                 | 317 ms: 2.66x slower                                  |
| unpack_sequence            | 60.2 ns                                                | 191 ns: 3.17x slower                                  |
| Geometric mean             | (ref)                                                  | 1.41x slower                                          |

Benchmark hidden because not significant (5): pickle_list, pickle, xml_etree_parse, create_gc_cycles, xml_etree_iterparse
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.15x