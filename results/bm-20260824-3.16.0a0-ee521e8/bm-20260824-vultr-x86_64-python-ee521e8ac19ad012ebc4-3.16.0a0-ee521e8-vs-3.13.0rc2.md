# Results vs. 3.13.0rc2

- fork: python
- ref: ee521e8ac19ad012ebc4
- machine: linux-x86_64
- commit hash: ee521e8
- commit date: 2026-08-24
- overall geometric mean: 1.033x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 259 ms: 1.00x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.37 sec: 1.11x faster                                                |
| html5lib       | 67.0 ms                                                      | 59.5 ms: 1.13x faster                                                 |
| Geometric mean | (ref)                                                        | 1.08x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                       | 545 ms: 1.22x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 378 ms: 1.22x faster                                                  |
| async_tree_io              | 876 ms                                                       | 721 ms: 1.21x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 759 ms: 1.20x faster                                                  |
| async_tree_none            | 354 ms                                                       | 294 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 560 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 370 ms: 1.12x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 300 ms: 1.12x faster                                                  |
| async_generators           | 377 ms                                                       | 347 ms: 1.09x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.13x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 195 ms: 1.11x faster                                                  |
| float          | 77.5 ms                                                      | 73.3 ms: 1.06x faster                                                 |
| nbody          | 85.1 ms                                                      | 89.7 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.63 ms: 1.17x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 21.6 ms: 1.05x faster                                                 |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                  |
| regex_compile  | 132 ms                                                       | 149 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.43 ms: 1.12x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.82 sec: 1.10x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.6 ms: 1.05x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.01x slower                                                  |
| json_loads           | 27.0 us                                                      | 27.5 us: 1.02x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 87.6 ms: 1.03x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 302 us: 1.03x slower                                                  |
| xml_etree_parse      | 136 ms                                                       | 142 ms: 1.04x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 61.9 ms: 1.04x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.70 ms: 1.04x slower                                                 |
| python_startup         | 11.0 ms                                                      | 12.9 ms: 1.18x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 12.1 ms: 1.07x slower                                                 |
| django_template | 34.1 ms                                                      | 36.6 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.07x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 114 ms: 2.77x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.13 sec: 2.08x faster                                                |
| deepcopy                   | 355 us                                                       | 235 us: 1.51x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 26.6 us: 1.47x faster                                                 |
| go                         | 141 ms                                                       | 102 ms: 1.38x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 120 us: 1.29x faster                                                  |
| scimark_sor                | 134 ms                                                       | 105 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 545 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.55 us: 1.22x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 378 ms: 1.22x faster                                                  |
| async_tree_io              | 876 ms                                                       | 721 ms: 1.21x faster                                                  |
| spectral_norm              | 111 ms                                                       | 92.2 ms: 1.20x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 759 ms: 1.20x faster                                                  |
| async_tree_none            | 354 ms                                                       | 294 ms: 1.20x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.63 ms: 1.17x faster                                                 |
| pyflate                    | 449 ms                                                       | 386 ms: 1.16x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 560 ms: 1.14x faster                                                  |
| scimark_fft                | 349 ms                                                       | 308 ms: 1.14x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 59.5 ms: 1.13x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 370 ms: 1.12x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 300 ms: 1.12x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.43 ms: 1.12x faster                                                 |
| pidigits                   | 217 ms                                                       | 195 ms: 1.11x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 67.6 ms: 1.11x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.37 sec: 1.11x faster                                                |
| tomli_loads                | 2.01 sec                                                     | 1.82 sec: 1.10x faster                                                |
| pathlib                    | 19.2 ms                                                      | 17.6 ms: 1.09x faster                                                 |
| async_generators           | 377 ms                                                       | 347 ms: 1.09x faster                                                  |
| chaos                      | 57.3 ms                                                      | 52.9 ms: 1.08x faster                                                 |
| logging_silent             | 103 ns                                                       | 94.8 ns: 1.08x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 73.1 ms: 1.07x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.65 ms: 1.06x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.5 us: 1.06x faster                                                 |
| float                      | 77.5 ms                                                      | 73.3 ms: 1.06x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.4 ms: 1.05x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.6 ms: 1.05x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.23 sec: 1.05x faster                                                |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.6 ms: 1.05x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.0 ms: 1.04x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.2 ms: 1.03x faster                                                 |
| richards                   | 45.2 ms                                                      | 44.4 ms: 1.02x faster                                                 |
| logging_simple             | 6.16 us                                                      | 6.05 us: 1.02x faster                                                 |
| raytrace                   | 253 ms                                                       | 248 ms: 1.02x faster                                                  |
| richards_super             | 51.6 ms                                                      | 50.8 ms: 1.02x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 728 ms: 1.01x faster                                                  |
| fannkuch                   | 370 ms                                                       | 367 ms: 1.01x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.00x faster                                                  |
| 2to3                       | 260 ms                                                       | 259 ms: 1.00x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 68.2 ms: 1.00x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.12 sec: 1.00x slower                                                |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                 |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                  |
| thrift                     | 778 us                                                       | 788 us: 1.01x slower                                                  |
| sympy_str                  | 275 ms                                                       | 278 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.01x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 158 ms: 1.02x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.5 us: 1.02x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 115 ms: 1.02x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 87.6 ms: 1.03x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 302 us: 1.03x slower                                                  |
| coverage                   | 83.0 ms                                                      | 85.5 ms: 1.03x slower                                                 |
| sympy_expand               | 457 ms                                                       | 476 ms: 1.04x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 142 ms: 1.04x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.70 ms: 1.04x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 61.9 ms: 1.04x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.28 ms: 1.05x slower                                                 |
| nbody                      | 85.1 ms                                                      | 89.7 ms: 1.05x slower                                                 |
| mako                       | 11.3 ms                                                      | 12.1 ms: 1.07x slower                                                 |
| django_template            | 34.1 ms                                                      | 36.6 ms: 1.07x slower                                                 |
| regex_compile              | 132 ms                                                       | 149 ms: 1.13x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.60 ms: 1.15x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.9 ms: 1.18x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.70 ms: 1.27x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.34 ms: 1.46x slower                                                 |
| telco                      | 7.82 ms                                                      | 159 ms: 20.27x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 299 ms: 27.21x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (4): scimark_sparse_mat_mult, logging_format, json, sqlite_synth
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260824-3.16.0a0-ee521e8/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.033x faster

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x