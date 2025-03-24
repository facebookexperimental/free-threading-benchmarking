# Results vs. 3.12.6

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.094x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 260 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 630 ms: 1.76x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.76x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 616 ms: 1.76x faster                                                   |
| async_tree_none            | 464 ms                                                 | 272 ms: 1.71x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 500 ms: 1.43x faster                                                   |
| async_generators           | 384 ms                                                 | 354 ms: 1.09x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.7 ms: 1.05x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 499 ms: 1.04x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.51 sec: 1.00x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.40x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 66.3 ms: 1.22x faster                                                  |
| nbody          | 89.3 ms                                                | 82.7 ms: 1.08x faster                                                  |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.72 ms: 1.16x faster                                                  |
| regex_compile  | 142 ms                                                 | 127 ms: 1.12x faster                                                   |
| regex_dna      | 168 ms                                                 | 175 ms: 1.04x slower                                                   |
| regex_v8       | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.84 sec: 1.14x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 205 us: 1.08x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 79.8 ms: 1.07x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 91.1 ms: 1.06x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 55.8 ms: 1.06x faster                                                  |
| unpickle             | 14.1 us                                                | 13.3 us: 1.06x faster                                                  |
| pickle_dict          | 31.8 us                                                | 30.8 us: 1.03x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 312 us: 1.02x slower                                                   |
| unpickle_list        | 4.67 us                                                | 4.79 us: 1.03x slower                                                  |
| pickle_list          | 4.77 us                                                | 5.00 us: 1.05x slower                                                  |
| json_loads           | 26.5 us                                                | 28.0 us: 1.05x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                  |
| pickle               | 10.9 us                                                | 12.1 us: 1.11x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.65 ms: 1.21x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.0 ms: 1.51x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 49.3 ms: 1.02x faster                                                  |
| django_template | 34.7 ms                                                | 35.0 ms: 1.01x slower                                                  |
| mako            | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 630 ms: 1.76x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.76x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 616 ms: 1.76x faster                                                   |
| async_tree_none            | 464 ms                                                 | 272 ms: 1.71x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 500 ms: 1.43x faster                                                   |
| deepcopy                   | 352 us                                                 | 252 us: 1.40x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.0 us: 1.34x faster                                                  |
| richards                   | 45.9 ms                                                | 34.9 ms: 1.32x faster                                                  |
| richards_super             | 51.9 ms                                                | 40.7 ms: 1.27x faster                                                  |
| spectral_norm              | 110 ms                                                 | 88.0 ms: 1.25x faster                                                  |
| float                      | 80.8 ms                                                | 66.3 ms: 1.22x faster                                                  |
| scimark_fft                | 342 ms                                                 | 285 ms: 1.20x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.59 us: 1.19x faster                                                  |
| generators                 | 32.2 ms                                                | 27.3 ms: 1.18x faster                                                  |
| deltablue                  | 3.45 ms                                                | 2.92 ms: 1.18x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 67.2 ms: 1.17x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.72 ms: 1.16x faster                                                  |
| scimark_sor                | 130 ms                                                 | 112 ms: 1.16x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.84 sec: 1.14x faster                                                 |
| raytrace                   | 299 ms                                                 | 263 ms: 1.14x faster                                                   |
| pylint                     | 319 ms                                                 | 282 ms: 1.13x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.88 us: 1.13x faster                                                  |
| regex_compile              | 142 ms                                                 | 127 ms: 1.12x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.23 sec: 1.12x faster                                                 |
| logging_format             | 7.35 us                                                | 6.57 us: 1.12x faster                                                  |
| logging_silent             | 109 ns                                                 | 97.9 ns: 1.11x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                  |
| chaos                      | 62.8 ms                                                | 57.1 ms: 1.10x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 130 ms: 1.10x faster                                                   |
| pyflate                    | 448 ms                                                 | 408 ms: 1.10x faster                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 20.0 ms: 1.09x faster                                                  |
| go                         | 139 ms                                                 | 128 ms: 1.09x faster                                                   |
| async_generators           | 384 ms                                                 | 354 ms: 1.09x faster                                                   |
| nbody                      | 89.3 ms                                                | 82.7 ms: 1.08x faster                                                  |
| comprehensions             | 19.8 us                                                | 18.4 us: 1.08x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 205 us: 1.08x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 71.4 ms: 1.07x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 64.0 ms: 1.07x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 79.8 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 91.1 ms: 1.06x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 157 ms: 1.06x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 55.8 ms: 1.06x faster                                                  |
| unpickle                   | 14.1 us                                                | 13.3 us: 1.06x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.7 ms: 1.05x faster                                                  |
| sympy_str                  | 292 ms                                                 | 278 ms: 1.05x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 156 us: 1.05x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 499 ms: 1.04x faster                                                   |
| mdp                        | 2.42 sec                                               | 2.33 sec: 1.04x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.13 us: 1.04x faster                                                  |
| pickle_dict                | 31.8 us                                                | 30.8 us: 1.03x faster                                                  |
| thrift                     | 791 us                                                 | 771 us: 1.03x faster                                                   |
| json                       | 5.02 ms                                                | 4.90 ms: 1.03x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 49.3 ms: 1.02x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.02x faster                                                 |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.01x faster                                                   |
| 2to3                       | 264 ms                                                 | 260 ms: 1.01x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.51 sec: 1.00x slower                                                 |
| django_template            | 34.7 ms                                                | 35.0 ms: 1.01x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 312 us: 1.02x slower                                                   |
| fannkuch                   | 372 ms                                                 | 380 ms: 1.02x slower                                                   |
| sympy_expand               | 468 ms                                                 | 478 ms: 1.02x slower                                                   |
| unpickle_list              | 4.67 us                                                | 4.79 us: 1.03x slower                                                  |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                   |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                  |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.04x slower                                                   |
| pickle_list                | 4.77 us                                                | 5.00 us: 1.05x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.05x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.62 sec: 1.07x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 795 ms: 1.07x slower                                                   |
| hexiom                     | 6.17 ms                                                | 6.61 ms: 1.07x slower                                                  |
| telco                      | 6.53 ms                                                | 7.12 ms: 1.09x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                  |
| pickle                     | 10.9 us                                                | 12.1 us: 1.11x slower                                                  |
| coverage                   | 71.4 ms                                                | 79.1 ms: 1.11x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.06 ms: 1.12x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 8.65 ms: 1.21x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.24 ms: 1.23x slower                                                  |
| unpack_sequence            | 52.1 ns                                                | 66.0 ns: 1.27x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.0 ms: 1.51x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 89.9 ms: 8.32x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (5): scimark_lu, asyncio_websockets, docutils, nqueens, scimark_sparse_mat_mult
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.094x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.14x