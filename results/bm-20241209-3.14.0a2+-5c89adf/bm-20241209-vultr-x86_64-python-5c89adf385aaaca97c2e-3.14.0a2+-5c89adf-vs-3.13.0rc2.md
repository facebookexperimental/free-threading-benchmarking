# Results vs. 3.13.0rc2

- fork: python
- ref: 5c89adf385aaaca97c2e
- machine: linux-x86_64
- commit hash: 5c89adf
- commit date: 2024-12-09
- overall geometric mean: 1.022x faster
- HPT reliability: 92.50%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 259 ms: 1.00x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                 |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 622 ms: 1.47x faster                                                   |
| async_tree_io              | 876 ms                                                       | 602 ms: 1.45x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 341 ms: 1.35x faster                                                   |
| async_tree_none            | 354 ms                                                       | 275 ms: 1.28x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 334 ms: 1.24x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 275 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 603 ms: 1.10x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 22.0 ms: 1.07x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 599 ms: 1.06x faster                                                   |
| async_generators           | 377 ms                                                       | 362 ms: 1.04x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.20x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 221 ms: 1.02x slower                                                   |
| float          | 77.5 ms                                                      | 79.3 ms: 1.02x slower                                                  |
| nbody          | 85.1 ms                                                      | 96.1 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                  |
| regex_compile  | 132 ms                                                       | 131 ms: 1.01x faster                                                   |
| regex_dna      | 180 ms                                                       | 179 ms: 1.01x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 25.2 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 24.9 us: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.0 ms: 1.04x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 215 us: 1.03x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.09 sec: 1.04x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 320 us: 1.09x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_generate, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 22.0 ms: 1.02x slower                                                  |
| mako            | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 50.4 ms: 1.03x slower                                                  |
| django_template | 34.1 ms                                                      | 35.8 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 622 ms: 1.47x faster                                                   |
| async_tree_io              | 876 ms                                                       | 602 ms: 1.45x faster                                                   |
| deepcopy                   | 355 us                                                       | 262 us: 1.35x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 341 ms: 1.35x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 30.1 us: 1.30x faster                                                  |
| async_tree_none            | 354 ms                                                       | 275 ms: 1.28x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 334 ms: 1.24x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 275 ms: 1.22x faster                                                   |
| go                         | 141 ms                                                       | 120 ms: 1.17x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.68 us: 1.16x faster                                                  |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 603 ms: 1.10x faster                                                   |
| json_loads                 | 27.0 us                                                      | 24.9 us: 1.08x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 22.0 ms: 1.07x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 599 ms: 1.06x faster                                                   |
| telco                      | 7.82 ms                                                      | 7.38 ms: 1.06x faster                                                  |
| json                       | 4.93 ms                                                      | 4.68 ms: 1.05x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.3 ms: 1.05x faster                                                  |
| coverage                   | 83.0 ms                                                      | 79.4 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.0 ms: 1.04x faster                                                  |
| async_generators           | 377 ms                                                       | 362 ms: 1.04x faster                                                   |
| thrift                     | 778 us                                                       | 750 us: 1.04x faster                                                   |
| spectral_norm              | 111 ms                                                       | 107 ms: 1.03x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.32 sec: 1.03x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 716 ms: 1.03x faster                                                   |
| meteor_contest             | 102 ms                                                       | 99.3 ms: 1.02x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.46 sec: 1.02x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 66.5 ms: 1.02x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                 |
| logging_simple             | 6.16 us                                                      | 6.06 us: 1.02x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.01x faster                                                   |
| regex_compile              | 132 ms                                                       | 131 ms: 1.01x faster                                                   |
| pyflate                    | 449 ms                                                       | 444 ms: 1.01x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 112 ms: 1.01x faster                                                   |
| regex_dna                  | 180 ms                                                       | 179 ms: 1.01x faster                                                   |
| logging_format             | 6.84 us                                                      | 6.79 us: 1.01x faster                                                  |
| 2to3                       | 260 ms                                                       | 259 ms: 1.00x faster                                                   |
| nqueens                    | 78.6 ms                                                      | 79.0 ms: 1.00x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.12 sec: 1.01x slower                                                 |
| generators                 | 28.8 ms                                                      | 29.0 ms: 1.01x slower                                                  |
| sympy_expand               | 457 ms                                                       | 461 ms: 1.01x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.76 ms: 1.01x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 76.0 ms: 1.02x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 20.1 ms: 1.02x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                   |
| pidigits                   | 217 ms                                                       | 221 ms: 1.02x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 22.0 ms: 1.02x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                  |
| float                      | 77.5 ms                                                      | 79.3 ms: 1.02x slower                                                  |
| richards_super             | 51.6 ms                                                      | 52.9 ms: 1.02x slower                                                  |
| richards                   | 45.2 ms                                                      | 46.3 ms: 1.02x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 215 us: 1.03x slower                                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 1.60 ms: 1.03x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 54.1 ms: 1.03x slower                                                  |
| chaos                      | 57.3 ms                                                      | 58.9 ms: 1.03x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.21 ms: 1.03x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 109 ms: 1.03x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 50.4 ms: 1.03x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.29 ms: 1.04x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.09 sec: 1.04x slower                                                 |
| django_template            | 34.1 ms                                                      | 35.8 ms: 1.05x slower                                                  |
| raytrace                   | 253 ms                                                       | 265 ms: 1.05x slower                                                   |
| logging_silent             | 103 ns                                                       | 108 ns: 1.05x slower                                                   |
| comprehensions             | 16.5 us                                                      | 17.5 us: 1.07x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 320 us: 1.09x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 25.2 ms: 1.11x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.13x slower                                                  |
| nbody                      | 85.1 ms                                                      | 96.1 ms: 1.13x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.69 ms: 1.27x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.02 ms: 1.28x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 86.0 ms: 7.82x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (10): mdp, xml_etree_generate, scimark_monte_carlo, hexiom, fannkuch, scimark_fft, sympy_str, scimark_sor, sqlite_synth, xml_etree_process
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 92.50% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x