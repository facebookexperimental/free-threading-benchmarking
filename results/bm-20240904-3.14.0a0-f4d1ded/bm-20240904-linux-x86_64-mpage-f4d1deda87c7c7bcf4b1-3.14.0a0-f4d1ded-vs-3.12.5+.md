# Results vs. 3.12.5+

- fork: mpage
- ref: f4d1deda87c7c7bcf4b1
- machine: linux-x86_64
- commit hash: f4d1ded
- commit date: 2024-09-04
- overall geometric mean: 1.21x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 456 ms                                               | 546 ms: 1.20x slower                                                 |
| docutils       | 4.05 sec                                             | 4.52 sec: 1.12x slower                                               |
| html5lib       | 100 ms                                               | 130 ms: 1.30x slower                                                 |
| tornado_http   | 261 ms                                               | 334 ms: 1.28x slower                                                 |
| Geometric mean | (ref)                                                | 1.22x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 636 ms: 1.29x faster                                                 |
| async_tree_memoization     | 975 ms                                               | 809 ms: 1.21x faster                                                 |
| async_tree_memoization_tg  | 912 ms                                               | 760 ms: 1.20x faster                                                 |
| async_tree_io_tg           | 1.87 sec                                             | 1.56 sec: 1.20x faster                                               |
| async_tree_io              | 1.86 sec                                             | 1.55 sec: 1.20x faster                                               |
| async_tree_none_tg         | 726 ms                                               | 609 ms: 1.19x faster                                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 1.01 sec: 1.13x faster                                               |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 1.01 sec: 1.11x faster                                               |
| asyncio_tcp_ssl            | 2.82 sec                                             | 2.75 sec: 1.02x faster                                               |
| async_generators           | 615 ms                                               | 637 ms: 1.04x slower                                                 |
| coroutines                 | 30.6 ms                                              | 38.7 ms: 1.26x slower                                                |
| Geometric mean             | (ref)                                                | 1.09x faster                                                         |

Benchmark hidden because not significant (2): asyncio_tcp, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 124 ms                                               | 171 ms: 1.38x slower                                                 |
| nbody          | 117 ms                                               | 226 ms: 1.94x slower                                                 |
| Geometric mean | (ref)                                                | 1.37x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 268 ms                                               | 304 ms: 1.13x slower                                                 |
| regex_v8       | 29.9 ms                                              | 38.6 ms: 1.29x slower                                                |
| regex_compile  | 186 ms                                               | 253 ms: 1.36x slower                                                 |
| Geometric mean | (ref)                                                | 1.18x slower                                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle             | 21.6 us                                              | 19.4 us: 1.12x faster                                                |
| xml_etree_parse      | 244 ms                                               | 223 ms: 1.09x faster                                                 |
| pickle               | 15.9 us                                              | 15.0 us: 1.06x faster                                                |
| pickle_list          | 7.01 us                                              | 6.68 us: 1.05x faster                                                |
| unpickle_list        | 6.83 us                                              | 7.52 us: 1.10x slower                                                |
| json_loads           | 35.9 us                                              | 40.3 us: 1.12x slower                                                |
| xml_etree_iterparse  | 173 ms                                               | 196 ms: 1.14x slower                                                 |
| json_dumps           | 14.0 ms                                              | 16.8 ms: 1.20x slower                                                |
| tomli_loads          | 2.86 sec                                             | 3.74 sec: 1.31x slower                                               |
| xml_etree_process    | 82.7 ms                                              | 110 ms: 1.33x slower                                                 |
| unpickle_pure_python | 304 us                                               | 461 us: 1.52x slower                                                 |
| pickle_pure_python   | 436 us                                               | 673 us: 1.54x slower                                                 |
| Geometric mean       | (ref)                                                | 1.12x slower                                                         |

Benchmark hidden because not significant (2): pickle_dict, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup | 22.7 ms                                              | 23.5 ms: 1.04x slower                                                |
| Geometric mean | (ref)                                                | 1.02x slower                                                         |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|-----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 16.1 ms                                              | 22.5 ms: 1.40x slower                                                |
| django_template | 45.4 ms                                              | 64.3 ms: 1.42x slower                                                |
| genshi_text     | 30.3 ms                                              | 43.7 ms: 1.44x slower                                                |
| genshi_xml      | 69.1 ms                                              | 101 ms: 1.47x slower                                                 |
| Geometric mean  | (ref)                                                | 1.43x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 636 ms: 1.29x faster                                                 |
| async_tree_memoization     | 975 ms                                               | 809 ms: 1.21x faster                                                 |
| async_tree_memoization_tg  | 912 ms                                               | 760 ms: 1.20x faster                                                 |
| async_tree_io_tg           | 1.87 sec                                             | 1.56 sec: 1.20x faster                                               |
| async_tree_io              | 1.86 sec                                             | 1.55 sec: 1.20x faster                                               |
| async_tree_none_tg         | 726 ms                                               | 609 ms: 1.19x faster                                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 1.01 sec: 1.13x faster                                               |
| unpickle                   | 21.6 us                                              | 19.4 us: 1.12x faster                                                |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 1.01 sec: 1.11x faster                                               |
| xml_etree_parse            | 244 ms                                               | 223 ms: 1.09x faster                                                 |
| pickle                     | 15.9 us                                              | 15.0 us: 1.06x faster                                                |
| pickle_list                | 7.01 us                                              | 6.68 us: 1.05x faster                                                |
| asyncio_tcp_ssl            | 2.82 sec                                             | 2.75 sec: 1.02x faster                                               |
| async_generators           | 615 ms                                               | 637 ms: 1.04x slower                                                 |
| python_startup             | 22.7 ms                                              | 23.5 ms: 1.04x slower                                                |
| pathlib                    | 31.6 ms                                              | 33.7 ms: 1.07x slower                                                |
| deepcopy_reduce            | 4.18 us                                              | 4.47 us: 1.07x slower                                                |
| json                       | 7.14 ms                                              | 7.67 ms: 1.07x slower                                                |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 7.49 ms: 1.08x slower                                                |
| mdp                        | 3.77 sec                                             | 4.07 sec: 1.08x slower                                               |
| comprehensions             | 28.6 us                                              | 31.0 us: 1.08x slower                                                |
| generators                 | 44.7 ms                                              | 48.5 ms: 1.08x slower                                                |
| bench_mp_pool              | 21.2 ms                                              | 23.1 ms: 1.09x slower                                                |
| unpickle_list              | 6.83 us                                              | 7.52 us: 1.10x slower                                                |
| docutils                   | 4.05 sec                                             | 4.52 sec: 1.12x slower                                               |
| scimark_fft                | 481 ms                                               | 538 ms: 1.12x slower                                                 |
| bpe_tokeniser              | 6.76 sec                                             | 7.57 sec: 1.12x slower                                               |
| json_loads                 | 35.9 us                                              | 40.3 us: 1.12x slower                                                |
| regex_dna                  | 268 ms                                               | 304 ms: 1.13x slower                                                 |
| xml_etree_iterparse        | 173 ms                                               | 196 ms: 1.14x slower                                                 |
| meteor_contest             | 146 ms                                               | 168 ms: 1.15x slower                                                 |
| sqlite_synth               | 3.77 us                                              | 4.40 us: 1.17x slower                                                |
| pylint                     | 480 ms                                               | 563 ms: 1.17x slower                                                 |
| nqueens                    | 116 ms                                               | 136 ms: 1.18x slower                                                 |
| coverage                   | 96.9 ms                                              | 114 ms: 1.18x slower                                                 |
| create_gc_cycles           | 2.00 ms                                              | 2.37 ms: 1.18x slower                                                |
| sympy_sum                  | 218 ms                                               | 260 ms: 1.19x slower                                                 |
| json_dumps                 | 14.0 ms                                              | 16.8 ms: 1.20x slower                                                |
| 2to3                       | 456 ms                                               | 546 ms: 1.20x slower                                                 |
| sympy_integrate            | 29.0 ms                                              | 35.0 ms: 1.21x slower                                                |
| bench_thread_pool          | 3.42 ms                                              | 4.17 ms: 1.22x slower                                                |
| pycparser                  | 1.68 sec                                             | 2.06 sec: 1.23x slower                                               |
| typing_runtime_protocols   | 224 us                                               | 275 us: 1.23x slower                                                 |
| crypto_pyaes               | 110 ms                                               | 137 ms: 1.25x slower                                                 |
| sympy_expand               | 591 ms                                               | 742 ms: 1.26x slower                                                 |
| telco                      | 9.53 ms                                              | 12.0 ms: 1.26x slower                                                |
| coroutines                 | 30.6 ms                                              | 38.7 ms: 1.26x slower                                                |
| sympy_str                  | 379 ms                                               | 480 ms: 1.27x slower                                                 |
| tornado_http               | 261 ms                                               | 334 ms: 1.28x slower                                                 |
| regex_v8                   | 29.9 ms                                              | 38.6 ms: 1.29x slower                                                |
| html5lib                   | 100 ms                                               | 130 ms: 1.30x slower                                                 |
| tomli_loads                | 2.86 sec                                             | 3.74 sec: 1.31x slower                                               |
| fannkuch                   | 525 ms                                               | 688 ms: 1.31x slower                                                 |
| thrift                     | 1.10 ms                                              | 1.45 ms: 1.31x slower                                                |
| sqlglot_optimize           | 80.2 ms                                              | 106 ms: 1.33x slower                                                 |
| xml_etree_process          | 82.7 ms                                              | 110 ms: 1.33x slower                                                 |
| logging_simple             | 9.68 us                                              | 12.9 us: 1.33x slower                                                |
| regex_compile              | 186 ms                                               | 253 ms: 1.36x slower                                                 |
| float                      | 124 ms                                               | 171 ms: 1.38x slower                                                 |
| pprint_pformat             | 1.99 sec                                             | 2.76 sec: 1.39x slower                                               |
| mako                       | 16.1 ms                                              | 22.5 ms: 1.40x slower                                                |
| chaos                      | 92.1 ms                                              | 129 ms: 1.40x slower                                                 |
| django_template            | 45.4 ms                                              | 64.3 ms: 1.42x slower                                                |
| sqlglot_normalize          | 144 ms                                               | 205 ms: 1.42x slower                                                 |
| pprint_safe_repr           | 972 ms                                               | 1.39 sec: 1.43x slower                                               |
| richards                   | 62.8 ms                                              | 90.4 ms: 1.44x slower                                                |
| genshi_text                | 30.3 ms                                              | 43.7 ms: 1.44x slower                                                |
| pyflate                    | 664 ms                                               | 961 ms: 1.45x slower                                                 |
| genshi_xml                 | 69.1 ms                                              | 101 ms: 1.47x slower                                                 |
| raytrace                   | 405 ms                                               | 608 ms: 1.50x slower                                                 |
| unpickle_pure_python       | 304 us                                               | 461 us: 1.52x slower                                                 |
| scimark_monte_carlo        | 96.8 ms                                              | 147 ms: 1.52x slower                                                 |
| logging_silent             | 139 ns                                               | 214 ns: 1.53x slower                                                 |
| pickle_pure_python         | 436 us                                               | 673 us: 1.54x slower                                                 |
| sqlglot_transpile          | 2.32 ms                                              | 3.66 ms: 1.58x slower                                                |
| sqlglot_parse              | 1.85 ms                                              | 2.93 ms: 1.58x slower                                                |
| spectral_norm              | 136 ms                                               | 216 ms: 1.58x slower                                                 |
| richards_super             | 69.7 ms                                              | 111 ms: 1.60x slower                                                 |
| logging_format             | 9.56 us                                              | 15.4 us: 1.61x slower                                                |
| scimark_lu                 | 155 ms                                               | 261 ms: 1.68x slower                                                 |
| hexiom                     | 8.19 ms                                              | 13.9 ms: 1.69x slower                                                |
| go                         | 173 ms                                               | 298 ms: 1.72x slower                                                 |
| scimark_sor                | 170 ms                                               | 304 ms: 1.78x slower                                                 |
| nbody                      | 117 ms                                               | 226 ms: 1.94x slower                                                 |
| deltablue                  | 4.45 ms                                              | 9.01 ms: 2.02x slower                                                |
| unpack_sequence            | 70.8 ns                                              | 149 ns: 2.10x slower                                                 |
| Geometric mean             | (ref)                                                | 1.21x slower                                                         |

Benchmark hidden because not significant (10): regex_effbot, pidigits, asyncio_tcp, pickle_dict, asyncio_websockets, deepcopy, python_startup_no_site, gc_traversal, xml_etree_generate, deepcopy_memo
Ignored benchmarks (9) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.01x