# Results vs. 3.12.0b1

- fork: mpage
- ref: gh_122712_fix_call_a
- machine: linux-x86_64
- commit hash: f483286
- commit date: 2024-08-07
- overall geometric mean: 1.36x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 2.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 444 ms                                                                | 646 ms: 1.45x slower                                                 |
| docutils       | 4.06 sec                                                              | 5.06 sec: 1.24x slower                                               |
| html5lib       | 95.8 ms                                                               | 140 ms: 1.46x slower                                                 |
| tornado_http   | 262 ms                                                                | 367 ms: 1.40x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.39x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.15 sec: 1.57x faster                                               |
| async_tree_io              | 1.79 sec                                                              | 1.25 sec: 1.43x faster                                               |
| async_tree_none_tg         | 692 ms                                                                | 491 ms: 1.41x faster                                                 |
| async_tree_memoization_tg  | 935 ms                                                                | 666 ms: 1.40x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 824 ms: 1.33x faster                                                 |
| async_tree_none            | 740 ms                                                                | 585 ms: 1.27x faster                                                 |
| async_tree_memoization     | 949 ms                                                                | 751 ms: 1.26x faster                                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 933 ms: 1.22x faster                                                 |
| asyncio_tcp                | 958 ms                                                                | 1.12 sec: 1.17x slower                                               |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.36 sec: 1.20x slower                                               |
| async_generators           | 617 ms                                                                | 753 ms: 1.22x slower                                                 |
| coroutines                 | 30.1 ms                                                               | 42.1 ms: 1.40x slower                                                |
| Geometric mean             | (ref)                                                                 | 1.13x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 255 ms                                                                | 242 ms: 1.05x faster                                                 |
| float          | 127 ms                                                                | 196 ms: 1.54x slower                                                 |
| nbody          | 125 ms                                                                | 284 ms: 2.27x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.49x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 287 ms                                                                | 301 ms: 1.05x slower                                                 |
| regex_v8       | 31.1 ms                                                               | 39.2 ms: 1.26x slower                                                |
| regex_compile  | 197 ms                                                                | 295 ms: 1.50x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.18x slower                                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_dict          | 46.5 us                                                               | 43.9 us: 1.06x faster                                                |
| pickle               | 14.8 us                                                               | 14.1 us: 1.05x faster                                                |
| pickle_list          | 6.40 us                                                               | 6.91 us: 1.08x slower                                                |
| unpickle_list        | 7.19 us                                                               | 7.94 us: 1.10x slower                                                |
| unpickle             | 19.7 us                                                               | 22.0 us: 1.11x slower                                                |
| xml_etree_iterparse  | 157 ms                                                                | 179 ms: 1.14x slower                                                 |
| json_loads           | 36.6 us                                                               | 45.4 us: 1.24x slower                                                |
| xml_etree_generate   | 128 ms                                                                | 164 ms: 1.27x slower                                                 |
| json_dumps           | 13.6 ms                                                               | 17.7 ms: 1.30x slower                                                |
| tomli_loads          | 2.99 sec                                                              | 4.20 sec: 1.41x slower                                               |
| xml_etree_process    | 85.7 ms                                                               | 135 ms: 1.57x slower                                                 |
| pickle_pure_python   | 447 us                                                                | 778 us: 1.74x slower                                                 |
| unpickle_pure_python | 319 us                                                                | 567 us: 1.78x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.24x slower                                                         |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 20.7 ms: 1.27x slower                                                |
| python_startup         | 21.2 ms                                                               | 29.3 ms: 1.38x slower                                                |
| Geometric mean         | (ref)                                                                 | 1.33x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 48.6 ms                                                               | 77.1 ms: 1.59x slower                                                |
| genshi_xml      | 73.6 ms                                                               | 118 ms: 1.60x slower                                                 |
| genshi_text     | 31.9 ms                                                               | 54.2 ms: 1.70x slower                                                |
| mako            | 17.2 ms                                                               | 32.1 ms: 1.86x slower                                                |
| Geometric mean  | (ref)                                                                 | 1.68x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.15 sec: 1.57x faster                                               |
| async_tree_io              | 1.79 sec                                                              | 1.25 sec: 1.43x faster                                               |
| async_tree_none_tg         | 692 ms                                                                | 491 ms: 1.41x faster                                                 |
| async_tree_memoization_tg  | 935 ms                                                                | 666 ms: 1.40x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 824 ms: 1.33x faster                                                 |
| async_tree_none            | 740 ms                                                                | 585 ms: 1.27x faster                                                 |
| async_tree_memoization     | 949 ms                                                                | 751 ms: 1.26x faster                                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 933 ms: 1.22x faster                                                 |
| gc_traversal               | 5.61 ms                                                               | 4.63 ms: 1.21x faster                                                |
| pickle_dict                | 46.5 us                                                               | 43.9 us: 1.06x faster                                                |
| pidigits                   | 255 ms                                                                | 242 ms: 1.05x faster                                                 |
| pickle                     | 14.8 us                                                               | 14.1 us: 1.05x faster                                                |
| regex_dna                  | 287 ms                                                                | 301 ms: 1.05x slower                                                 |
| pickle_list                | 6.40 us                                                               | 6.91 us: 1.08x slower                                                |
| unpickle_list              | 7.19 us                                                               | 7.94 us: 1.10x slower                                                |
| deepcopy                   | 503 us                                                                | 556 us: 1.11x slower                                                 |
| unpickle                   | 19.7 us                                                               | 22.0 us: 1.11x slower                                                |
| pathlib                    | 31.7 ms                                                               | 35.6 ms: 1.12x slower                                                |
| xml_etree_iterparse        | 157 ms                                                                | 179 ms: 1.14x slower                                                 |
| asyncio_tcp                | 958 ms                                                                | 1.12 sec: 1.17x slower                                               |
| pylint                     | 501 ms                                                                | 590 ms: 1.18x slower                                                 |
| sqlite_synth               | 3.75 us                                                               | 4.44 us: 1.18x slower                                                |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.36 sec: 1.20x slower                                               |
| deepcopy_memo              | 57.5 us                                                               | 69.7 us: 1.21x slower                                                |
| async_generators           | 617 ms                                                                | 753 ms: 1.22x slower                                                 |
| json                       | 6.68 ms                                                               | 8.22 ms: 1.23x slower                                                |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 9.23 ms: 1.23x slower                                                |
| json_loads                 | 36.6 us                                                               | 45.4 us: 1.24x slower                                                |
| docutils                   | 4.06 sec                                                              | 5.06 sec: 1.24x slower                                               |
| generators                 | 46.0 ms                                                               | 57.5 ms: 1.25x slower                                                |
| regex_v8                   | 31.1 ms                                                               | 39.2 ms: 1.26x slower                                                |
| scimark_fft                | 499 ms                                                                | 635 ms: 1.27x slower                                                 |
| python_startup_no_site     | 16.3 ms                                                               | 20.7 ms: 1.27x slower                                                |
| xml_etree_generate         | 128 ms                                                                | 164 ms: 1.27x slower                                                 |
| comprehensions             | 29.6 us                                                               | 38.3 us: 1.30x slower                                                |
| json_dumps                 | 13.6 ms                                                               | 17.7 ms: 1.30x slower                                                |
| meteor_contest             | 149 ms                                                                | 194 ms: 1.30x slower                                                 |
| deepcopy_reduce            | 4.45 us                                                               | 5.84 us: 1.31x slower                                                |
| pycparser                  | 1.73 sec                                                              | 2.29 sec: 1.32x slower                                               |
| mdp                        | 3.84 sec                                                              | 5.16 sec: 1.34x slower                                               |
| crypto_pyaes               | 112 ms                                                                | 152 ms: 1.36x slower                                                 |
| python_startup             | 21.2 ms                                                               | 29.3 ms: 1.38x slower                                                |
| bench_thread_pool          | 3.11 ms                                                               | 4.33 ms: 1.39x slower                                                |
| coroutines                 | 30.1 ms                                                               | 42.1 ms: 1.40x slower                                                |
| tornado_http               | 262 ms                                                                | 367 ms: 1.40x slower                                                 |
| tomli_loads                | 2.99 sec                                                              | 4.20 sec: 1.41x slower                                               |
| fannkuch                   | 551 ms                                                                | 776 ms: 1.41x slower                                                 |
| sympy_integrate            | 31.4 ms                                                               | 44.3 ms: 1.41x slower                                                |
| telco                      | 9.71 ms                                                               | 13.8 ms: 1.42x slower                                                |
| 2to3                       | 444 ms                                                                | 646 ms: 1.45x slower                                                 |
| nqueens                    | 110 ms                                                                | 161 ms: 1.46x slower                                                 |
| html5lib                   | 95.8 ms                                                               | 140 ms: 1.46x slower                                                 |
| coverage                   | 97.6 ms                                                               | 146 ms: 1.49x slower                                                 |
| regex_compile              | 197 ms                                                                | 295 ms: 1.50x slower                                                 |
| thrift                     | 1.17 ms                                                               | 1.77 ms: 1.51x slower                                                |
| logging_simple             | 9.89 us                                                               | 15.0 us: 1.52x slower                                                |
| float                      | 127 ms                                                                | 196 ms: 1.54x slower                                                 |
| bpe_tokeniser              | 6.63 sec                                                              | 10.3 sec: 1.55x slower                                               |
| logging_format             | 11.8 us                                                               | 18.5 us: 1.57x slower                                                |
| xml_etree_process          | 85.7 ms                                                               | 135 ms: 1.57x slower                                                 |
| sympy_str                  | 425 ms                                                                | 673 ms: 1.58x slower                                                 |
| django_template            | 48.6 ms                                                               | 77.1 ms: 1.59x slower                                                |
| genshi_xml                 | 73.6 ms                                                               | 118 ms: 1.60x slower                                                 |
| spectral_norm              | 158 ms                                                                | 253 ms: 1.60x slower                                                 |
| scimark_monte_carlo        | 98.5 ms                                                               | 160 ms: 1.63x slower                                                 |
| sqlglot_normalize          | 148 ms                                                                | 242 ms: 1.63x slower                                                 |
| pyflate                    | 661 ms                                                                | 1.09 sec: 1.65x slower                                               |
| pprint_safe_repr           | 970 ms                                                                | 1.64 sec: 1.70x slower                                               |
| genshi_text                | 31.9 ms                                                               | 54.2 ms: 1.70x slower                                                |
| pprint_pformat             | 2.03 sec                                                              | 3.45 sec: 1.70x slower                                               |
| richards                   | 63.4 ms                                                               | 110 ms: 1.74x slower                                                 |
| pickle_pure_python         | 447 us                                                                | 778 us: 1.74x slower                                                 |
| unpickle_pure_python       | 319 us                                                                | 567 us: 1.78x slower                                                 |
| typing_runtime_protocols   | 199 us                                                                | 356 us: 1.78x slower                                                 |
| chaos                      | 93.7 ms                                                               | 169 ms: 1.80x slower                                                 |
| richards_super             | 67.9 ms                                                               | 124 ms: 1.83x slower                                                 |
| raytrace                   | 418 ms                                                                | 765 ms: 1.83x slower                                                 |
| sympy_expand               | 689 ms                                                                | 1.26 sec: 1.83x slower                                               |
| mako                       | 17.2 ms                                                               | 32.1 ms: 1.86x slower                                                |
| sqlglot_optimize           | 76.5 ms                                                               | 143 ms: 1.87x slower                                                 |
| logging_silent             | 135 ns                                                                | 254 ns: 1.88x slower                                                 |
| hexiom                     | 8.87 ms                                                               | 17.2 ms: 1.93x slower                                                |
| scimark_lu                 | 155 ms                                                                | 303 ms: 1.96x slower                                                 |
| scimark_sor                | 171 ms                                                                | 342 ms: 2.00x slower                                                 |
| sqlglot_transpile          | 2.28 ms                                                               | 4.62 ms: 2.02x slower                                                |
| sympy_sum                  | 229 ms                                                                | 465 ms: 2.03x slower                                                 |
| deltablue                  | 5.05 ms                                                               | 11.3 ms: 2.25x slower                                                |
| nbody                      | 125 ms                                                                | 284 ms: 2.27x slower                                                 |
| sqlglot_parse              | 1.89 ms                                                               | 4.43 ms: 2.34x slower                                                |
| go                         | 185 ms                                                                | 446 ms: 2.41x slower                                                 |
| unpack_sequence            | 68.5 ns                                                               | 211 ns: 3.08x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.36x slower                                                         |

Benchmark hidden because not significant (5): bench_mp_pool, create_gc_cycles, regex_effbot, asyncio_websockets, xml_etree_parse
Ignored benchmarks (9) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.31x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 2.23x