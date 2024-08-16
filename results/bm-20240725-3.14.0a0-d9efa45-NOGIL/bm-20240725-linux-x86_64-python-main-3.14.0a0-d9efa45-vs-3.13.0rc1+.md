# Results vs. 3.13.0rc1+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d9efa45
- commit date: 2024-07-25
- overall geometric mean: 1.41x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.30x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 442 ms                                                  | 690 ms: 1.56x slower                                  |
| docutils       | 4.01 sec                                                | 5.03 sec: 1.25x slower                                |
| html5lib       | 98.1 ms                                                 | 138 ms: 1.40x slower                                  |
| tornado_http   | 248 ms                                                  | 358 ms: 1.44x slower                                  |
| Geometric mean | (ref)                                                   | 1.41x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|-------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg        | 1.46 sec                                                | 1.19 sec: 1.22x faster                                |
| async_tree_none_tg      | 521 ms                                                  | 471 ms: 1.11x faster                                  |
| async_tree_io           | 1.38 sec                                                | 1.28 sec: 1.08x faster                                |
| async_tree_cpu_io_mixed | 899 ms                                                  | 975 ms: 1.09x slower                                  |
| asyncio_tcp             | 985 ms                                                  | 1.10 sec: 1.12x slower                                |
| asyncio_tcp_ssl         | 2.79 sec                                                | 3.42 sec: 1.23x slower                                |
| async_generators        | 592 ms                                                  | 741 ms: 1.25x slower                                  |
| coroutines              | 29.2 ms                                                 | 42.7 ms: 1.46x slower                                 |
| Geometric mean          | (ref)                                                   | 1.05x slower                                          |

Benchmark hidden because not significant (5): async_tree_memoization_tg, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 115 ms                                                  | 201 ms: 1.75x slower                                  |
| nbody          | 124 ms                                                  | 291 ms: 2.35x slower                                  |
| Geometric mean | (ref)                                                   | 1.60x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 32.4 ms                                                 | 36.8 ms: 1.13x slower                                 |
| regex_compile  | 177 ms                                                  | 292 ms: 1.65x slower                                  |
| Geometric mean | (ref)                                                   | 1.17x slower                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_parse      | 236 ms                                                  | 213 ms: 1.11x faster                                  |
| pickle               | 15.4 us                                                 | 14.4 us: 1.06x faster                                 |
| pickle_list          | 6.82 us                                                 | 6.46 us: 1.06x faster                                 |
| json_loads           | 36.1 us                                                 | 44.5 us: 1.23x slower                                 |
| json_dumps           | 14.9 ms                                                 | 18.3 ms: 1.23x slower                                 |
| xml_etree_generate   | 129 ms                                                  | 163 ms: 1.26x slower                                  |
| tomli_loads          | 2.80 sec                                                | 4.33 sec: 1.54x slower                                |
| xml_etree_process    | 86.5 ms                                                 | 137 ms: 1.59x slower                                  |
| pickle_pure_python   | 417 us                                                  | 768 us: 1.84x slower                                  |
| unpickle_pure_python | 296 us                                                  | 573 us: 1.94x slower                                  |
| Geometric mean       | (ref)                                                   | 1.20x slower                                          |

Benchmark hidden because not significant (4): pickle_dict, xml_etree_iterparse, unpickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 22.0 ms                                                 | 29.3 ms: 1.33x slower                                 |
| python_startup_no_site | 14.6 ms                                                 | 19.9 ms: 1.36x slower                                 |
| Geometric mean         | (ref)                                                   | 1.34x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|-----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 68.3 ms                                                 | 117 ms: 1.71x slower                                  |
| django_template | 46.9 ms                                                 | 81.6 ms: 1.74x slower                                 |
| genshi_text     | 31.7 ms                                                 | 57.9 ms: 1.83x slower                                 |
| mako            | 16.1 ms                                                 | 29.5 ms: 1.84x slower                                 |
| Geometric mean  | (ref)                                                   | 1.78x slower                                          |

All benchmarks:
===============

| Benchmark                | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|--------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| create_gc_cycles         | 2.46 ms                                                 | 1.87 ms: 1.32x faster                                 |
| gc_traversal             | 5.91 ms                                                 | 4.66 ms: 1.27x faster                                 |
| bench_mp_pool            | 19.4 ms                                                 | 15.8 ms: 1.23x faster                                 |
| async_tree_io_tg         | 1.46 sec                                                | 1.19 sec: 1.22x faster                                |
| xml_etree_parse          | 236 ms                                                  | 213 ms: 1.11x faster                                  |
| async_tree_none_tg       | 521 ms                                                  | 471 ms: 1.11x faster                                  |
| async_tree_io            | 1.38 sec                                                | 1.28 sec: 1.08x faster                                |
| pickle                   | 15.4 us                                                 | 14.4 us: 1.06x faster                                 |
| pickle_list              | 6.82 us                                                 | 6.46 us: 1.06x faster                                 |
| async_tree_cpu_io_mixed  | 899 ms                                                  | 975 ms: 1.09x slower                                  |
| asyncio_tcp              | 985 ms                                                  | 1.10 sec: 1.12x slower                                |
| regex_v8                 | 32.4 ms                                                 | 36.8 ms: 1.13x slower                                 |
| deepcopy                 | 484 us                                                  | 566 us: 1.17x slower                                  |
| pathlib                  | 29.3 ms                                                 | 35.5 ms: 1.21x slower                                 |
| telco                    | 11.4 ms                                                 | 13.8 ms: 1.21x slower                                 |
| asyncio_tcp_ssl          | 2.79 sec                                                | 3.42 sec: 1.23x slower                                |
| json_loads               | 36.1 us                                                 | 44.5 us: 1.23x slower                                 |
| json_dumps               | 14.9 ms                                                 | 18.3 ms: 1.23x slower                                 |
| async_generators         | 592 ms                                                  | 741 ms: 1.25x slower                                  |
| docutils                 | 4.01 sec                                                | 5.03 sec: 1.25x slower                                |
| xml_etree_generate       | 129 ms                                                  | 163 ms: 1.26x slower                                  |
| pylint                   | 472 ms                                                  | 595 ms: 1.26x slower                                  |
| scimark_sparse_mat_mult  | 6.98 ms                                                 | 9.05 ms: 1.30x slower                                 |
| json                     | 6.55 ms                                                 | 8.50 ms: 1.30x slower                                 |
| bench_thread_pool        | 3.06 ms                                                 | 3.97 ms: 1.30x slower                                 |
| scimark_fft              | 477 ms                                                  | 621 ms: 1.30x slower                                  |
| meteor_contest           | 157 ms                                                  | 206 ms: 1.31x slower                                  |
| deepcopy_memo            | 51.7 us                                                 | 67.8 us: 1.31x slower                                 |
| python_startup           | 22.0 ms                                                 | 29.3 ms: 1.33x slower                                 |
| mdp                      | 3.80 sec                                                | 5.12 sec: 1.35x slower                                |
| python_startup_no_site   | 14.6 ms                                                 | 19.9 ms: 1.36x slower                                 |
| coverage                 | 110 ms                                                  | 149 ms: 1.36x slower                                  |
| nqueens                  | 108 ms                                                  | 151 ms: 1.40x slower                                  |
| html5lib                 | 98.1 ms                                                 | 138 ms: 1.40x slower                                  |
| pycparser                | 1.57 sec                                                | 2.21 sec: 1.40x slower                                |
| deepcopy_reduce          | 4.27 us                                                 | 6.02 us: 1.41x slower                                 |
| tornado_http             | 248 ms                                                  | 358 ms: 1.44x slower                                  |
| coroutines               | 29.2 ms                                                 | 42.7 ms: 1.46x slower                                 |
| generators               | 39.2 ms                                                 | 57.4 ms: 1.47x slower                                 |
| fannkuch                 | 543 ms                                                  | 802 ms: 1.48x slower                                  |
| sympy_integrate          | 29.7 ms                                                 | 44.3 ms: 1.49x slower                                 |
| crypto_pyaes             | 99.8 ms                                                 | 149 ms: 1.49x slower                                  |
| spectral_norm            | 159 ms                                                  | 244 ms: 1.53x slower                                  |
| tomli_loads              | 2.80 sec                                                | 4.33 sec: 1.54x slower                                |
| 2to3                     | 442 ms                                                  | 690 ms: 1.56x slower                                  |
| thrift                   | 1.11 ms                                                 | 1.77 ms: 1.59x slower                                 |
| xml_etree_process        | 86.5 ms                                                 | 137 ms: 1.59x slower                                  |
| bpe_tokeniser            | 6.25 sec                                                | 9.93 sec: 1.59x slower                                |
| richards                 | 65.8 ms                                                 | 105 ms: 1.59x slower                                  |
| sqlglot_normalize        | 146 ms                                                  | 233 ms: 1.60x slower                                  |
| sqlglot_optimize         | 76.2 ms                                                 | 123 ms: 1.61x slower                                  |
| regex_compile            | 177 ms                                                  | 292 ms: 1.65x slower                                  |
| pyflate                  | 661 ms                                                  | 1.09 sec: 1.66x slower                                |
| genshi_xml               | 68.3 ms                                                 | 117 ms: 1.71x slower                                  |
| django_template          | 46.9 ms                                                 | 81.6 ms: 1.74x slower                                 |
| typing_runtime_protocols | 216 us                                                  | 377 us: 1.75x slower                                  |
| float                    | 115 ms                                                  | 201 ms: 1.75x slower                                  |
| richards_super           | 76.3 ms                                                 | 134 ms: 1.75x slower                                  |
| logging_simple           | 8.98 us                                                 | 15.9 us: 1.77x slower                                 |
| pprint_pformat           | 2.00 sec                                                | 3.60 sec: 1.81x slower                                |
| pprint_safe_repr         | 959 ms                                                  | 1.74 sec: 1.81x slower                                |
| genshi_text              | 31.7 ms                                                 | 57.9 ms: 1.83x slower                                 |
| mako                     | 16.1 ms                                                 | 29.5 ms: 1.84x slower                                 |
| pickle_pure_python       | 417 us                                                  | 768 us: 1.84x slower                                  |
| comprehensions           | 20.9 us                                                 | 39.2 us: 1.87x slower                                 |
| scimark_monte_carlo      | 89.9 ms                                                 | 168 ms: 1.87x slower                                  |
| logging_format           | 9.48 us                                                 | 18.2 us: 1.92x slower                                 |
| unpickle_pure_python     | 296 us                                                  | 573 us: 1.94x slower                                  |
| sympy_str                | 367 ms                                                  | 713 ms: 1.94x slower                                  |
| hexiom                   | 8.35 ms                                                 | 16.3 ms: 1.96x slower                                 |
| scimark_sor              | 172 ms                                                  | 342 ms: 1.99x slower                                  |
| logging_silent           | 130 ns                                                  | 259 ns: 1.99x slower                                  |
| sqlglot_transpile        | 2.30 ms                                                 | 4.65 ms: 2.02x slower                                 |
| sympy_expand             | 631 ms                                                  | 1.29 sec: 2.05x slower                                |
| chaos                    | 84.7 ms                                                 | 175 ms: 2.06x slower                                  |
| go                       | 195 ms                                                  | 405 ms: 2.07x slower                                  |
| scimark_lu               | 154 ms                                                  | 323 ms: 2.10x slower                                  |
| sqlglot_parse            | 1.80 ms                                                 | 3.81 ms: 2.12x slower                                 |
| sympy_sum                | 213 ms                                                  | 487 ms: 2.29x slower                                  |
| raytrace                 | 350 ms                                                  | 805 ms: 2.30x slower                                  |
| nbody                    | 124 ms                                                  | 291 ms: 2.35x slower                                  |
| unpack_sequence          | 73.9 ns                                                 | 190 ns: 2.58x slower                                  |
| deltablue                | 4.56 ms                                                 | 12.1 ms: 2.66x slower                                 |
| Geometric mean           | (ref)                                                   | 1.41x slower                                          |

Benchmark hidden because not significant (13): pickle_dict, async_tree_memoization_tg, asyncio_websockets, regex_effbot, pidigits, async_tree_cpu_io_mixed_tg, async_tree_memoization, regex_dna, xml_etree_iterparse, unpickle_list, unpickle, sqlite_synth, async_tree_none
Ignored benchmarks (6) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.36x
- 95% likely to have a slowdown of 1.33x
- 99% likely to have a slowdown of 1.30x

# Memory
- memory change: 1.16x