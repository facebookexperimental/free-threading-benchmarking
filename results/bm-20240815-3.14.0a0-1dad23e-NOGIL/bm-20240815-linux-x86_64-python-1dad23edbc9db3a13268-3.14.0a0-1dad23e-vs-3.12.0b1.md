# Results vs. 3.12.0b1

- fork: python
- ref: 1dad23edbc9db3a13268
- machine: linux-x86_64
- commit hash: 1dad23e
- commit date: 2024-08-15
- overall geometric mean: 1.38x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 2.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 444 ms                                                                | 687 ms: 1.55x slower                                                  |
| docutils       | 4.06 sec                                                              | 5.35 sec: 1.32x slower                                                |
| html5lib       | 95.8 ms                                                               | 147 ms: 1.54x slower                                                  |
| tornado_http   | 262 ms                                                                | 350 ms: 1.33x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.43x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.14 sec: 1.58x faster                                                |
| async_tree_none_tg         | 692 ms                                                                | 490 ms: 1.41x faster                                                  |
| async_tree_io              | 1.79 sec                                                              | 1.28 sec: 1.40x faster                                                |
| async_tree_memoization_tg  | 935 ms                                                                | 672 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 836 ms: 1.32x faster                                                  |
| async_tree_memoization     | 949 ms                                                                | 774 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 926 ms: 1.23x faster                                                  |
| async_tree_none            | 740 ms                                                                | 626 ms: 1.18x faster                                                  |
| async_generators           | 617 ms                                                                | 731 ms: 1.19x slower                                                  |
| asyncio_tcp                | 958 ms                                                                | 1.16 sec: 1.21x slower                                                |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.47 sec: 1.24x slower                                                |
| coroutines                 | 30.1 ms                                                               | 42.9 ms: 1.43x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.11x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 127 ms                                                                | 195 ms: 1.54x slower                                                  |
| nbody          | 125 ms                                                                | 307 ms: 2.46x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.55x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 287 ms                                                                | 300 ms: 1.04x slower                                                  |
| regex_v8       | 31.1 ms                                                               | 36.8 ms: 1.18x slower                                                 |
| regex_compile  | 197 ms                                                                | 310 ms: 1.57x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.18x slower                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 46.5 us                                                               | 42.2 us: 1.10x faster                                                 |
| pickle               | 14.8 us                                                               | 13.8 us: 1.07x faster                                                 |
| pickle_list          | 6.40 us                                                               | 6.72 us: 1.05x slower                                                 |
| unpickle_list        | 7.19 us                                                               | 7.89 us: 1.10x slower                                                 |
| xml_etree_iterparse  | 157 ms                                                                | 176 ms: 1.12x slower                                                  |
| unpickle             | 19.7 us                                                               | 23.4 us: 1.19x slower                                                 |
| json_loads           | 36.6 us                                                               | 44.8 us: 1.22x slower                                                 |
| xml_etree_generate   | 128 ms                                                                | 167 ms: 1.30x slower                                                  |
| json_dumps           | 13.6 ms                                                               | 19.0 ms: 1.40x slower                                                 |
| tomli_loads          | 2.99 sec                                                              | 4.23 sec: 1.42x slower                                                |
| xml_etree_process    | 85.7 ms                                                               | 130 ms: 1.52x slower                                                  |
| pickle_pure_python   | 447 us                                                                | 783 us: 1.75x slower                                                  |
| unpickle_pure_python | 319 us                                                                | 578 us: 1.81x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.24x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 20.9 ms: 1.29x slower                                                 |
| python_startup         | 21.2 ms                                                               | 30.8 ms: 1.45x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                               | 124 ms: 1.69x slower                                                  |
| genshi_text     | 31.9 ms                                                               | 55.2 ms: 1.73x slower                                                 |
| django_template | 48.6 ms                                                               | 87.7 ms: 1.81x slower                                                 |
| mako            | 17.2 ms                                                               | 31.5 ms: 1.83x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.76x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.14 sec: 1.58x faster                                                |
| async_tree_none_tg         | 692 ms                                                                | 490 ms: 1.41x faster                                                  |
| async_tree_io              | 1.79 sec                                                              | 1.28 sec: 1.40x faster                                                |
| async_tree_memoization_tg  | 935 ms                                                                | 672 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 836 ms: 1.32x faster                                                  |
| async_tree_memoization     | 949 ms                                                                | 774 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 926 ms: 1.23x faster                                                  |
| async_tree_none            | 740 ms                                                                | 626 ms: 1.18x faster                                                  |
| gc_traversal               | 5.61 ms                                                               | 5.05 ms: 1.11x faster                                                 |
| pickle_dict                | 46.5 us                                                               | 42.2 us: 1.10x faster                                                 |
| create_gc_cycles           | 2.02 ms                                                               | 1.87 ms: 1.08x faster                                                 |
| pickle                     | 14.8 us                                                               | 13.8 us: 1.07x faster                                                 |
| regex_dna                  | 287 ms                                                                | 300 ms: 1.04x slower                                                  |
| pickle_list                | 6.40 us                                                               | 6.72 us: 1.05x slower                                                 |
| unpickle_list              | 7.19 us                                                               | 7.89 us: 1.10x slower                                                 |
| xml_etree_iterparse        | 157 ms                                                                | 176 ms: 1.12x slower                                                  |
| sqlite_synth               | 3.75 us                                                               | 4.29 us: 1.14x slower                                                 |
| pathlib                    | 31.7 ms                                                               | 37.4 ms: 1.18x slower                                                 |
| regex_v8                   | 31.1 ms                                                               | 36.8 ms: 1.18x slower                                                 |
| async_generators           | 617 ms                                                                | 731 ms: 1.19x slower                                                  |
| unpickle                   | 19.7 us                                                               | 23.4 us: 1.19x slower                                                 |
| asyncio_tcp                | 958 ms                                                                | 1.16 sec: 1.21x slower                                                |
| pylint                     | 501 ms                                                                | 606 ms: 1.21x slower                                                  |
| json_loads                 | 36.6 us                                                               | 44.8 us: 1.22x slower                                                 |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.47 sec: 1.24x slower                                                |
| deepcopy                   | 503 us                                                                | 626 us: 1.24x slower                                                  |
| generators                 | 46.0 ms                                                               | 58.2 ms: 1.26x slower                                                 |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 9.49 ms: 1.27x slower                                                 |
| pycparser                  | 1.73 sec                                                              | 2.23 sec: 1.28x slower                                                |
| json                       | 6.68 ms                                                               | 8.59 ms: 1.29x slower                                                 |
| python_startup_no_site     | 16.3 ms                                                               | 20.9 ms: 1.29x slower                                                 |
| xml_etree_generate         | 128 ms                                                                | 167 ms: 1.30x slower                                                  |
| scimark_fft                | 499 ms                                                                | 657 ms: 1.32x slower                                                  |
| docutils                   | 4.06 sec                                                              | 5.35 sec: 1.32x slower                                                |
| comprehensions             | 29.6 us                                                               | 39.2 us: 1.33x slower                                                 |
| tornado_http               | 262 ms                                                                | 350 ms: 1.33x slower                                                  |
| deepcopy_memo              | 57.5 us                                                               | 77.4 us: 1.35x slower                                                 |
| meteor_contest             | 149 ms                                                                | 202 ms: 1.36x slower                                                  |
| mdp                        | 3.84 sec                                                              | 5.24 sec: 1.36x slower                                                |
| json_dumps                 | 13.6 ms                                                               | 19.0 ms: 1.40x slower                                                 |
| telco                      | 9.71 ms                                                               | 13.7 ms: 1.41x slower                                                 |
| tomli_loads                | 2.99 sec                                                              | 4.23 sec: 1.42x slower                                                |
| thrift                     | 1.17 ms                                                               | 1.66 ms: 1.42x slower                                                 |
| coroutines                 | 30.1 ms                                                               | 42.9 ms: 1.43x slower                                                 |
| crypto_pyaes               | 112 ms                                                                | 161 ms: 1.44x slower                                                  |
| sympy_integrate            | 31.4 ms                                                               | 45.4 ms: 1.45x slower                                                 |
| python_startup             | 21.2 ms                                                               | 30.8 ms: 1.45x slower                                                 |
| logging_format             | 11.8 us                                                               | 17.3 us: 1.46x slower                                                 |
| fannkuch                   | 551 ms                                                                | 814 ms: 1.48x slower                                                  |
| deepcopy_reduce            | 4.45 us                                                               | 6.61 us: 1.49x slower                                                 |
| nqueens                    | 110 ms                                                                | 164 ms: 1.49x slower                                                  |
| logging_simple             | 9.89 us                                                               | 14.9 us: 1.51x slower                                                 |
| xml_etree_process          | 85.7 ms                                                               | 130 ms: 1.52x slower                                                  |
| html5lib                   | 95.8 ms                                                               | 147 ms: 1.54x slower                                                  |
| float                      | 127 ms                                                                | 195 ms: 1.54x slower                                                  |
| 2to3                       | 444 ms                                                                | 687 ms: 1.55x slower                                                  |
| spectral_norm              | 158 ms                                                                | 247 ms: 1.57x slower                                                  |
| regex_compile              | 197 ms                                                                | 310 ms: 1.57x slower                                                  |
| sqlglot_normalize          | 148 ms                                                                | 235 ms: 1.58x slower                                                  |
| sqlglot_optimize           | 76.5 ms                                                               | 122 ms: 1.59x slower                                                  |
| bpe_tokeniser              | 6.63 sec                                                              | 10.7 sec: 1.61x slower                                                |
| coverage                   | 97.6 ms                                                               | 159 ms: 1.63x slower                                                  |
| scimark_monte_carlo        | 98.5 ms                                                               | 161 ms: 1.63x slower                                                  |
| sympy_str                  | 425 ms                                                                | 697 ms: 1.64x slower                                                  |
| richards                   | 63.4 ms                                                               | 107 ms: 1.68x slower                                                  |
| genshi_xml                 | 73.6 ms                                                               | 124 ms: 1.69x slower                                                  |
| pyflate                    | 661 ms                                                                | 1.12 sec: 1.70x slower                                                |
| typing_runtime_protocols   | 199 us                                                                | 342 us: 1.71x slower                                                  |
| bench_thread_pool          | 3.11 ms                                                               | 5.33 ms: 1.71x slower                                                 |
| genshi_text                | 31.9 ms                                                               | 55.2 ms: 1.73x slower                                                 |
| pickle_pure_python         | 447 us                                                                | 783 us: 1.75x slower                                                  |
| pprint_pformat             | 2.03 sec                                                              | 3.62 sec: 1.79x slower                                                |
| django_template            | 48.6 ms                                                               | 87.7 ms: 1.81x slower                                                 |
| unpickle_pure_python       | 319 us                                                                | 578 us: 1.81x slower                                                  |
| sympy_expand               | 689 ms                                                                | 1.26 sec: 1.83x slower                                                |
| mako                       | 17.2 ms                                                               | 31.5 ms: 1.83x slower                                                 |
| pprint_safe_repr           | 970 ms                                                                | 1.80 sec: 1.85x slower                                                |
| raytrace                   | 418 ms                                                                | 789 ms: 1.89x slower                                                  |
| chaos                      | 93.7 ms                                                               | 177 ms: 1.89x slower                                                  |
| hexiom                     | 8.87 ms                                                               | 16.9 ms: 1.91x slower                                                 |
| richards_super             | 67.9 ms                                                               | 133 ms: 1.96x slower                                                  |
| logging_silent             | 135 ns                                                                | 266 ns: 1.97x slower                                                  |
| sqlglot_parse              | 1.89 ms                                                               | 3.77 ms: 1.99x slower                                                 |
| sympy_sum                  | 229 ms                                                                | 462 ms: 2.02x slower                                                  |
| sqlglot_transpile          | 2.28 ms                                                               | 4.65 ms: 2.04x slower                                                 |
| scimark_lu                 | 155 ms                                                                | 319 ms: 2.06x slower                                                  |
| scimark_sor                | 171 ms                                                                | 355 ms: 2.07x slower                                                  |
| deltablue                  | 5.05 ms                                                               | 11.8 ms: 2.34x slower                                                 |
| go                         | 185 ms                                                                | 440 ms: 2.38x slower                                                  |
| nbody                      | 125 ms                                                                | 307 ms: 2.46x slower                                                  |
| unpack_sequence            | 68.5 ns                                                               | 212 ns: 3.10x slower                                                  |
| Geometric mean             | (ref)                                                                 | 1.38x slower                                                          |

Benchmark hidden because not significant (5): pidigits, xml_etree_parse, regex_effbot, bench_mp_pool, asyncio_websockets
Ignored benchmarks (9) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 2.23x