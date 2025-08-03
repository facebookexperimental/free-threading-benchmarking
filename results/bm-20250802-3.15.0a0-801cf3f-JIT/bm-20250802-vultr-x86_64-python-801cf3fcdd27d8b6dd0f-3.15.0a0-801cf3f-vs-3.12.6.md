# Results vs. 3.12.6

- fork: python
- ref: 801cf3fcdd27d8b6dd0f
- machine: linux-x86_64
- commit hash: 801cf3f
- commit date: 2025-08-02
- overall geometric mean: 1.074x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                                  |
| docutils       | 2.64 sec                                               | 2.62 sec: 1.01x faster                                                |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 618 ms: 1.75x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 638 ms: 1.74x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 257 ms: 1.74x faster                                                  |
| async_tree_none            | 464 ms                                                 | 272 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 534 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 533 ms: 1.34x faster                                                  |
| async_generators           | 384 ms                                                 | 363 ms: 1.06x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 502 ms: 1.03x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.52 sec: 1.00x slower                                                |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 65.0 ms: 1.24x faster                                                 |
| nbody          | 89.3 ms                                                | 86.9 ms: 1.03x faster                                                 |
| pidigits       | 184 ms                                                 | 230 ms: 1.25x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                 |
| regex_v8       | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                 |
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.77 sec: 1.19x faster                                                |
| unpickle_pure_python | 221 us                                                 | 189 us: 1.17x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 54.1 ms: 1.09x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 78.3 ms: 1.09x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 93.4 ms: 1.03x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 305 us: 1.01x faster                                                  |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.04x slower                                                 |
| pickle_dict          | 31.8 us                                                | 33.0 us: 1.04x slower                                                 |
| json_loads           | 26.5 us                                                | 29.0 us: 1.09x slower                                                 |
| unpickle_list        | 4.67 us                                                | 5.11 us: 1.09x slower                                                 |
| pickle_list          | 4.77 us                                                | 5.27 us: 1.11x slower                                                 |
| pickle               | 10.9 us                                                | 12.6 us: 1.15x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.29 ms: 1.02x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                 |
| mako           | 11.0 ms                                                | 10.7 ms: 1.02x faster                                                 |
| genshi_xml     | 50.2 ms                                                | 49.6 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.16 sec: 2.08x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 618 ms: 1.75x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 638 ms: 1.74x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 257 ms: 1.74x faster                                                  |
| async_tree_none            | 464 ms                                                 | 272 ms: 1.71x faster                                                  |
| richards                   | 45.9 ms                                                | 29.7 ms: 1.55x faster                                                 |
| richards_super             | 51.9 ms                                                | 34.3 ms: 1.51x faster                                                 |
| deepcopy                   | 352 us                                                 | 256 us: 1.38x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.3 us: 1.37x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 534 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 533 ms: 1.34x faster                                                  |
| spectral_norm              | 110 ms                                                 | 84.9 ms: 1.30x faster                                                 |
| go                         | 139 ms                                                 | 111 ms: 1.26x faster                                                  |
| float                      | 80.8 ms                                                | 65.0 ms: 1.24x faster                                                 |
| deltablue                  | 3.45 ms                                                | 2.83 ms: 1.22x faster                                                 |
| comprehensions             | 19.8 us                                                | 16.3 us: 1.21x faster                                                 |
| scimark_fft                | 342 ms                                                 | 282 ms: 1.21x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 3.97 sec: 1.19x faster                                                |
| tomli_loads                | 2.11 sec                                               | 1.77 sec: 1.19x faster                                                |
| scimark_sor                | 130 ms                                                 | 110 ms: 1.17x faster                                                  |
| raytrace                   | 299 ms                                                 | 256 ms: 1.17x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 189 us: 1.17x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 67.7 ms: 1.16x faster                                                 |
| pyflate                    | 448 ms                                                 | 389 ms: 1.15x faster                                                  |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 59.9 ms: 1.14x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 68.1 ms: 1.12x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.74 us: 1.12x faster                                                 |
| pylint                     | 319 ms                                                 | 285 ms: 1.12x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                 |
| generators                 | 32.2 ms                                                | 29.2 ms: 1.11x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.11x faster                                                 |
| chaos                      | 62.8 ms                                                | 56.9 ms: 1.10x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                 |
| logging_silent             | 109 ns                                                 | 100.0 ns: 1.09x faster                                                |
| xml_etree_process          | 59.0 ms                                                | 54.1 ms: 1.09x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 78.3 ms: 1.09x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.11 us: 1.09x faster                                                 |
| unpack_sequence            | 52.1 ns                                                | 48.3 ns: 1.08x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.41 sec: 1.08x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 692 ms: 1.07x faster                                                  |
| logging_format             | 7.35 us                                                | 6.85 us: 1.07x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 156 ms: 1.07x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.3 ms: 1.07x faster                                                 |
| async_generators           | 384 ms                                                 | 363 ms: 1.06x faster                                                  |
| sympy_str                  | 292 ms                                                 | 275 ms: 1.06x faster                                                  |
| meteor_contest             | 104 ms                                                 | 98.1 ms: 1.06x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.87 ms: 1.05x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 157 us: 1.04x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 93.4 ms: 1.03x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 502 ms: 1.03x faster                                                  |
| 2to3                       | 264 ms                                                 | 255 ms: 1.03x faster                                                  |
| thrift                     | 791 us                                                 | 768 us: 1.03x faster                                                  |
| nbody                      | 89.3 ms                                                | 86.9 ms: 1.03x faster                                                 |
| mako                       | 11.0 ms                                                | 10.7 ms: 1.02x faster                                                 |
| nqueens                    | 80.1 ms                                                | 78.6 ms: 1.02x faster                                                 |
| fannkuch                   | 372 ms                                                 | 367 ms: 1.02x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.01x faster                                                |
| genshi_xml                 | 50.2 ms                                                | 49.6 ms: 1.01x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 305 us: 1.01x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.62 sec: 1.01x faster                                                |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.52 sec: 1.00x slower                                                |
| sympy_expand               | 468 ms                                                 | 473 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.23 us: 1.01x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.29 ms: 1.02x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.04x slower                                                 |
| pickle_dict                | 31.8 us                                                | 33.0 us: 1.04x slower                                                 |
| json                       | 5.02 ms                                                | 5.22 ms: 1.04x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.64 ms: 1.06x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                 |
| json_loads                 | 26.5 us                                                | 29.0 us: 1.09x slower                                                 |
| unpickle_list              | 4.67 us                                                | 5.11 us: 1.09x slower                                                 |
| pickle_list                | 4.77 us                                                | 5.27 us: 1.11x slower                                                 |
| regex_dna                  | 168 ms                                                 | 186 ms: 1.11x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.12x slower                                                 |
| coverage                   | 71.4 ms                                                | 81.8 ms: 1.15x slower                                                 |
| pickle                     | 10.9 us                                                | 12.6 us: 1.15x slower                                                 |
| pidigits                   | 184 ms                                                 | 230 ms: 1.25x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.73 ms: 1.37x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.96 ms: 1.80x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.54x slower                                                  |
| telco                      | 6.53 ms                                                | 156 ms: 23.96x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (5): html5lib, unpickle, django_template, asyncio_websockets, coroutines
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.074x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.17x