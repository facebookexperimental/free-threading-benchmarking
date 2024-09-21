# Results vs. 3.13.0rc2

- fork: python
- ref: b2afe2aae487ebf89897
- machine: linux-x86_64
- commit hash: b2afe2a
- commit date: 2024-09-12
- overall geometric mean: 1.45x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.33x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 721 ms: 1.62x slower                                                  |
| docutils       | 4.01 sec                                                     | 5.09 sec: 1.27x slower                                                |
| html5lib       | 92.6 ms                                                      | 141 ms: 1.52x slower                                                  |
| tornado_http   | 251 ms                                                       | 369 ms: 1.47x slower                                                  |
| Geometric mean | (ref)                                                        | 1.46x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.26 sec: 1.11x faster                                                |
| async_tree_memoization     | 709 ms                                                       | 750 ms: 1.06x slower                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 906 ms: 1.06x slower                                                  |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.12 sec: 1.12x slower                                                |
| async_tree_none            | 572 ms                                                       | 647 ms: 1.13x slower                                                  |
| asyncio_tcp                | 948 ms                                                       | 1.19 sec: 1.25x slower                                                |
| async_generators           | 567 ms                                                       | 726 ms: 1.28x slower                                                  |
| coroutines                 | 30.9 ms                                                      | 44.1 ms: 1.43x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                          |

Benchmark hidden because not significant (5): async_tree_memoization_tg, async_tree_io, async_tree_none_tg, async_tree_cpu_io_mixed, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 116 ms                                                       | 202 ms: 1.74x slower                                                  |
| nbody          | 119 ms                                                       | 286 ms: 2.41x slower                                                  |
| Geometric mean | (ref)                                                        | 1.63x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 36.2 ms: 1.10x slower                                                 |
| regex_compile  | 182 ms                                                       | 301 ms: 1.65x slower                                                  |
| Geometric mean | (ref)                                                        | 1.18x slower                                                          |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle               | 15.1 us                                                      | 14.5 us: 1.05x faster                                                 |
| unpickle_list        | 6.68 us                                                      | 7.76 us: 1.16x slower                                                 |
| unpickle             | 20.5 us                                                      | 24.2 us: 1.18x slower                                                 |
| json_loads           | 34.3 us                                                      | 42.8 us: 1.25x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 18.0 ms: 1.28x slower                                                 |
| xml_etree_generate   | 122 ms                                                       | 165 ms: 1.35x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 128 ms: 1.50x slower                                                  |
| tomli_loads          | 2.78 sec                                                     | 4.26 sec: 1.53x slower                                                |
| unpickle_pure_python | 290 us                                                       | 581 us: 2.00x slower                                                  |
| pickle_pure_python   | 416 us                                                       | 835 us: 2.00x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.26x slower                                                          |

Benchmark hidden because not significant (4): xml_etree_iterparse, pickle_dict, xml_etree_parse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 23.8 ms: 1.55x slower                                                 |
| python_startup         | 22.4 ms                                                      | 35.1 ms: 1.57x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.56x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 114 ms: 1.58x slower                                                  |
| django_template | 44.3 ms                                                      | 82.9 ms: 1.87x slower                                                 |
| mako            | 15.9 ms                                                      | 30.3 ms: 1.90x slower                                                 |
| genshi_text     | 31.7 ms                                                      | 61.0 ms: 1.93x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.82x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| create_gc_cycles           | 2.41 ms                                                      | 1.83 ms: 1.32x faster                                                 |
| gc_traversal               | 5.70 ms                                                      | 4.51 ms: 1.26x faster                                                 |
| bench_mp_pool              | 18.7 ms                                                      | 16.5 ms: 1.13x faster                                                 |
| async_tree_io_tg           | 1.40 sec                                                     | 1.26 sec: 1.11x faster                                                |
| pickle                     | 15.1 us                                                      | 14.5 us: 1.05x faster                                                 |
| async_tree_memoization     | 709 ms                                                       | 750 ms: 1.06x slower                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 906 ms: 1.06x slower                                                  |
| regex_v8                   | 32.8 ms                                                      | 36.2 ms: 1.10x slower                                                 |
| sqlite_synth               | 3.99 us                                                      | 4.43 us: 1.11x slower                                                 |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.12 sec: 1.12x slower                                                |
| async_tree_none            | 572 ms                                                       | 647 ms: 1.13x slower                                                  |
| unpickle_list              | 6.68 us                                                      | 7.76 us: 1.16x slower                                                 |
| unpickle                   | 20.5 us                                                      | 24.2 us: 1.18x slower                                                 |
| deepcopy                   | 498 us                                                       | 595 us: 1.19x slower                                                  |
| telco                      | 12.2 ms                                                      | 14.6 ms: 1.20x slower                                                 |
| pathlib                    | 29.9 ms                                                      | 36.3 ms: 1.21x slower                                                 |
| json_loads                 | 34.3 us                                                      | 42.8 us: 1.25x slower                                                 |
| json                       | 6.51 ms                                                      | 8.13 ms: 1.25x slower                                                 |
| asyncio_tcp                | 948 ms                                                       | 1.19 sec: 1.25x slower                                                |
| docutils                   | 4.01 sec                                                     | 5.09 sec: 1.27x slower                                                |
| json_dumps                 | 14.1 ms                                                      | 18.0 ms: 1.28x slower                                                 |
| async_generators           | 567 ms                                                       | 726 ms: 1.28x slower                                                  |
| meteor_contest             | 150 ms                                                       | 199 ms: 1.33x slower                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.99 ms: 1.33x slower                                                 |
| pylint                     | 470 ms                                                       | 627 ms: 1.33x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 125 ms: 1.34x slower                                                  |
| scimark_fft                | 473 ms                                                       | 636 ms: 1.34x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 165 ms: 1.35x slower                                                  |
| mdp                        | 3.80 sec                                                     | 5.18 sec: 1.36x slower                                                |
| deepcopy_reduce            | 4.10 us                                                      | 5.61 us: 1.37x slower                                                 |
| generators                 | 40.0 ms                                                      | 56.1 ms: 1.40x slower                                                 |
| deepcopy_memo              | 50.1 us                                                      | 71.2 us: 1.42x slower                                                 |
| coroutines                 | 30.9 ms                                                      | 44.1 ms: 1.43x slower                                                 |
| fannkuch                   | 547 ms                                                       | 786 ms: 1.44x slower                                                  |
| coverage                   | 107 ms                                                       | 154 ms: 1.44x slower                                                  |
| thrift                     | 1.10 ms                                                      | 1.61 ms: 1.47x slower                                                 |
| tornado_http               | 251 ms                                                       | 369 ms: 1.47x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 4.27 ms: 1.48x slower                                                 |
| typing_runtime_protocols   | 226 us                                                       | 334 us: 1.48x slower                                                  |
| sympy_integrate            | 30.2 ms                                                      | 44.8 ms: 1.48x slower                                                 |
| xml_etree_process          | 85.9 ms                                                      | 128 ms: 1.50x slower                                                  |
| html5lib                   | 92.6 ms                                                      | 141 ms: 1.52x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 153 ms: 1.53x slower                                                  |
| tomli_loads                | 2.78 sec                                                     | 4.26 sec: 1.53x slower                                                |
| pycparser                  | 1.57 sec                                                     | 2.43 sec: 1.55x slower                                                |
| python_startup_no_site     | 15.3 ms                                                      | 23.8 ms: 1.55x slower                                                 |
| python_startup             | 22.4 ms                                                      | 35.1 ms: 1.57x slower                                                 |
| nqueens                    | 112 ms                                                       | 177 ms: 1.58x slower                                                  |
| genshi_xml                 | 72.1 ms                                                      | 114 ms: 1.58x slower                                                  |
| pyflate                    | 664 ms                                                       | 1.06 sec: 1.59x slower                                                |
| 2to3                       | 445 ms                                                       | 721 ms: 1.62x slower                                                  |
| richards                   | 65.5 ms                                                      | 107 ms: 1.64x slower                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 10.4 sec: 1.65x slower                                                |
| regex_compile              | 182 ms                                                       | 301 ms: 1.65x slower                                                  |
| spectral_norm              | 157 ms                                                       | 260 ms: 1.66x slower                                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.70 sec: 1.72x slower                                                |
| float                      | 116 ms                                                       | 202 ms: 1.74x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 245 ms: 1.75x slower                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 134 ms: 1.79x slower                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 164 ms: 1.81x slower                                                  |
| comprehensions             | 22.2 us                                                      | 40.4 us: 1.82x slower                                                 |
| pprint_pformat             | 1.94 sec                                                     | 3.58 sec: 1.84x slower                                                |
| richards_super             | 73.2 ms                                                      | 137 ms: 1.86x slower                                                  |
| django_template            | 44.3 ms                                                      | 82.9 ms: 1.87x slower                                                 |
| go                         | 191 ms                                                       | 363 ms: 1.90x slower                                                  |
| sympy_str                  | 379 ms                                                       | 721 ms: 1.90x slower                                                  |
| mako                       | 15.9 ms                                                      | 30.3 ms: 1.90x slower                                                 |
| genshi_text                | 31.7 ms                                                      | 61.0 ms: 1.93x slower                                                 |
| logging_format             | 9.24 us                                                      | 17.9 us: 1.93x slower                                                 |
| logging_simple             | 8.56 us                                                      | 16.7 us: 1.94x slower                                                 |
| unpickle_pure_python       | 290 us                                                       | 581 us: 2.00x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 835 us: 2.00x slower                                                  |
| logging_silent             | 130 ns                                                       | 262 ns: 2.02x slower                                                  |
| scimark_sor                | 179 ms                                                       | 367 ms: 2.06x slower                                                  |
| chaos                      | 83.6 ms                                                      | 172 ms: 2.06x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 302 ms: 2.06x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 16.9 ms: 2.08x slower                                                 |
| sqlglot_transpile          | 2.20 ms                                                      | 4.66 ms: 2.12x slower                                                 |
| sqlglot_parse              | 1.76 ms                                                      | 3.75 ms: 2.14x slower                                                 |
| sympy_expand               | 601 ms                                                       | 1.31 sec: 2.18x slower                                                |
| sympy_sum                  | 210 ms                                                       | 460 ms: 2.19x slower                                                  |
| raytrace                   | 344 ms                                                       | 764 ms: 2.22x slower                                                  |
| nbody                      | 119 ms                                                       | 286 ms: 2.41x slower                                                  |
| deltablue                  | 4.44 ms                                                      | 11.4 ms: 2.56x slower                                                 |
| unpack_sequence            | 74.3 ns                                                      | 220 ns: 2.96x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.45x slower                                                          |

Benchmark hidden because not significant (12): xml_etree_iterparse, async_tree_memoization_tg, async_tree_io, async_tree_none_tg, pickle_dict, xml_etree_parse, pickle_list, pidigits, regex_dna, async_tree_cpu_io_mixed, asyncio_websockets, regex_effbot
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.38x
- 95% likely to have a slowdown of 1.37x
- 99% likely to have a slowdown of 1.33x

# Memory
- memory change: 1.15x