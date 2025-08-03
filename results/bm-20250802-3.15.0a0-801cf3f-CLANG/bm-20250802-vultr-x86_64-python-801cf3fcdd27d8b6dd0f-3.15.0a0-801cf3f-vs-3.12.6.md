# Results vs. 3.12.6

- fork: python
- ref: 801cf3fcdd27d8b6dd0f
- machine: linux-x86_64
- commit hash: 801cf3f
- commit date: 2025-08-02
- overall geometric mean: 1.114x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 246 ms: 1.07x faster                                                  |
| docutils       | 2.64 sec                                               | 2.51 sec: 1.05x faster                                                |
| html5lib       | 63.6 ms                                                | 57.9 ms: 1.10x faster                                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 555 ms                                                 | 296 ms: 1.87x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 587 ms: 1.85x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 605 ms: 1.83x faster                                                  |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.78x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 252 ms: 1.77x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 471 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 470 ms: 1.52x faster                                                  |
| async_generators           | 384 ms                                                 | 322 ms: 1.19x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.6 ms: 1.11x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 492 ms: 1.05x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 66.4 ms: 1.22x faster                                                 |
| nbody          | 89.3 ms                                                | 78.6 ms: 1.14x faster                                                 |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 119 ms: 1.19x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 3.11 ms: 1.02x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.5 ms: 1.05x slower                                                 |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.79 sec: 1.18x faster                                                |
| unpickle_pure_python | 221 us                                                 | 200 us: 1.10x faster                                                  |
| unpickle_list        | 4.67 us                                                | 4.33 us: 1.08x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 79.9 ms: 1.07x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 55.6 ms: 1.06x faster                                                 |
| json_loads           | 26.5 us                                                | 25.5 us: 1.04x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 296 us: 1.04x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 94.8 ms: 1.02x faster                                                 |
| pickle_dict          | 31.8 us                                                | 32.3 us: 1.02x slower                                                 |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| unpickle             | 14.1 us                                                | 14.7 us: 1.05x slower                                                 |
| xml_etree_parse      | 139 ms                                                 | 145 ms: 1.05x slower                                                  |
| pickle_list          | 4.77 us                                                | 5.02 us: 1.05x slower                                                 |
| pickle               | 10.9 us                                                | 13.0 us: 1.19x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.35 ms: 1.03x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.7 ms: 1.28x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 19.4 ms: 1.18x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 46.5 ms: 1.08x faster                                                 |
| django_template | 34.7 ms                                                | 32.6 ms: 1.06x faster                                                 |
| mako            | 11.0 ms                                                | 11.4 ms: 1.03x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.07x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.10 sec: 2.20x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 296 ms: 1.87x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 587 ms: 1.85x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 605 ms: 1.83x faster                                                  |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.78x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 252 ms: 1.77x faster                                                  |
| deepcopy                   | 352 us                                                 | 226 us: 1.55x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 471 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 470 ms: 1.52x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 26.5 us: 1.52x faster                                                 |
| go                         | 139 ms                                                 | 100 ms: 1.39x faster                                                  |
| spectral_norm              | 110 ms                                                 | 80.5 ms: 1.37x faster                                                 |
| comprehensions             | 19.8 us                                                | 14.6 us: 1.35x faster                                                 |
| logging_silent             | 109 ns                                                 | 82.2 ns: 1.32x faster                                                 |
| scimark_sor                | 130 ms                                                 | 100 ms: 1.29x faster                                                  |
| raytrace                   | 299 ms                                                 | 233 ms: 1.29x faster                                                  |
| chaos                      | 62.8 ms                                                | 49.4 ms: 1.27x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.42 us: 1.27x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 56.1 ms: 1.22x faster                                                 |
| float                      | 80.8 ms                                                | 66.4 ms: 1.22x faster                                                 |
| richards                   | 45.9 ms                                                | 38.0 ms: 1.21x faster                                                 |
| scimark_fft                | 342 ms                                                 | 283 ms: 1.21x faster                                                  |
| generators                 | 32.2 ms                                                | 27.0 ms: 1.19x faster                                                 |
| async_generators           | 384 ms                                                 | 322 ms: 1.19x faster                                                  |
| regex_compile              | 142 ms                                                 | 119 ms: 1.19x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.5 ms: 1.19x faster                                                 |
| richards_super             | 51.9 ms                                                | 43.9 ms: 1.18x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.79 sec: 1.18x faster                                                |
| pathlib                    | 21.5 ms                                                | 18.3 ms: 1.18x faster                                                 |
| genshi_text                | 22.8 ms                                                | 19.4 ms: 1.18x faster                                                 |
| pylint                     | 319 ms                                                 | 271 ms: 1.18x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.04 sec: 1.17x faster                                                |
| hexiom                     | 6.17 ms                                                | 5.31 ms: 1.16x faster                                                 |
| deltablue                  | 3.45 ms                                                | 2.97 ms: 1.16x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 66.2 ms: 1.16x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 17.9 ms: 1.15x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.79 us: 1.14x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 100 ms: 1.14x faster                                                  |
| pyflate                    | 448 ms                                                 | 394 ms: 1.14x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 144 us: 1.14x faster                                                  |
| nbody                      | 89.3 ms                                                | 78.6 ms: 1.14x faster                                                 |
| logging_format             | 7.35 us                                                | 6.52 us: 1.13x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 147 ms: 1.13x faster                                                  |
| sympy_str                  | 292 ms                                                 | 260 ms: 1.12x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.6 ms: 1.11x faster                                                 |
| unpack_sequence            | 52.1 ns                                                | 47.0 ns: 1.11x faster                                                 |
| nqueens                    | 80.1 ms                                                | 72.4 ms: 1.11x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 200 us: 1.10x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 3.98 ms: 1.10x faster                                                 |
| html5lib                   | 63.6 ms                                                | 57.9 ms: 1.10x faster                                                 |
| thrift                     | 791 us                                                 | 725 us: 1.09x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.08 sec: 1.09x faster                                                |
| unpickle_list              | 4.67 us                                                | 4.33 us: 1.08x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 46.5 ms: 1.08x faster                                                 |
| sympy_expand               | 468 ms                                                 | 435 ms: 1.08x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.41 sec: 1.07x faster                                                |
| 2to3                       | 264 ms                                                 | 246 ms: 1.07x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 79.9 ms: 1.07x faster                                                 |
| django_template            | 34.7 ms                                                | 32.6 ms: 1.06x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 700 ms: 1.06x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 55.6 ms: 1.06x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 492 ms: 1.05x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.51 sec: 1.05x faster                                                |
| json_loads                 | 26.5 us                                                | 25.5 us: 1.04x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 296 us: 1.04x faster                                                  |
| fannkuch                   | 372 ms                                                 | 362 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 94.8 ms: 1.02x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 3.11 ms: 1.02x faster                                                 |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.02x faster                                                  |
| json                       | 5.02 ms                                                | 4.96 ms: 1.01x faster                                                 |
| pickle_dict                | 31.8 us                                                | 32.3 us: 1.02x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.35 ms: 1.03x slower                                                 |
| mako                       | 11.0 ms                                                | 11.4 ms: 1.03x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| coverage                   | 71.4 ms                                                | 74.5 ms: 1.04x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.5 ms: 1.05x slower                                                 |
| unpickle                   | 14.1 us                                                | 14.7 us: 1.05x slower                                                 |
| xml_etree_parse            | 139 ms                                                 | 145 ms: 1.05x slower                                                  |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                  |
| pickle_list                | 4.77 us                                                | 5.02 us: 1.05x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.01 ms: 1.07x slower                                                 |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                                  |
| pickle                     | 10.9 us                                                | 13.0 us: 1.19x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.7 ms: 1.28x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.51 ms: 1.30x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 2.04 ms: 1.87x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.54x slower                                                  |
| telco                      | 6.53 ms                                                | 155 ms: 23.69x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                          |

Benchmark hidden because not significant (3): sqlite_synth, asyncio_websockets, asyncio_tcp_ssl
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250802-3.15.0a0-801cf3f-CLANG/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.114x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.18x