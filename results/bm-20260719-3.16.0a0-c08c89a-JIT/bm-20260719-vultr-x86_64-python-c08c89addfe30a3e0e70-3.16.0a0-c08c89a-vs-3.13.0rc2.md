# Results vs. 3.13.0rc2

- fork: python
- ref: c08c89addfe30a3e0e70
- machine: linux-x86_64
- commit hash: c08c89a
- commit date: 2026-07-19
- overall geometric mean: 1.134x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 257 ms: 1.01x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.50 sec: 1.05x faster                                                |
| html5lib       | 67.0 ms                                                      | 59.9 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 347 ms: 1.33x faster                                                  |
| async_tree_none            | 354 ms                                                       | 266 ms: 1.33x faster                                                  |
| async_tree_io              | 876 ms                                                       | 680 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 520 ms: 1.28x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 722 ms: 1.26x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 341 ms: 1.21x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 282 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 537 ms: 1.19x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 450 ms: 1.12x faster                                                  |
| async_generators           | 377 ms                                                       | 352 ms: 1.07x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.45 sec: 1.04x faster                                                |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.16x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 55.8 ms: 1.39x faster                                                 |
| nbody          | 85.1 ms                                                      | 63.6 ms: 1.34x faster                                                 |
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| Geometric mean | (ref)                                                        | 1.30x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.64 ms: 1.17x faster                                                 |
| regex_dna      | 180 ms                                                       | 166 ms: 1.08x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.5 ms: 1.05x faster                                                 |
| regex_compile  | 132 ms                                                       | 143 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.13 ms: 1.15x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 182 us: 1.15x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.79 sec: 1.12x faster                                                |
| pickle_pure_python   | 294 us                                                       | 266 us: 1.11x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 86.7 ms: 1.09x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 55.4 ms: 1.07x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 81.3 ms: 1.05x faster                                                 |
| json_loads           | 27.0 us                                                      | 26.6 us: 1.01x faster                                                 |
| unpickle             | 14.3 us                                                      | 14.7 us: 1.02x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 141 ms: 1.04x slower                                                  |
| pickle_dict          | 32.5 us                                                      | 34.6 us: 1.06x slower                                                 |
| unpickle_list        | 4.71 us                                                      | 5.29 us: 1.12x slower                                                 |
| pickle_list          | 4.93 us                                                      | 5.64 us: 1.15x slower                                                 |
| pickle               | 11.3 us                                                      | 13.2 us: 1.16x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.15 ms: 1.03x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.1 ms: 1.12x faster                                                 |
| django_template | 34.1 ms                                                      | 38.7 ms: 1.14x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 112 ms: 2.82x faster                                                  |
| richards_super             | 51.6 ms                                                      | 20.3 ms: 2.55x faster                                                 |
| richards                   | 45.2 ms                                                      | 18.2 ms: 2.48x faster                                                 |
| mdp                        | 2.36 sec                                                     | 1.23 sec: 1.92x faster                                                |
| deepcopy_memo              | 39.1 us                                                      | 21.7 us: 1.80x faster                                                 |
| scimark_sor                | 134 ms                                                       | 77.8 ms: 1.73x faster                                                 |
| spectral_norm              | 111 ms                                                       | 68.6 ms: 1.62x faster                                                 |
| deepcopy                   | 355 us                                                       | 231 us: 1.54x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 106 us: 1.46x faster                                                  |
| go                         | 141 ms                                                       | 99.0 ms: 1.42x faster                                                 |
| float                      | 77.5 ms                                                      | 55.8 ms: 1.39x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 81.7 ms: 1.38x faster                                                 |
| scimark_fft                | 349 ms                                                       | 259 ms: 1.35x faster                                                  |
| nbody                      | 85.1 ms                                                      | 63.6 ms: 1.34x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 347 ms: 1.33x faster                                                  |
| async_tree_none            | 354 ms                                                       | 266 ms: 1.33x faster                                                  |
| pyflate                    | 449 ms                                                       | 345 ms: 1.30x faster                                                  |
| async_tree_io              | 876 ms                                                       | 680 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 520 ms: 1.28x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 51.4 ms: 1.27x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 722 ms: 1.26x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.54 us: 1.22x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 341 ms: 1.21x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 64.9 ms: 1.21x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 615 ms: 1.20x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 282 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 537 ms: 1.19x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.26 sec: 1.18x faster                                                |
| chaos                      | 57.3 ms                                                      | 48.4 ms: 1.18x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 2.65 ms: 1.18x faster                                                 |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.24 us: 1.18x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.64 ms: 1.17x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.13 ms: 1.15x faster                                                 |
| comprehensions             | 16.5 us                                                      | 14.3 us: 1.15x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 182 us: 1.15x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 16.9 ms: 1.14x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.04 us: 1.13x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 3.93 sec: 1.13x faster                                                |
| asyncio_tcp                | 505 ms                                                       | 450 ms: 1.12x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.79 sec: 1.12x faster                                                |
| fannkuch                   | 370 ms                                                       | 331 ms: 1.12x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 59.9 ms: 1.12x faster                                                 |
| mako                       | 11.3 ms                                                      | 10.1 ms: 1.12x faster                                                 |
| pickle_pure_python         | 294 us                                                       | 266 us: 1.11x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.29 ms: 1.10x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 86.7 ms: 1.09x faster                                                 |
| regex_dna                  | 180 ms                                                       | 166 ms: 1.08x faster                                                  |
| async_generators           | 377 ms                                                       | 352 ms: 1.07x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 55.4 ms: 1.07x faster                                                 |
| logging_silent             | 103 ns                                                       | 96.3 ns: 1.07x faster                                                 |
| meteor_contest             | 102 ms                                                       | 95.9 ms: 1.06x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.5 ms: 1.05x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.68 ms: 1.05x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 71.1 ms: 1.05x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 81.3 ms: 1.05x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 64.7 ms: 1.05x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.50 sec: 1.05x faster                                                |
| sqlite_synth               | 2.21 us                                                      | 2.11 us: 1.05x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.45 sec: 1.04x faster                                                |
| python_startup_no_site     | 7.39 ms                                                      | 7.15 ms: 1.03x faster                                                 |
| raytrace                   | 253 ms                                                       | 247 ms: 1.02x faster                                                  |
| json                       | 4.93 ms                                                      | 4.85 ms: 1.02x faster                                                 |
| json_loads                 | 27.0 us                                                      | 26.6 us: 1.01x faster                                                 |
| 2to3                       | 260 ms                                                       | 257 ms: 1.01x faster                                                  |
| coverage                   | 83.0 ms                                                      | 83.4 ms: 1.01x slower                                                 |
| thrift                     | 778 us                                                       | 784 us: 1.01x slower                                                  |
| unpickle                   | 14.3 us                                                      | 14.7 us: 1.02x slower                                                 |
| xml_etree_parse            | 136 ms                                                       | 141 ms: 1.04x slower                                                  |
| sympy_str                  | 275 ms                                                       | 286 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                                 |
| generators                 | 28.8 ms                                                      | 30.5 ms: 1.06x slower                                                 |
| pickle_dict                | 32.5 us                                                      | 34.6 us: 1.06x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 167 ms: 1.07x slower                                                  |
| regex_compile              | 132 ms                                                       | 143 ms: 1.08x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.53 ms: 1.12x slower                                                 |
| unpickle_list              | 4.71 us                                                      | 5.29 us: 1.12x slower                                                 |
| django_template            | 34.1 ms                                                      | 38.7 ms: 1.14x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                 |
| pickle_list                | 4.93 us                                                      | 5.64 us: 1.15x slower                                                 |
| pickle                     | 11.3 us                                                      | 13.2 us: 1.16x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.63 ms: 1.22x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.44x slower                                                 |
| unpack_sequence            | 44.8 ns                                                      | 65.8 ns: 1.47x slower                                                 |
| telco                      | 7.82 ms                                                      | 136 ms: 17.35x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 197 ms: 17.94x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                          |

Benchmark hidden because not significant (3): sympy_integrate, sympy_expand, pycparser
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260719-3.16.0a0-c08c89a-JIT/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.134x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.19x