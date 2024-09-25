# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_122712_fix_call_a
- machine: linux-x86_64
- commit hash: f483286
- commit date: 2024-08-07
- overall geometric mean: 1.43x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.31x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 646 ms: 1.45x slower                                                 |
| docutils       | 4.01 sec                                                     | 5.06 sec: 1.26x slower                                               |
| html5lib       | 92.6 ms                                                      | 140 ms: 1.51x slower                                                 |
| tornado_http   | 251 ms                                                       | 367 ms: 1.46x slower                                                 |
| Geometric mean | (ref)                                                        | 1.42x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.15 sec: 1.22x faster                                               |
| async_tree_io              | 1.39 sec                                                     | 1.25 sec: 1.11x faster                                               |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 824 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 933 ms: 1.05x slower                                                 |
| async_tree_memoization     | 709 ms                                                       | 751 ms: 1.06x slower                                                 |
| asyncio_tcp                | 948 ms                                                       | 1.12 sec: 1.18x slower                                               |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.36 sec: 1.21x slower                                               |
| async_generators           | 567 ms                                                       | 753 ms: 1.33x slower                                                 |
| coroutines                 | 30.9 ms                                                      | 42.1 ms: 1.36x slower                                                |
| Geometric mean             | (ref)                                                        | 1.05x slower                                                         |

Benchmark hidden because not significant (4): async_tree_none_tg, asyncio_websockets, async_tree_memoization_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 116 ms                                                       | 196 ms: 1.69x slower                                                 |
| nbody          | 119 ms                                                       | 284 ms: 2.39x slower                                                 |
| Geometric mean | (ref)                                                        | 1.57x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 301 ms: 1.07x slower                                                 |
| regex_v8       | 32.8 ms                                                      | 39.2 ms: 1.19x slower                                                |
| regex_compile  | 182 ms                                                       | 295 ms: 1.62x slower                                                 |
| Geometric mean | (ref)                                                        | 1.20x slower                                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_dict          | 47.2 us                                                      | 43.9 us: 1.08x faster                                                |
| pickle               | 15.1 us                                                      | 14.1 us: 1.07x faster                                                |
| unpickle             | 20.5 us                                                      | 22.0 us: 1.07x slower                                                |
| unpickle_list        | 6.68 us                                                      | 7.94 us: 1.19x slower                                                |
| json_dumps           | 14.1 ms                                                      | 17.7 ms: 1.25x slower                                                |
| json_loads           | 34.3 us                                                      | 45.4 us: 1.32x slower                                                |
| xml_etree_generate   | 122 ms                                                       | 164 ms: 1.34x slower                                                 |
| tomli_loads          | 2.78 sec                                                     | 4.20 sec: 1.51x slower                                               |
| xml_etree_process    | 85.9 ms                                                      | 135 ms: 1.57x slower                                                 |
| pickle_pure_python   | 416 us                                                       | 778 us: 1.87x slower                                                 |
| unpickle_pure_python | 290 us                                                       | 567 us: 1.96x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.25x slower                                                         |

Benchmark hidden because not significant (3): xml_etree_parse, pickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 29.3 ms: 1.31x slower                                                |
| python_startup_no_site | 15.3 ms                                                      | 20.7 ms: 1.35x slower                                                |
| Geometric mean         | (ref)                                                        | 1.33x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 118 ms: 1.63x slower                                                 |
| genshi_text     | 31.7 ms                                                      | 54.2 ms: 1.71x slower                                                |
| django_template | 44.3 ms                                                      | 77.1 ms: 1.74x slower                                                |
| mako            | 15.9 ms                                                      | 32.1 ms: 2.01x slower                                                |
| Geometric mean  | (ref)                                                        | 1.77x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| create_gc_cycles           | 2.41 ms                                                      | 1.92 ms: 1.25x faster                                                |
| gc_traversal               | 5.70 ms                                                      | 4.63 ms: 1.23x faster                                                |
| async_tree_io_tg           | 1.40 sec                                                     | 1.15 sec: 1.22x faster                                               |
| bench_mp_pool              | 18.7 ms                                                      | 16.8 ms: 1.12x faster                                                |
| async_tree_io              | 1.39 sec                                                     | 1.25 sec: 1.11x faster                                               |
| pickle_dict                | 47.2 us                                                      | 43.9 us: 1.08x faster                                                |
| pickle                     | 15.1 us                                                      | 14.1 us: 1.07x faster                                                |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 824 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 933 ms: 1.05x slower                                                 |
| async_tree_memoization     | 709 ms                                                       | 751 ms: 1.06x slower                                                 |
| regex_dna                  | 282 ms                                                       | 301 ms: 1.07x slower                                                 |
| unpickle                   | 20.5 us                                                      | 22.0 us: 1.07x slower                                                |
| sqlite_synth               | 3.99 us                                                      | 4.44 us: 1.11x slower                                                |
| deepcopy                   | 498 us                                                       | 556 us: 1.12x slower                                                 |
| telco                      | 12.2 ms                                                      | 13.8 ms: 1.13x slower                                                |
| asyncio_tcp                | 948 ms                                                       | 1.12 sec: 1.18x slower                                               |
| unpickle_list              | 6.68 us                                                      | 7.94 us: 1.19x slower                                                |
| pathlib                    | 29.9 ms                                                      | 35.6 ms: 1.19x slower                                                |
| regex_v8                   | 32.8 ms                                                      | 39.2 ms: 1.19x slower                                                |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.36 sec: 1.21x slower                                               |
| json_dumps                 | 14.1 ms                                                      | 17.7 ms: 1.25x slower                                                |
| pylint                     | 470 ms                                                       | 590 ms: 1.26x slower                                                 |
| docutils                   | 4.01 sec                                                     | 5.06 sec: 1.26x slower                                               |
| json                       | 6.51 ms                                                      | 8.22 ms: 1.26x slower                                                |
| meteor_contest             | 150 ms                                                       | 194 ms: 1.29x slower                                                 |
| python_startup             | 22.4 ms                                                      | 29.3 ms: 1.31x slower                                                |
| json_loads                 | 34.3 us                                                      | 45.4 us: 1.32x slower                                                |
| async_generators           | 567 ms                                                       | 753 ms: 1.33x slower                                                 |
| xml_etree_generate         | 122 ms                                                       | 164 ms: 1.34x slower                                                 |
| scimark_fft                | 473 ms                                                       | 635 ms: 1.34x slower                                                 |
| python_startup_no_site     | 15.3 ms                                                      | 20.7 ms: 1.35x slower                                                |
| coverage                   | 107 ms                                                       | 146 ms: 1.36x slower                                                 |
| mdp                        | 3.80 sec                                                     | 5.16 sec: 1.36x slower                                               |
| coroutines                 | 30.9 ms                                                      | 42.1 ms: 1.36x slower                                                |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 9.23 ms: 1.37x slower                                                |
| deepcopy_memo              | 50.1 us                                                      | 69.7 us: 1.39x slower                                                |
| fannkuch                   | 547 ms                                                       | 776 ms: 1.42x slower                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 5.84 us: 1.42x slower                                                |
| generators                 | 40.0 ms                                                      | 57.5 ms: 1.44x slower                                                |
| nqueens                    | 112 ms                                                       | 161 ms: 1.44x slower                                                 |
| 2to3                       | 445 ms                                                       | 646 ms: 1.45x slower                                                 |
| pycparser                  | 1.57 sec                                                     | 2.29 sec: 1.46x slower                                               |
| tornado_http               | 251 ms                                                       | 367 ms: 1.46x slower                                                 |
| sympy_integrate            | 30.2 ms                                                      | 44.3 ms: 1.47x slower                                                |
| bench_thread_pool          | 2.89 ms                                                      | 4.33 ms: 1.50x slower                                                |
| tomli_loads                | 2.78 sec                                                     | 4.20 sec: 1.51x slower                                               |
| html5lib                   | 92.6 ms                                                      | 140 ms: 1.51x slower                                                 |
| crypto_pyaes               | 100 ms                                                       | 152 ms: 1.52x slower                                                 |
| xml_etree_process          | 85.9 ms                                                      | 135 ms: 1.57x slower                                                 |
| typing_runtime_protocols   | 226 us                                                       | 356 us: 1.58x slower                                                 |
| thrift                     | 1.10 ms                                                      | 1.77 ms: 1.61x slower                                                |
| spectral_norm              | 157 ms                                                       | 253 ms: 1.61x slower                                                 |
| regex_compile              | 182 ms                                                       | 295 ms: 1.62x slower                                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 10.3 sec: 1.63x slower                                               |
| genshi_xml                 | 72.1 ms                                                      | 118 ms: 1.63x slower                                                 |
| pyflate                    | 664 ms                                                       | 1.09 sec: 1.64x slower                                               |
| pprint_safe_repr           | 987 ms                                                       | 1.64 sec: 1.67x slower                                               |
| richards                   | 65.5 ms                                                      | 110 ms: 1.68x slower                                                 |
| float                      | 116 ms                                                       | 196 ms: 1.69x slower                                                 |
| richards_super             | 73.2 ms                                                      | 124 ms: 1.70x slower                                                 |
| genshi_text                | 31.7 ms                                                      | 54.2 ms: 1.71x slower                                                |
| comprehensions             | 22.2 us                                                      | 38.3 us: 1.72x slower                                                |
| sqlglot_normalize          | 140 ms                                                       | 242 ms: 1.73x slower                                                 |
| django_template            | 44.3 ms                                                      | 77.1 ms: 1.74x slower                                                |
| logging_simple             | 8.56 us                                                      | 15.0 us: 1.76x slower                                                |
| scimark_monte_carlo        | 90.6 ms                                                      | 160 ms: 1.77x slower                                                 |
| pprint_pformat             | 1.94 sec                                                     | 3.45 sec: 1.77x slower                                               |
| sympy_str                  | 379 ms                                                       | 673 ms: 1.78x slower                                                 |
| pickle_pure_python         | 416 us                                                       | 778 us: 1.87x slower                                                 |
| scimark_sor                | 179 ms                                                       | 342 ms: 1.91x slower                                                 |
| sqlglot_optimize           | 74.7 ms                                                      | 143 ms: 1.92x slower                                                 |
| unpickle_pure_python       | 290 us                                                       | 567 us: 1.96x slower                                                 |
| logging_silent             | 130 ns                                                       | 254 ns: 1.96x slower                                                 |
| logging_format             | 9.24 us                                                      | 18.5 us: 2.01x slower                                                |
| mako                       | 15.9 ms                                                      | 32.1 ms: 2.01x slower                                                |
| chaos                      | 83.6 ms                                                      | 169 ms: 2.02x slower                                                 |
| scimark_lu                 | 146 ms                                                       | 303 ms: 2.07x slower                                                 |
| sqlglot_transpile          | 2.20 ms                                                      | 4.62 ms: 2.10x slower                                                |
| sympy_expand               | 601 ms                                                       | 1.26 sec: 2.10x slower                                               |
| hexiom                     | 8.11 ms                                                      | 17.2 ms: 2.12x slower                                                |
| sympy_sum                  | 210 ms                                                       | 465 ms: 2.21x slower                                                 |
| raytrace                   | 344 ms                                                       | 765 ms: 2.22x slower                                                 |
| go                         | 191 ms                                                       | 446 ms: 2.33x slower                                                 |
| nbody                      | 119 ms                                                       | 284 ms: 2.39x slower                                                 |
| sqlglot_parse              | 1.76 ms                                                      | 4.43 ms: 2.52x slower                                                |
| deltablue                  | 4.44 ms                                                      | 11.3 ms: 2.56x slower                                                |
| unpack_sequence            | 74.3 ns                                                      | 211 ns: 2.83x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.43x slower                                                         |

Benchmark hidden because not significant (9): pidigits, async_tree_none_tg, asyncio_websockets, async_tree_memoization_tg, xml_etree_parse, pickle_list, xml_etree_iterparse, regex_effbot, async_tree_none
Ignored benchmarks (6) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.36x
- 95% likely to have a slowdown of 1.35x
- 99% likely to have a slowdown of 1.31x

# Memory
- memory change: 1.14x