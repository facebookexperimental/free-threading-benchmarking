# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5a4fb7e
- commit date: 2024-09-06
- overall geometric mean: 1.42x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.33x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                                 | 682 ms: 1.50x slower                                  |
| docutils       | 4.00 sec                                               | 5.10 sec: 1.28x slower                                |
| html5lib       | 88.9 ms                                                | 147 ms: 1.66x slower                                  |
| tornado_http   | 266 ms                                                 | 420 ms: 1.58x slower                                  |
| Geometric mean | (ref)                                                  | 1.50x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.24 sec: 1.56x faster                                |
| async_tree_io              | 1.85 sec                                               | 1.32 sec: 1.40x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 674 ms: 1.38x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 540 ms: 1.30x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 770 ms: 1.27x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 885 ms: 1.24x faster                                  |
| async_tree_none            | 741 ms                                                 | 607 ms: 1.22x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 937 ms: 1.15x faster                                  |
| asyncio_websockets         | 748 ms                                                 | 818 ms: 1.09x slower                                  |
| async_generators           | 589 ms                                                 | 723 ms: 1.23x slower                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.67 sec: 1.31x slower                                |
| asyncio_tcp                | 923 ms                                                 | 1.22 sec: 1.32x slower                                |
| coroutines                 | 29.5 ms                                                | 42.2 ms: 1.43x slower                                 |
| Geometric mean             | (ref)                                                  | 1.08x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 123 ms                                                 | 203 ms: 1.65x slower                                  |
| nbody          | 119 ms                                                 | 315 ms: 2.65x slower                                  |
| Geometric mean | (ref)                                                  | 1.65x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 278 ms                                                 | 299 ms: 1.07x slower                                  |
| regex_v8       | 32.5 ms                                                | 37.6 ms: 1.16x slower                                 |
| regex_compile  | 187 ms                                                 | 305 ms: 1.63x slower                                  |
| Geometric mean | (ref)                                                  | 1.20x slower                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pickle               | 16.4 us                                                | 13.8 us: 1.19x faster                                 |
| pickle_dict          | 52.7 us                                                | 46.1 us: 1.14x faster                                 |
| pickle_list          | 6.97 us                                                | 6.51 us: 1.07x faster                                 |
| xml_etree_parse      | 241 ms                                                 | 229 ms: 1.05x faster                                  |
| unpickle             | 21.2 us                                                | 23.1 us: 1.09x slower                                 |
| unpickle_list        | 6.83 us                                                | 7.45 us: 1.09x slower                                 |
| json_dumps           | 14.3 ms                                                | 18.0 ms: 1.26x slower                                 |
| json_loads           | 37.9 us                                                | 47.7 us: 1.26x slower                                 |
| xml_etree_generate   | 127 ms                                                 | 179 ms: 1.41x slower                                  |
| tomli_loads          | 2.88 sec                                               | 4.37 sec: 1.52x slower                                |
| xml_etree_process    | 83.7 ms                                                | 136 ms: 1.62x slower                                  |
| pickle_pure_python   | 436 us                                                 | 762 us: 1.75x slower                                  |
| unpickle_pure_python | 300 us                                                 | 563 us: 1.88x slower                                  |
| Geometric mean       | (ref)                                                  | 1.21x slower                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 24.3 ms: 1.38x slower                                 |
| python_startup         | 23.7 ms                                                | 37.1 ms: 1.56x slower                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 44.9 ms                                                | 83.6 ms: 1.86x slower                                 |
| genshi_text     | 30.2 ms                                                | 57.6 ms: 1.91x slower                                 |
| mako            | 15.7 ms                                                | 31.9 ms: 2.03x slower                                 |
| genshi_xml      | 67.6 ms                                                | 141 ms: 2.08x slower                                  |
| Geometric mean  | (ref)                                                  | 1.97x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.24 sec: 1.56x faster                                |
| async_tree_io              | 1.85 sec                                               | 1.32 sec: 1.40x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 674 ms: 1.38x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 540 ms: 1.30x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 770 ms: 1.27x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 885 ms: 1.24x faster                                  |
| gc_traversal               | 5.86 ms                                                | 4.74 ms: 1.24x faster                                 |
| async_tree_none            | 741 ms                                                 | 607 ms: 1.22x faster                                  |
| pickle                     | 16.4 us                                                | 13.8 us: 1.19x faster                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 937 ms: 1.15x faster                                  |
| pickle_dict                | 52.7 us                                                | 46.1 us: 1.14x faster                                 |
| pickle_list                | 6.97 us                                                | 6.51 us: 1.07x faster                                 |
| xml_etree_parse            | 241 ms                                                 | 229 ms: 1.05x faster                                  |
| regex_dna                  | 278 ms                                                 | 299 ms: 1.07x slower                                  |
| unpickle                   | 21.2 us                                                | 23.1 us: 1.09x slower                                 |
| unpickle_list              | 6.83 us                                                | 7.45 us: 1.09x slower                                 |
| asyncio_websockets         | 748 ms                                                 | 818 ms: 1.09x slower                                  |
| sqlite_synth               | 3.87 us                                                | 4.25 us: 1.10x slower                                 |
| pathlib                    | 31.6 ms                                                | 36.2 ms: 1.15x slower                                 |
| regex_v8                   | 32.5 ms                                                | 37.6 ms: 1.16x slower                                 |
| async_generators           | 589 ms                                                 | 723 ms: 1.23x slower                                  |
| json_dumps                 | 14.3 ms                                                | 18.0 ms: 1.26x slower                                 |
| json_loads                 | 37.9 us                                                | 47.7 us: 1.26x slower                                 |
| mdp                        | 3.97 sec                                               | 5.07 sec: 1.28x slower                                |
| docutils                   | 4.00 sec                                               | 5.10 sec: 1.28x slower                                |
| pycparser                  | 1.79 sec                                               | 2.29 sec: 1.28x slower                                |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.67 sec: 1.31x slower                                |
| json                       | 6.85 ms                                                | 9.01 ms: 1.32x slower                                 |
| scimark_fft                | 500 ms                                                 | 659 ms: 1.32x slower                                  |
| deepcopy                   | 468 us                                                 | 617 us: 1.32x slower                                  |
| asyncio_tcp                | 923 ms                                                 | 1.22 sec: 1.32x slower                                |
| meteor_contest             | 146 ms                                                 | 196 ms: 1.34x slower                                  |
| deepcopy_memo              | 52.4 us                                                | 71.0 us: 1.35x slower                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 9.21 ms: 1.37x slower                                 |
| generators                 | 41.1 ms                                                | 56.6 ms: 1.38x slower                                 |
| pylint                     | 465 ms                                                 | 641 ms: 1.38x slower                                  |
| python_startup_no_site     | 17.6 ms                                                | 24.3 ms: 1.38x slower                                 |
| xml_etree_generate         | 127 ms                                                 | 179 ms: 1.41x slower                                  |
| dulwich_log                | 100 ms                                                 | 143 ms: 1.43x slower                                  |
| coroutines                 | 29.5 ms                                                | 42.2 ms: 1.43x slower                                 |
| deepcopy_reduce            | 4.04 us                                                | 5.81 us: 1.44x slower                                 |
| nqueens                    | 117 ms                                                 | 170 ms: 1.46x slower                                  |
| crypto_pyaes               | 107 ms                                                 | 158 ms: 1.47x slower                                  |
| fannkuch                   | 540 ms                                                 | 807 ms: 1.49x slower                                  |
| 2to3                       | 456 ms                                                 | 682 ms: 1.50x slower                                  |
| coverage                   | 95.4 ms                                                | 144 ms: 1.52x slower                                  |
| tomli_loads                | 2.88 sec                                               | 4.37 sec: 1.52x slower                                |
| comprehensions             | 27.1 us                                                | 41.3 us: 1.52x slower                                 |
| pyflate                    | 727 ms                                                 | 1.11 sec: 1.53x slower                                |
| bench_thread_pool          | 3.48 ms                                                | 5.33 ms: 1.53x slower                                 |
| telco                      | 9.59 ms                                                | 14.9 ms: 1.55x slower                                 |
| python_startup             | 23.7 ms                                                | 37.1 ms: 1.56x slower                                 |
| sqlglot_normalize          | 157 ms                                                 | 248 ms: 1.58x slower                                  |
| tornado_http               | 266 ms                                                 | 420 ms: 1.58x slower                                  |
| thrift                     | 1.06 ms                                                | 1.68 ms: 1.58x slower                                 |
| typing_runtime_protocols   | 224 us                                                 | 357 us: 1.59x slower                                  |
| xml_etree_process          | 83.7 ms                                                | 136 ms: 1.62x slower                                  |
| spectral_norm              | 156 ms                                                 | 253 ms: 1.63x slower                                  |
| bpe_tokeniser              | 6.59 sec                                               | 10.8 sec: 1.63x slower                                |
| regex_compile              | 187 ms                                                 | 305 ms: 1.63x slower                                  |
| sqlglot_optimize           | 76.0 ms                                                | 125 ms: 1.64x slower                                  |
| float                      | 123 ms                                                 | 203 ms: 1.65x slower                                  |
| sympy_integrate            | 29.8 ms                                                | 49.3 ms: 1.66x slower                                 |
| html5lib                   | 88.9 ms                                                | 147 ms: 1.66x slower                                  |
| logging_simple             | 9.45 us                                                | 16.0 us: 1.69x slower                                 |
| pprint_safe_repr           | 967 ms                                                 | 1.66 sec: 1.72x slower                                |
| richards_super             | 72.8 ms                                                | 126 ms: 1.73x slower                                  |
| pickle_pure_python         | 436 us                                                 | 762 us: 1.75x slower                                  |
| richards                   | 60.3 ms                                                | 107 ms: 1.77x slower                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 171 ms: 1.77x slower                                  |
| pprint_pformat             | 1.98 sec                                               | 3.55 sec: 1.79x slower                                |
| logging_format             | 9.59 us                                                | 17.5 us: 1.82x slower                                 |
| sympy_str                  | 385 ms                                                 | 708 ms: 1.84x slower                                  |
| django_template            | 44.9 ms                                                | 83.6 ms: 1.86x slower                                 |
| unpickle_pure_python       | 300 us                                                 | 563 us: 1.88x slower                                  |
| genshi_text                | 30.2 ms                                                | 57.6 ms: 1.91x slower                                 |
| logging_silent             | 139 ns                                                 | 266 ns: 1.91x slower                                  |
| chaos                      | 84.9 ms                                                | 163 ms: 1.92x slower                                  |
| raytrace                   | 408 ms                                                 | 798 ms: 1.96x slower                                  |
| sqlglot_transpile          | 2.34 ms                                                | 4.73 ms: 2.02x slower                                 |
| mako                       | 15.7 ms                                                | 31.9 ms: 2.03x slower                                 |
| hexiom                     | 8.27 ms                                                | 17.1 ms: 2.07x slower                                 |
| genshi_xml                 | 67.6 ms                                                | 141 ms: 2.08x slower                                  |
| sqlglot_parse              | 1.79 ms                                                | 3.76 ms: 2.10x slower                                 |
| sympy_sum                  | 222 ms                                                 | 472 ms: 2.13x slower                                  |
| go                         | 172 ms                                                 | 370 ms: 2.15x slower                                  |
| scimark_lu                 | 152 ms                                                 | 328 ms: 2.16x slower                                  |
| scimark_sor                | 167 ms                                                 | 360 ms: 2.16x slower                                  |
| sympy_expand               | 582 ms                                                 | 1.32 sec: 2.26x slower                                |
| nbody                      | 119 ms                                                 | 315 ms: 2.65x slower                                  |
| deltablue                  | 4.27 ms                                                | 12.2 ms: 2.85x slower                                 |
| unpack_sequence            | 60.2 ns                                                | 207 ns: 3.44x slower                                  |
| Geometric mean             | (ref)                                                  | 1.42x slower                                          |

Benchmark hidden because not significant (5): bench_mp_pool, xml_etree_iterparse, create_gc_cycles, regex_effbot, pidigits
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.37x
- 95% likely to have a slowdown of 1.35x
- 99% likely to have a slowdown of 1.33x

# Memory
- memory change: 1.15x