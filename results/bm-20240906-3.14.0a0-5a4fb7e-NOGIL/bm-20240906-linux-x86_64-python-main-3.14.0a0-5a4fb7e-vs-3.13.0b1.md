# Results vs. 3.13.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5a4fb7e
- commit date: 2024-09-06
- overall geometric mean: 1.41x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.31x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 441 ms                                                                | 682 ms: 1.55x slower                                  |
| docutils       | 3.94 sec                                                              | 5.10 sec: 1.29x slower                                |
| html5lib       | 92.0 ms                                                               | 147 ms: 1.60x slower                                  |
| tornado_http   | 253 ms                                                                | 420 ms: 1.66x slower                                  |
| Geometric mean | (ref)                                                                 | 1.52x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|-------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg        | 1.43 sec                                                              | 1.24 sec: 1.16x faster                                |
| async_tree_io           | 1.39 sec                                                              | 1.32 sec: 1.05x faster                                |
| async_tree_cpu_io_mixed | 898 ms                                                                | 937 ms: 1.04x slower                                  |
| asyncio_websockets      | 728 ms                                                                | 818 ms: 1.12x slower                                  |
| async_tree_none         | 523 ms                                                                | 607 ms: 1.16x slower                                  |
| async_generators        | 588 ms                                                                | 723 ms: 1.23x slower                                  |
| asyncio_tcp             | 972 ms                                                                | 1.22 sec: 1.25x slower                                |
| asyncio_tcp_ssl         | 2.83 sec                                                              | 3.67 sec: 1.30x slower                                |
| coroutines              | 29.3 ms                                                               | 42.2 ms: 1.44x slower                                 |
| Geometric mean          | (ref)                                                                 | 1.09x slower                                          |

Benchmark hidden because not significant (4): async_tree_memoization_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 115 ms                                                                | 203 ms: 1.76x slower                                  |
| nbody          | 126 ms                                                                | 315 ms: 2.51x slower                                  |
| Geometric mean | (ref)                                                                 | 1.65x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 284 ms                                                                | 299 ms: 1.05x slower                                  |
| regex_effbot   | 4.63 ms                                                               | 5.21 ms: 1.12x slower                                 |
| regex_compile  | 189 ms                                                                | 305 ms: 1.61x slower                                  |
| Geometric mean | (ref)                                                                 | 1.18x slower                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.51 us: 1.15x faster                                 |
| pickle               | 15.2 us                                                               | 13.8 us: 1.10x faster                                 |
| xml_etree_parse      | 216 ms                                                                | 229 ms: 1.06x slower                                  |
| unpickle_list        | 6.78 us                                                               | 7.45 us: 1.10x slower                                 |
| json_loads           | 37.9 us                                                               | 47.7 us: 1.26x slower                                 |
| json_dumps           | 13.9 ms                                                               | 18.0 ms: 1.29x slower                                 |
| xml_etree_generate   | 120 ms                                                                | 179 ms: 1.50x slower                                  |
| tomli_loads          | 2.84 sec                                                              | 4.37 sec: 1.54x slower                                |
| xml_etree_process    | 82.2 ms                                                               | 136 ms: 1.65x slower                                  |
| pickle_pure_python   | 428 us                                                                | 762 us: 1.78x slower                                  |
| unpickle_pure_python | 285 us                                                                | 563 us: 1.97x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.24x slower                                          |

Benchmark hidden because not significant (3): pickle_dict, xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.0 ms                                                               | 24.3 ms: 1.52x slower                                 |
| python_startup         | 23.5 ms                                                               | 37.1 ms: 1.58x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.55x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 46.1 ms                                                               | 83.6 ms: 1.81x slower                                 |
| genshi_text     | 31.6 ms                                                               | 57.6 ms: 1.82x slower                                 |
| mako            | 16.7 ms                                                               | 31.9 ms: 1.91x slower                                 |
| genshi_xml      | 71.9 ms                                                               | 141 ms: 1.96x slower                                  |
| Geometric mean  | (ref)                                                                 | 1.87x slower                                          |

All benchmarks:
===============

| Benchmark                | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|--------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| telco                    | 229 ms                                                                | 14.9 ms: 15.41x faster                                |
| create_gc_cycles         | 2.49 ms                                                               | 1.96 ms: 1.27x faster                                 |
| gc_traversal             | 5.80 ms                                                               | 4.74 ms: 1.23x faster                                 |
| async_tree_io_tg         | 1.43 sec                                                              | 1.24 sec: 1.16x faster                                |
| pickle_list              | 7.48 us                                                               | 6.51 us: 1.15x faster                                 |
| pickle                   | 15.2 us                                                               | 13.8 us: 1.10x faster                                 |
| async_tree_io            | 1.39 sec                                                              | 1.32 sec: 1.05x faster                                |
| async_tree_cpu_io_mixed  | 898 ms                                                                | 937 ms: 1.04x slower                                  |
| regex_dna                | 284 ms                                                                | 299 ms: 1.05x slower                                  |
| xml_etree_parse          | 216 ms                                                                | 229 ms: 1.06x slower                                  |
| sqlite_synth             | 3.94 us                                                               | 4.25 us: 1.08x slower                                 |
| unpickle_list            | 6.78 us                                                               | 7.45 us: 1.10x slower                                 |
| regex_effbot             | 4.63 ms                                                               | 5.21 ms: 1.12x slower                                 |
| asyncio_websockets       | 728 ms                                                                | 818 ms: 1.12x slower                                  |
| pathlib                  | 31.8 ms                                                               | 36.2 ms: 1.14x slower                                 |
| async_tree_none          | 523 ms                                                                | 607 ms: 1.16x slower                                  |
| coverage                 | 121 ms                                                                | 144 ms: 1.20x slower                                  |
| async_generators         | 588 ms                                                                | 723 ms: 1.23x slower                                  |
| deepcopy                 | 498 us                                                                | 617 us: 1.24x slower                                  |
| meteor_contest           | 156 ms                                                                | 196 ms: 1.25x slower                                  |
| asyncio_tcp              | 972 ms                                                                | 1.22 sec: 1.25x slower                                |
| json_loads               | 37.9 us                                                               | 47.7 us: 1.26x slower                                 |
| mdp                      | 4.01 sec                                                              | 5.07 sec: 1.26x slower                                |
| json_dumps               | 13.9 ms                                                               | 18.0 ms: 1.29x slower                                 |
| docutils                 | 3.94 sec                                                              | 5.10 sec: 1.29x slower                                |
| asyncio_tcp_ssl          | 2.83 sec                                                              | 3.67 sec: 1.30x slower                                |
| json                     | 6.79 ms                                                               | 9.01 ms: 1.33x slower                                 |
| pycparser                | 1.71 sec                                                              | 2.29 sec: 1.34x slower                                |
| scimark_sparse_mat_mult  | 6.84 ms                                                               | 9.21 ms: 1.35x slower                                 |
| deepcopy_reduce          | 4.31 us                                                               | 5.81 us: 1.35x slower                                 |
| pylint                   | 466 ms                                                                | 641 ms: 1.37x slower                                  |
| generators               | 40.7 ms                                                               | 56.6 ms: 1.39x slower                                 |
| deepcopy_memo            | 50.9 us                                                               | 71.0 us: 1.40x slower                                 |
| scimark_fft              | 469 ms                                                                | 659 ms: 1.40x slower                                  |
| coroutines               | 29.3 ms                                                               | 42.2 ms: 1.44x slower                                 |
| dulwich_log              | 97.5 ms                                                               | 143 ms: 1.47x slower                                  |
| xml_etree_generate       | 120 ms                                                                | 179 ms: 1.50x slower                                  |
| fannkuch                 | 535 ms                                                                | 807 ms: 1.51x slower                                  |
| python_startup_no_site   | 16.0 ms                                                               | 24.3 ms: 1.52x slower                                 |
| tomli_loads              | 2.84 sec                                                              | 4.37 sec: 1.54x slower                                |
| 2to3                     | 441 ms                                                                | 682 ms: 1.55x slower                                  |
| thrift                   | 1.09 ms                                                               | 1.68 ms: 1.55x slower                                 |
| richards                 | 68.8 ms                                                               | 107 ms: 1.55x slower                                  |
| crypto_pyaes             | 102 ms                                                                | 158 ms: 1.55x slower                                  |
| pyflate                  | 710 ms                                                                | 1.11 sec: 1.56x slower                                |
| nqueens                  | 108 ms                                                                | 170 ms: 1.57x slower                                  |
| python_startup           | 23.5 ms                                                               | 37.1 ms: 1.58x slower                                 |
| html5lib                 | 92.0 ms                                                               | 147 ms: 1.60x slower                                  |
| sqlglot_optimize         | 77.9 ms                                                               | 125 ms: 1.60x slower                                  |
| typing_runtime_protocols | 222 us                                                                | 357 us: 1.61x slower                                  |
| regex_compile            | 189 ms                                                                | 305 ms: 1.61x slower                                  |
| bpe_tokeniser            | 6.53 sec                                                              | 10.8 sec: 1.65x slower                                |
| xml_etree_process        | 82.2 ms                                                               | 136 ms: 1.65x slower                                  |
| sqlglot_normalize        | 150 ms                                                                | 248 ms: 1.65x slower                                  |
| tornado_http             | 253 ms                                                                | 420 ms: 1.66x slower                                  |
| spectral_norm            | 151 ms                                                                | 253 ms: 1.68x slower                                  |
| pprint_safe_repr         | 991 ms                                                                | 1.66 sec: 1.68x slower                                |
| richards_super           | 73.5 ms                                                               | 126 ms: 1.71x slower                                  |
| sympy_integrate          | 28.7 ms                                                               | 49.3 ms: 1.72x slower                                 |
| pprint_pformat           | 2.04 sec                                                              | 3.55 sec: 1.74x slower                                |
| logging_simple           | 9.16 us                                                               | 16.0 us: 1.75x slower                                 |
| float                    | 115 ms                                                                | 203 ms: 1.76x slower                                  |
| bench_thread_pool        | 3.01 ms                                                               | 5.33 ms: 1.77x slower                                 |
| pickle_pure_python       | 428 us                                                                | 762 us: 1.78x slower                                  |
| django_template          | 46.1 ms                                                               | 83.6 ms: 1.81x slower                                 |
| genshi_text              | 31.6 ms                                                               | 57.6 ms: 1.82x slower                                 |
| comprehensions           | 22.6 us                                                               | 41.3 us: 1.82x slower                                 |
| logging_format           | 9.36 us                                                               | 17.5 us: 1.87x slower                                 |
| sympy_str                | 376 ms                                                                | 708 ms: 1.88x slower                                  |
| mako                     | 16.7 ms                                                               | 31.9 ms: 1.91x slower                                 |
| go                       | 193 ms                                                                | 370 ms: 1.92x slower                                  |
| scimark_monte_carlo      | 89.0 ms                                                               | 171 ms: 1.92x slower                                  |
| logging_silent           | 137 ns                                                                | 266 ns: 1.94x slower                                  |
| genshi_xml               | 71.9 ms                                                               | 141 ms: 1.96x slower                                  |
| sqlglot_parse            | 1.92 ms                                                               | 3.76 ms: 1.96x slower                                 |
| unpickle_pure_python     | 285 us                                                                | 563 us: 1.97x slower                                  |
| chaos                    | 81.5 ms                                                               | 163 ms: 1.99x slower                                  |
| hexiom                   | 8.42 ms                                                               | 17.1 ms: 2.03x slower                                 |
| scimark_sor              | 176 ms                                                                | 360 ms: 2.04x slower                                  |
| sympy_expand             | 638 ms                                                                | 1.32 sec: 2.06x slower                                |
| sympy_sum                | 226 ms                                                                | 472 ms: 2.08x slower                                  |
| sqlglot_transpile        | 2.24 ms                                                               | 4.73 ms: 2.11x slower                                 |
| scimark_lu               | 150 ms                                                                | 328 ms: 2.19x slower                                  |
| raytrace                 | 351 ms                                                                | 798 ms: 2.27x slower                                  |
| nbody                    | 126 ms                                                                | 315 ms: 2.51x slower                                  |
| deltablue                | 4.55 ms                                                               | 12.2 ms: 2.67x slower                                 |
| unpack_sequence          | 54.6 ns                                                               | 207 ns: 3.79x slower                                  |
| Geometric mean           | (ref)                                                                 | 1.41x slower                                          |

Benchmark hidden because not significant (10): async_tree_memoization_tg, bench_mp_pool, pickle_dict, async_tree_memoization, pidigits, async_tree_cpu_io_mixed_tg, regex_v8, async_tree_none_tg, xml_etree_iterparse, unpickle
Ignored benchmarks (5) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.36x
- 95% likely to have a slowdown of 1.33x
- 99% likely to have a slowdown of 1.31x

# Memory
- memory change: 1.15x