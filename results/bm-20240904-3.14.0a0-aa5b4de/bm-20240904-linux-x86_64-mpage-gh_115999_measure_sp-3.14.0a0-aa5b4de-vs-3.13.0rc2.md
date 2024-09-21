# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_measure_sp
- machine: linux-x86_64
- commit hash: aa5b4de
- commit date: 2024-09-04
- overall geometric mean: 1.25x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 526 ms: 1.18x slower                                                 |
| docutils       | 4.01 sec                                                     | 4.57 sec: 1.14x slower                                               |
| html5lib       | 92.6 ms                                                      | 128 ms: 1.38x slower                                                 |
| tornado_http   | 251 ms                                                       | 279 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                        | 1.20x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_tcp                | 948 ms                                                       | 997 ms: 1.05x slower                                                 |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 2.93 sec: 1.06x slower                                               |
| async_generators           | 567 ms                                                       | 624 ms: 1.10x slower                                                 |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 983 ms: 1.11x slower                                                 |
| async_tree_io              | 1.39 sec                                                     | 1.58 sec: 1.14x slower                                               |
| async_tree_none            | 572 ms                                                       | 656 ms: 1.15x slower                                                 |
| async_tree_io_tg           | 1.40 sec                                                     | 1.62 sec: 1.16x slower                                               |
| async_tree_memoization     | 709 ms                                                       | 822 ms: 1.16x slower                                                 |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 1.03 sec: 1.21x slower                                               |
| async_tree_none_tg         | 504 ms                                                       | 620 ms: 1.23x slower                                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 827 ms: 1.23x slower                                                 |
| coroutines                 | 30.9 ms                                                      | 40.5 ms: 1.31x slower                                                |
| Geometric mean             | (ref)                                                        | 1.14x slower                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 266 ms: 1.06x slower                                                 |
| float          | 116 ms                                                       | 169 ms: 1.46x slower                                                 |
| nbody          | 119 ms                                                       | 191 ms: 1.61x slower                                                 |
| Geometric mean | (ref)                                                        | 1.36x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 296 ms: 1.05x slower                                                 |
| regex_v8       | 32.8 ms                                                      | 36.1 ms: 1.10x slower                                                |
| regex_effbot   | 4.74 ms                                                      | 5.30 ms: 1.12x slower                                                |
| regex_compile  | 182 ms                                                       | 252 ms: 1.38x slower                                                 |
| Geometric mean | (ref)                                                        | 1.16x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 164 ms: 1.08x faster                                                 |
| unpickle             | 20.5 us                                                      | 19.3 us: 1.06x faster                                                |
| unpickle_list        | 6.68 us                                                      | 7.01 us: 1.05x slower                                                |
| pickle               | 15.1 us                                                      | 16.0 us: 1.06x slower                                                |
| json_loads           | 34.3 us                                                      | 40.2 us: 1.17x slower                                                |
| xml_etree_generate   | 122 ms                                                       | 148 ms: 1.21x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 17.8 ms: 1.26x slower                                                |
| xml_etree_process    | 85.9 ms                                                      | 110 ms: 1.28x slower                                                 |
| tomli_loads          | 2.78 sec                                                     | 3.60 sec: 1.30x slower                                               |
| unpickle_pure_python | 290 us                                                       | 434 us: 1.50x slower                                                 |
| pickle_pure_python   | 416 us                                                       | 755 us: 1.81x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.16x slower                                                         |

Benchmark hidden because not significant (3): xml_etree_parse, pickle_list, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup | 22.4 ms                                                      | 23.4 ms: 1.05x slower                                                |
| Geometric mean | (ref)                                                        | 1.04x slower                                                         |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 94.1 ms: 1.31x slower                                                |
| genshi_text     | 31.7 ms                                                      | 43.1 ms: 1.36x slower                                                |
| django_template | 44.3 ms                                                      | 65.8 ms: 1.49x slower                                                |
| mako            | 15.9 ms                                                      | 24.1 ms: 1.51x slower                                                |
| Geometric mean  | (ref)                                                        | 1.41x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpack_sequence            | 74.3 ns                                                      | 65.7 ns: 1.13x faster                                                |
| xml_etree_iterparse        | 177 ms                                                       | 164 ms: 1.08x faster                                                 |
| telco                      | 12.2 ms                                                      | 11.4 ms: 1.07x faster                                                |
| unpickle                   | 20.5 us                                                      | 19.3 us: 1.06x faster                                                |
| mdp                        | 3.80 sec                                                     | 3.96 sec: 1.04x slower                                               |
| coverage                   | 107 ms                                                       | 112 ms: 1.05x slower                                                 |
| python_startup             | 22.4 ms                                                      | 23.4 ms: 1.05x slower                                                |
| unpickle_list              | 6.68 us                                                      | 7.01 us: 1.05x slower                                                |
| meteor_contest             | 150 ms                                                       | 158 ms: 1.05x slower                                                 |
| asyncio_tcp                | 948 ms                                                       | 997 ms: 1.05x slower                                                 |
| regex_dna                  | 282 ms                                                       | 296 ms: 1.05x slower                                                 |
| pickle                     | 15.1 us                                                      | 16.0 us: 1.06x slower                                                |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 2.93 sec: 1.06x slower                                               |
| pidigits                   | 251 ms                                                       | 266 ms: 1.06x slower                                                 |
| gc_traversal               | 5.70 ms                                                      | 6.09 ms: 1.07x slower                                                |
| regex_v8                   | 32.8 ms                                                      | 36.1 ms: 1.10x slower                                                |
| async_generators           | 567 ms                                                       | 624 ms: 1.10x slower                                                 |
| create_gc_cycles           | 2.41 ms                                                      | 2.65 ms: 1.10x slower                                                |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 983 ms: 1.11x slower                                                 |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.48 ms: 1.11x slower                                                |
| tornado_http               | 251 ms                                                       | 279 ms: 1.11x slower                                                 |
| sympy_str                  | 379 ms                                                       | 423 ms: 1.12x slower                                                 |
| regex_effbot               | 4.74 ms                                                      | 5.30 ms: 1.12x slower                                                |
| nqueens                    | 112 ms                                                       | 125 ms: 1.12x slower                                                 |
| sympy_integrate            | 30.2 ms                                                      | 34.0 ms: 1.13x slower                                                |
| async_tree_io              | 1.39 sec                                                     | 1.58 sec: 1.14x slower                                               |
| docutils                   | 4.01 sec                                                     | 4.57 sec: 1.14x slower                                               |
| async_tree_none            | 572 ms                                                       | 656 ms: 1.15x slower                                                 |
| pylint                     | 470 ms                                                       | 542 ms: 1.15x slower                                                 |
| async_tree_io_tg           | 1.40 sec                                                     | 1.62 sec: 1.16x slower                                               |
| async_tree_memoization     | 709 ms                                                       | 822 ms: 1.16x slower                                                 |
| sympy_sum                  | 210 ms                                                       | 246 ms: 1.17x slower                                                 |
| scimark_fft                | 473 ms                                                       | 555 ms: 1.17x slower                                                 |
| json_loads                 | 34.3 us                                                      | 40.2 us: 1.17x slower                                                |
| 2to3                       | 445 ms                                                       | 526 ms: 1.18x slower                                                 |
| typing_runtime_protocols   | 226 us                                                       | 269 us: 1.19x slower                                                 |
| generators                 | 40.0 ms                                                      | 48.0 ms: 1.20x slower                                                |
| deepcopy_memo              | 50.1 us                                                      | 60.6 us: 1.21x slower                                                |
| xml_etree_generate         | 122 ms                                                       | 148 ms: 1.21x slower                                                 |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 1.03 sec: 1.21x slower                                               |
| sympy_expand               | 601 ms                                                       | 729 ms: 1.21x slower                                                 |
| fannkuch                   | 547 ms                                                       | 670 ms: 1.23x slower                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 5.02 us: 1.23x slower                                                |
| thrift                     | 1.10 ms                                                      | 1.35 ms: 1.23x slower                                                |
| bpe_tokeniser              | 6.28 sec                                                     | 7.74 sec: 1.23x slower                                               |
| async_tree_none_tg         | 504 ms                                                       | 620 ms: 1.23x slower                                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 827 ms: 1.23x slower                                                 |
| crypto_pyaes               | 100 ms                                                       | 126 ms: 1.26x slower                                                 |
| bench_thread_pool          | 2.89 ms                                                      | 3.64 ms: 1.26x slower                                                |
| spectral_norm              | 157 ms                                                       | 198 ms: 1.26x slower                                                 |
| json_dumps                 | 14.1 ms                                                      | 17.8 ms: 1.26x slower                                                |
| xml_etree_process          | 85.9 ms                                                      | 110 ms: 1.28x slower                                                 |
| richards                   | 65.5 ms                                                      | 84.3 ms: 1.29x slower                                                |
| tomli_loads                | 2.78 sec                                                     | 3.60 sec: 1.30x slower                                               |
| genshi_xml                 | 72.1 ms                                                      | 94.1 ms: 1.31x slower                                                |
| coroutines                 | 30.9 ms                                                      | 40.5 ms: 1.31x slower                                                |
| json                       | 6.51 ms                                                      | 8.58 ms: 1.32x slower                                                |
| pycparser                  | 1.57 sec                                                     | 2.07 sec: 1.32x slower                                               |
| sqlglot_optimize           | 74.7 ms                                                      | 99.9 ms: 1.34x slower                                                |
| genshi_text                | 31.7 ms                                                      | 43.1 ms: 1.36x slower                                                |
| pprint_safe_repr           | 987 ms                                                       | 1.36 sec: 1.38x slower                                               |
| html5lib                   | 92.6 ms                                                      | 128 ms: 1.38x slower                                                 |
| regex_compile              | 182 ms                                                       | 252 ms: 1.38x slower                                                 |
| pprint_pformat             | 1.94 sec                                                     | 2.69 sec: 1.39x slower                                               |
| sqlglot_normalize          | 140 ms                                                       | 196 ms: 1.40x slower                                                 |
| pyflate                    | 664 ms                                                       | 934 ms: 1.41x slower                                                 |
| bench_mp_pool              | 18.7 ms                                                      | 26.3 ms: 1.41x slower                                                |
| comprehensions             | 22.2 us                                                      | 31.3 us: 1.41x slower                                                |
| float                      | 116 ms                                                       | 169 ms: 1.46x slower                                                 |
| scimark_monte_carlo        | 90.6 ms                                                      | 134 ms: 1.48x slower                                                 |
| django_template            | 44.3 ms                                                      | 65.8 ms: 1.49x slower                                                |
| unpickle_pure_python       | 290 us                                                       | 434 us: 1.50x slower                                                 |
| mako                       | 15.9 ms                                                      | 24.1 ms: 1.51x slower                                                |
| go                         | 191 ms                                                       | 291 ms: 1.52x slower                                                 |
| logging_simple             | 8.56 us                                                      | 13.3 us: 1.55x slower                                                |
| chaos                      | 83.6 ms                                                      | 133 ms: 1.59x slower                                                 |
| logging_format             | 9.24 us                                                      | 14.8 us: 1.60x slower                                                |
| richards_super             | 73.2 ms                                                      | 117 ms: 1.60x slower                                                 |
| nbody                      | 119 ms                                                       | 191 ms: 1.61x slower                                                 |
| scimark_sor                | 179 ms                                                       | 290 ms: 1.63x slower                                                 |
| sqlglot_parse              | 1.76 ms                                                      | 2.87 ms: 1.63x slower                                                |
| sqlglot_transpile          | 2.20 ms                                                      | 3.62 ms: 1.65x slower                                                |
| logging_silent             | 130 ns                                                       | 218 ns: 1.68x slower                                                 |
| raytrace                   | 344 ms                                                       | 605 ms: 1.76x slower                                                 |
| scimark_lu                 | 146 ms                                                       | 259 ms: 1.77x slower                                                 |
| pickle_pure_python         | 416 us                                                       | 755 us: 1.81x slower                                                 |
| hexiom                     | 8.11 ms                                                      | 15.0 ms: 1.85x slower                                                |
| deltablue                  | 4.44 ms                                                      | 9.49 ms: 2.14x slower                                                |
| Geometric mean             | (ref)                                                        | 1.25x slower                                                         |

Benchmark hidden because not significant (8): asyncio_websockets, deepcopy, xml_etree_parse, pickle_list, pickle_dict, pathlib, python_startup_no_site, sqlite_synth
Ignored benchmarks (6) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.18x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.16x

# Memory
- memory change: 1.00x