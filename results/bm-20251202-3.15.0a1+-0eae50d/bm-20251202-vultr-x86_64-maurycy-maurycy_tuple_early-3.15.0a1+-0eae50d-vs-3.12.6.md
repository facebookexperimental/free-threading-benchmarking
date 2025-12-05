# Results vs. 3.12.6

- fork: maurycy
- ref: maurycy_tuple_early
- machine: linux-x86_64
- commit hash: 0eae50d
- commit date: 2025-12-02
- overall geometric mean: 1.079x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 247 ms: 1.06x faster                                                   |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                 |
| html5lib       | 63.6 ms                                                | 61.7 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 552 ms: 1.96x faster                                                   |
| async_tree_none            | 464 ms                                                 | 244 ms: 1.90x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 589 ms: 1.89x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 304 ms: 1.83x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.81x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 484 ms: 1.48x faster                                                   |
| async_generators           | 384 ms                                                 | 341 ms: 1.13x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.52x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 68.6 ms: 1.18x faster                                                  |
| pidigits       | 184 ms                                                 | 203 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.64 ms: 1.20x faster                                                  |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                                   |
| regex_v8       | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.9 ms: 1.14x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.88 sec: 1.12x faster                                                 |
| json_dumps           | 10.4 ms                                                | 9.66 ms: 1.07x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.05x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 82.1 ms: 1.04x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 58.2 ms: 1.01x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 305 us: 1.01x faster                                                   |
| json_loads           | 26.5 us                                                | 27.6 us: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.25 ms: 1.01x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 48.2 ms: 1.04x faster                                                  |
| django_template | 34.7 ms                                                | 34.8 ms: 1.00x slower                                                  |
| mako            | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.11x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 552 ms: 1.96x faster                                                   |
| async_tree_none            | 464 ms                                                 | 244 ms: 1.90x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 589 ms: 1.89x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 304 ms: 1.83x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.81x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.5 us: 1.52x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 484 ms: 1.48x faster                                                   |
| deepcopy                   | 352 us                                                 | 242 us: 1.45x faster                                                   |
| go                         | 139 ms                                                 | 105 ms: 1.32x faster                                                   |
| comprehensions             | 19.8 us                                                | 15.7 us: 1.26x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.21x faster                                                  |
| spectral_norm              | 110 ms                                                 | 90.9 ms: 1.21x faster                                                  |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.21x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.64 ms: 1.20x faster                                                  |
| raytrace                   | 299 ms                                                 | 250 ms: 1.19x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.58 us: 1.19x faster                                                  |
| float                      | 80.8 ms                                                | 68.6 ms: 1.18x faster                                                  |
| generators                 | 32.2 ms                                                | 28.1 ms: 1.15x faster                                                  |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 69.2 ms: 1.14x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 84.9 ms: 1.14x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.17 sec: 1.13x faster                                                 |
| scimark_fft                | 342 ms                                                 | 302 ms: 1.13x faster                                                   |
| async_generators           | 384 ms                                                 | 341 ms: 1.13x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 68.2 ms: 1.12x faster                                                  |
| chaos                      | 62.8 ms                                                | 56.2 ms: 1.12x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.88 sec: 1.12x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 61.2 ms: 1.12x faster                                                  |
| logging_silent             | 109 ns                                                 | 97.8 ns: 1.11x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.10 ms: 1.11x faster                                                  |
| richards                   | 45.9 ms                                                | 41.6 ms: 1.11x faster                                                  |
| pylint                     | 319 ms                                                 | 289 ms: 1.10x faster                                                   |
| genshi_text                | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                  |
| richards_super             | 51.9 ms                                                | 47.4 ms: 1.09x faster                                                  |
| logging_simple             | 6.63 us                                                | 6.09 us: 1.09x faster                                                  |
| pyflate                    | 448 ms                                                 | 412 ms: 1.09x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 18.9 ms: 1.08x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.70 ms: 1.08x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 9.66 ms: 1.07x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 153 us: 1.07x faster                                                   |
| sympy_str                  | 292 ms                                                 | 273 ms: 1.07x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| 2to3                       | 264 ms                                                 | 247 ms: 1.06x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.06x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 703 ms: 1.06x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.05x faster                                                   |
| logging_format             | 7.35 us                                                | 7.00 us: 1.05x faster                                                  |
| thrift                     | 791 us                                                 | 758 us: 1.04x faster                                                   |
| genshi_xml                 | 50.2 ms                                                | 48.2 ms: 1.04x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 82.1 ms: 1.04x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                   |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                 |
| html5lib                   | 63.6 ms                                                | 61.7 ms: 1.03x faster                                                  |
| nqueens                    | 80.1 ms                                                | 78.1 ms: 1.03x faster                                                  |
| json                       | 5.02 ms                                                | 4.93 ms: 1.02x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.32 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 58.2 ms: 1.01x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 305 us: 1.01x faster                                                   |
| django_template            | 34.7 ms                                                | 34.8 ms: 1.00x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.25 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                  |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                                   |
| sqlite_synth               | 2.20 us                                                | 2.26 us: 1.03x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.6 us: 1.04x slower                                                  |
| fannkuch                   | 372 ms                                                 | 390 ms: 1.05x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                  |
| pidigits                   | 184 ms                                                 | 203 ms: 1.10x slower                                                   |
| coverage                   | 71.4 ms                                                | 81.2 ms: 1.14x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.24 ms: 1.31x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.58 ms: 1.33x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.70x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 247 ms: 22.92x slower                                                  |
| telco                      | 6.53 ms                                                | 156 ms: 23.95x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (2): sympy_expand, nbody
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251202-3.15.0a1+-0eae50d/bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1+-0eae50d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.079x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.17x