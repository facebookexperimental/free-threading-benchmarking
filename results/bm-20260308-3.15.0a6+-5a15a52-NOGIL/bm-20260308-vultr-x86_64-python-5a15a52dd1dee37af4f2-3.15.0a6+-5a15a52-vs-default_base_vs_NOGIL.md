# Results vs. default_base_vs_NOGIL

- fork: python
- ref: 5a15a52dd1dee37af4f2
- machine: linux-x86_64
- commit hash: 5a15a52
- commit date: 2026-03-08
- overall geometric mean: 1.098x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                 | 281 ms: 1.12x slower                                                   |
| docutils       | 2.54 sec                                                               | 2.73 sec: 1.08x slower                                                 |
| html5lib       | 59.9 ms                                                                | 65.9 ms: 1.10x slower                                                  |
| sphinx         | 966 ms                                                                 | 1.05 sec: 1.09x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets         | 544 ms                                                                 | 514 ms: 1.06x faster                                                   |
| async_tree_io_tg           | 567 ms                                                                 | 590 ms: 1.04x slower                                                   |
| async_tree_io              | 590 ms                                                                 | 628 ms: 1.06x slower                                                   |
| async_tree_memoization_tg  | 301 ms                                                                 | 323 ms: 1.07x slower                                                   |
| async_tree_none_tg         | 240 ms                                                                 | 262 ms: 1.09x slower                                                   |
| async_generators           | 339 ms                                                                 | 372 ms: 1.10x slower                                                   |
| async_tree_cpu_io_mixed_tg | 509 ms                                                                 | 570 ms: 1.12x slower                                                   |
| async_tree_memoization     | 310 ms                                                                 | 353 ms: 1.14x slower                                                   |
| async_tree_none            | 247 ms                                                                 | 282 ms: 1.14x slower                                                   |
| async_tree_cpu_io_mixed    | 503 ms                                                                 | 598 ms: 1.19x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 198 ms                                                                 | 203 ms: 1.03x slower                                                   |
| float          | 70.4 ms                                                                | 72.5 ms: 1.03x slower                                                  |
| nbody          | 92.9 ms                                                                | 123 ms: 1.32x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 22.6 ms                                                                | 20.9 ms: 1.08x faster                                                  |
| regex_dna      | 173 ms                                                                 | 169 ms: 1.02x faster                                                   |
| regex_effbot   | 2.73 ms                                                                | 2.87 ms: 1.05x slower                                                  |
| regex_compile  | 124 ms                                                                 | 142 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 84.6 ms                                                                | 89.2 ms: 1.05x slower                                                  |
| tomli_loads          | 1.83 sec                                                               | 1.94 sec: 1.06x slower                                                 |
| pickle_pure_python   | 309 us                                                                 | 330 us: 1.07x slower                                                   |
| json_loads           | 28.5 us                                                                | 31.4 us: 1.10x slower                                                  |
| unpickle_pure_python | 211 us                                                                 | 234 us: 1.11x slower                                                   |
| json_dumps           | 9.94 ms                                                                | 11.1 ms: 1.12x slower                                                  |
| xml_etree_generate   | 84.0 ms                                                                | 96.0 ms: 1.14x slower                                                  |
| xml_etree_process    | 59.0 ms                                                                | 69.1 ms: 1.17x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                | 16.0 ms: 1.26x slower                                                  |
| python_startup_no_site | 7.44 ms                                                                | 9.79 ms: 1.32x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.29x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.7 ms                                                                | 54.2 ms: 1.09x slower                                                  |
| django_template | 34.7 ms                                                                | 40.4 ms: 1.17x slower                                                  |
| genshi_text     | 21.2 ms                                                                | 25.6 ms: 1.21x slower                                                  |
| mako            | 12.0 ms                                                                | 15.8 ms: 1.32x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.19x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| bench_mp_pool              | 270 ms                                                                 | 7.08 ms: 38.15x faster                                                 |
| gc_traversal               | 4.02 ms                                                                | 1.93 ms: 2.08x faster                                                  |
| create_gc_cycles           | 1.89 ms                                                                | 1.47 ms: 1.29x faster                                                  |
| sqlite_synth               | 2.23 us                                                                | 1.91 us: 1.17x faster                                                  |
| regex_v8                   | 22.6 ms                                                                | 20.9 ms: 1.08x faster                                                  |
| asyncio_websockets         | 544 ms                                                                 | 514 ms: 1.06x faster                                                   |
| logging_silent             | 102 ns                                                                 | 98.9 ns: 1.03x faster                                                  |
| regex_dna                  | 173 ms                                                                 | 169 ms: 1.02x faster                                                   |
| pycparser                  | 1.13 sec                                                               | 1.11 sec: 1.01x faster                                                 |
| pathlib                    | 17.4 ms                                                                | 17.7 ms: 1.01x slower                                                  |
| pidigits                   | 198 ms                                                                 | 203 ms: 1.03x slower                                                   |
| json                       | 5.15 ms                                                                | 5.29 ms: 1.03x slower                                                  |
| float                      | 70.4 ms                                                                | 72.5 ms: 1.03x slower                                                  |
| dulwich_log                | 67.5 ms                                                                | 69.8 ms: 1.03x slower                                                  |
| async_tree_io_tg           | 567 ms                                                                 | 590 ms: 1.04x slower                                                   |
| pylint                     | 287 ms                                                                 | 300 ms: 1.05x slower                                                   |
| bpe_tokeniser              | 4.12 sec                                                               | 4.33 sec: 1.05x slower                                                 |
| regex_effbot               | 2.73 ms                                                                | 2.87 ms: 1.05x slower                                                  |
| xml_etree_iterparse        | 84.6 ms                                                                | 89.2 ms: 1.05x slower                                                  |
| deltablue                  | 3.31 ms                                                                | 3.49 ms: 1.06x slower                                                  |
| tomli_loads                | 1.83 sec                                                               | 1.94 sec: 1.06x slower                                                 |
| async_tree_io              | 590 ms                                                                 | 628 ms: 1.06x slower                                                   |
| pickle_pure_python         | 309 us                                                                 | 330 us: 1.07x slower                                                   |
| sympy_expand               | 487 ms                                                                 | 522 ms: 1.07x slower                                                   |
| async_tree_memoization_tg  | 301 ms                                                                 | 323 ms: 1.07x slower                                                   |
| docutils                   | 2.54 sec                                                               | 2.73 sec: 1.08x slower                                                 |
| scimark_fft                | 314 ms                                                                 | 340 ms: 1.08x slower                                                   |
| many_optionals             | 934 us                                                                 | 1.02 ms: 1.09x slower                                                  |
| async_tree_none_tg         | 240 ms                                                                 | 262 ms: 1.09x slower                                                   |
| sphinx                     | 966 ms                                                                 | 1.05 sec: 1.09x slower                                                 |
| genshi_xml                 | 49.7 ms                                                                | 54.2 ms: 1.09x slower                                                  |
| async_generators           | 339 ms                                                                 | 372 ms: 1.10x slower                                                   |
| telco                      | 159 ms                                                                 | 174 ms: 1.10x slower                                                   |
| html5lib                   | 59.9 ms                                                                | 65.9 ms: 1.10x slower                                                  |
| json_loads                 | 28.5 us                                                                | 31.4 us: 1.10x slower                                                  |
| subparsers                 | 9.19 ms                                                                | 10.2 ms: 1.11x slower                                                  |
| pprint_safe_repr           | 714 ms                                                                 | 791 ms: 1.11x slower                                                   |
| unpickle_pure_python       | 211 us                                                                 | 234 us: 1.11x slower                                                   |
| sympy_str                  | 280 ms                                                                 | 313 ms: 1.12x slower                                                   |
| json_dumps                 | 9.94 ms                                                                | 11.1 ms: 1.12x slower                                                  |
| async_tree_cpu_io_mixed_tg | 509 ms                                                                 | 570 ms: 1.12x slower                                                   |
| sqlglot_v2_optimize        | 51.0 ms                                                                | 57.2 ms: 1.12x slower                                                  |
| pprint_pformat             | 1.45 sec                                                               | 1.63 sec: 1.12x slower                                                 |
| 2to3                       | 250 ms                                                                 | 281 ms: 1.12x slower                                                   |
| comprehensions             | 16.2 us                                                                | 18.3 us: 1.13x slower                                                  |
| sympy_sum                  | 160 ms                                                                 | 180 ms: 1.13x slower                                                   |
| chaos                      | 54.1 ms                                                                | 61.3 ms: 1.13x slower                                                  |
| sqlglot_v2_normalize       | 102 ms                                                                 | 115 ms: 1.13x slower                                                   |
| sympy_integrate            | 19.4 ms                                                                | 22.1 ms: 1.14x slower                                                  |
| regex_compile              | 124 ms                                                                 | 142 ms: 1.14x slower                                                   |
| async_tree_memoization     | 310 ms                                                                 | 353 ms: 1.14x slower                                                   |
| go                         | 105 ms                                                                 | 119 ms: 1.14x slower                                                   |
| hexiom                     | 5.67 ms                                                                | 6.47 ms: 1.14x slower                                                  |
| async_tree_none            | 247 ms                                                                 | 282 ms: 1.14x slower                                                   |
| pyflate                    | 406 ms                                                                 | 463 ms: 1.14x slower                                                   |
| xml_etree_generate         | 84.0 ms                                                                | 96.0 ms: 1.14x slower                                                  |
| mdp                        | 1.15 sec                                                               | 1.32 sec: 1.14x slower                                                 |
| scimark_sparse_mat_mult    | 4.63 ms                                                                | 5.30 ms: 1.14x slower                                                  |
| logging_simple             | 5.88 us                                                                | 6.74 us: 1.15x slower                                                  |
| scimark_sor                | 106 ms                                                                 | 121 ms: 1.15x slower                                                   |
| deepcopy                   | 232 us                                                                 | 267 us: 1.15x slower                                                   |
| nqueens                    | 75.1 ms                                                                | 87.1 ms: 1.16x slower                                                  |
| logging_format             | 6.58 us                                                                | 7.64 us: 1.16x slower                                                  |
| scimark_lu                 | 109 ms                                                                 | 127 ms: 1.17x slower                                                   |
| django_template            | 34.7 ms                                                                | 40.4 ms: 1.17x slower                                                  |
| generators                 | 27.9 ms                                                                | 32.6 ms: 1.17x slower                                                  |
| deepcopy_reduce            | 2.55 us                                                                | 2.98 us: 1.17x slower                                                  |
| xml_etree_process          | 59.0 ms                                                                | 69.1 ms: 1.17x slower                                                  |
| k_core                     | 1.88 sec                                                               | 2.21 sec: 1.18x slower                                                 |
| raytrace                   | 251 ms                                                                 | 296 ms: 1.18x slower                                                   |
| thrift                     | 776 us                                                                 | 918 us: 1.18x slower                                                   |
| async_tree_cpu_io_mixed    | 503 ms                                                                 | 598 ms: 1.19x slower                                                   |
| fannkuch                   | 378 ms                                                                 | 452 ms: 1.19x slower                                                   |
| deepcopy_memo              | 26.3 us                                                                | 31.5 us: 1.20x slower                                                  |
| sqlglot_v2_transpile       | 1.50 ms                                                                | 1.80 ms: 1.20x slower                                                  |
| spectral_norm              | 92.9 ms                                                                | 112 ms: 1.20x slower                                                   |
| meteor_contest             | 101 ms                                                                 | 122 ms: 1.20x slower                                                   |
| genshi_text                | 21.2 ms                                                                | 25.6 ms: 1.21x slower                                                  |
| sqlglot_v2_parse           | 1.21 ms                                                                | 1.46 ms: 1.21x slower                                                  |
| richards                   | 42.2 ms                                                                | 52.0 ms: 1.23x slower                                                  |
| shortest_path              | 431 ms                                                                 | 532 ms: 1.24x slower                                                   |
| bench_thread_pool          | 1.31 ms                                                                | 1.62 ms: 1.24x slower                                                  |
| typing_runtime_protocols   | 160 us                                                                 | 198 us: 1.24x slower                                                   |
| scimark_monte_carlo        | 62.6 ms                                                                | 77.9 ms: 1.25x slower                                                  |
| connected_components       | 392 ms                                                                 | 490 ms: 1.25x slower                                                   |
| python_startup             | 12.6 ms                                                                | 16.0 ms: 1.26x slower                                                  |
| richards_super             | 47.7 ms                                                                | 60.7 ms: 1.27x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 87.5 ms: 1.28x slower                                                  |
| python_startup_no_site     | 7.44 ms                                                                | 9.79 ms: 1.32x slower                                                  |
| mako                       | 12.0 ms                                                                | 15.8 ms: 1.32x slower                                                  |
| nbody                      | 92.9 ms                                                                | 123 ms: 1.32x slower                                                   |
| coverage                   | 83.2 ms                                                                | 113 ms: 1.35x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.07x slower                                                           |

Benchmark hidden because not significant (2): coroutines, xml_etree_parse
Ignored benchmarks (8) of results/bm-20260307-3.15.0a6+-149c465/bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.098x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.20x