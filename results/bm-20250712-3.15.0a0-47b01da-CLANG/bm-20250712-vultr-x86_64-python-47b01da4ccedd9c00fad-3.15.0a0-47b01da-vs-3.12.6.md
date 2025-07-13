# Results vs. 3.12.6

- fork: python
- ref: 47b01da4ccedd9c00fad
- machine: linux-x86_64
- commit hash: 47b01da
- commit date: 2025-07-12
- overall geometric mean: 1.119x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 245 ms: 1.08x faster                                                  |
| docutils       | 2.64 sec                                               | 2.50 sec: 1.06x faster                                                |
| html5lib       | 63.6 ms                                                | 56.9 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                  | 1.08x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 246 ms: 1.89x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 574 ms: 1.89x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 300 ms: 1.87x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 599 ms: 1.85x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 302 ms: 1.84x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 473 ms: 1.51x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 479 ms: 1.51x faster                                                  |
| async_generators           | 384 ms                                                 | 318 ms: 1.21x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.8 ms: 1.10x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 496 ms: 1.05x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                          |

Benchmark hidden because not significant (2): asyncio_tcp_ssl, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 67.0 ms: 1.21x faster                                                 |
| nbody          | 89.3 ms                                                | 80.4 ms: 1.11x faster                                                 |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 118 ms: 1.21x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 3.06 ms: 1.03x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                 |
| regex_dna      | 168 ms                                                 | 187 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.79 sec: 1.18x faster                                                |
| unpickle_pure_python | 221 us                                                 | 197 us: 1.12x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 55.0 ms: 1.07x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 79.8 ms: 1.07x faster                                                 |
| json_loads           | 26.5 us                                                | 25.0 us: 1.06x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 295 us: 1.04x faster                                                  |
| unpickle_list        | 4.67 us                                                | 4.51 us: 1.04x faster                                                 |
| pickle_dict          | 31.8 us                                                | 30.9 us: 1.03x faster                                                 |
| pickle_list          | 4.77 us                                                | 4.90 us: 1.03x slower                                                 |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| unpickle             | 14.1 us                                                | 14.7 us: 1.04x slower                                                 |
| xml_etree_parse      | 139 ms                                                 | 149 ms: 1.07x slower                                                  |
| pickle               | 10.9 us                                                | 12.9 us: 1.18x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.36 ms: 1.03x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 19.1 ms: 1.19x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 46.6 ms: 1.08x faster                                                 |
| django_template | 34.7 ms                                                | 32.7 ms: 1.06x faster                                                 |
| mako            | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.07x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.08 sec: 2.24x faster                                                |
| async_tree_none            | 464 ms                                                 | 246 ms: 1.89x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 574 ms: 1.89x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 300 ms: 1.87x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 599 ms: 1.85x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 302 ms: 1.84x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                  |
| deepcopy                   | 352 us                                                 | 227 us: 1.55x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 26.5 us: 1.52x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 473 ms: 1.51x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 479 ms: 1.51x faster                                                  |
| go                         | 139 ms                                                 | 97.7 ms: 1.43x faster                                                 |
| comprehensions             | 19.8 us                                                | 14.1 us: 1.40x faster                                                 |
| logging_silent             | 109 ns                                                 | 79.0 ns: 1.38x faster                                                 |
| spectral_norm              | 110 ms                                                 | 80.2 ms: 1.37x faster                                                 |
| raytrace                   | 299 ms                                                 | 231 ms: 1.30x faster                                                  |
| scimark_sor                | 130 ms                                                 | 101 ms: 1.29x faster                                                  |
| chaos                      | 62.8 ms                                                | 48.9 ms: 1.29x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.42 us: 1.27x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 54.6 ms: 1.25x faster                                                 |
| richards                   | 45.9 ms                                                | 37.3 ms: 1.23x faster                                                 |
| deltablue                  | 3.45 ms                                                | 2.84 ms: 1.21x faster                                                 |
| async_generators           | 384 ms                                                 | 318 ms: 1.21x faster                                                  |
| regex_compile              | 142 ms                                                 | 118 ms: 1.21x faster                                                  |
| float                      | 80.8 ms                                                | 67.0 ms: 1.21x faster                                                 |
| richards_super             | 51.9 ms                                                | 43.4 ms: 1.20x faster                                                 |
| genshi_text                | 22.8 ms                                                | 19.1 ms: 1.19x faster                                                 |
| scimark_fft                | 342 ms                                                 | 287 ms: 1.19x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.3 ms: 1.19x faster                                                 |
| pylint                     | 319 ms                                                 | 269 ms: 1.18x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.01 sec: 1.18x faster                                                |
| tomli_loads                | 2.11 sec                                               | 1.79 sec: 1.18x faster                                                |
| generators                 | 32.2 ms                                                | 27.5 ms: 1.17x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.28 ms: 1.17x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 98.6 ms: 1.16x faster                                                 |
| pyflate                    | 448 ms                                                 | 389 ms: 1.15x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.8 ms: 1.15x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.78 us: 1.15x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 17.9 ms: 1.15x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 66.9 ms: 1.14x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 146 ms: 1.14x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 144 us: 1.14x faster                                                  |
| sympy_str                  | 292 ms                                                 | 258 ms: 1.13x faster                                                  |
| logging_format             | 7.35 us                                                | 6.50 us: 1.13x faster                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 3.90 ms: 1.12x faster                                                 |
| thrift                     | 791 us                                                 | 705 us: 1.12x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 197 us: 1.12x faster                                                  |
| html5lib                   | 63.6 ms                                                | 56.9 ms: 1.12x faster                                                 |
| unpack_sequence            | 52.1 ns                                                | 46.8 ns: 1.11x faster                                                 |
| nbody                      | 89.3 ms                                                | 80.4 ms: 1.11x faster                                                 |
| nqueens                    | 80.1 ms                                                | 72.9 ms: 1.10x faster                                                 |
| coroutines                 | 23.9 ms                                                | 21.8 ms: 1.10x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.39 sec: 1.09x faster                                                |
| sympy_expand               | 468 ms                                                 | 433 ms: 1.08x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 689 ms: 1.08x faster                                                  |
| 2to3                       | 264 ms                                                 | 245 ms: 1.08x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 46.6 ms: 1.08x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 55.0 ms: 1.07x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 79.8 ms: 1.07x faster                                                 |
| json_loads                 | 26.5 us                                                | 25.0 us: 1.06x faster                                                 |
| django_template            | 34.7 ms                                                | 32.7 ms: 1.06x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.50 sec: 1.06x faster                                                |
| json                       | 5.02 ms                                                | 4.80 ms: 1.05x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 496 ms: 1.05x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 295 us: 1.04x faster                                                  |
| meteor_contest             | 104 ms                                                 | 99.5 ms: 1.04x faster                                                 |
| unpickle_list              | 4.67 us                                                | 4.51 us: 1.04x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 3.06 ms: 1.03x faster                                                 |
| pickle_dict                | 31.8 us                                                | 30.9 us: 1.03x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.02x faster                                                |
| fannkuch                   | 372 ms                                                 | 371 ms: 1.00x faster                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.36 ms: 1.03x slower                                                 |
| pickle_list                | 4.77 us                                                | 4.90 us: 1.03x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| unpickle                   | 14.1 us                                                | 14.7 us: 1.04x slower                                                 |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                 |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                 |
| coverage                   | 71.4 ms                                                | 76.1 ms: 1.07x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.00 ms: 1.07x slower                                                 |
| xml_etree_parse            | 139 ms                                                 | 149 ms: 1.07x slower                                                  |
| regex_dna                  | 168 ms                                                 | 187 ms: 1.12x slower                                                  |
| pickle                     | 10.9 us                                                | 12.9 us: 1.18x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.38 ms: 1.27x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 2.03 ms: 1.86x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 101 ms: 9.36x slower                                                  |
| telco                      | 6.53 ms                                                | 155 ms: 23.68x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                          |

Benchmark hidden because not significant (4): sqlite_synth, xml_etree_iterparse, asyncio_tcp_ssl, asyncio_websockets
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250712-3.15.0a0-47b01da-CLANG/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.119x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.18x