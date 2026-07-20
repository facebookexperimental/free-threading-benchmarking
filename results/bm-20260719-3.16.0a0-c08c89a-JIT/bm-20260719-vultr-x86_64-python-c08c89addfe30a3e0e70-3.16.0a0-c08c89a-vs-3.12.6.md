# Results vs. 3.12.6

- fork: python
- ref: c08c89addfe30a3e0e70
- machine: linux-x86_64
- commit hash: c08c89a
- commit date: 2026-07-19
- overall geometric mean: 1.173x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 257 ms: 1.03x faster                                                  |
| docutils       | 2.64 sec                                               | 2.50 sec: 1.06x faster                                                |
| html5lib       | 63.6 ms                                                | 59.9 ms: 1.06x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 266 ms: 1.74x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 341 ms: 1.64x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 347 ms: 1.60x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 680 ms: 1.59x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 282 ms: 1.58x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 722 ms: 1.54x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 520 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 537 ms: 1.34x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 450 ms: 1.15x faster                                                  |
| async_generators           | 384 ms                                                 | 352 ms: 1.09x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.45 sec: 1.04x faster                                                |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.33x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 55.8 ms: 1.45x faster                                                 |
| nbody          | 89.3 ms                                                | 63.6 ms: 1.40x faster                                                 |
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                  | 1.27x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.64 ms: 1.20x faster                                                 |
| regex_dna      | 168 ms                                                 | 166 ms: 1.01x faster                                                  |
| regex_v8       | 20.6 ms                                                | 21.5 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 182 us: 1.21x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.79 sec: 1.18x faster                                                |
| pickle_pure_python   | 308 us                                                 | 266 us: 1.16x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.13 ms: 1.13x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 86.7 ms: 1.11x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 55.4 ms: 1.06x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 81.3 ms: 1.05x faster                                                 |
| json_loads           | 26.5 us                                                | 26.6 us: 1.00x slower                                                 |
| xml_etree_parse      | 139 ms                                                 | 141 ms: 1.02x slower                                                  |
| unpickle             | 14.1 us                                                | 14.7 us: 1.04x slower                                                 |
| pickle_dict          | 31.8 us                                                | 34.6 us: 1.09x slower                                                 |
| unpickle_list        | 4.67 us                                                | 5.29 us: 1.13x slower                                                 |
| pickle_list          | 4.77 us                                                | 5.64 us: 1.18x slower                                                 |
| pickle               | 10.9 us                                                | 13.2 us: 1.20x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.15 ms: 1.00x faster                                                 |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.12x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.0 ms                                                | 10.1 ms: 1.08x faster                                                 |
| django_template | 34.7 ms                                                | 38.7 ms: 1.12x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 112 ms: 2.83x faster                                                  |
| richards_super             | 51.9 ms                                                | 20.3 ms: 2.56x faster                                                 |
| richards                   | 45.9 ms                                                | 18.2 ms: 2.52x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.23 sec: 1.97x faster                                                |
| deepcopy_memo              | 40.3 us                                                | 21.7 us: 1.86x faster                                                 |
| async_tree_none            | 464 ms                                                 | 266 ms: 1.74x faster                                                  |
| scimark_sor                | 130 ms                                                 | 77.8 ms: 1.67x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 341 ms: 1.64x faster                                                  |
| spectral_norm              | 110 ms                                                 | 68.6 ms: 1.61x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 347 ms: 1.60x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 680 ms: 1.59x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 282 ms: 1.58x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 106 us: 1.54x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 722 ms: 1.54x faster                                                  |
| deepcopy                   | 352 us                                                 | 231 us: 1.52x faster                                                  |
| float                      | 80.8 ms                                                | 55.8 ms: 1.45x faster                                                 |
| go                         | 139 ms                                                 | 99.0 ms: 1.41x faster                                                 |
| nbody                      | 89.3 ms                                                | 63.6 ms: 1.40x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 81.7 ms: 1.40x faster                                                 |
| comprehensions             | 19.8 us                                                | 14.3 us: 1.39x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 520 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 537 ms: 1.34x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 51.4 ms: 1.33x faster                                                 |
| scimark_fft                | 342 ms                                                 | 259 ms: 1.32x faster                                                  |
| deltablue                  | 3.45 ms                                                | 2.65 ms: 1.30x faster                                                 |
| pyflate                    | 448 ms                                                 | 345 ms: 1.30x faster                                                  |
| chaos                      | 62.8 ms                                                | 48.4 ms: 1.30x faster                                                 |
| pathlib                    | 21.5 ms                                                | 16.9 ms: 1.28x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.24 us: 1.27x faster                                                 |
| nqueens                    | 80.1 ms                                                | 64.9 ms: 1.23x faster                                                 |
| logging_format             | 7.35 us                                                | 6.04 us: 1.22x faster                                                 |
| raytrace                   | 299 ms                                                 | 247 ms: 1.21x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.54 us: 1.21x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 182 us: 1.21x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 615 ms: 1.21x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 3.93 sec: 1.20x faster                                                |
| pprint_pformat             | 1.52 sec                                               | 1.26 sec: 1.20x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.64 ms: 1.20x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 64.7 ms: 1.18x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.79 sec: 1.18x faster                                                |
| pickle_pure_python         | 308 us                                                 | 266 us: 1.16x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 450 ms: 1.15x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.13 ms: 1.13x faster                                                 |
| logging_silent             | 109 ns                                                 | 96.3 ns: 1.13x faster                                                 |
| fannkuch                   | 372 ms                                                 | 331 ms: 1.13x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 86.7 ms: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.1 ms: 1.11x faster                                                 |
| async_generators           | 384 ms                                                 | 352 ms: 1.09x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.68 ms: 1.09x faster                                                 |
| mako                       | 11.0 ms                                                | 10.1 ms: 1.08x faster                                                 |
| meteor_contest             | 104 ms                                                 | 95.9 ms: 1.08x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 55.4 ms: 1.06x faster                                                 |
| html5lib                   | 63.6 ms                                                | 59.9 ms: 1.06x faster                                                 |
| generators                 | 32.2 ms                                                | 30.5 ms: 1.06x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.50 sec: 1.06x faster                                                |
| xml_etree_generate         | 85.2 ms                                                | 81.3 ms: 1.05x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.11 us: 1.04x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.45 sec: 1.04x faster                                                |
| json                       | 5.02 ms                                                | 4.85 ms: 1.04x faster                                                 |
| 2to3                       | 264 ms                                                 | 257 ms: 1.03x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.29 ms: 1.02x faster                                                 |
| sympy_expand               | 468 ms                                                 | 458 ms: 1.02x faster                                                  |
| sympy_str                  | 292 ms                                                 | 286 ms: 1.02x faster                                                  |
| regex_dna                  | 168 ms                                                 | 166 ms: 1.01x faster                                                  |
| thrift                     | 791 us                                                 | 784 us: 1.01x faster                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.15 ms: 1.00x faster                                                 |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| json_loads                 | 26.5 us                                                | 26.6 us: 1.00x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 167 ms: 1.01x slower                                                  |
| xml_etree_parse            | 139 ms                                                 | 141 ms: 1.02x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 3.53 ms: 1.02x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                 |
| unpickle                   | 14.1 us                                                | 14.7 us: 1.04x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.5 ms: 1.04x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                  |
| pickle_dict                | 31.8 us                                                | 34.6 us: 1.09x slower                                                 |
| django_template            | 34.7 ms                                                | 38.7 ms: 1.12x slower                                                 |
| unpickle_list              | 4.67 us                                                | 5.29 us: 1.13x slower                                                 |
| coverage                   | 71.4 ms                                                | 83.4 ms: 1.17x slower                                                 |
| pickle_list                | 4.77 us                                                | 5.64 us: 1.18x slower                                                 |
| pickle                     | 10.9 us                                                | 13.2 us: 1.20x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| unpack_sequence            | 52.1 ns                                                | 65.8 ns: 1.26x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.32 ms: 1.40x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.63 ms: 1.49x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 197 ms: 18.26x slower                                                 |
| telco                      | 6.53 ms                                                | 136 ms: 20.79x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                          |

Benchmark hidden because not significant (1): regex_compile
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260719-3.16.0a0-c08c89a-JIT/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.173x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.21x