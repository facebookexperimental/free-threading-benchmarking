# Results vs. 3.12.0b1

- fork: mpage
- ref: gh_115999_measure_sp
- machine: linux-x86_64
- commit hash: aa5b4de
- commit date: 2024-09-04
- overall geometric mean: 1.18x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.87x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 444 ms                                                                | 526 ms: 1.18x slower                                                 |
| docutils       | 4.06 sec                                                              | 4.57 sec: 1.13x slower                                               |
| html5lib       | 95.8 ms                                                               | 128 ms: 1.33x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.17x slower                                                         |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_memoization     | 949 ms                                                                | 822 ms: 1.15x faster                                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 983 ms: 1.15x faster                                                 |
| async_tree_io              | 1.79 sec                                                              | 1.58 sec: 1.13x faster                                               |
| async_tree_memoization_tg  | 935 ms                                                                | 827 ms: 1.13x faster                                                 |
| async_tree_none            | 740 ms                                                                | 656 ms: 1.13x faster                                                 |
| async_tree_none_tg         | 692 ms                                                                | 620 ms: 1.12x faster                                                 |
| async_tree_io_tg           | 1.80 sec                                                              | 1.62 sec: 1.11x faster                                               |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 1.03 sec: 1.06x faster                                               |
| asyncio_tcp                | 958 ms                                                                | 997 ms: 1.04x slower                                                 |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 2.93 sec: 1.05x slower                                               |
| coroutines                 | 30.1 ms                                                               | 40.5 ms: 1.34x slower                                                |
| Geometric mean             | (ref)                                                                 | 1.04x faster                                                         |

Benchmark hidden because not significant (2): asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 255 ms                                                                | 266 ms: 1.05x slower                                                 |
| float          | 127 ms                                                                | 169 ms: 1.33x slower                                                 |
| nbody          | 125 ms                                                                | 191 ms: 1.54x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.29x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 4.97 ms                                                               | 5.30 ms: 1.07x slower                                                |
| regex_v8       | 31.1 ms                                                               | 36.1 ms: 1.16x slower                                                |
| regex_compile  | 197 ms                                                                | 252 ms: 1.28x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.13x slower                                                         |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 157 ms                                                                | 164 ms: 1.04x slower                                                 |
| pickle               | 14.8 us                                                               | 16.0 us: 1.08x slower                                                |
| pickle_list          | 6.40 us                                                               | 6.97 us: 1.09x slower                                                |
| json_loads           | 36.6 us                                                               | 40.2 us: 1.10x slower                                                |
| xml_etree_generate   | 128 ms                                                                | 148 ms: 1.15x slower                                                 |
| tomli_loads          | 2.99 sec                                                              | 3.60 sec: 1.21x slower                                               |
| xml_etree_process    | 85.7 ms                                                               | 110 ms: 1.28x slower                                                 |
| json_dumps           | 13.6 ms                                                               | 17.8 ms: 1.31x slower                                                |
| unpickle_pure_python | 319 us                                                                | 434 us: 1.36x slower                                                 |
| pickle_pure_python   | 447 us                                                                | 755 us: 1.69x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.15x slower                                                         |

Benchmark hidden because not significant (4): unpickle_list, unpickle, xml_etree_parse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup | 21.2 ms                                                               | 23.4 ms: 1.10x slower                                                |
| Geometric mean | (ref)                                                                 | 1.03x slower                                                         |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                               | 94.1 ms: 1.28x slower                                                |
| genshi_text     | 31.9 ms                                                               | 43.1 ms: 1.35x slower                                                |
| django_template | 48.6 ms                                                               | 65.8 ms: 1.35x slower                                                |
| mako            | 17.2 ms                                                               | 24.1 ms: 1.40x slower                                                |
| Geometric mean  | (ref)                                                                 | 1.35x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_memoization     | 949 ms                                                                | 822 ms: 1.15x faster                                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 983 ms: 1.15x faster                                                 |
| async_tree_io              | 1.79 sec                                                              | 1.58 sec: 1.13x faster                                               |
| async_tree_memoization_tg  | 935 ms                                                                | 827 ms: 1.13x faster                                                 |
| async_tree_none            | 740 ms                                                                | 656 ms: 1.13x faster                                                 |
| async_tree_none_tg         | 692 ms                                                                | 620 ms: 1.12x faster                                                 |
| async_tree_io_tg           | 1.80 sec                                                              | 1.62 sec: 1.11x faster                                               |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 1.03 sec: 1.06x faster                                               |
| unpack_sequence            | 68.5 ns                                                               | 65.7 ns: 1.04x faster                                                |
| mdp                        | 3.84 sec                                                              | 3.96 sec: 1.03x slower                                               |
| asyncio_tcp                | 958 ms                                                                | 997 ms: 1.04x slower                                                 |
| xml_etree_iterparse        | 157 ms                                                                | 164 ms: 1.04x slower                                                 |
| pidigits                   | 255 ms                                                                | 266 ms: 1.05x slower                                                 |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 2.93 sec: 1.05x slower                                               |
| sympy_expand               | 689 ms                                                                | 729 ms: 1.06x slower                                                 |
| comprehensions             | 29.6 us                                                               | 31.3 us: 1.06x slower                                                |
| meteor_contest             | 149 ms                                                                | 158 ms: 1.06x slower                                                 |
| regex_effbot               | 4.97 ms                                                               | 5.30 ms: 1.07x slower                                                |
| sympy_sum                  | 229 ms                                                                | 246 ms: 1.07x slower                                                 |
| pickle                     | 14.8 us                                                               | 16.0 us: 1.08x slower                                                |
| sympy_integrate            | 31.4 ms                                                               | 34.0 ms: 1.08x slower                                                |
| gc_traversal               | 5.61 ms                                                               | 6.09 ms: 1.09x slower                                                |
| pickle_list                | 6.40 us                                                               | 6.97 us: 1.09x slower                                                |
| sqlite_synth               | 3.75 us                                                               | 4.11 us: 1.10x slower                                                |
| json_loads                 | 36.6 us                                                               | 40.2 us: 1.10x slower                                                |
| python_startup             | 21.2 ms                                                               | 23.4 ms: 1.10x slower                                                |
| scimark_fft                | 499 ms                                                                | 555 ms: 1.11x slower                                                 |
| docutils                   | 4.06 sec                                                              | 4.57 sec: 1.13x slower                                               |
| deepcopy_reduce            | 4.45 us                                                               | 5.02 us: 1.13x slower                                                |
| crypto_pyaes               | 112 ms                                                                | 126 ms: 1.13x slower                                                 |
| nqueens                    | 110 ms                                                                | 125 ms: 1.14x slower                                                 |
| coverage                   | 97.6 ms                                                               | 112 ms: 1.15x slower                                                 |
| xml_etree_generate         | 128 ms                                                                | 148 ms: 1.15x slower                                                 |
| thrift                     | 1.17 ms                                                               | 1.35 ms: 1.15x slower                                                |
| regex_v8                   | 31.1 ms                                                               | 36.1 ms: 1.16x slower                                                |
| bpe_tokeniser              | 6.63 sec                                                              | 7.74 sec: 1.17x slower                                               |
| telco                      | 9.71 ms                                                               | 11.4 ms: 1.17x slower                                                |
| bench_thread_pool          | 3.11 ms                                                               | 3.64 ms: 1.17x slower                                                |
| 2to3                       | 444 ms                                                                | 526 ms: 1.18x slower                                                 |
| pycparser                  | 1.73 sec                                                              | 2.07 sec: 1.19x slower                                               |
| tomli_loads                | 2.99 sec                                                              | 3.60 sec: 1.21x slower                                               |
| fannkuch                   | 551 ms                                                                | 670 ms: 1.22x slower                                                 |
| logging_format             | 11.8 us                                                               | 14.8 us: 1.25x slower                                                |
| spectral_norm              | 158 ms                                                                | 198 ms: 1.25x slower                                                 |
| genshi_xml                 | 73.6 ms                                                               | 94.1 ms: 1.28x slower                                                |
| regex_compile              | 197 ms                                                                | 252 ms: 1.28x slower                                                 |
| xml_etree_process          | 85.7 ms                                                               | 110 ms: 1.28x slower                                                 |
| json                       | 6.68 ms                                                               | 8.58 ms: 1.28x slower                                                |
| sqlglot_optimize           | 76.5 ms                                                               | 99.9 ms: 1.31x slower                                                |
| create_gc_cycles           | 2.02 ms                                                               | 2.65 ms: 1.31x slower                                                |
| json_dumps                 | 13.6 ms                                                               | 17.8 ms: 1.31x slower                                                |
| sqlglot_normalize          | 148 ms                                                                | 196 ms: 1.32x slower                                                 |
| richards                   | 63.4 ms                                                               | 84.3 ms: 1.33x slower                                                |
| pprint_pformat             | 2.03 sec                                                              | 2.69 sec: 1.33x slower                                               |
| float                      | 127 ms                                                                | 169 ms: 1.33x slower                                                 |
| html5lib                   | 95.8 ms                                                               | 128 ms: 1.33x slower                                                 |
| logging_simple             | 9.89 us                                                               | 13.3 us: 1.34x slower                                                |
| coroutines                 | 30.1 ms                                                               | 40.5 ms: 1.34x slower                                                |
| typing_runtime_protocols   | 199 us                                                                | 269 us: 1.35x slower                                                 |
| genshi_text                | 31.9 ms                                                               | 43.1 ms: 1.35x slower                                                |
| django_template            | 48.6 ms                                                               | 65.8 ms: 1.35x slower                                                |
| scimark_monte_carlo        | 98.5 ms                                                               | 134 ms: 1.36x slower                                                 |
| unpickle_pure_python       | 319 us                                                                | 434 us: 1.36x slower                                                 |
| pprint_safe_repr           | 970 ms                                                                | 1.36 sec: 1.40x slower                                               |
| mako                       | 17.2 ms                                                               | 24.1 ms: 1.40x slower                                                |
| pyflate                    | 661 ms                                                                | 934 ms: 1.41x slower                                                 |
| chaos                      | 93.7 ms                                                               | 133 ms: 1.42x slower                                                 |
| bench_mp_pool              | 18.4 ms                                                               | 26.3 ms: 1.43x slower                                                |
| raytrace                   | 418 ms                                                                | 605 ms: 1.45x slower                                                 |
| sqlglot_parse              | 1.89 ms                                                               | 2.87 ms: 1.51x slower                                                |
| nbody                      | 125 ms                                                                | 191 ms: 1.54x slower                                                 |
| go                         | 185 ms                                                                | 291 ms: 1.57x slower                                                 |
| sqlglot_transpile          | 2.28 ms                                                               | 3.62 ms: 1.59x slower                                                |
| logging_silent             | 135 ns                                                                | 218 ns: 1.61x slower                                                 |
| scimark_lu                 | 155 ms                                                                | 259 ms: 1.67x slower                                                 |
| pickle_pure_python         | 447 us                                                                | 755 us: 1.69x slower                                                 |
| hexiom                     | 8.87 ms                                                               | 15.0 ms: 1.69x slower                                                |
| scimark_sor                | 171 ms                                                                | 290 ms: 1.70x slower                                                 |
| richards_super             | 67.9 ms                                                               | 117 ms: 1.72x slower                                                 |
| deltablue                  | 5.05 ms                                                               | 9.49 ms: 1.88x slower                                                |
| Geometric mean             | (ref)                                                                 | 1.18x slower                                                         |

Benchmark hidden because not significant (16): pathlib, python_startup_no_site, unpickle_list, unpickle, asyncio_websockets, deepcopy, sympy_str, scimark_sparse_mat_mult, async_generators, xml_etree_parse, regex_dna, pickle_dict, generators, deepcopy_memo, tornado_http, pylint
Ignored benchmarks (9) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.87x