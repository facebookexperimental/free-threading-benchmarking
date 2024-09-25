# Results vs. 3.12.0b1

- fork: mpage
- ref: gh_115999_thread_loc
- machine: linux-x86_64
- commit hash: d8a840b
- commit date: 2024-09-03
- overall geometric mean: 1.36x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x slower
- Memory change: 2.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 444 ms                                                                | 698 ms: 1.57x slower                                                 |
| docutils       | 4.06 sec                                                              | 4.84 sec: 1.19x slower                                               |
| html5lib       | 95.8 ms                                                               | 142 ms: 1.48x slower                                                 |
| tornado_http   | 262 ms                                                                | 399 ms: 1.52x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.43x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.15 sec: 1.56x faster                                               |
| async_tree_memoization_tg  | 935 ms                                                                | 676 ms: 1.38x faster                                                 |
| async_tree_io              | 1.79 sec                                                              | 1.30 sec: 1.37x faster                                               |
| async_tree_none_tg         | 692 ms                                                                | 505 ms: 1.37x faster                                                 |
| async_tree_memoization     | 949 ms                                                                | 727 ms: 1.31x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 851 ms: 1.29x faster                                                 |
| async_tree_none            | 740 ms                                                                | 581 ms: 1.27x faster                                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 974 ms: 1.17x faster                                                 |
| async_generators           | 617 ms                                                                | 712 ms: 1.15x slower                                                 |
| asyncio_tcp                | 958 ms                                                                | 1.12 sec: 1.17x slower                                               |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.41 sec: 1.22x slower                                               |
| coroutines                 | 30.1 ms                                                               | 41.6 ms: 1.38x slower                                                |
| Geometric mean             | (ref)                                                                 | 1.12x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 127 ms                                                                | 192 ms: 1.52x slower                                                 |
| nbody          | 125 ms                                                                | 271 ms: 2.18x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.47x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 4.97 ms                                                               | 4.57 ms: 1.09x faster                                                |
| regex_dna      | 287 ms                                                                | 297 ms: 1.04x slower                                                 |
| regex_v8       | 31.1 ms                                                               | 35.5 ms: 1.14x slower                                                |
| regex_compile  | 197 ms                                                                | 312 ms: 1.59x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.15x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle               | 14.8 us                                                               | 13.8 us: 1.07x faster                                                |
| pickle_dict          | 46.5 us                                                               | 44.6 us: 1.04x faster                                                |
| xml_etree_parse      | 230 ms                                                                | 243 ms: 1.06x slower                                                 |
| xml_etree_iterparse  | 157 ms                                                                | 173 ms: 1.10x slower                                                 |
| pickle_list          | 6.40 us                                                               | 7.10 us: 1.11x slower                                                |
| unpickle_list        | 7.19 us                                                               | 8.26 us: 1.15x slower                                                |
| unpickle             | 19.7 us                                                               | 22.9 us: 1.16x slower                                                |
| json_loads           | 36.6 us                                                               | 43.5 us: 1.19x slower                                                |
| json_dumps           | 13.6 ms                                                               | 17.3 ms: 1.28x slower                                                |
| xml_etree_generate   | 128 ms                                                                | 166 ms: 1.29x slower                                                 |
| tomli_loads          | 2.99 sec                                                              | 4.40 sec: 1.47x slower                                               |
| xml_etree_process    | 85.7 ms                                                               | 131 ms: 1.53x slower                                                 |
| pickle_pure_python   | 447 us                                                                | 812 us: 1.82x slower                                                 |
| unpickle_pure_python | 319 us                                                                | 597 us: 1.87x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.25x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 21.7 ms: 1.34x slower                                                |
| python_startup         | 21.2 ms                                                               | 35.2 ms: 1.66x slower                                                |
| Geometric mean         | (ref)                                                                 | 1.49x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                               | 120 ms: 1.62x slower                                                 |
| django_template | 48.6 ms                                                               | 82.3 ms: 1.69x slower                                                |
| genshi_text     | 31.9 ms                                                               | 55.2 ms: 1.73x slower                                                |
| mako            | 17.2 ms                                                               | 32.1 ms: 1.86x slower                                                |
| Geometric mean  | (ref)                                                                 | 1.73x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.15 sec: 1.56x faster                                               |
| async_tree_memoization_tg  | 935 ms                                                                | 676 ms: 1.38x faster                                                 |
| async_tree_io              | 1.79 sec                                                              | 1.30 sec: 1.37x faster                                               |
| async_tree_none_tg         | 692 ms                                                                | 505 ms: 1.37x faster                                                 |
| async_tree_memoization     | 949 ms                                                                | 727 ms: 1.31x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 851 ms: 1.29x faster                                                 |
| async_tree_none            | 740 ms                                                                | 581 ms: 1.27x faster                                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 974 ms: 1.17x faster                                                 |
| gc_traversal               | 5.61 ms                                                               | 5.05 ms: 1.11x faster                                                |
| create_gc_cycles           | 2.02 ms                                                               | 1.85 ms: 1.09x faster                                                |
| regex_effbot               | 4.97 ms                                                               | 4.57 ms: 1.09x faster                                                |
| pickle                     | 14.8 us                                                               | 13.8 us: 1.07x faster                                                |
| pickle_dict                | 46.5 us                                                               | 44.6 us: 1.04x faster                                                |
| regex_dna                  | 287 ms                                                                | 297 ms: 1.04x slower                                                 |
| xml_etree_parse            | 230 ms                                                                | 243 ms: 1.06x slower                                                 |
| scimark_fft                | 499 ms                                                                | 539 ms: 1.08x slower                                                 |
| xml_etree_iterparse        | 157 ms                                                                | 173 ms: 1.10x slower                                                 |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 8.22 ms: 1.10x slower                                                |
| pickle_list                | 6.40 us                                                               | 7.10 us: 1.11x slower                                                |
| deepcopy                   | 503 us                                                                | 564 us: 1.12x slower                                                 |
| regex_v8                   | 31.1 ms                                                               | 35.5 ms: 1.14x slower                                                |
| pathlib                    | 31.7 ms                                                               | 36.3 ms: 1.14x slower                                                |
| unpickle_list              | 7.19 us                                                               | 8.26 us: 1.15x slower                                                |
| async_generators           | 617 ms                                                                | 712 ms: 1.15x slower                                                 |
| unpickle                   | 19.7 us                                                               | 22.9 us: 1.16x slower                                                |
| generators                 | 46.0 ms                                                               | 53.5 ms: 1.16x slower                                                |
| asyncio_tcp                | 958 ms                                                                | 1.12 sec: 1.17x slower                                               |
| docutils                   | 4.06 sec                                                              | 4.84 sec: 1.19x slower                                               |
| json_loads                 | 36.6 us                                                               | 43.5 us: 1.19x slower                                                |
| pylint                     | 501 ms                                                                | 609 ms: 1.22x slower                                                 |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.41 sec: 1.22x slower                                               |
| sqlite_synth               | 3.75 us                                                               | 4.64 us: 1.24x slower                                                |
| deepcopy_memo              | 57.5 us                                                               | 72.1 us: 1.25x slower                                                |
| pycparser                  | 1.73 sec                                                              | 2.20 sec: 1.27x slower                                               |
| mdp                        | 3.84 sec                                                              | 4.90 sec: 1.27x slower                                               |
| json_dumps                 | 13.6 ms                                                               | 17.3 ms: 1.28x slower                                                |
| json                       | 6.68 ms                                                               | 8.56 ms: 1.28x slower                                                |
| xml_etree_generate         | 128 ms                                                                | 166 ms: 1.29x slower                                                 |
| comprehensions             | 29.6 us                                                               | 38.6 us: 1.31x slower                                                |
| meteor_contest             | 149 ms                                                                | 195 ms: 1.31x slower                                                 |
| python_startup_no_site     | 16.3 ms                                                               | 21.7 ms: 1.34x slower                                                |
| coroutines                 | 30.1 ms                                                               | 41.6 ms: 1.38x slower                                                |
| fannkuch                   | 551 ms                                                                | 761 ms: 1.38x slower                                                 |
| crypto_pyaes               | 112 ms                                                                | 156 ms: 1.40x slower                                                 |
| deepcopy_reduce            | 4.45 us                                                               | 6.24 us: 1.40x slower                                                |
| spectral_norm              | 158 ms                                                                | 224 ms: 1.42x slower                                                 |
| telco                      | 9.71 ms                                                               | 14.0 ms: 1.44x slower                                                |
| bench_thread_pool          | 3.11 ms                                                               | 4.51 ms: 1.45x slower                                                |
| nqueens                    | 110 ms                                                                | 160 ms: 1.46x slower                                                 |
| tomli_loads                | 2.99 sec                                                              | 4.40 sec: 1.47x slower                                               |
| thrift                     | 1.17 ms                                                               | 1.73 ms: 1.48x slower                                                |
| coverage                   | 97.6 ms                                                               | 144 ms: 1.48x slower                                                 |
| html5lib                   | 95.8 ms                                                               | 142 ms: 1.48x slower                                                 |
| bpe_tokeniser              | 6.63 sec                                                              | 9.87 sec: 1.49x slower                                               |
| float                      | 127 ms                                                                | 192 ms: 1.52x slower                                                 |
| tornado_http               | 262 ms                                                                | 399 ms: 1.52x slower                                                 |
| xml_etree_process          | 85.7 ms                                                               | 131 ms: 1.53x slower                                                 |
| sqlglot_optimize           | 76.5 ms                                                               | 119 ms: 1.56x slower                                                 |
| 2to3                       | 444 ms                                                                | 698 ms: 1.57x slower                                                 |
| pyflate                    | 661 ms                                                                | 1.04 sec: 1.58x slower                                               |
| regex_compile              | 197 ms                                                                | 312 ms: 1.59x slower                                                 |
| logging_format             | 11.8 us                                                               | 19.1 us: 1.61x slower                                                |
| genshi_xml                 | 73.6 ms                                                               | 120 ms: 1.62x slower                                                 |
| scimark_monte_carlo        | 98.5 ms                                                               | 160 ms: 1.63x slower                                                 |
| sympy_integrate            | 31.4 ms                                                               | 51.4 ms: 1.64x slower                                                |
| sympy_str                  | 425 ms                                                                | 698 ms: 1.64x slower                                                 |
| chaos                      | 93.7 ms                                                               | 154 ms: 1.65x slower                                                 |
| python_startup             | 21.2 ms                                                               | 35.2 ms: 1.66x slower                                                |
| sqlglot_normalize          | 148 ms                                                                | 249 ms: 1.68x slower                                                 |
| logging_simple             | 9.89 us                                                               | 16.6 us: 1.68x slower                                                |
| richards                   | 63.4 ms                                                               | 107 ms: 1.69x slower                                                 |
| django_template            | 48.6 ms                                                               | 82.3 ms: 1.69x slower                                                |
| pprint_pformat             | 2.03 sec                                                              | 3.47 sec: 1.71x slower                                               |
| genshi_text                | 31.9 ms                                                               | 55.2 ms: 1.73x slower                                                |
| hexiom                     | 8.87 ms                                                               | 15.8 ms: 1.78x slower                                                |
| pickle_pure_python         | 447 us                                                                | 812 us: 1.82x slower                                                 |
| pprint_safe_repr           | 970 ms                                                                | 1.77 sec: 1.82x slower                                               |
| mako                       | 17.2 ms                                                               | 32.1 ms: 1.86x slower                                                |
| unpickle_pure_python       | 319 us                                                                | 597 us: 1.87x slower                                                 |
| raytrace                   | 418 ms                                                                | 788 ms: 1.88x slower                                                 |
| typing_runtime_protocols   | 199 us                                                                | 381 us: 1.91x slower                                                 |
| scimark_sor                | 171 ms                                                                | 331 ms: 1.93x slower                                                 |
| logging_silent             | 135 ns                                                                | 262 ns: 1.94x slower                                                 |
| sympy_expand               | 689 ms                                                                | 1.35 sec: 1.95x slower                                               |
| go                         | 185 ms                                                                | 370 ms: 2.00x slower                                                 |
| richards_super             | 67.9 ms                                                               | 137 ms: 2.01x slower                                                 |
| sqlglot_transpile          | 2.28 ms                                                               | 4.66 ms: 2.04x slower                                                |
| scimark_lu                 | 155 ms                                                                | 317 ms: 2.05x slower                                                 |
| sqlglot_parse              | 1.89 ms                                                               | 4.06 ms: 2.14x slower                                                |
| nbody                      | 125 ms                                                                | 271 ms: 2.18x slower                                                 |
| sympy_sum                  | 229 ms                                                                | 512 ms: 2.24x slower                                                 |
| deltablue                  | 5.05 ms                                                               | 11.5 ms: 2.28x slower                                                |
| unpack_sequence            | 68.5 ns                                                               | 191 ns: 2.79x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.36x slower                                                         |

Benchmark hidden because not significant (3): pidigits, asyncio_websockets, bench_mp_pool
Ignored benchmarks (9) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.30x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.21x

# Memory
- memory change: 2.29x