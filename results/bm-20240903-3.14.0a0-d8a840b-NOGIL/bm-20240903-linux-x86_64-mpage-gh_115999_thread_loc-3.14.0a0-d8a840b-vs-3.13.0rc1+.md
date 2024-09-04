# Results vs. 3.13.0rc1+

- fork: mpage
- ref: gh_115999_thread_loc
- machine: linux-x86_64
- commit hash: d8a840b
- commit date: 2024-09-03
- overall geometric mean: 1.42x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 442 ms                                                  | 698 ms: 1.58x slower                                                 |
| docutils       | 4.01 sec                                                | 4.84 sec: 1.21x slower                                               |
| html5lib       | 98.1 ms                                                 | 142 ms: 1.45x slower                                                 |
| tornado_http   | 248 ms                                                  | 399 ms: 1.61x slower                                                 |
| Geometric mean | (ref)                                                   | 1.45x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|-------------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg        | 1.46 sec                                                | 1.15 sec: 1.26x faster                                               |
| async_tree_io           | 1.38 sec                                                | 1.30 sec: 1.06x faster                                               |
| asyncio_websockets      | 772 ms                                                  | 748 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed | 899 ms                                                  | 974 ms: 1.08x slower                                                 |
| asyncio_tcp             | 985 ms                                                  | 1.12 sec: 1.14x slower                                               |
| async_generators        | 592 ms                                                  | 712 ms: 1.20x slower                                                 |
| asyncio_tcp_ssl         | 2.79 sec                                                | 3.41 sec: 1.22x slower                                               |
| coroutines              | 29.2 ms                                                 | 41.6 ms: 1.42x slower                                                |
| Geometric mean          | (ref)                                                   | 1.05x slower                                                         |

Benchmark hidden because not significant (5): async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 115 ms                                                  | 192 ms: 1.67x slower                                                 |
| nbody          | 124 ms                                                  | 271 ms: 2.19x slower                                                 |
| Geometric mean | (ref)                                                   | 1.54x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 4.84 ms                                                 | 4.57 ms: 1.06x faster                                                |
| regex_dna      | 288 ms                                                  | 297 ms: 1.03x slower                                                 |
| regex_v8       | 32.4 ms                                                 | 35.5 ms: 1.09x slower                                                |
| regex_compile  | 177 ms                                                  | 312 ms: 1.76x slower                                                 |
| Geometric mean | (ref)                                                   | 1.17x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle               | 15.4 us                                                 | 13.8 us: 1.11x faster                                                |
| unpickle             | 21.4 us                                                 | 22.9 us: 1.07x slower                                                |
| json_dumps           | 14.9 ms                                                 | 17.3 ms: 1.16x slower                                                |
| json_loads           | 36.1 us                                                 | 43.5 us: 1.20x slower                                                |
| unpickle_list        | 6.67 us                                                 | 8.26 us: 1.24x slower                                                |
| xml_etree_generate   | 129 ms                                                  | 166 ms: 1.29x slower                                                 |
| xml_etree_process    | 86.5 ms                                                 | 131 ms: 1.52x slower                                                 |
| tomli_loads          | 2.80 sec                                                | 4.40 sec: 1.57x slower                                               |
| pickle_pure_python   | 417 us                                                  | 812 us: 1.95x slower                                                 |
| unpickle_pure_python | 296 us                                                  | 597 us: 2.02x slower                                                 |
| Geometric mean       | (ref)                                                   | 1.24x slower                                                         |

Benchmark hidden because not significant (4): pickle_dict, xml_etree_iterparse, xml_etree_parse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|------------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 14.6 ms                                                 | 21.7 ms: 1.48x slower                                                |
| python_startup         | 22.0 ms                                                 | 35.2 ms: 1.60x slower                                                |
| Geometric mean         | (ref)                                                   | 1.54x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|-----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                 | 55.2 ms: 1.74x slower                                                |
| genshi_xml      | 68.3 ms                                                 | 120 ms: 1.75x slower                                                 |
| django_template | 46.9 ms                                                 | 82.3 ms: 1.75x slower                                                |
| mako            | 16.1 ms                                                 | 32.1 ms: 2.00x slower                                                |
| Geometric mean  | (ref)                                                   | 1.81x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|--------------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| create_gc_cycles         | 2.46 ms                                                 | 1.85 ms: 1.33x faster                                                |
| async_tree_io_tg         | 1.46 sec                                                | 1.15 sec: 1.26x faster                                               |
| gc_traversal             | 5.91 ms                                                 | 5.05 ms: 1.17x faster                                                |
| pickle                   | 15.4 us                                                 | 13.8 us: 1.11x faster                                                |
| regex_effbot             | 4.84 ms                                                 | 4.57 ms: 1.06x faster                                                |
| async_tree_io            | 1.38 sec                                                | 1.30 sec: 1.06x faster                                               |
| asyncio_websockets       | 772 ms                                                  | 748 ms: 1.03x faster                                                 |
| regex_dna                | 288 ms                                                  | 297 ms: 1.03x slower                                                 |
| unpickle                 | 21.4 us                                                 | 22.9 us: 1.07x slower                                                |
| async_tree_cpu_io_mixed  | 899 ms                                                  | 974 ms: 1.08x slower                                                 |
| regex_v8                 | 32.4 ms                                                 | 35.5 ms: 1.09x slower                                                |
| scimark_fft              | 477 ms                                                  | 539 ms: 1.13x slower                                                 |
| asyncio_tcp              | 985 ms                                                  | 1.12 sec: 1.14x slower                                               |
| sqlite_synth             | 4.07 us                                                 | 4.64 us: 1.14x slower                                                |
| json_dumps               | 14.9 ms                                                 | 17.3 ms: 1.16x slower                                                |
| deepcopy                 | 484 us                                                  | 564 us: 1.16x slower                                                 |
| scimark_sparse_mat_mult  | 6.98 ms                                                 | 8.22 ms: 1.18x slower                                                |
| async_generators         | 592 ms                                                  | 712 ms: 1.20x slower                                                 |
| json_loads               | 36.1 us                                                 | 43.5 us: 1.20x slower                                                |
| docutils                 | 4.01 sec                                                | 4.84 sec: 1.21x slower                                               |
| asyncio_tcp_ssl          | 2.79 sec                                                | 3.41 sec: 1.22x slower                                               |
| telco                    | 11.4 ms                                                 | 14.0 ms: 1.23x slower                                                |
| pathlib                  | 29.3 ms                                                 | 36.3 ms: 1.24x slower                                                |
| unpickle_list            | 6.67 us                                                 | 8.26 us: 1.24x slower                                                |
| meteor_contest           | 157 ms                                                  | 195 ms: 1.24x slower                                                 |
| xml_etree_generate       | 129 ms                                                  | 166 ms: 1.29x slower                                                 |
| mdp                      | 3.80 sec                                                | 4.90 sec: 1.29x slower                                               |
| pylint                   | 472 ms                                                  | 609 ms: 1.29x slower                                                 |
| json                     | 6.55 ms                                                 | 8.56 ms: 1.31x slower                                                |
| coverage                 | 110 ms                                                  | 144 ms: 1.31x slower                                                 |
| generators               | 39.2 ms                                                 | 53.5 ms: 1.36x slower                                                |
| deepcopy_memo            | 51.7 us                                                 | 72.1 us: 1.39x slower                                                |
| pycparser                | 1.57 sec                                                | 2.20 sec: 1.40x slower                                               |
| fannkuch                 | 543 ms                                                  | 761 ms: 1.40x slower                                                 |
| spectral_norm            | 159 ms                                                  | 224 ms: 1.41x slower                                                 |
| coroutines               | 29.2 ms                                                 | 41.6 ms: 1.42x slower                                                |
| html5lib                 | 98.1 ms                                                 | 142 ms: 1.45x slower                                                 |
| deepcopy_reduce          | 4.27 us                                                 | 6.24 us: 1.46x slower                                                |
| bench_thread_pool        | 3.06 ms                                                 | 4.51 ms: 1.47x slower                                                |
| nqueens                  | 108 ms                                                  | 160 ms: 1.48x slower                                                 |
| python_startup_no_site   | 14.6 ms                                                 | 21.7 ms: 1.48x slower                                                |
| xml_etree_process        | 86.5 ms                                                 | 131 ms: 1.52x slower                                                 |
| thrift                   | 1.11 ms                                                 | 1.73 ms: 1.56x slower                                                |
| sqlglot_optimize         | 76.2 ms                                                 | 119 ms: 1.56x slower                                                 |
| crypto_pyaes             | 99.8 ms                                                 | 156 ms: 1.57x slower                                                 |
| tomli_loads              | 2.80 sec                                                | 4.40 sec: 1.57x slower                                               |
| pyflate                  | 661 ms                                                  | 1.04 sec: 1.58x slower                                               |
| bpe_tokeniser            | 6.25 sec                                                | 9.87 sec: 1.58x slower                                               |
| 2to3                     | 442 ms                                                  | 698 ms: 1.58x slower                                                 |
| python_startup           | 22.0 ms                                                 | 35.2 ms: 1.60x slower                                                |
| tornado_http             | 248 ms                                                  | 399 ms: 1.61x slower                                                 |
| richards                 | 65.8 ms                                                 | 107 ms: 1.63x slower                                                 |
| float                    | 115 ms                                                  | 192 ms: 1.67x slower                                                 |
| sqlglot_normalize        | 146 ms                                                  | 249 ms: 1.71x slower                                                 |
| sympy_integrate          | 29.7 ms                                                 | 51.4 ms: 1.73x slower                                                |
| genshi_text              | 31.7 ms                                                 | 55.2 ms: 1.74x slower                                                |
| pprint_pformat           | 2.00 sec                                                | 3.47 sec: 1.74x slower                                               |
| genshi_xml               | 68.3 ms                                                 | 120 ms: 1.75x slower                                                 |
| django_template          | 46.9 ms                                                 | 82.3 ms: 1.75x slower                                                |
| regex_compile            | 177 ms                                                  | 312 ms: 1.76x slower                                                 |
| typing_runtime_protocols | 216 us                                                  | 381 us: 1.77x slower                                                 |
| scimark_monte_carlo      | 89.9 ms                                                 | 160 ms: 1.78x slower                                                 |
| richards_super           | 76.3 ms                                                 | 137 ms: 1.79x slower                                                 |
| chaos                    | 84.7 ms                                                 | 154 ms: 1.82x slower                                                 |
| pprint_safe_repr         | 959 ms                                                  | 1.77 sec: 1.84x slower                                               |
| comprehensions           | 20.9 us                                                 | 38.6 us: 1.85x slower                                                |
| logging_simple           | 8.98 us                                                 | 16.6 us: 1.85x slower                                                |
| hexiom                   | 8.35 ms                                                 | 15.8 ms: 1.89x slower                                                |
| go                       | 195 ms                                                  | 370 ms: 1.89x slower                                                 |
| sympy_str                | 367 ms                                                  | 698 ms: 1.90x slower                                                 |
| scimark_sor              | 172 ms                                                  | 331 ms: 1.92x slower                                                 |
| pickle_pure_python       | 417 us                                                  | 812 us: 1.95x slower                                                 |
| mako                     | 16.1 ms                                                 | 32.1 ms: 2.00x slower                                                |
| logging_format           | 9.48 us                                                 | 19.1 us: 2.01x slower                                                |
| logging_silent           | 130 ns                                                  | 262 ns: 2.01x slower                                                 |
| unpickle_pure_python     | 296 us                                                  | 597 us: 2.02x slower                                                 |
| sqlglot_transpile        | 2.30 ms                                                 | 4.66 ms: 2.03x slower                                                |
| scimark_lu               | 154 ms                                                  | 317 ms: 2.06x slower                                                 |
| sympy_expand             | 631 ms                                                  | 1.35 sec: 2.13x slower                                               |
| nbody                    | 124 ms                                                  | 271 ms: 2.19x slower                                                 |
| raytrace                 | 350 ms                                                  | 788 ms: 2.25x slower                                                 |
| sqlglot_parse            | 1.80 ms                                                 | 4.06 ms: 2.26x slower                                                |
| sympy_sum                | 213 ms                                                  | 512 ms: 2.40x slower                                                 |
| deltablue                | 4.56 ms                                                 | 11.5 ms: 2.52x slower                                                |
| unpack_sequence          | 73.9 ns                                                 | 191 ns: 2.59x slower                                                 |
| Geometric mean           | (ref)                                                   | 1.42x slower                                                         |

Benchmark hidden because not significant (11): bench_mp_pool, pickle_dict, async_tree_none_tg, async_tree_memoization, xml_etree_iterparse, pidigits, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none, xml_etree_parse, pickle_list
Ignored benchmarks (6) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.31x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.17x