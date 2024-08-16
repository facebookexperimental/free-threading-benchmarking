# Results vs. 3.13.0rc1+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 4767a6e
- commit date: 2024-08-06
- overall geometric mean: 1.43x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.30x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 442 ms                                                  | 666 ms: 1.51x slower                                  |
| docutils       | 4.01 sec                                                | 5.00 sec: 1.25x slower                                |
| html5lib       | 98.1 ms                                                 | 162 ms: 1.65x slower                                  |
| tornado_http   | 248 ms                                                  | 337 ms: 1.36x slower                                  |
| Geometric mean | (ref)                                                   | 1.43x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.46 sec                                                | 1.14 sec: 1.28x faster                                |
| async_tree_io              | 1.38 sec                                                | 1.24 sec: 1.11x faster                                |
| async_tree_none_tg         | 521 ms                                                  | 483 ms: 1.08x faster                                  |
| async_tree_memoization_tg  | 672 ms                                                  | 634 ms: 1.06x faster                                  |
| asyncio_websockets         | 772 ms                                                  | 737 ms: 1.05x faster                                  |
| async_tree_none            | 576 ms                                                  | 607 ms: 1.05x slower                                  |
| async_tree_cpu_io_mixed    | 899 ms                                                  | 961 ms: 1.07x slower                                  |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 909 ms: 1.07x slower                                  |
| asyncio_tcp                | 985 ms                                                  | 1.11 sec: 1.13x slower                                |
| asyncio_tcp_ssl            | 2.79 sec                                                | 3.33 sec: 1.19x slower                                |
| async_generators           | 592 ms                                                  | 740 ms: 1.25x slower                                  |
| coroutines                 | 29.2 ms                                                 | 43.8 ms: 1.50x slower                                 |
| Geometric mean             | (ref)                                                   | 1.05x slower                                          |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 248 ms                                                  | 267 ms: 1.08x slower                                  |
| float          | 115 ms                                                  | 190 ms: 1.66x slower                                  |
| nbody          | 124 ms                                                  | 309 ms: 2.50x slower                                  |
| Geometric mean | (ref)                                                   | 1.65x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 288 ms                                                  | 304 ms: 1.06x slower                                  |
| regex_v8       | 32.4 ms                                                 | 36.9 ms: 1.14x slower                                 |
| regex_compile  | 177 ms                                                  | 288 ms: 1.62x slower                                  |
| Geometric mean | (ref)                                                   | 1.19x slower                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| pickle               | 15.4 us                                                 | 14.1 us: 1.09x faster                                 |
| pickle_dict          | 46.5 us                                                 | 42.8 us: 1.09x faster                                 |
| xml_etree_parse      | 236 ms                                                  | 222 ms: 1.06x faster                                  |
| pickle_list          | 6.82 us                                                 | 6.56 us: 1.04x faster                                 |
| unpickle_list        | 6.67 us                                                 | 7.55 us: 1.13x slower                                 |
| unpickle             | 21.4 us                                                 | 24.7 us: 1.16x slower                                 |
| json_dumps           | 14.9 ms                                                 | 18.6 ms: 1.25x slower                                 |
| xml_etree_generate   | 129 ms                                                  | 162 ms: 1.25x slower                                  |
| json_loads           | 36.1 us                                                 | 45.4 us: 1.26x slower                                 |
| tomli_loads          | 2.80 sec                                                | 4.21 sec: 1.50x slower                                |
| xml_etree_process    | 86.5 ms                                                 | 132 ms: 1.52x slower                                  |
| unpickle_pure_python | 296 us                                                  | 537 us: 1.82x slower                                  |
| pickle_pure_python   | 417 us                                                  | 764 us: 1.83x slower                                  |
| Geometric mean       | (ref)                                                   | 1.21x slower                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 14.6 ms                                                 | 19.2 ms: 1.31x slower                                 |
| python_startup         | 22.0 ms                                                 | 29.3 ms: 1.33x slower                                 |
| Geometric mean         | (ref)                                                   | 1.32x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|-----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 46.9 ms                                                 | 81.9 ms: 1.75x slower                                 |
| genshi_text     | 31.7 ms                                                 | 56.5 ms: 1.78x slower                                 |
| genshi_xml      | 68.3 ms                                                 | 123 ms: 1.80x slower                                  |
| mako            | 16.1 ms                                                 | 30.3 ms: 1.89x slower                                 |
| Geometric mean  | (ref)                                                   | 1.80x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.46 sec                                                | 1.14 sec: 1.28x faster                                |
| create_gc_cycles           | 2.46 ms                                                 | 1.99 ms: 1.24x faster                                 |
| bench_mp_pool              | 19.4 ms                                                 | 16.0 ms: 1.21x faster                                 |
| gc_traversal               | 5.91 ms                                                 | 5.03 ms: 1.17x faster                                 |
| async_tree_io              | 1.38 sec                                                | 1.24 sec: 1.11x faster                                |
| pickle                     | 15.4 us                                                 | 14.1 us: 1.09x faster                                 |
| pickle_dict                | 46.5 us                                                 | 42.8 us: 1.09x faster                                 |
| async_tree_none_tg         | 521 ms                                                  | 483 ms: 1.08x faster                                  |
| xml_etree_parse            | 236 ms                                                  | 222 ms: 1.06x faster                                  |
| async_tree_memoization_tg  | 672 ms                                                  | 634 ms: 1.06x faster                                  |
| asyncio_websockets         | 772 ms                                                  | 737 ms: 1.05x faster                                  |
| pickle_list                | 6.82 us                                                 | 6.56 us: 1.04x faster                                 |
| async_tree_none            | 576 ms                                                  | 607 ms: 1.05x slower                                  |
| regex_dna                  | 288 ms                                                  | 304 ms: 1.06x slower                                  |
| async_tree_cpu_io_mixed    | 899 ms                                                  | 961 ms: 1.07x slower                                  |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 909 ms: 1.07x slower                                  |
| pidigits                   | 248 ms                                                  | 267 ms: 1.08x slower                                  |
| asyncio_tcp                | 985 ms                                                  | 1.11 sec: 1.13x slower                                |
| unpickle_list              | 6.67 us                                                 | 7.55 us: 1.13x slower                                 |
| regex_v8                   | 32.4 ms                                                 | 36.9 ms: 1.14x slower                                 |
| pathlib                    | 29.3 ms                                                 | 33.6 ms: 1.14x slower                                 |
| unpickle                   | 21.4 us                                                 | 24.7 us: 1.16x slower                                 |
| asyncio_tcp_ssl            | 2.79 sec                                                | 3.33 sec: 1.19x slower                                |
| deepcopy                   | 484 us                                                  | 602 us: 1.24x slower                                  |
| docutils                   | 4.01 sec                                                | 5.00 sec: 1.25x slower                                |
| json_dumps                 | 14.9 ms                                                 | 18.6 ms: 1.25x slower                                 |
| async_generators           | 592 ms                                                  | 740 ms: 1.25x slower                                  |
| pylint                     | 472 ms                                                  | 591 ms: 1.25x slower                                  |
| xml_etree_generate         | 129 ms                                                  | 162 ms: 1.25x slower                                  |
| json_loads                 | 36.1 us                                                 | 45.4 us: 1.26x slower                                 |
| telco                      | 11.4 ms                                                 | 14.8 ms: 1.29x slower                                 |
| python_startup_no_site     | 14.6 ms                                                 | 19.2 ms: 1.31x slower                                 |
| mdp                        | 3.80 sec                                                | 5.00 sec: 1.32x slower                                |
| python_startup             | 22.0 ms                                                 | 29.3 ms: 1.33x slower                                 |
| meteor_contest             | 157 ms                                                  | 212 ms: 1.35x slower                                  |
| tornado_http               | 248 ms                                                  | 337 ms: 1.36x slower                                  |
| json                       | 6.55 ms                                                 | 8.93 ms: 1.36x slower                                 |
| scimark_fft                | 477 ms                                                  | 651 ms: 1.37x slower                                  |
| generators                 | 39.2 ms                                                 | 53.8 ms: 1.37x slower                                 |
| deepcopy_memo              | 51.7 us                                                 | 72.1 us: 1.39x slower                                 |
| deepcopy_reduce            | 4.27 us                                                 | 5.96 us: 1.40x slower                                 |
| pycparser                  | 1.57 sec                                                | 2.23 sec: 1.42x slower                                |
| scimark_sparse_mat_mult    | 6.98 ms                                                 | 9.98 ms: 1.43x slower                                 |
| coverage                   | 110 ms                                                  | 157 ms: 1.43x slower                                  |
| bench_thread_pool          | 3.06 ms                                                 | 4.44 ms: 1.45x slower                                 |
| fannkuch                   | 543 ms                                                  | 806 ms: 1.48x slower                                  |
| nqueens                    | 108 ms                                                  | 161 ms: 1.49x slower                                  |
| sympy_integrate            | 29.7 ms                                                 | 44.2 ms: 1.49x slower                                 |
| coroutines                 | 29.2 ms                                                 | 43.8 ms: 1.50x slower                                 |
| tomli_loads                | 2.80 sec                                                | 4.21 sec: 1.50x slower                                |
| 2to3                       | 442 ms                                                  | 666 ms: 1.51x slower                                  |
| xml_etree_process          | 86.5 ms                                                 | 132 ms: 1.52x slower                                  |
| crypto_pyaes               | 99.8 ms                                                 | 154 ms: 1.54x slower                                  |
| bpe_tokeniser              | 6.25 sec                                                | 9.70 sec: 1.55x slower                                |
| spectral_norm              | 159 ms                                                  | 247 ms: 1.55x slower                                  |
| sqlglot_optimize           | 76.2 ms                                                 | 122 ms: 1.60x slower                                  |
| thrift                     | 1.11 ms                                                 | 1.78 ms: 1.60x slower                                 |
| regex_compile              | 177 ms                                                  | 288 ms: 1.62x slower                                  |
| sqlglot_normalize          | 146 ms                                                  | 237 ms: 1.62x slower                                  |
| html5lib                   | 98.1 ms                                                 | 162 ms: 1.65x slower                                  |
| float                      | 115 ms                                                  | 190 ms: 1.66x slower                                  |
| richards_super             | 76.3 ms                                                 | 127 ms: 1.66x slower                                  |
| pyflate                    | 661 ms                                                  | 1.10 sec: 1.67x slower                                |
| logging_simple             | 8.98 us                                                 | 15.1 us: 1.68x slower                                 |
| pprint_pformat             | 2.00 sec                                                | 3.44 sec: 1.72x slower                                |
| pprint_safe_repr           | 959 ms                                                  | 1.65 sec: 1.72x slower                                |
| django_template            | 46.9 ms                                                 | 81.9 ms: 1.75x slower                                 |
| richards                   | 65.8 ms                                                 | 116 ms: 1.76x slower                                  |
| typing_runtime_protocols   | 216 us                                                  | 383 us: 1.77x slower                                  |
| genshi_text                | 31.7 ms                                                 | 56.5 ms: 1.78x slower                                 |
| genshi_xml                 | 68.3 ms                                                 | 123 ms: 1.80x slower                                  |
| unpickle_pure_python       | 296 us                                                  | 537 us: 1.82x slower                                  |
| pickle_pure_python         | 417 us                                                  | 764 us: 1.83x slower                                  |
| scimark_monte_carlo        | 89.9 ms                                                 | 168 ms: 1.87x slower                                  |
| mako                       | 16.1 ms                                                 | 30.3 ms: 1.89x slower                                 |
| sympy_str                  | 367 ms                                                  | 698 ms: 1.90x slower                                  |
| hexiom                     | 8.35 ms                                                 | 16.2 ms: 1.94x slower                                 |
| logging_format             | 9.48 us                                                 | 18.8 us: 1.98x slower                                 |
| comprehensions             | 20.9 us                                                 | 41.9 us: 2.00x slower                                 |
| scimark_sor                | 172 ms                                                  | 347 ms: 2.02x slower                                  |
| sqlglot_transpile          | 2.30 ms                                                 | 4.65 ms: 2.02x slower                                 |
| logging_silent             | 130 ns                                                  | 267 ns: 2.05x slower                                  |
| sympy_expand               | 631 ms                                                  | 1.30 sec: 2.06x slower                                |
| sqlglot_parse              | 1.80 ms                                                 | 3.79 ms: 2.10x slower                                 |
| chaos                      | 84.7 ms                                                 | 179 ms: 2.11x slower                                  |
| scimark_lu                 | 154 ms                                                  | 336 ms: 2.18x slower                                  |
| sympy_sum                  | 213 ms                                                  | 470 ms: 2.20x slower                                  |
| raytrace                   | 350 ms                                                  | 800 ms: 2.28x slower                                  |
| go                         | 195 ms                                                  | 457 ms: 2.34x slower                                  |
| nbody                      | 124 ms                                                  | 309 ms: 2.50x slower                                  |
| deltablue                  | 4.56 ms                                                 | 11.9 ms: 2.60x slower                                 |
| unpack_sequence            | 73.9 ns                                                 | 217 ns: 2.93x slower                                  |
| Geometric mean             | (ref)                                                   | 1.43x slower                                          |

Benchmark hidden because not significant (4): xml_etree_iterparse, async_tree_memoization, regex_effbot, sqlite_synth
Ignored benchmarks (6) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.35x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.30x

# Memory
- memory change: 1.14x