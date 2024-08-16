# Results vs. 3.13.0rc1+

- fork: python
- ref: 04eb5c8db1e24cabd0cb
- machine: linux-x86_64
- commit hash: 04eb5c8
- commit date: 2024-07-27
- overall geometric mean: 1.39x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 442 ms                                                  | 647 ms: 1.46x slower                                                  |
| docutils       | 4.01 sec                                                | 4.82 sec: 1.20x slower                                                |
| html5lib       | 98.1 ms                                                 | 141 ms: 1.44x slower                                                  |
| tornado_http   | 248 ms                                                  | 342 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                   | 1.37x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|---------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg          | 1.46 sec                                                | 1.12 sec: 1.30x faster                                                |
| async_tree_io             | 1.38 sec                                                | 1.23 sec: 1.12x faster                                                |
| async_tree_none_tg        | 521 ms                                                  | 482 ms: 1.08x faster                                                  |
| async_tree_memoization_tg | 672 ms                                                  | 632 ms: 1.06x faster                                                  |
| asyncio_websockets        | 772 ms                                                  | 735 ms: 1.05x faster                                                  |
| asyncio_tcp               | 985 ms                                                  | 1.02 sec: 1.04x slower                                                |
| asyncio_tcp_ssl           | 2.79 sec                                                | 3.18 sec: 1.14x slower                                                |
| async_generators          | 592 ms                                                  | 723 ms: 1.22x slower                                                  |
| coroutines                | 29.2 ms                                                 | 39.3 ms: 1.35x slower                                                 |
| Geometric mean            | (ref)                                                   | 1.00x slower                                                          |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 115 ms                                                  | 193 ms: 1.68x slower                                                  |
| nbody          | 124 ms                                                  | 280 ms: 2.26x slower                                                  |
| Geometric mean | (ref)                                                   | 1.55x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.84 ms                                                 | 4.47 ms: 1.08x faster                                                 |
| regex_v8       | 32.4 ms                                                 | 35.3 ms: 1.09x slower                                                 |
| regex_compile  | 177 ms                                                  | 293 ms: 1.65x slower                                                  |
| Geometric mean | (ref)                                                   | 1.14x slower                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 236 ms                                                  | 201 ms: 1.18x faster                                                  |
| xml_etree_iterparse  | 176 ms                                                  | 159 ms: 1.11x faster                                                  |
| pickle_dict          | 46.5 us                                                 | 44.0 us: 1.06x faster                                                 |
| pickle               | 15.4 us                                                 | 14.5 us: 1.06x faster                                                 |
| pickle_list          | 6.82 us                                                 | 6.53 us: 1.04x faster                                                 |
| unpickle_list        | 6.67 us                                                 | 7.76 us: 1.16x slower                                                 |
| json_dumps           | 14.9 ms                                                 | 17.8 ms: 1.20x slower                                                 |
| json_loads           | 36.1 us                                                 | 43.6 us: 1.21x slower                                                 |
| xml_etree_generate   | 129 ms                                                  | 160 ms: 1.24x slower                                                  |
| xml_etree_process    | 86.5 ms                                                 | 126 ms: 1.46x slower                                                  |
| tomli_loads          | 2.80 sec                                                | 4.22 sec: 1.51x slower                                                |
| unpickle_pure_python | 296 us                                                  | 558 us: 1.89x slower                                                  |
| pickle_pure_python   | 417 us                                                  | 830 us: 1.99x slower                                                  |
| Geometric mean       | (ref)                                                   | 1.19x slower                                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                 | 28.9 ms: 1.31x slower                                                 |
| python_startup_no_site | 14.6 ms                                                 | 19.5 ms: 1.33x slower                                                 |
| Geometric mean         | (ref)                                                   | 1.32x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|-----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                 | 54.4 ms: 1.71x slower                                                 |
| django_template | 46.9 ms                                                 | 80.6 ms: 1.72x slower                                                 |
| genshi_xml      | 68.3 ms                                                 | 120 ms: 1.75x slower                                                  |
| mako            | 16.1 ms                                                 | 29.9 ms: 1.86x slower                                                 |
| Geometric mean  | (ref)                                                   | 1.76x slower                                                          |

All benchmarks:
===============

| Benchmark                 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|---------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| bench_mp_pool             | 19.4 ms                                                 | 13.6 ms: 1.42x faster                                                 |
| gc_traversal              | 5.91 ms                                                 | 4.28 ms: 1.38x faster                                                 |
| async_tree_io_tg          | 1.46 sec                                                | 1.12 sec: 1.30x faster                                                |
| create_gc_cycles          | 2.46 ms                                                 | 1.95 ms: 1.26x faster                                                 |
| xml_etree_parse           | 236 ms                                                  | 201 ms: 1.18x faster                                                  |
| async_tree_io             | 1.38 sec                                                | 1.23 sec: 1.12x faster                                                |
| xml_etree_iterparse       | 176 ms                                                  | 159 ms: 1.11x faster                                                  |
| regex_effbot              | 4.84 ms                                                 | 4.47 ms: 1.08x faster                                                 |
| async_tree_none_tg        | 521 ms                                                  | 482 ms: 1.08x faster                                                  |
| async_tree_memoization_tg | 672 ms                                                  | 632 ms: 1.06x faster                                                  |
| pickle_dict               | 46.5 us                                                 | 44.0 us: 1.06x faster                                                 |
| pickle                    | 15.4 us                                                 | 14.5 us: 1.06x faster                                                 |
| asyncio_websockets        | 772 ms                                                  | 735 ms: 1.05x faster                                                  |
| pickle_list               | 6.82 us                                                 | 6.53 us: 1.04x faster                                                 |
| asyncio_tcp               | 985 ms                                                  | 1.02 sec: 1.04x slower                                                |
| sqlite_synth              | 4.07 us                                                 | 4.28 us: 1.05x slower                                                 |
| regex_v8                  | 32.4 ms                                                 | 35.3 ms: 1.09x slower                                                 |
| pathlib                   | 29.3 ms                                                 | 33.2 ms: 1.13x slower                                                 |
| asyncio_tcp_ssl           | 2.79 sec                                                | 3.18 sec: 1.14x slower                                                |
| unpickle_list             | 6.67 us                                                 | 7.76 us: 1.16x slower                                                 |
| json                      | 6.55 ms                                                 | 7.69 ms: 1.17x slower                                                 |
| pylint                    | 472 ms                                                  | 562 ms: 1.19x slower                                                  |
| json_dumps                | 14.9 ms                                                 | 17.8 ms: 1.20x slower                                                 |
| docutils                  | 4.01 sec                                                | 4.82 sec: 1.20x slower                                                |
| json_loads                | 36.1 us                                                 | 43.6 us: 1.21x slower                                                 |
| async_generators          | 592 ms                                                  | 723 ms: 1.22x slower                                                  |
| telco                     | 11.4 ms                                                 | 14.1 ms: 1.23x slower                                                 |
| deepcopy                  | 484 us                                                  | 600 us: 1.24x slower                                                  |
| xml_etree_generate        | 129 ms                                                  | 160 ms: 1.24x slower                                                  |
| scimark_sparse_mat_mult   | 6.98 ms                                                 | 8.68 ms: 1.24x slower                                                 |
| coverage                  | 110 ms                                                  | 141 ms: 1.28x slower                                                  |
| python_startup            | 22.0 ms                                                 | 28.9 ms: 1.31x slower                                                 |
| meteor_contest            | 157 ms                                                  | 208 ms: 1.32x slower                                                  |
| mdp                       | 3.80 sec                                                | 5.02 sec: 1.32x slower                                                |
| python_startup_no_site    | 14.6 ms                                                 | 19.5 ms: 1.33x slower                                                 |
| deepcopy_memo             | 51.7 us                                                 | 69.1 us: 1.34x slower                                                 |
| deepcopy_reduce           | 4.27 us                                                 | 5.73 us: 1.34x slower                                                 |
| scimark_fft               | 477 ms                                                  | 641 ms: 1.34x slower                                                  |
| coroutines                | 29.2 ms                                                 | 39.3 ms: 1.35x slower                                                 |
| tornado_http              | 248 ms                                                  | 342 ms: 1.38x slower                                                  |
| pycparser                 | 1.57 sec                                                | 2.18 sec: 1.38x slower                                                |
| bench_thread_pool         | 3.06 ms                                                 | 4.27 ms: 1.39x slower                                                 |
| generators                | 39.2 ms                                                 | 54.8 ms: 1.40x slower                                                 |
| fannkuch                  | 543 ms                                                  | 772 ms: 1.42x slower                                                  |
| html5lib                  | 98.1 ms                                                 | 141 ms: 1.44x slower                                                  |
| sympy_integrate           | 29.7 ms                                                 | 42.8 ms: 1.44x slower                                                 |
| xml_etree_process         | 86.5 ms                                                 | 126 ms: 1.46x slower                                                  |
| 2to3                      | 442 ms                                                  | 647 ms: 1.46x slower                                                  |
| nqueens                   | 108 ms                                                  | 162 ms: 1.50x slower                                                  |
| tomli_loads               | 2.80 sec                                                | 4.22 sec: 1.51x slower                                                |
| spectral_norm             | 159 ms                                                  | 242 ms: 1.52x slower                                                  |
| thrift                    | 1.11 ms                                                 | 1.70 ms: 1.53x slower                                                 |
| bpe_tokeniser             | 6.25 sec                                                | 9.90 sec: 1.59x slower                                                |
| crypto_pyaes              | 99.8 ms                                                 | 159 ms: 1.59x slower                                                  |
| pyflate                   | 661 ms                                                  | 1.07 sec: 1.62x slower                                                |
| richards_super            | 76.3 ms                                                 | 125 ms: 1.64x slower                                                  |
| regex_compile             | 177 ms                                                  | 293 ms: 1.65x slower                                                  |
| typing_runtime_protocols  | 216 us                                                  | 362 us: 1.67x slower                                                  |
| float                     | 115 ms                                                  | 193 ms: 1.68x slower                                                  |
| sqlglot_normalize         | 146 ms                                                  | 246 ms: 1.69x slower                                                  |
| richards                  | 65.8 ms                                                 | 111 ms: 1.69x slower                                                  |
| genshi_text               | 31.7 ms                                                 | 54.4 ms: 1.71x slower                                                 |
| django_template           | 46.9 ms                                                 | 80.6 ms: 1.72x slower                                                 |
| pprint_pformat            | 2.00 sec                                                | 3.48 sec: 1.74x slower                                                |
| sqlglot_optimize          | 76.2 ms                                                 | 133 ms: 1.74x slower                                                  |
| genshi_xml                | 68.3 ms                                                 | 120 ms: 1.75x slower                                                  |
| logging_simple            | 8.98 us                                                 | 15.9 us: 1.77x slower                                                 |
| pprint_safe_repr          | 959 ms                                                  | 1.73 sec: 1.80x slower                                                |
| sympy_str                 | 367 ms                                                  | 663 ms: 1.81x slower                                                  |
| comprehensions            | 20.9 us                                                 | 38.3 us: 1.83x slower                                                 |
| logging_format            | 9.48 us                                                 | 17.6 us: 1.86x slower                                                 |
| mako                      | 16.1 ms                                                 | 29.9 ms: 1.86x slower                                                 |
| unpickle_pure_python      | 296 us                                                  | 558 us: 1.89x slower                                                  |
| scimark_monte_carlo       | 89.9 ms                                                 | 171 ms: 1.90x slower                                                  |
| chaos                     | 84.7 ms                                                 | 163 ms: 1.93x slower                                                  |
| sqlglot_transpile         | 2.30 ms                                                 | 4.53 ms: 1.97x slower                                                 |
| pickle_pure_python        | 417 us                                                  | 830 us: 1.99x slower                                                  |
| logging_silent            | 130 ns                                                  | 259 ns: 2.00x slower                                                  |
| sympy_expand              | 631 ms                                                  | 1.27 sec: 2.01x slower                                                |
| scimark_lu                | 154 ms                                                  | 313 ms: 2.03x slower                                                  |
| scimark_sor               | 172 ms                                                  | 351 ms: 2.04x slower                                                  |
| go                        | 195 ms                                                  | 406 ms: 2.08x slower                                                  |
| hexiom                    | 8.35 ms                                                 | 17.4 ms: 2.09x slower                                                 |
| sqlglot_parse             | 1.80 ms                                                 | 3.76 ms: 2.09x slower                                                 |
| nbody                     | 124 ms                                                  | 280 ms: 2.26x slower                                                  |
| raytrace                  | 350 ms                                                  | 806 ms: 2.30x slower                                                  |
| sympy_sum                 | 213 ms                                                  | 493 ms: 2.31x slower                                                  |
| deltablue                 | 4.56 ms                                                 | 11.7 ms: 2.55x slower                                                 |
| unpack_sequence           | 73.9 ns                                                 | 201 ns: 2.72x slower                                                  |
| Geometric mean            | (ref)                                                   | 1.39x slower                                                          |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed_tg, async_tree_memoization, pidigits, async_tree_none, async_tree_cpu_io_mixed, regex_dna, unpickle
Ignored benchmarks (6) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.16x