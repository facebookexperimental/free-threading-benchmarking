# Results vs. 3.13.0rc2

- fork: maurycy
- ref: maurycy_tuple_early
- machine: linux-x86_64
- commit hash: 0eae50d
- commit date: 2025-12-02
- overall geometric mean: 1.043x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 247 ms: 1.05x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.02x faster                                                 |
| html5lib       | 67.0 ms                                                      | 61.7 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 552 ms: 1.59x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 589 ms: 1.55x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 304 ms: 1.52x faster                                                   |
| async_tree_none            | 354 ms                                                       | 244 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 484 ms: 1.38x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 485 ms: 1.32x faster                                                   |
| async_generators           | 377 ms                                                       | 341 ms: 1.11x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 68.6 ms: 1.13x faster                                                  |
| pidigits       | 217 ms                                                       | 203 ms: 1.07x faster                                                   |
| nbody          | 85.1 ms                                                      | 89.4 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.64 ms: 1.17x faster                                                  |
| regex_compile  | 132 ms                                                       | 124 ms: 1.06x faster                                                   |
| regex_dna      | 180 ms                                                       | 171 ms: 1.05x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 22.2 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.9 ms: 1.12x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 9.66 ms: 1.09x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.88 sec: 1.06x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 82.1 ms: 1.04x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.2 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 209 us: 1.00x faster                                                   |
| json_loads           | 27.0 us                                                      | 27.6 us: 1.02x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 305 us: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.25 ms: 1.02x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.7 ms: 1.04x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 48.2 ms: 1.01x faster                                                  |
| django_template | 34.1 ms                                                      | 34.8 ms: 1.02x slower                                                  |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.00x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.05x faster                                                 |
| async_tree_io              | 876 ms                                                       | 552 ms: 1.59x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 589 ms: 1.55x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 304 ms: 1.52x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.5 us: 1.47x faster                                                  |
| deepcopy                   | 355 us                                                       | 242 us: 1.47x faster                                                   |
| async_tree_none            | 354 ms                                                       | 244 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 484 ms: 1.38x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                   |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 485 ms: 1.32x faster                                                   |
| scimark_sor                | 134 ms                                                       | 107 ms: 1.25x faster                                                   |
| spectral_norm              | 111 ms                                                       | 90.9 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.58 us: 1.21x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.64 ms: 1.17x faster                                                  |
| scimark_fft                | 349 ms                                                       | 302 ms: 1.16x faster                                                   |
| float                      | 77.5 ms                                                      | 68.6 ms: 1.13x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.9 ms: 1.12x faster                                                  |
| async_generators           | 377 ms                                                       | 341 ms: 1.11x faster                                                   |
| pylint                     | 317 ms                                                       | 289 ms: 1.10x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 9.66 ms: 1.09x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.32 ms: 1.09x faster                                                  |
| richards_super             | 51.6 ms                                                      | 47.4 ms: 1.09x faster                                                  |
| richards                   | 45.2 ms                                                      | 41.6 ms: 1.09x faster                                                  |
| pyflate                    | 449 ms                                                       | 412 ms: 1.09x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 61.7 ms: 1.09x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 69.2 ms: 1.08x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.08x faster                                                  |
| pidigits                   | 217 ms                                                       | 203 ms: 1.07x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.2 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.17 sec: 1.06x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.88 sec: 1.06x faster                                                 |
| regex_compile              | 132 ms                                                       | 124 ms: 1.06x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.70 ms: 1.05x faster                                                  |
| regex_dna                  | 180 ms                                                       | 171 ms: 1.05x faster                                                   |
| 2to3                       | 260 ms                                                       | 247 ms: 1.05x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 703 ms: 1.05x faster                                                   |
| logging_silent             | 103 ns                                                       | 97.8 ns: 1.05x faster                                                  |
| comprehensions             | 16.5 us                                                      | 15.7 us: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 18.9 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.05x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 20.7 ms: 1.04x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 82.1 ms: 1.04x faster                                                  |
| thrift                     | 778 us                                                       | 758 us: 1.03x faster                                                   |
| generators                 | 28.8 ms                                                      | 28.1 ms: 1.02x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.02x faster                                                 |
| coverage                   | 83.0 ms                                                      | 81.2 ms: 1.02x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.02x faster                                                   |
| regex_v8                   | 22.7 ms                                                      | 22.2 ms: 1.02x faster                                                  |
| chaos                      | 57.3 ms                                                      | 56.2 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 58.2 ms: 1.02x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.25 ms: 1.02x faster                                                  |
| meteor_contest             | 102 ms                                                       | 100 ms: 1.02x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.10 sec: 1.01x faster                                                 |
| genshi_xml                 | 48.8 ms                                                      | 48.2 ms: 1.01x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 153 us: 1.01x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                   |
| logging_simple             | 6.16 us                                                      | 6.09 us: 1.01x faster                                                  |
| deltablue                  | 3.12 ms                                                      | 3.10 ms: 1.01x faster                                                  |
| raytrace                   | 253 ms                                                       | 250 ms: 1.01x faster                                                   |
| nqueens                    | 78.6 ms                                                      | 78.1 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 209 us: 1.00x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 68.2 ms: 1.00x slower                                                  |
| django_template            | 34.1 ms                                                      | 34.8 ms: 1.02x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.6 us: 1.02x slower                                                  |
| sympy_expand               | 457 ms                                                       | 467 ms: 1.02x slower                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.26 us: 1.02x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.00 us: 1.02x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 305 us: 1.04x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| nbody                      | 85.1 ms                                                      | 89.4 ms: 1.05x slower                                                  |
| fannkuch                   | 370 ms                                                       | 390 ms: 1.05x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.24 ms: 1.35x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.58 ms: 1.46x slower                                                  |
| telco                      | 7.82 ms                                                      | 156 ms: 19.98x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 247 ms: 22.51x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.00x faster                                                           |

Benchmark hidden because not significant (2): sympy_str, json
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251202-3.15.0a1+-0eae50d/bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.043x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.16x