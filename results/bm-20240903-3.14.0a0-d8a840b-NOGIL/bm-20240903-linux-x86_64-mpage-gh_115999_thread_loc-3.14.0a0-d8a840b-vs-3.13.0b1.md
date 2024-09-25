# Results vs. 3.13.0b1

- fork: mpage
- ref: gh_115999_thread_loc
- machine: linux-x86_64
- commit hash: d8a840b
- commit date: 2024-09-03
- overall geometric mean: 1.37x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 441 ms                                                                | 698 ms: 1.58x slower                                                 |
| docutils       | 3.94 sec                                                              | 4.84 sec: 1.23x slower                                               |
| html5lib       | 92.0 ms                                                               | 142 ms: 1.54x slower                                                 |
| tornado_http   | 253 ms                                                                | 399 ms: 1.58x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.47x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|-------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg        | 1.43 sec                                                              | 1.15 sec: 1.24x faster                                               |
| async_tree_io           | 1.39 sec                                                              | 1.30 sec: 1.07x faster                                               |
| async_tree_memoization  | 775 ms                                                                | 727 ms: 1.07x faster                                                 |
| async_tree_cpu_io_mixed | 898 ms                                                                | 974 ms: 1.08x slower                                                 |
| async_tree_none         | 523 ms                                                                | 581 ms: 1.11x slower                                                 |
| asyncio_tcp             | 972 ms                                                                | 1.12 sec: 1.15x slower                                               |
| asyncio_tcp_ssl         | 2.83 sec                                                              | 3.41 sec: 1.21x slower                                               |
| async_generators        | 588 ms                                                                | 712 ms: 1.21x slower                                                 |
| coroutines              | 29.3 ms                                                               | 41.6 ms: 1.42x slower                                                |
| Geometric mean          | (ref)                                                                 | 1.05x slower                                                         |

Benchmark hidden because not significant (4): async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 115 ms                                                                | 192 ms: 1.67x slower                                                 |
| nbody          | 126 ms                                                                | 271 ms: 2.16x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.51x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 284 ms                                                                | 297 ms: 1.05x slower                                                 |
| regex_compile  | 189 ms                                                                | 312 ms: 1.65x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.13x slower                                                         |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle               | 15.2 us                                                               | 13.8 us: 1.10x faster                                                |
| xml_etree_iterparse  | 163 ms                                                                | 173 ms: 1.06x slower                                                 |
| xml_etree_parse      | 216 ms                                                                | 243 ms: 1.12x slower                                                 |
| json_loads           | 37.9 us                                                               | 43.5 us: 1.15x slower                                                |
| unpickle_list        | 6.78 us                                                               | 8.26 us: 1.22x slower                                                |
| json_dumps           | 13.9 ms                                                               | 17.3 ms: 1.24x slower                                                |
| xml_etree_generate   | 120 ms                                                                | 166 ms: 1.39x slower                                                 |
| tomli_loads          | 2.84 sec                                                              | 4.40 sec: 1.55x slower                                               |
| xml_etree_process    | 82.2 ms                                                               | 131 ms: 1.60x slower                                                 |
| pickle_pure_python   | 428 us                                                                | 812 us: 1.90x slower                                                 |
| unpickle_pure_python | 285 us                                                                | 597 us: 2.09x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.26x slower                                                         |

Benchmark hidden because not significant (3): pickle_list, pickle_dict, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 16.0 ms                                                               | 21.7 ms: 1.36x slower                                                |
| python_startup         | 23.5 ms                                                               | 35.2 ms: 1.50x slower                                                |
| Geometric mean         | (ref)                                                                 | 1.43x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 120 ms: 1.66x slower                                                 |
| genshi_text     | 31.6 ms                                                               | 55.2 ms: 1.75x slower                                                |
| django_template | 46.1 ms                                                               | 82.3 ms: 1.78x slower                                                |
| mako            | 16.7 ms                                                               | 32.1 ms: 1.92x slower                                                |
| Geometric mean  | (ref)                                                                 | 1.78x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|--------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| telco                    | 229 ms                                                                | 14.0 ms: 16.32x faster                                               |
| create_gc_cycles         | 2.49 ms                                                               | 1.85 ms: 1.35x faster                                                |
| async_tree_io_tg         | 1.43 sec                                                              | 1.15 sec: 1.24x faster                                               |
| gc_traversal             | 5.80 ms                                                               | 5.05 ms: 1.15x faster                                                |
| pickle                   | 15.2 us                                                               | 13.8 us: 1.10x faster                                                |
| async_tree_io            | 1.39 sec                                                              | 1.30 sec: 1.07x faster                                               |
| async_tree_memoization   | 775 ms                                                                | 727 ms: 1.07x faster                                                 |
| regex_dna                | 284 ms                                                                | 297 ms: 1.05x slower                                                 |
| xml_etree_iterparse      | 163 ms                                                                | 173 ms: 1.06x slower                                                 |
| async_tree_cpu_io_mixed  | 898 ms                                                                | 974 ms: 1.08x slower                                                 |
| async_tree_none          | 523 ms                                                                | 581 ms: 1.11x slower                                                 |
| xml_etree_parse          | 216 ms                                                                | 243 ms: 1.12x slower                                                 |
| deepcopy                 | 498 us                                                                | 564 us: 1.13x slower                                                 |
| pathlib                  | 31.8 ms                                                               | 36.3 ms: 1.14x slower                                                |
| scimark_fft              | 469 ms                                                                | 539 ms: 1.15x slower                                                 |
| json_loads               | 37.9 us                                                               | 43.5 us: 1.15x slower                                                |
| asyncio_tcp              | 972 ms                                                                | 1.12 sec: 1.15x slower                                               |
| sqlite_synth             | 3.94 us                                                               | 4.64 us: 1.18x slower                                                |
| coverage                 | 121 ms                                                                | 144 ms: 1.20x slower                                                 |
| scimark_sparse_mat_mult  | 6.84 ms                                                               | 8.22 ms: 1.20x slower                                                |
| asyncio_tcp_ssl          | 2.83 sec                                                              | 3.41 sec: 1.21x slower                                               |
| async_generators         | 588 ms                                                                | 712 ms: 1.21x slower                                                 |
| unpickle_list            | 6.78 us                                                               | 8.26 us: 1.22x slower                                                |
| mdp                      | 4.01 sec                                                              | 4.90 sec: 1.22x slower                                               |
| docutils                 | 3.94 sec                                                              | 4.84 sec: 1.23x slower                                               |
| json_dumps               | 13.9 ms                                                               | 17.3 ms: 1.24x slower                                                |
| meteor_contest           | 156 ms                                                                | 195 ms: 1.24x slower                                                 |
| json                     | 6.79 ms                                                               | 8.56 ms: 1.26x slower                                                |
| pycparser                | 1.71 sec                                                              | 2.20 sec: 1.29x slower                                               |
| pylint                   | 466 ms                                                                | 609 ms: 1.31x slower                                                 |
| generators               | 40.7 ms                                                               | 53.5 ms: 1.31x slower                                                |
| python_startup_no_site   | 16.0 ms                                                               | 21.7 ms: 1.36x slower                                                |
| xml_etree_generate       | 120 ms                                                                | 166 ms: 1.39x slower                                                 |
| deepcopy_memo            | 50.9 us                                                               | 72.1 us: 1.42x slower                                                |
| coroutines               | 29.3 ms                                                               | 41.6 ms: 1.42x slower                                                |
| fannkuch                 | 535 ms                                                                | 761 ms: 1.42x slower                                                 |
| deepcopy_reduce          | 4.31 us                                                               | 6.24 us: 1.45x slower                                                |
| pyflate                  | 710 ms                                                                | 1.04 sec: 1.47x slower                                               |
| nqueens                  | 108 ms                                                                | 160 ms: 1.48x slower                                                 |
| spectral_norm            | 151 ms                                                                | 224 ms: 1.48x slower                                                 |
| bench_thread_pool        | 3.01 ms                                                               | 4.51 ms: 1.50x slower                                                |
| python_startup           | 23.5 ms                                                               | 35.2 ms: 1.50x slower                                                |
| bpe_tokeniser            | 6.53 sec                                                              | 9.87 sec: 1.51x slower                                               |
| sqlglot_optimize         | 77.9 ms                                                               | 119 ms: 1.53x slower                                                 |
| crypto_pyaes             | 102 ms                                                                | 156 ms: 1.54x slower                                                 |
| html5lib                 | 92.0 ms                                                               | 142 ms: 1.54x slower                                                 |
| tomli_loads              | 2.84 sec                                                              | 4.40 sec: 1.55x slower                                               |
| richards                 | 68.8 ms                                                               | 107 ms: 1.55x slower                                                 |
| tornado_http             | 253 ms                                                                | 399 ms: 1.58x slower                                                 |
| 2to3                     | 441 ms                                                                | 698 ms: 1.58x slower                                                 |
| thrift                   | 1.09 ms                                                               | 1.73 ms: 1.60x slower                                                |
| xml_etree_process        | 82.2 ms                                                               | 131 ms: 1.60x slower                                                 |
| regex_compile            | 189 ms                                                                | 312 ms: 1.65x slower                                                 |
| sqlglot_normalize        | 150 ms                                                                | 249 ms: 1.66x slower                                                 |
| genshi_xml               | 71.9 ms                                                               | 120 ms: 1.66x slower                                                 |
| float                    | 115 ms                                                                | 192 ms: 1.67x slower                                                 |
| pprint_pformat           | 2.04 sec                                                              | 3.47 sec: 1.71x slower                                               |
| comprehensions           | 22.6 us                                                               | 38.6 us: 1.71x slower                                                |
| typing_runtime_protocols | 222 us                                                                | 381 us: 1.72x slower                                                 |
| genshi_text              | 31.6 ms                                                               | 55.2 ms: 1.75x slower                                                |
| pprint_safe_repr         | 991 ms                                                                | 1.77 sec: 1.78x slower                                               |
| django_template          | 46.1 ms                                                               | 82.3 ms: 1.78x slower                                                |
| sympy_integrate          | 28.7 ms                                                               | 51.4 ms: 1.79x slower                                                |
| scimark_monte_carlo      | 89.0 ms                                                               | 160 ms: 1.80x slower                                                 |
| logging_simple           | 9.16 us                                                               | 16.6 us: 1.81x slower                                                |
| sympy_str                | 376 ms                                                                | 698 ms: 1.85x slower                                                 |
| richards_super           | 73.5 ms                                                               | 137 ms: 1.86x slower                                                 |
| hexiom                   | 8.42 ms                                                               | 15.8 ms: 1.87x slower                                                |
| scimark_sor              | 176 ms                                                                | 331 ms: 1.88x slower                                                 |
| chaos                    | 81.5 ms                                                               | 154 ms: 1.89x slower                                                 |
| pickle_pure_python       | 428 us                                                                | 812 us: 1.90x slower                                                 |
| logging_silent           | 137 ns                                                                | 262 ns: 1.92x slower                                                 |
| go                       | 193 ms                                                                | 370 ms: 1.92x slower                                                 |
| mako                     | 16.7 ms                                                               | 32.1 ms: 1.92x slower                                                |
| logging_format           | 9.36 us                                                               | 19.1 us: 2.04x slower                                                |
| sqlglot_transpile        | 2.24 ms                                                               | 4.66 ms: 2.08x slower                                                |
| unpickle_pure_python     | 285 us                                                                | 597 us: 2.09x slower                                                 |
| sympy_expand             | 638 ms                                                                | 1.35 sec: 2.11x slower                                               |
| sqlglot_parse            | 1.92 ms                                                               | 4.06 ms: 2.12x slower                                                |
| scimark_lu               | 150 ms                                                                | 317 ms: 2.12x slower                                                 |
| nbody                    | 126 ms                                                                | 271 ms: 2.16x slower                                                 |
| raytrace                 | 351 ms                                                                | 788 ms: 2.24x slower                                                 |
| sympy_sum                | 226 ms                                                                | 512 ms: 2.26x slower                                                 |
| deltablue                | 4.55 ms                                                               | 11.5 ms: 2.53x slower                                                |
| unpack_sequence          | 54.6 ns                                                               | 191 ns: 3.50x slower                                                 |
| Geometric mean           | (ref)                                                                 | 1.37x slower                                                         |

Benchmark hidden because not significant (11): bench_mp_pool, pickle_list, regex_v8, pickle_dict, async_tree_none_tg, pidigits, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, regex_effbot, asyncio_websockets, unpickle
Ignored benchmarks (6) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.27x
- 95% likely to have a slowdown of 1.24x
- 99% likely to have a slowdown of 1.22x

# Memory
- memory change: 1.18x