# Results vs. 3.13.0rc2

- fork: python
- ref: 801cf3fcdd27d8b6dd0f
- machine: linux-x86_64
- commit hash: 801cf3f
- commit date: 2025-08-02
- overall geometric mean: 1.077x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 246 ms: 1.06x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.51 sec: 1.04x faster                                                |
| html5lib       | 67.0 ms                                                      | 57.9 ms: 1.16x faster                                                 |
| Geometric mean | (ref)                                                        | 1.08x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 296 ms: 1.56x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 605 ms: 1.51x faster                                                  |
| async_tree_io              | 876 ms                                                       | 587 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 470 ms: 1.42x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                  |
| async_tree_none            | 354 ms                                                       | 260 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 471 ms: 1.35x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 252 ms: 1.33x faster                                                  |
| async_generators           | 377 ms                                                       | 322 ms: 1.17x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.6 ms: 1.09x faster                                                 |
| asyncio_tcp                | 505 ms                                                       | 492 ms: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                          |

Benchmark hidden because not significant (1): asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 66.4 ms: 1.17x faster                                                 |
| pidigits       | 217 ms                                                       | 194 ms: 1.12x faster                                                  |
| nbody          | 85.1 ms                                                      | 78.6 ms: 1.08x faster                                                 |
| Geometric mean | (ref)                                                        | 1.12x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 119 ms: 1.11x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.5 ms: 1.05x faster                                                 |
| regex_effbot   | 3.08 ms                                                      | 3.11 ms: 1.01x slower                                                 |
| regex_dna      | 180 ms                                                       | 188 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.79 sec: 1.12x faster                                                |
| unpickle_list        | 4.71 us                                                      | 4.33 us: 1.09x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 79.9 ms: 1.07x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 55.6 ms: 1.07x faster                                                 |
| json_loads           | 27.0 us                                                      | 25.5 us: 1.06x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 200 us: 1.05x faster                                                  |
| pickle_dict          | 32.5 us                                                      | 32.3 us: 1.01x faster                                                 |
| pickle_pure_python   | 294 us                                                       | 296 us: 1.01x slower                                                  |
| pickle_list          | 4.93 us                                                      | 5.02 us: 1.02x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 10.8 ms: 1.02x slower                                                 |
| unpickle             | 14.3 us                                                      | 14.7 us: 1.03x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 145 ms: 1.07x slower                                                  |
| pickle               | 11.3 us                                                      | 13.0 us: 1.14x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.35 ms: 1.01x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.7 ms: 1.15x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 19.4 ms: 1.11x faster                                                 |
| genshi_xml      | 48.8 ms                                                      | 46.5 ms: 1.05x faster                                                 |
| django_template | 34.1 ms                                                      | 32.6 ms: 1.05x faster                                                 |
| Geometric mean  | (ref)                                                        | 1.05x faster                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.10 sec: 2.14x faster                                                |
| deepcopy                   | 355 us                                                       | 226 us: 1.57x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 296 ms: 1.56x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 605 ms: 1.51x faster                                                  |
| async_tree_io              | 876 ms                                                       | 587 ms: 1.49x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 26.5 us: 1.47x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 470 ms: 1.42x faster                                                  |
| go                         | 141 ms                                                       | 100 ms: 1.40x faster                                                  |
| spectral_norm              | 111 ms                                                       | 80.5 ms: 1.38x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                  |
| async_tree_none            | 354 ms                                                       | 260 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 471 ms: 1.35x faster                                                  |
| scimark_sor                | 134 ms                                                       | 100 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 252 ms: 1.33x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.42 us: 1.28x faster                                                 |
| logging_silent             | 103 ns                                                       | 82.2 ns: 1.25x faster                                                 |
| scimark_fft                | 349 ms                                                       | 283 ms: 1.23x faster                                                  |
| richards                   | 45.2 ms                                                      | 38.0 ms: 1.19x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 3.98 ms: 1.18x faster                                                 |
| richards_super             | 51.6 ms                                                      | 43.9 ms: 1.18x faster                                                 |
| async_generators           | 377 ms                                                       | 322 ms: 1.17x faster                                                  |
| pylint                     | 317 ms                                                       | 271 ms: 1.17x faster                                                  |
| float                      | 77.5 ms                                                      | 66.4 ms: 1.17x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 56.1 ms: 1.16x faster                                                 |
| chaos                      | 57.3 ms                                                      | 49.4 ms: 1.16x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 57.9 ms: 1.16x faster                                                 |
| pyflate                    | 449 ms                                                       | 394 ms: 1.14x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.31 ms: 1.13x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 66.5 ms: 1.13x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 100 ms: 1.13x faster                                                  |
| comprehensions             | 16.5 us                                                      | 14.6 us: 1.12x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.79 sec: 1.12x faster                                                |
| pidigits                   | 217 ms                                                       | 194 ms: 1.12x faster                                                  |
| coverage                   | 83.0 ms                                                      | 74.5 ms: 1.11x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 19.4 ms: 1.11x faster                                                 |
| regex_compile              | 132 ms                                                       | 119 ms: 1.11x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 17.9 ms: 1.10x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.04 sec: 1.10x faster                                                |
| coroutines                 | 23.6 ms                                                      | 21.6 ms: 1.09x faster                                                 |
| unpickle_list              | 4.71 us                                                      | 4.33 us: 1.09x faster                                                 |
| raytrace                   | 253 ms                                                       | 233 ms: 1.09x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 72.4 ms: 1.08x faster                                                 |
| nbody                      | 85.1 ms                                                      | 78.6 ms: 1.08x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 144 us: 1.08x faster                                                  |
| thrift                     | 778 us                                                       | 725 us: 1.07x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 79.9 ms: 1.07x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.0 ms: 1.07x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 55.6 ms: 1.07x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.79 us: 1.06x faster                                                 |
| json_loads                 | 27.0 us                                                      | 25.5 us: 1.06x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                                |
| 2to3                       | 260 ms                                                       | 246 ms: 1.06x faster                                                  |
| sympy_str                  | 275 ms                                                       | 260 ms: 1.06x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 147 ms: 1.05x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.5 ms: 1.05x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 700 ms: 1.05x faster                                                  |
| sympy_expand               | 457 ms                                                       | 435 ms: 1.05x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 200 us: 1.05x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.3 ms: 1.05x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 2.97 ms: 1.05x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.52 us: 1.05x faster                                                 |
| genshi_xml                 | 48.8 ms                                                      | 46.5 ms: 1.05x faster                                                 |
| django_template            | 34.1 ms                                                      | 32.6 ms: 1.05x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.51 sec: 1.04x faster                                                |
| pycparser                  | 1.12 sec                                                     | 1.08 sec: 1.04x faster                                                |
| asyncio_tcp                | 505 ms                                                       | 492 ms: 1.03x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 66.2 ms: 1.03x faster                                                 |
| fannkuch                   | 370 ms                                                       | 362 ms: 1.02x faster                                                  |
| pickle_dict                | 32.5 us                                                      | 32.3 us: 1.01x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.35 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| pickle_pure_python         | 294 us                                                       | 296 us: 1.01x slower                                                  |
| regex_effbot               | 3.08 ms                                                      | 3.11 ms: 1.01x slower                                                 |
| pickle_list                | 4.93 us                                                      | 5.02 us: 1.02x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 10.8 ms: 1.02x slower                                                 |
| unpickle                   | 14.3 us                                                      | 14.7 us: 1.03x slower                                                 |
| regex_dna                  | 180 ms                                                       | 188 ms: 1.04x slower                                                  |
| unpack_sequence            | 44.8 ns                                                      | 47.0 ns: 1.05x slower                                                 |
| xml_etree_parse            | 136 ms                                                       | 145 ms: 1.07x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.01 ms: 1.10x slower                                                 |
| pickle                     | 11.3 us                                                      | 13.0 us: 1.14x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.7 ms: 1.15x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.51 ms: 1.43x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 2.04 ms: 1.52x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 103 ms: 9.37x slower                                                  |
| telco                      | 7.82 ms                                                      | 155 ms: 19.76x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (6): sqlite_synth, xml_etree_iterparse, asyncio_tcp_ssl, meteor_contest, mako, json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250802-3.15.0a0-801cf3f-CLANG/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.077x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.17x