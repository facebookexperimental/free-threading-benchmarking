# Results vs. 3.12.0b1

- fork: mpage
- ref: f4d1deda87c7c7bcf4b1
- machine: linux-x86_64
- commit hash: f4d1ded
- commit date: 2024-09-04
- overall geometric mean: 1.20x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.87x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 444 ms                                                                | 546 ms: 1.23x slower                                                 |
| docutils       | 4.06 sec                                                              | 4.52 sec: 1.11x slower                                               |
| html5lib       | 95.8 ms                                                               | 130 ms: 1.36x slower                                                 |
| tornado_http   | 262 ms                                                                | 334 ms: 1.27x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.24x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_memoization_tg  | 935 ms                                                                | 760 ms: 1.23x faster                                                 |
| async_tree_memoization     | 949 ms                                                                | 809 ms: 1.17x faster                                                 |
| async_tree_none            | 740 ms                                                                | 636 ms: 1.16x faster                                                 |
| async_tree_io_tg           | 1.80 sec                                                              | 1.56 sec: 1.16x faster                                               |
| async_tree_io              | 1.79 sec                                                              | 1.55 sec: 1.15x faster                                               |
| async_tree_none_tg         | 692 ms                                                                | 609 ms: 1.14x faster                                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 1.01 sec: 1.12x faster                                               |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 1.01 sec: 1.09x faster                                               |
| async_generators           | 617 ms                                                                | 637 ms: 1.03x slower                                                 |
| coroutines                 | 30.1 ms                                                               | 38.7 ms: 1.28x slower                                                |
| Geometric mean             | (ref)                                                                 | 1.07x faster                                                         |

Benchmark hidden because not significant (3): asyncio_websockets, asyncio_tcp_ssl, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 127 ms                                                                | 171 ms: 1.35x slower                                                 |
| nbody          | 125 ms                                                                | 226 ms: 1.81x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.34x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 287 ms                                                                | 304 ms: 1.06x slower                                                 |
| regex_v8       | 31.1 ms                                                               | 38.6 ms: 1.24x slower                                                |
| regex_compile  | 197 ms                                                                | 253 ms: 1.28x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.13x slower                                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_dict          | 46.5 us                                                               | 45.2 us: 1.03x faster                                                |
| pickle_list          | 6.40 us                                                               | 6.68 us: 1.04x slower                                                |
| xml_etree_generate   | 128 ms                                                                | 142 ms: 1.10x slower                                                 |
| json_loads           | 36.6 us                                                               | 40.3 us: 1.10x slower                                                |
| json_dumps           | 13.6 ms                                                               | 16.8 ms: 1.23x slower                                                |
| xml_etree_iterparse  | 157 ms                                                                | 196 ms: 1.25x slower                                                 |
| tomli_loads          | 2.99 sec                                                              | 3.74 sec: 1.25x slower                                               |
| xml_etree_process    | 85.7 ms                                                               | 110 ms: 1.28x slower                                                 |
| unpickle_pure_python | 319 us                                                                | 461 us: 1.45x slower                                                 |
| pickle_pure_python   | 447 us                                                                | 673 us: 1.50x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.15x slower                                                         |

Benchmark hidden because not significant (4): xml_etree_parse, unpickle, pickle, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup | 21.2 ms                                                               | 23.5 ms: 1.11x slower                                                |
| Geometric mean | (ref)                                                                 | 1.05x slower                                                         |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 17.2 ms                                                               | 22.5 ms: 1.31x slower                                                |
| django_template | 48.6 ms                                                               | 64.3 ms: 1.32x slower                                                |
| genshi_text     | 31.9 ms                                                               | 43.7 ms: 1.37x slower                                                |
| genshi_xml      | 73.6 ms                                                               | 101 ms: 1.38x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.34x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_memoization_tg  | 935 ms                                                                | 760 ms: 1.23x faster                                                 |
| async_tree_memoization     | 949 ms                                                                | 809 ms: 1.17x faster                                                 |
| async_tree_none            | 740 ms                                                                | 636 ms: 1.16x faster                                                 |
| async_tree_io_tg           | 1.80 sec                                                              | 1.56 sec: 1.16x faster                                               |
| async_tree_io              | 1.79 sec                                                              | 1.55 sec: 1.15x faster                                               |
| async_tree_none_tg         | 692 ms                                                                | 609 ms: 1.14x faster                                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 1.01 sec: 1.12x faster                                               |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 1.01 sec: 1.09x faster                                               |
| deepcopy_memo              | 57.5 us                                                               | 53.1 us: 1.08x faster                                                |
| pickle_dict                | 46.5 us                                                               | 45.2 us: 1.03x faster                                                |
| async_generators           | 617 ms                                                                | 637 ms: 1.03x slower                                                 |
| pickle_list                | 6.40 us                                                               | 6.68 us: 1.04x slower                                                |
| comprehensions             | 29.6 us                                                               | 31.0 us: 1.05x slower                                                |
| generators                 | 46.0 ms                                                               | 48.5 ms: 1.05x slower                                                |
| regex_dna                  | 287 ms                                                                | 304 ms: 1.06x slower                                                 |
| mdp                        | 3.84 sec                                                              | 4.07 sec: 1.06x slower                                               |
| pathlib                    | 31.7 ms                                                               | 33.7 ms: 1.06x slower                                                |
| sympy_expand               | 689 ms                                                                | 742 ms: 1.08x slower                                                 |
| scimark_fft                | 499 ms                                                                | 538 ms: 1.08x slower                                                 |
| xml_etree_generate         | 128 ms                                                                | 142 ms: 1.10x slower                                                 |
| json_loads                 | 36.6 us                                                               | 40.3 us: 1.10x slower                                                |
| python_startup             | 21.2 ms                                                               | 23.5 ms: 1.11x slower                                                |
| docutils                   | 4.06 sec                                                              | 4.52 sec: 1.11x slower                                               |
| sympy_integrate            | 31.4 ms                                                               | 35.0 ms: 1.12x slower                                                |
| pylint                     | 501 ms                                                                | 563 ms: 1.12x slower                                                 |
| meteor_contest             | 149 ms                                                                | 168 ms: 1.13x slower                                                 |
| sympy_str                  | 425 ms                                                                | 480 ms: 1.13x slower                                                 |
| sympy_sum                  | 229 ms                                                                | 260 ms: 1.14x slower                                                 |
| bpe_tokeniser              | 6.63 sec                                                              | 7.57 sec: 1.14x slower                                               |
| json                       | 6.68 ms                                                               | 7.67 ms: 1.15x slower                                                |
| gc_traversal               | 5.61 ms                                                               | 6.46 ms: 1.15x slower                                                |
| coverage                   | 97.6 ms                                                               | 114 ms: 1.17x slower                                                 |
| create_gc_cycles           | 2.02 ms                                                               | 2.37 ms: 1.17x slower                                                |
| sqlite_synth               | 3.75 us                                                               | 4.40 us: 1.17x slower                                                |
| pycparser                  | 1.73 sec                                                              | 2.06 sec: 1.19x slower                                               |
| crypto_pyaes               | 112 ms                                                                | 137 ms: 1.23x slower                                                 |
| 2to3                       | 444 ms                                                                | 546 ms: 1.23x slower                                                 |
| json_dumps                 | 13.6 ms                                                               | 16.8 ms: 1.23x slower                                                |
| nqueens                    | 110 ms                                                                | 136 ms: 1.24x slower                                                 |
| thrift                     | 1.17 ms                                                               | 1.45 ms: 1.24x slower                                                |
| telco                      | 9.71 ms                                                               | 12.0 ms: 1.24x slower                                                |
| regex_v8                   | 31.1 ms                                                               | 38.6 ms: 1.24x slower                                                |
| xml_etree_iterparse        | 157 ms                                                                | 196 ms: 1.25x slower                                                 |
| fannkuch                   | 551 ms                                                                | 688 ms: 1.25x slower                                                 |
| tomli_loads                | 2.99 sec                                                              | 3.74 sec: 1.25x slower                                               |
| bench_mp_pool              | 18.4 ms                                                               | 23.1 ms: 1.26x slower                                                |
| tornado_http               | 262 ms                                                                | 334 ms: 1.27x slower                                                 |
| xml_etree_process          | 85.7 ms                                                               | 110 ms: 1.28x slower                                                 |
| regex_compile              | 197 ms                                                                | 253 ms: 1.28x slower                                                 |
| coroutines                 | 30.1 ms                                                               | 38.7 ms: 1.28x slower                                                |
| logging_format             | 11.8 us                                                               | 15.4 us: 1.30x slower                                                |
| logging_simple             | 9.89 us                                                               | 12.9 us: 1.30x slower                                                |
| mako                       | 17.2 ms                                                               | 22.5 ms: 1.31x slower                                                |
| django_template            | 48.6 ms                                                               | 64.3 ms: 1.32x slower                                                |
| bench_thread_pool          | 3.11 ms                                                               | 4.17 ms: 1.34x slower                                                |
| float                      | 127 ms                                                                | 171 ms: 1.35x slower                                                 |
| html5lib                   | 95.8 ms                                                               | 130 ms: 1.36x slower                                                 |
| pprint_pformat             | 2.03 sec                                                              | 2.76 sec: 1.36x slower                                               |
| spectral_norm              | 158 ms                                                                | 216 ms: 1.37x slower                                                 |
| genshi_text                | 31.9 ms                                                               | 43.7 ms: 1.37x slower                                                |
| chaos                      | 93.7 ms                                                               | 129 ms: 1.38x slower                                                 |
| genshi_xml                 | 73.6 ms                                                               | 101 ms: 1.38x slower                                                 |
| sqlglot_normalize          | 148 ms                                                                | 205 ms: 1.38x slower                                                 |
| typing_runtime_protocols   | 199 us                                                                | 275 us: 1.38x slower                                                 |
| sqlglot_optimize           | 76.5 ms                                                               | 106 ms: 1.39x slower                                                 |
| richards                   | 63.4 ms                                                               | 90.4 ms: 1.42x slower                                                |
| pprint_safe_repr           | 970 ms                                                                | 1.39 sec: 1.44x slower                                               |
| unpickle_pure_python       | 319 us                                                                | 461 us: 1.45x slower                                                 |
| raytrace                   | 418 ms                                                                | 608 ms: 1.45x slower                                                 |
| pyflate                    | 661 ms                                                                | 961 ms: 1.45x slower                                                 |
| scimark_monte_carlo        | 98.5 ms                                                               | 147 ms: 1.49x slower                                                 |
| pickle_pure_python         | 447 us                                                                | 673 us: 1.50x slower                                                 |
| sqlglot_parse              | 1.89 ms                                                               | 2.93 ms: 1.55x slower                                                |
| hexiom                     | 8.87 ms                                                               | 13.9 ms: 1.56x slower                                                |
| logging_silent             | 135 ns                                                                | 214 ns: 1.58x slower                                                 |
| sqlglot_transpile          | 2.28 ms                                                               | 3.66 ms: 1.60x slower                                                |
| go                         | 185 ms                                                                | 298 ms: 1.61x slower                                                 |
| richards_super             | 67.9 ms                                                               | 111 ms: 1.64x slower                                                 |
| scimark_lu                 | 155 ms                                                                | 261 ms: 1.68x slower                                                 |
| scimark_sor                | 171 ms                                                                | 304 ms: 1.77x slower                                                 |
| deltablue                  | 5.05 ms                                                               | 9.01 ms: 1.78x slower                                                |
| nbody                      | 125 ms                                                                | 226 ms: 1.81x slower                                                 |
| unpack_sequence            | 68.5 ns                                                               | 149 ns: 2.17x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.20x slower                                                         |

Benchmark hidden because not significant (13): deepcopy, xml_etree_parse, regex_effbot, pidigits, unpickle, asyncio_websockets, asyncio_tcp_ssl, scimark_sparse_mat_mult, python_startup_no_site, deepcopy_reduce, pickle, asyncio_tcp, unpickle_list
Ignored benchmarks (9) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.87x