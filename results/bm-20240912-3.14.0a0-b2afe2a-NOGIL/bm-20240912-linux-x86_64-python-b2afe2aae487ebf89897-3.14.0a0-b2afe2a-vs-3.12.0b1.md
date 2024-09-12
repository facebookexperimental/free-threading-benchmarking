# Results vs. 3.12.0b1

- fork: python
- ref: b2afe2aae487ebf89897
- machine: linux-x86_64
- commit hash: b2afe2a
- commit date: 2024-09-12
- overall geometric mean: 1.37x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 2.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 444 ms                                                                | 721 ms: 1.62x slower                                                  |
| docutils       | 4.06 sec                                                              | 5.09 sec: 1.25x slower                                                |
| html5lib       | 95.8 ms                                                               | 141 ms: 1.47x slower                                                  |
| tornado_http   | 262 ms                                                                | 369 ms: 1.40x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.43x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 935 ms                                                                | 649 ms: 1.44x faster                                                  |
| async_tree_io_tg           | 1.80 sec                                                              | 1.26 sec: 1.43x faster                                                |
| async_tree_none_tg         | 692 ms                                                                | 491 ms: 1.41x faster                                                  |
| async_tree_io              | 1.79 sec                                                              | 1.35 sec: 1.32x faster                                                |
| async_tree_memoization     | 949 ms                                                                | 750 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 915 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 906 ms: 1.21x faster                                                  |
| async_tree_none            | 740 ms                                                                | 647 ms: 1.14x faster                                                  |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.12 sec: 1.11x slower                                                |
| async_generators           | 617 ms                                                                | 726 ms: 1.18x slower                                                  |
| asyncio_tcp                | 958 ms                                                                | 1.19 sec: 1.24x slower                                                |
| coroutines                 | 30.1 ms                                                               | 44.1 ms: 1.46x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.10x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 127 ms                                                                | 202 ms: 1.59x slower                                                  |
| nbody          | 125 ms                                                                | 286 ms: 2.29x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.55x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 31.1 ms                                                               | 36.2 ms: 1.16x slower                                                 |
| regex_compile  | 197 ms                                                                | 301 ms: 1.53x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.15x slower                                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_list          | 6.40 us                                                               | 6.85 us: 1.07x slower                                                 |
| unpickle_list        | 7.19 us                                                               | 7.76 us: 1.08x slower                                                 |
| xml_etree_iterparse  | 157 ms                                                                | 170 ms: 1.08x slower                                                  |
| json_loads           | 36.6 us                                                               | 42.8 us: 1.17x slower                                                 |
| unpickle             | 19.7 us                                                               | 24.2 us: 1.22x slower                                                 |
| xml_etree_generate   | 128 ms                                                                | 165 ms: 1.29x slower                                                  |
| json_dumps           | 13.6 ms                                                               | 18.0 ms: 1.33x slower                                                 |
| tomli_loads          | 2.99 sec                                                              | 4.26 sec: 1.43x slower                                                |
| xml_etree_process    | 85.7 ms                                                               | 128 ms: 1.50x slower                                                  |
| unpickle_pure_python | 319 us                                                                | 581 us: 1.82x slower                                                  |
| pickle_pure_python   | 447 us                                                                | 835 us: 1.87x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.24x slower                                                          |

Benchmark hidden because not significant (3): pickle, pickle_dict, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 23.8 ms: 1.47x slower                                                 |
| python_startup         | 21.2 ms                                                               | 35.1 ms: 1.65x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.56x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                               | 114 ms: 1.55x slower                                                  |
| django_template | 48.6 ms                                                               | 82.9 ms: 1.71x slower                                                 |
| mako            | 17.2 ms                                                               | 30.3 ms: 1.76x slower                                                 |
| genshi_text     | 31.9 ms                                                               | 61.0 ms: 1.91x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.73x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 935 ms                                                                | 649 ms: 1.44x faster                                                  |
| async_tree_io_tg           | 1.80 sec                                                              | 1.26 sec: 1.43x faster                                                |
| async_tree_none_tg         | 692 ms                                                                | 491 ms: 1.41x faster                                                  |
| async_tree_io              | 1.79 sec                                                              | 1.35 sec: 1.32x faster                                                |
| async_tree_memoization     | 949 ms                                                                | 750 ms: 1.27x faster                                                  |
| gc_traversal               | 5.61 ms                                                               | 4.51 ms: 1.24x faster                                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 915 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 906 ms: 1.21x faster                                                  |
| async_tree_none            | 740 ms                                                                | 647 ms: 1.14x faster                                                  |
| bench_mp_pool              | 18.4 ms                                                               | 16.5 ms: 1.11x faster                                                 |
| create_gc_cycles           | 2.02 ms                                                               | 1.83 ms: 1.10x faster                                                 |
| pickle_list                | 6.40 us                                                               | 6.85 us: 1.07x slower                                                 |
| unpickle_list              | 7.19 us                                                               | 7.76 us: 1.08x slower                                                 |
| xml_etree_iterparse        | 157 ms                                                                | 170 ms: 1.08x slower                                                  |
| dulwich_log                | 114 ms                                                                | 125 ms: 1.10x slower                                                  |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.12 sec: 1.11x slower                                                |
| pathlib                    | 31.7 ms                                                               | 36.3 ms: 1.14x slower                                                 |
| regex_v8                   | 31.1 ms                                                               | 36.2 ms: 1.16x slower                                                 |
| json_loads                 | 36.6 us                                                               | 42.8 us: 1.17x slower                                                 |
| async_generators           | 617 ms                                                                | 726 ms: 1.18x slower                                                  |
| deepcopy                   | 503 us                                                                | 595 us: 1.18x slower                                                  |
| sqlite_synth               | 3.75 us                                                               | 4.43 us: 1.18x slower                                                 |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 8.99 ms: 1.20x slower                                                 |
| json                       | 6.68 ms                                                               | 8.13 ms: 1.22x slower                                                 |
| generators                 | 46.0 ms                                                               | 56.1 ms: 1.22x slower                                                 |
| unpickle                   | 19.7 us                                                               | 24.2 us: 1.22x slower                                                 |
| deepcopy_memo              | 57.5 us                                                               | 71.2 us: 1.24x slower                                                 |
| asyncio_tcp                | 958 ms                                                                | 1.19 sec: 1.24x slower                                                |
| docutils                   | 4.06 sec                                                              | 5.09 sec: 1.25x slower                                                |
| pylint                     | 501 ms                                                                | 627 ms: 1.25x slower                                                  |
| deepcopy_reduce            | 4.45 us                                                               | 5.61 us: 1.26x slower                                                 |
| scimark_fft                | 499 ms                                                                | 636 ms: 1.27x slower                                                  |
| xml_etree_generate         | 128 ms                                                                | 165 ms: 1.29x slower                                                  |
| json_dumps                 | 13.6 ms                                                               | 18.0 ms: 1.33x slower                                                 |
| meteor_contest             | 149 ms                                                                | 199 ms: 1.34x slower                                                  |
| mdp                        | 3.84 sec                                                              | 5.18 sec: 1.35x slower                                                |
| comprehensions             | 29.6 us                                                               | 40.4 us: 1.37x slower                                                 |
| crypto_pyaes               | 112 ms                                                                | 153 ms: 1.37x slower                                                  |
| bench_thread_pool          | 3.11 ms                                                               | 4.27 ms: 1.37x slower                                                 |
| thrift                     | 1.17 ms                                                               | 1.61 ms: 1.38x slower                                                 |
| pycparser                  | 1.73 sec                                                              | 2.43 sec: 1.40x slower                                                |
| tornado_http               | 262 ms                                                                | 369 ms: 1.40x slower                                                  |
| tomli_loads                | 2.99 sec                                                              | 4.26 sec: 1.43x slower                                                |
| fannkuch                   | 551 ms                                                                | 786 ms: 1.43x slower                                                  |
| sympy_integrate            | 31.4 ms                                                               | 44.8 ms: 1.43x slower                                                 |
| coroutines                 | 30.1 ms                                                               | 44.1 ms: 1.46x slower                                                 |
| python_startup_no_site     | 16.3 ms                                                               | 23.8 ms: 1.47x slower                                                 |
| html5lib                   | 95.8 ms                                                               | 141 ms: 1.47x slower                                                  |
| xml_etree_process          | 85.7 ms                                                               | 128 ms: 1.50x slower                                                  |
| telco                      | 9.71 ms                                                               | 14.6 ms: 1.50x slower                                                 |
| logging_format             | 11.8 us                                                               | 17.9 us: 1.51x slower                                                 |
| regex_compile              | 197 ms                                                                | 301 ms: 1.53x slower                                                  |
| genshi_xml                 | 73.6 ms                                                               | 114 ms: 1.55x slower                                                  |
| bpe_tokeniser              | 6.63 sec                                                              | 10.4 sec: 1.57x slower                                                |
| coverage                   | 97.6 ms                                                               | 154 ms: 1.58x slower                                                  |
| float                      | 127 ms                                                                | 202 ms: 1.59x slower                                                  |
| pyflate                    | 661 ms                                                                | 1.06 sec: 1.60x slower                                                |
| nqueens                    | 110 ms                                                                | 177 ms: 1.61x slower                                                  |
| 2to3                       | 444 ms                                                                | 721 ms: 1.62x slower                                                  |
| spectral_norm              | 158 ms                                                                | 260 ms: 1.65x slower                                                  |
| sqlglot_normalize          | 148 ms                                                                | 245 ms: 1.65x slower                                                  |
| python_startup             | 21.2 ms                                                               | 35.1 ms: 1.65x slower                                                 |
| scimark_monte_carlo        | 98.5 ms                                                               | 164 ms: 1.66x slower                                                  |
| typing_runtime_protocols   | 199 us                                                                | 334 us: 1.67x slower                                                  |
| logging_simple             | 9.89 us                                                               | 16.7 us: 1.68x slower                                                 |
| richards                   | 63.4 ms                                                               | 107 ms: 1.69x slower                                                  |
| sympy_str                  | 425 ms                                                                | 721 ms: 1.70x slower                                                  |
| django_template            | 48.6 ms                                                               | 82.9 ms: 1.71x slower                                                 |
| sqlglot_optimize           | 76.5 ms                                                               | 134 ms: 1.75x slower                                                  |
| pprint_safe_repr           | 970 ms                                                                | 1.70 sec: 1.75x slower                                                |
| mako                       | 17.2 ms                                                               | 30.3 ms: 1.76x slower                                                 |
| pprint_pformat             | 2.03 sec                                                              | 3.58 sec: 1.76x slower                                                |
| unpickle_pure_python       | 319 us                                                                | 581 us: 1.82x slower                                                  |
| raytrace                   | 418 ms                                                                | 764 ms: 1.83x slower                                                  |
| chaos                      | 93.7 ms                                                               | 172 ms: 1.84x slower                                                  |
| pickle_pure_python         | 447 us                                                                | 835 us: 1.87x slower                                                  |
| hexiom                     | 8.87 ms                                                               | 16.9 ms: 1.90x slower                                                 |
| sympy_expand               | 689 ms                                                                | 1.31 sec: 1.90x slower                                                |
| genshi_text                | 31.9 ms                                                               | 61.0 ms: 1.91x slower                                                 |
| logging_silent             | 135 ns                                                                | 262 ns: 1.94x slower                                                  |
| scimark_lu                 | 155 ms                                                                | 302 ms: 1.95x slower                                                  |
| go                         | 185 ms                                                                | 363 ms: 1.96x slower                                                  |
| sqlglot_parse              | 1.89 ms                                                               | 3.75 ms: 1.98x slower                                                 |
| sympy_sum                  | 229 ms                                                                | 460 ms: 2.01x slower                                                  |
| richards_super             | 67.9 ms                                                               | 137 ms: 2.01x slower                                                  |
| sqlglot_transpile          | 2.28 ms                                                               | 4.66 ms: 2.04x slower                                                 |
| scimark_sor                | 171 ms                                                                | 367 ms: 2.15x slower                                                  |
| deltablue                  | 5.05 ms                                                               | 11.4 ms: 2.25x slower                                                 |
| nbody                      | 125 ms                                                                | 286 ms: 2.29x slower                                                  |
| unpack_sequence            | 68.5 ns                                                               | 220 ns: 3.21x slower                                                  |
| Geometric mean             | (ref)                                                                 | 1.37x slower                                                          |

Benchmark hidden because not significant (7): pickle, regex_effbot, pickle_dict, xml_etree_parse, regex_dna, pidigits, asyncio_websockets
Ignored benchmarks (8) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 2.24x