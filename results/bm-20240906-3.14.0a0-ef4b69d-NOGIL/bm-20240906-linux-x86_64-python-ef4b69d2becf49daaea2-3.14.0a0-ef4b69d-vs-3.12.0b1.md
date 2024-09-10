# Results vs. 3.12.0b1

- fork: python
- ref: ef4b69d2becf49daaea2
- machine: linux-x86_64
- commit hash: ef4b69d
- commit date: 2024-09-06
- overall geometric mean: 1.37x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 2.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 444 ms                                                                | 719 ms: 1.62x slower                                                  |
| docutils       | 4.06 sec                                                              | 4.96 sec: 1.22x slower                                                |
| html5lib       | 95.8 ms                                                               | 139 ms: 1.45x slower                                                  |
| tornado_http   | 262 ms                                                                | 350 ms: 1.33x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.40x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.17 sec: 1.54x faster                                                |
| async_tree_memoization_tg  | 935 ms                                                                | 660 ms: 1.42x faster                                                  |
| async_tree_none_tg         | 692 ms                                                                | 514 ms: 1.35x faster                                                  |
| async_tree_io              | 1.79 sec                                                              | 1.34 sec: 1.33x faster                                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 863 ms: 1.27x faster                                                  |
| async_tree_memoization     | 949 ms                                                                | 747 ms: 1.27x faster                                                  |
| async_tree_none            | 740 ms                                                                | 610 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 952 ms: 1.19x faster                                                  |
| async_generators           | 617 ms                                                                | 734 ms: 1.19x slower                                                  |
| asyncio_tcp                | 958 ms                                                                | 1.22 sec: 1.27x slower                                                |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.56 sec: 1.27x slower                                                |
| coroutines                 | 30.1 ms                                                               | 41.7 ms: 1.38x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.10x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 127 ms                                                                | 204 ms: 1.61x slower                                                  |
| nbody          | 125 ms                                                                | 300 ms: 2.41x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.56x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 31.1 ms                                                               | 37.7 ms: 1.21x slower                                                 |
| regex_compile  | 197 ms                                                                | 284 ms: 1.44x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.15x slower                                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 46.5 us                                                               | 40.9 us: 1.14x faster                                                 |
| xml_etree_parse      | 230 ms                                                                | 215 ms: 1.07x faster                                                  |
| xml_etree_iterparse  | 157 ms                                                                | 171 ms: 1.09x slower                                                  |
| unpickle             | 19.7 us                                                               | 21.8 us: 1.10x slower                                                 |
| json_loads           | 36.6 us                                                               | 44.0 us: 1.20x slower                                                 |
| xml_etree_generate   | 128 ms                                                                | 163 ms: 1.27x slower                                                  |
| json_dumps           | 13.6 ms                                                               | 18.1 ms: 1.33x slower                                                 |
| tomli_loads          | 2.99 sec                                                              | 4.30 sec: 1.44x slower                                                |
| xml_etree_process    | 85.7 ms                                                               | 128 ms: 1.49x slower                                                  |
| unpickle_pure_python | 319 us                                                                | 550 us: 1.72x slower                                                  |
| pickle_pure_python   | 447 us                                                                | 870 us: 1.94x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.22x slower                                                          |

Benchmark hidden because not significant (3): unpickle_list, pickle_list, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 21.5 ms: 1.32x slower                                                 |
| python_startup         | 21.2 ms                                                               | 32.8 ms: 1.55x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.43x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.9 ms                                                               | 55.1 ms: 1.73x slower                                                 |
| mako            | 17.2 ms                                                               | 30.1 ms: 1.75x slower                                                 |
| genshi_xml      | 73.6 ms                                                               | 129 ms: 1.76x slower                                                  |
| django_template | 48.6 ms                                                               | 85.9 ms: 1.77x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.75x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.17 sec: 1.54x faster                                                |
| async_tree_memoization_tg  | 935 ms                                                                | 660 ms: 1.42x faster                                                  |
| async_tree_none_tg         | 692 ms                                                                | 514 ms: 1.35x faster                                                  |
| async_tree_io              | 1.79 sec                                                              | 1.34 sec: 1.33x faster                                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 863 ms: 1.27x faster                                                  |
| async_tree_memoization     | 949 ms                                                                | 747 ms: 1.27x faster                                                  |
| gc_traversal               | 5.61 ms                                                               | 4.60 ms: 1.22x faster                                                 |
| async_tree_none            | 740 ms                                                                | 610 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 952 ms: 1.19x faster                                                  |
| pickle_dict                | 46.5 us                                                               | 40.9 us: 1.14x faster                                                 |
| xml_etree_parse            | 230 ms                                                                | 215 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 157 ms                                                                | 171 ms: 1.09x slower                                                  |
| unpickle                   | 19.7 us                                                               | 21.8 us: 1.10x slower                                                 |
| deepcopy                   | 503 us                                                                | 568 us: 1.13x slower                                                  |
| pathlib                    | 31.7 ms                                                               | 37.2 ms: 1.17x slower                                                 |
| deepcopy_memo              | 57.5 us                                                               | 67.4 us: 1.17x slower                                                 |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 8.80 ms: 1.18x slower                                                 |
| generators                 | 46.0 ms                                                               | 54.6 ms: 1.19x slower                                                 |
| async_generators           | 617 ms                                                                | 734 ms: 1.19x slower                                                  |
| json_loads                 | 36.6 us                                                               | 44.0 us: 1.20x slower                                                 |
| regex_v8                   | 31.1 ms                                                               | 37.7 ms: 1.21x slower                                                 |
| json                       | 6.68 ms                                                               | 8.10 ms: 1.21x slower                                                 |
| docutils                   | 4.06 sec                                                              | 4.96 sec: 1.22x slower                                                |
| sqlite_synth               | 3.75 us                                                               | 4.60 us: 1.23x slower                                                 |
| pylint                     | 501 ms                                                                | 625 ms: 1.25x slower                                                  |
| pycparser                  | 1.73 sec                                                              | 2.18 sec: 1.26x slower                                                |
| comprehensions             | 29.6 us                                                               | 37.3 us: 1.26x slower                                                 |
| xml_etree_generate         | 128 ms                                                                | 163 ms: 1.27x slower                                                  |
| asyncio_tcp                | 958 ms                                                                | 1.22 sec: 1.27x slower                                                |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.56 sec: 1.27x slower                                                |
| bench_mp_pool              | 18.4 ms                                                               | 24.0 ms: 1.31x slower                                                 |
| scimark_fft                | 499 ms                                                                | 652 ms: 1.31x slower                                                  |
| logging_format             | 11.8 us                                                               | 15.5 us: 1.31x slower                                                 |
| python_startup_no_site     | 16.3 ms                                                               | 21.5 ms: 1.32x slower                                                 |
| json_dumps                 | 13.6 ms                                                               | 18.1 ms: 1.33x slower                                                 |
| tornado_http               | 262 ms                                                                | 350 ms: 1.33x slower                                                  |
| dulwich_log                | 114 ms                                                                | 152 ms: 1.33x slower                                                  |
| meteor_contest             | 149 ms                                                                | 199 ms: 1.34x slower                                                  |
| deepcopy_reduce            | 4.45 us                                                               | 5.97 us: 1.34x slower                                                 |
| mdp                        | 3.84 sec                                                              | 5.18 sec: 1.35x slower                                                |
| coroutines                 | 30.1 ms                                                               | 41.7 ms: 1.38x slower                                                 |
| crypto_pyaes               | 112 ms                                                                | 156 ms: 1.40x slower                                                  |
| tomli_loads                | 2.99 sec                                                              | 4.30 sec: 1.44x slower                                                |
| regex_compile              | 197 ms                                                                | 284 ms: 1.44x slower                                                  |
| html5lib                   | 95.8 ms                                                               | 139 ms: 1.45x slower                                                  |
| thrift                     | 1.17 ms                                                               | 1.70 ms: 1.45x slower                                                 |
| xml_etree_process          | 85.7 ms                                                               | 128 ms: 1.49x slower                                                  |
| fannkuch                   | 551 ms                                                                | 831 ms: 1.51x slower                                                  |
| telco                      | 9.71 ms                                                               | 14.7 ms: 1.51x slower                                                 |
| sympy_integrate            | 31.4 ms                                                               | 48.3 ms: 1.54x slower                                                 |
| bpe_tokeniser              | 6.63 sec                                                              | 10.2 sec: 1.55x slower                                                |
| python_startup             | 21.2 ms                                                               | 32.8 ms: 1.55x slower                                                 |
| spectral_norm              | 158 ms                                                                | 249 ms: 1.58x slower                                                  |
| nqueens                    | 110 ms                                                                | 174 ms: 1.58x slower                                                  |
| coverage                   | 97.6 ms                                                               | 157 ms: 1.61x slower                                                  |
| float                      | 127 ms                                                                | 204 ms: 1.61x slower                                                  |
| sqlglot_normalize          | 148 ms                                                                | 240 ms: 1.62x slower                                                  |
| 2to3                       | 444 ms                                                                | 719 ms: 1.62x slower                                                  |
| scimark_monte_carlo        | 98.5 ms                                                               | 160 ms: 1.63x slower                                                  |
| pyflate                    | 661 ms                                                                | 1.08 sec: 1.63x slower                                                |
| sympy_str                  | 425 ms                                                                | 696 ms: 1.64x slower                                                  |
| sqlglot_optimize           | 76.5 ms                                                               | 130 ms: 1.70x slower                                                  |
| pprint_pformat             | 2.03 sec                                                              | 3.48 sec: 1.71x slower                                                |
| unpickle_pure_python       | 319 us                                                                | 550 us: 1.72x slower                                                  |
| genshi_text                | 31.9 ms                                                               | 55.1 ms: 1.73x slower                                                 |
| pprint_safe_repr           | 970 ms                                                                | 1.68 sec: 1.73x slower                                                |
| mako                       | 17.2 ms                                                               | 30.1 ms: 1.75x slower                                                 |
| bench_thread_pool          | 3.11 ms                                                               | 5.45 ms: 1.75x slower                                                 |
| genshi_xml                 | 73.6 ms                                                               | 129 ms: 1.76x slower                                                  |
| typing_runtime_protocols   | 199 us                                                                | 353 us: 1.77x slower                                                  |
| django_template            | 48.6 ms                                                               | 85.9 ms: 1.77x slower                                                 |
| logging_simple             | 9.89 us                                                               | 17.7 us: 1.79x slower                                                 |
| raytrace                   | 418 ms                                                                | 751 ms: 1.80x slower                                                  |
| richards                   | 63.4 ms                                                               | 114 ms: 1.80x slower                                                  |
| richards_super             | 67.9 ms                                                               | 123 ms: 1.81x slower                                                  |
| hexiom                     | 8.87 ms                                                               | 16.4 ms: 1.85x slower                                                 |
| chaos                      | 93.7 ms                                                               | 176 ms: 1.88x slower                                                  |
| logging_silent             | 135 ns                                                                | 260 ns: 1.92x slower                                                  |
| sympy_expand               | 689 ms                                                                | 1.33 sec: 1.93x slower                                                |
| sqlglot_transpile          | 2.28 ms                                                               | 4.43 ms: 1.94x slower                                                 |
| pickle_pure_python         | 447 us                                                                | 870 us: 1.94x slower                                                  |
| go                         | 185 ms                                                                | 361 ms: 1.95x slower                                                  |
| sqlglot_parse              | 1.89 ms                                                               | 3.72 ms: 1.96x slower                                                 |
| scimark_lu                 | 155 ms                                                                | 305 ms: 1.97x slower                                                  |
| scimark_sor                | 171 ms                                                                | 340 ms: 1.99x slower                                                  |
| sympy_sum                  | 229 ms                                                                | 492 ms: 2.15x slower                                                  |
| deltablue                  | 5.05 ms                                                               | 11.3 ms: 2.25x slower                                                 |
| nbody                      | 125 ms                                                                | 300 ms: 2.41x slower                                                  |
| unpack_sequence            | 68.5 ns                                                               | 180 ns: 2.63x slower                                                  |
| Geometric mean             | (ref)                                                                 | 1.37x slower                                                          |

Benchmark hidden because not significant (8): pidigits, asyncio_websockets, regex_effbot, unpickle_list, regex_dna, pickle_list, pickle, create_gc_cycles
Ignored benchmarks (8) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 2.24x