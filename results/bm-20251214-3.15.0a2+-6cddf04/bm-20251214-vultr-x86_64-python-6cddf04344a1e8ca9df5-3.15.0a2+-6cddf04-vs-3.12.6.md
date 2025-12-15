# Results vs. 3.12.6

- fork: python
- ref: 6cddf04344a1e8ca9df5
- machine: linux-x86_64
- commit hash: 6cddf04
- commit date: 2025-12-14
- overall geometric mean: 1.077x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 244 ms: 1.08x faster                                                   |
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                 |
| html5lib       | 63.6 ms                                                | 59.2 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 543 ms: 2.00x faster                                                   |
| async_tree_none            | 464 ms                                                 | 239 ms: 1.94x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 581 ms: 1.91x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 242 ms: 1.85x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 301 ms: 1.84x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 522 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 521 ms: 1.37x faster                                                   |
| asyncio_tcp                | 519 ms                                                 | 450 ms: 1.15x faster                                                   |
| async_generators           | 384 ms                                                 | 343 ms: 1.12x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.45 sec: 1.04x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.8 ms: 1.16x faster                                                  |
| pidigits       | 184 ms                                                 | 215 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 122 ms: 1.17x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                  |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                                   |
| regex_v8       | 20.6 ms                                                | 22.4 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 83.8 ms: 1.15x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                   |
| json_dumps           | 10.4 ms                                                | 9.84 ms: 1.05x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 211 us: 1.04x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 82.0 ms: 1.04x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 57.5 ms: 1.03x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 306 us: 1.00x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                 |
| pickle_dict          | 31.8 us                                                | 32.5 us: 1.02x slower                                                  |
| json_loads           | 26.5 us                                                | 27.5 us: 1.04x slower                                                  |
| pickle_list          | 4.77 us                                                | 5.28 us: 1.11x slower                                                  |
| unpickle_list        | 4.67 us                                                | 5.20 us: 1.11x slower                                                  |
| pickle               | 10.9 us                                                | 12.7 us: 1.16x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.24 ms: 1.01x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.3 ms: 1.24x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.9 ms: 1.09x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 49.2 ms: 1.02x faster                                                  |
| django_template | 34.7 ms                                                | 35.6 ms: 1.03x slower                                                  |
| mako            | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.11x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 543 ms: 2.00x faster                                                   |
| async_tree_none            | 464 ms                                                 | 239 ms: 1.94x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 581 ms: 1.91x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 242 ms: 1.85x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 301 ms: 1.84x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.3 us: 1.53x faster                                                  |
| deepcopy                   | 352 us                                                 | 237 us: 1.49x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 522 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 521 ms: 1.37x faster                                                   |
| go                         | 139 ms                                                 | 106 ms: 1.32x faster                                                   |
| unpack_sequence            | 52.1 ns                                                | 41.5 ns: 1.26x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.8 us: 1.25x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.4 ms: 1.24x faster                                                  |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.21x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.56 us: 1.20x faster                                                  |
| raytrace                   | 299 ms                                                 | 252 ms: 1.19x faster                                                   |
| generators                 | 32.2 ms                                                | 27.4 ms: 1.18x faster                                                  |
| spectral_norm              | 110 ms                                                 | 93.9 ms: 1.17x faster                                                  |
| regex_compile              | 142 ms                                                 | 122 ms: 1.17x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 68.1 ms: 1.16x faster                                                  |
| float                      | 80.8 ms                                                | 69.8 ms: 1.16x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 83.8 ms: 1.15x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 450 ms: 1.15x faster                                                   |
| chaos                      | 62.8 ms                                                | 55.1 ms: 1.14x faster                                                  |
| scimark_fft                | 342 ms                                                 | 300 ms: 1.14x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.84 us: 1.14x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.18 sec: 1.13x faster                                                 |
| pylint                     | 319 ms                                                 | 281 ms: 1.13x faster                                                   |
| async_generators           | 384 ms                                                 | 343 ms: 1.12x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 68.7 ms: 1.12x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.55 ms: 1.11x faster                                                  |
| logging_format             | 7.35 us                                                | 6.66 us: 1.10x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 18.7 ms: 1.10x faster                                                  |
| richards                   | 45.9 ms                                                | 42.1 ms: 1.09x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.9 ms: 1.09x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 62.9 ms: 1.09x faster                                                  |
| pyflate                    | 448 ms                                                 | 413 ms: 1.09x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 685 ms: 1.09x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.40 sec: 1.08x faster                                                 |
| richards_super             | 51.9 ms                                                | 47.8 ms: 1.08x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                                   |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                                   |
| 2to3                       | 264 ms                                                 | 244 ms: 1.08x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 152 us: 1.08x faster                                                   |
| html5lib                   | 63.6 ms                                                | 59.2 ms: 1.07x faster                                                  |
| sympy_str                  | 292 ms                                                 | 272 ms: 1.07x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 107 ms: 1.07x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.06x faster                                                 |
| json_dumps                 | 10.4 ms                                                | 9.84 ms: 1.05x faster                                                  |
| thrift                     | 791 us                                                 | 758 us: 1.04x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 211 us: 1.04x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.31 ms: 1.04x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.45 sec: 1.04x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 82.0 ms: 1.04x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 57.5 ms: 1.03x faster                                                  |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.02x faster                                                   |
| genshi_xml                 | 50.2 ms                                                | 49.2 ms: 1.02x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                  |
| nqueens                    | 80.1 ms                                                | 78.8 ms: 1.02x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.35 ms: 1.01x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 306 us: 1.00x faster                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.24 ms: 1.01x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                 |
| pickle_dict                | 31.8 us                                                | 32.5 us: 1.02x slower                                                  |
| django_template            | 34.7 ms                                                | 35.6 ms: 1.03x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.5 us: 1.04x slower                                                  |
| fannkuch                   | 372 ms                                                 | 388 ms: 1.04x slower                                                   |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                                   |
| sqlite_synth               | 2.20 us                                                | 2.33 us: 1.06x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.4 ms: 1.09x slower                                                  |
| pickle_list                | 4.77 us                                                | 5.28 us: 1.11x slower                                                  |
| unpickle_list              | 4.67 us                                                | 5.20 us: 1.11x slower                                                  |
| coverage                   | 71.4 ms                                                | 82.0 ms: 1.15x slower                                                  |
| pickle                     | 10.9 us                                                | 12.7 us: 1.16x slower                                                  |
| pidigits                   | 184 ms                                                 | 215 ms: 1.17x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.3 ms: 1.24x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.43 ms: 1.28x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.31 ms: 1.39x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                  |
| telco                      | 6.53 ms                                                | 159 ms: 24.41x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 329 ms: 30.48x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (4): json, unpickle, sympy_expand, nbody
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20251214-3.15.0a2+-6cddf04/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.077x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x