# Results vs. 3.12.6

- fork: python
- ref: 6cddf04344a1e8ca9df5
- machine: linux-x86_64
- commit hash: 6cddf04
- commit date: 2025-12-14
- overall geometric mean: 1.129x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 247 ms: 1.07x faster                                                   |
| html5lib       | 63.6 ms                                                | 66.9 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 547 ms: 1.98x faster                                                   |
| async_tree_none            | 464 ms                                                 | 240 ms: 1.93x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 590 ms: 1.88x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 300 ms: 1.85x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 242 ms: 1.84x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.83x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 480 ms: 1.49x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                   |
| asyncio_tcp                | 519 ms                                                 | 442 ms: 1.17x faster                                                   |
| async_generators           | 384 ms                                                 | 358 ms: 1.07x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.47 sec: 1.03x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 58.9 ms: 1.37x faster                                                  |
| nbody          | 89.3 ms                                                | 71.5 ms: 1.25x faster                                                  |
| pidigits       | 184 ms                                                 | 195 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                  | 1.17x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                  |
| regex_compile  | 142 ms                                                 | 122 ms: 1.17x faster                                                   |
| regex_dna      | 168 ms                                                 | 167 ms: 1.01x faster                                                   |
| regex_v8       | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 182 us: 1.21x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 83.9 ms: 1.15x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 77.3 ms: 1.10x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 53.6 ms: 1.10x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.41 ms: 1.10x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| pickle_pure_python   | 308 us                                                 | 288 us: 1.07x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 1.98 sec: 1.07x faster                                                 |
| pickle_dict          | 31.8 us                                                | 31.6 us: 1.00x faster                                                  |
| unpickle             | 14.1 us                                                | 14.5 us: 1.03x slower                                                  |
| json_loads           | 26.5 us                                                | 27.6 us: 1.04x slower                                                  |
| pickle_list          | 4.77 us                                                | 5.06 us: 1.06x slower                                                  |
| unpickle_list        | 4.67 us                                                | 5.14 us: 1.10x slower                                                  |
| pickle               | 10.9 us                                                | 12.4 us: 1.13x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.32 ms: 1.02x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 21.2 ms: 1.08x faster                                                  |
| mako           | 11.0 ms                                                | 10.6 ms: 1.04x faster                                                  |
| genshi_xml     | 50.2 ms                                                | 53.0 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 19.7 ms: 2.34x faster                                                  |
| richards_super             | 51.9 ms                                                | 23.8 ms: 2.18x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 547 ms: 1.98x faster                                                   |
| async_tree_none            | 464 ms                                                 | 240 ms: 1.93x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 590 ms: 1.88x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 300 ms: 1.85x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 242 ms: 1.84x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.83x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.34 sec: 1.81x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 24.3 us: 1.66x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 480 ms: 1.49x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                   |
| deepcopy                   | 352 us                                                 | 237 us: 1.49x faster                                                   |
| go                         | 139 ms                                                 | 100 ms: 1.39x faster                                                   |
| float                      | 80.8 ms                                                | 58.9 ms: 1.37x faster                                                  |
| scimark_fft                | 342 ms                                                 | 249 ms: 1.37x faster                                                   |
| scimark_sor                | 130 ms                                                 | 97.7 ms: 1.33x faster                                                  |
| spectral_norm              | 110 ms                                                 | 85.3 ms: 1.29x faster                                                  |
| logging_silent             | 109 ns                                                 | 86.1 ns: 1.27x faster                                                  |
| deltablue                  | 3.45 ms                                                | 2.73 ms: 1.26x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 54.6 ms: 1.25x faster                                                  |
| nbody                      | 89.3 ms                                                | 71.5 ms: 1.25x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.5 ms: 1.23x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.50 us: 1.23x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.2 us: 1.22x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 182 us: 1.21x faster                                                   |
| pyflate                    | 448 ms                                                 | 371 ms: 1.21x faster                                                   |
| chaos                      | 62.8 ms                                                | 53.2 ms: 1.18x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.01 sec: 1.18x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 442 ms: 1.17x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                  |
| regex_compile              | 142 ms                                                 | 122 ms: 1.17x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 639 ms: 1.16x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 66.1 ms: 1.16x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 83.9 ms: 1.15x faster                                                  |
| raytrace                   | 299 ms                                                 | 260 ms: 1.15x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.33 sec: 1.15x faster                                                 |
| generators                 | 32.2 ms                                                | 28.1 ms: 1.15x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.82 us: 1.14x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 103 ms: 1.10x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 77.3 ms: 1.10x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 53.6 ms: 1.10x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.41 ms: 1.10x faster                                                  |
| logging_format             | 7.35 us                                                | 6.70 us: 1.10x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 73.0 ms: 1.08x faster                                                  |
| thrift                     | 791 us                                                 | 735 us: 1.08x faster                                                   |
| genshi_text                | 22.8 ms                                                | 21.2 ms: 1.08x faster                                                  |
| async_generators           | 384 ms                                                 | 358 ms: 1.07x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| pickle_pure_python         | 308 us                                                 | 288 us: 1.07x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.98 sec: 1.07x faster                                                 |
| 2to3                       | 264 ms                                                 | 247 ms: 1.07x faster                                                   |
| meteor_contest             | 104 ms                                                 | 97.9 ms: 1.06x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 156 us: 1.05x faster                                                   |
| pylint                     | 319 ms                                                 | 305 ms: 1.04x faster                                                   |
| mako                       | 11.0 ms                                                | 10.6 ms: 1.04x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.25 ms: 1.03x faster                                                  |
| json                       | 5.02 ms                                                | 4.89 ms: 1.03x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.47 sec: 1.03x faster                                                 |
| fannkuch                   | 372 ms                                                 | 363 ms: 1.03x faster                                                   |
| hexiom                     | 6.17 ms                                                | 6.08 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                  |
| regex_dna                  | 168 ms                                                 | 167 ms: 1.01x faster                                                   |
| pickle_dict                | 31.8 us                                                | 31.6 us: 1.00x faster                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.32 ms: 1.02x slower                                                  |
| unpickle                   | 14.1 us                                                | 14.5 us: 1.03x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.6 us: 1.04x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| html5lib                   | 63.6 ms                                                | 66.9 ms: 1.05x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 53.0 ms: 1.06x slower                                                  |
| pidigits                   | 184 ms                                                 | 195 ms: 1.06x slower                                                   |
| pickle_list                | 4.77 us                                                | 5.06 us: 1.06x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                  |
| nqueens                    | 80.1 ms                                                | 85.9 ms: 1.07x slower                                                  |
| unpickle_list              | 4.67 us                                                | 5.14 us: 1.10x slower                                                  |
| pickle                     | 10.9 us                                                | 12.4 us: 1.13x slower                                                  |
| coverage                   | 71.4 ms                                                | 81.2 ms: 1.14x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.48 ms: 1.30x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.32 ms: 1.40x slower                                                  |
| unpack_sequence            | 52.1 ns                                                | 81.2 ns: 1.56x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.71x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 238 ms: 22.06x slower                                                  |
| telco                      | 6.53 ms                                                | 162 ms: 24.81x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (2): sqlite_synth, django_template
Ignored benchmarks (18) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, docutils, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, sympy_expand, sympy_integrate, sympy_str, sympy_sum, tornado_http
Ignored benchmarks (10) of results/bm-20251214-3.15.0a2+-6cddf04-JIT/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2+-6cddf04.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.129x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.20x