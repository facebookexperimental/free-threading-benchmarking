# Results vs. 3.12.6

- fork: python
- ref: 801cf3fcdd27d8b6dd0f
- machine: linux-x86_64
- commit hash: 801cf3f
- commit date: 2025-08-02
- overall geometric mean: 1.026x slower
- HPT reliability: 95.43%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 285 ms: 1.08x slower                                                  |
| docutils       | 2.64 sec                                               | 2.71 sec: 1.03x slower                                                |
| html5lib       | 63.6 ms                                                | 67.3 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 513 ms: 2.16x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 541 ms: 2.00x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.97x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                                  |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.82x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 510 ms: 1.40x faster                                                  |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 514 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.80 sec: 1.20x slower                                                |
| Geometric mean             | (ref)                                                  | 1.42x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 68.7 ms: 1.18x faster                                                 |
| pidigits       | 184 ms                                                 | 202 ms: 1.10x slower                                                  |
| nbody          | 89.3 ms                                                | 123 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.63 ms: 1.21x faster                                                 |
| regex_compile  | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.1 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| pickle_dict          | 31.8 us                                                | 32.6 us: 1.03x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.17 sec: 1.03x slower                                                |
| unpickle_pure_python | 221 us                                                 | 234 us: 1.06x slower                                                  |
| unpickle             | 14.1 us                                                | 15.5 us: 1.10x slower                                                 |
| pickle_list          | 4.77 us                                                | 5.27 us: 1.11x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 342 us: 1.11x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 95.7 ms: 1.12x slower                                                 |
| pickle               | 10.9 us                                                | 12.4 us: 1.13x slower                                                 |
| unpickle_list        | 4.67 us                                                | 5.36 us: 1.15x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.5 ms: 1.18x slower                                                 |
| json_loads           | 26.5 us                                                | 31.8 us: 1.20x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.5 ms: 1.15x slower                                                 |
| django_template | 34.7 ms                                                | 40.8 ms: 1.18x slower                                                 |
| genshi_text     | 22.8 ms                                                | 27.0 ms: 1.18x slower                                                 |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 513 ms: 2.16x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 541 ms: 2.00x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.97x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.84x faster                                                |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.82x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.96 ms: 1.76x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 510 ms: 1.40x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.63 ms: 1.21x faster                                                 |
| deepcopy                   | 352 us                                                 | 298 us: 1.18x faster                                                  |
| float                      | 80.8 ms                                                | 68.7 ms: 1.18x faster                                                 |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 35.2 us: 1.15x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.0 ms: 1.13x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.1 ms: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 72.2 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.38 sec: 1.08x faster                                                |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| scimark_sor                | 130 ms                                                 | 124 ms: 1.05x faster                                                  |
| logging_silent             | 109 ns                                                 | 105 ns: 1.04x faster                                                  |
| pylint                     | 319 ms                                                 | 308 ms: 1.04x faster                                                  |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.01x faster                                                |
| asyncio_tcp                | 519 ms                                                 | 514 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                                 |
| regex_compile              | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| chaos                      | 62.8 ms                                                | 63.6 ms: 1.01x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.11 us: 1.01x slower                                                 |
| generators                 | 32.2 ms                                                | 32.6 ms: 1.01x slower                                                 |
| raytrace                   | 299 ms                                                 | 303 ms: 1.01x slower                                                  |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                                  |
| pyflate                    | 448 ms                                                 | 459 ms: 1.02x slower                                                  |
| pickle_dict                | 31.8 us                                                | 32.6 us: 1.03x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.71 sec: 1.03x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.17 sec: 1.03x slower                                                |
| deltablue                  | 3.45 ms                                                | 3.55 ms: 1.03x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.39 ms: 1.04x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.00 us: 1.06x slower                                                 |
| html5lib                   | 63.6 ms                                                | 67.3 ms: 1.06x slower                                                 |
| spectral_norm              | 110 ms                                                 | 117 ms: 1.06x slower                                                  |
| unpack_sequence            | 52.1 ns                                                | 55.1 ns: 1.06x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 234 us: 1.06x slower                                                  |
| logging_format             | 7.35 us                                                | 7.87 us: 1.07x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 796 ms: 1.07x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 22.1 ms: 1.07x slower                                                 |
| sympy_str                  | 292 ms                                                 | 315 ms: 1.08x slower                                                  |
| json                       | 5.02 ms                                                | 5.43 ms: 1.08x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.64 sec: 1.08x slower                                                |
| 2to3                       | 264 ms                                                 | 285 ms: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.08x slower                                                  |
| pidigits                   | 184 ms                                                 | 202 ms: 1.10x slower                                                  |
| nqueens                    | 80.1 ms                                                | 88.1 ms: 1.10x slower                                                 |
| unpickle                   | 14.1 us                                                | 15.5 us: 1.10x slower                                                 |
| scimark_fft                | 342 ms                                                 | 377 ms: 1.10x slower                                                  |
| pickle_list                | 4.77 us                                                | 5.27 us: 1.11x slower                                                 |
| richards                   | 45.9 ms                                                | 50.9 ms: 1.11x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 342 us: 1.11x slower                                                  |
| thrift                     | 791 us                                                 | 882 us: 1.11x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 95.7 ms: 1.12x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 86.3 ms: 1.13x slower                                                 |
| sympy_expand               | 468 ms                                                 | 528 ms: 1.13x slower                                                  |
| pickle                     | 10.9 us                                                | 12.4 us: 1.13x slower                                                 |
| richards_super             | 51.9 ms                                                | 59.1 ms: 1.14x slower                                                 |
| meteor_contest             | 104 ms                                                 | 118 ms: 1.14x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 78.3 ms: 1.14x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 57.5 ms: 1.15x slower                                                 |
| unpickle_list              | 4.67 us                                                | 5.36 us: 1.15x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.15x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 190 us: 1.16x slower                                                  |
| django_template            | 34.7 ms                                                | 40.8 ms: 1.18x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 69.5 ms: 1.18x slower                                                 |
| genshi_text                | 22.8 ms                                                | 27.0 ms: 1.18x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.80 sec: 1.20x slower                                                |
| json_loads                 | 26.5 us                                                | 31.8 us: 1.20x slower                                                 |
| fannkuch                   | 372 ms                                                 | 458 ms: 1.23x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.66 ms: 1.29x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                 |
| nbody                      | 89.3 ms                                                | 123 ms: 1.38x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.55 ms: 1.42x slower                                                 |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                 |
| coverage                   | 71.4 ms                                                | 111 ms: 1.56x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.15 ms: 3.35x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 10.01x slower                                                 |
| telco                      | 6.53 ms                                                | 175 ms: 26.84x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (1): regex_v8
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250802-3.15.0a0-801cf3f-NOGIL/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.026x slower

# HPT report

- Reliability score: 95.43% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x