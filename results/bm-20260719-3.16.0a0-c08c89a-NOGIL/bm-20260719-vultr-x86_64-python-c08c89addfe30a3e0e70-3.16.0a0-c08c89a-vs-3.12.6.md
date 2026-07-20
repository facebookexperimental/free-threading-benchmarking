# Results vs. 3.12.6

- fork: python
- ref: c08c89addfe30a3e0e70
- machine: linux-x86_64
- commit hash: c08c89a
- commit date: 2026-07-19
- overall geometric mean: 1.042x slower
- HPT reliability: 93.15%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 295 ms: 1.12x slower                                                  |
| docutils       | 2.64 sec                                               | 2.97 sec: 1.13x slower                                                |
| html5lib       | 63.6 ms                                                | 66.9 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 685 ms: 1.62x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 706 ms: 1.53x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 391 ms: 1.43x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 323 ms: 1.38x faster                                                  |
| async_tree_none            | 464 ms                                                 | 338 ms: 1.37x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 416 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 609 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 630 ms: 1.13x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 464 ms: 1.12x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| async_generators           | 384 ms                                                 | 388 ms: 1.01x slower                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.71 sec: 1.13x slower                                                |
| Geometric mean             | (ref)                                                  | 1.21x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 85.3 ms: 1.06x slower                                                 |
| pidigits       | 184 ms                                                 | 205 ms: 1.11x slower                                                  |
| nbody          | 89.3 ms                                                | 127 ms: 1.42x slower                                                  |
| Geometric mean | (ref)                                                  | 1.19x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                 |
| regex_v8       | 20.6 ms                                                | 20.3 ms: 1.01x faster                                                 |
| regex_dna      | 168 ms                                                 | 178 ms: 1.06x slower                                                  |
| regex_compile  | 142 ms                                                 | 169 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 95.9 ms: 1.01x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 141 ms: 1.02x slower                                                  |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                 |
| pickle_dict          | 31.8 us                                                | 33.1 us: 1.04x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 239 us: 1.08x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 342 us: 1.11x slower                                                  |
| json_loads           | 26.5 us                                                | 30.3 us: 1.14x slower                                                 |
| pickle_list          | 4.77 us                                                | 5.51 us: 1.16x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.20x slower                                                  |
| pickle               | 10.9 us                                                | 13.1 us: 1.20x slower                                                 |
| unpickle             | 14.1 us                                                | 17.2 us: 1.22x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 75.0 ms: 1.27x slower                                                 |
| unpickle_list        | 4.67 us                                                | 5.96 us: 1.28x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.32 ms: 1.30x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 40.4 ms: 1.17x slower                                                 |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 132 ms: 2.42x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.78 ms: 1.94x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.86x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 685 ms: 1.62x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 706 ms: 1.53x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 391 ms: 1.43x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 323 ms: 1.38x faster                                                  |
| async_tree_none            | 464 ms                                                 | 338 ms: 1.37x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 416 ms: 1.33x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 31.7 us: 1.27x faster                                                 |
| deepcopy                   | 352 us                                                 | 279 us: 1.26x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 609 ms: 1.19x faster                                                  |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 630 ms: 1.13x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 144 us: 1.13x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 1.95 us: 1.13x faster                                                 |
| unpack_sequence            | 52.1 ns                                                | 46.4 ns: 1.12x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 464 ms: 1.12x faster                                                  |
| comprehensions             | 19.8 us                                                | 18.0 us: 1.10x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.7 ms: 1.10x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                |
| bpe_tokeniser              | 4.74 sec                                               | 4.40 sec: 1.08x faster                                                |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.05x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                |
| deepcopy_reduce            | 3.08 us                                                | 3.00 us: 1.03x faster                                                 |
| regex_v8                   | 20.6 ms                                                | 20.3 ms: 1.01x faster                                                 |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 95.9 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| chaos                      | 62.8 ms                                                | 62.6 ms: 1.00x faster                                                 |
| async_generators           | 384 ms                                                 | 388 ms: 1.01x slower                                                  |
| raytrace                   | 299 ms                                                 | 304 ms: 1.02x slower                                                  |
| xml_etree_parse            | 139 ms                                                 | 141 ms: 1.02x slower                                                  |
| generators                 | 32.2 ms                                                | 33.0 ms: 1.02x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                 |
| pyflate                    | 448 ms                                                 | 464 ms: 1.04x slower                                                  |
| scimark_fft                | 342 ms                                                 | 354 ms: 1.04x slower                                                  |
| pickle_dict                | 31.8 us                                                | 33.1 us: 1.04x slower                                                 |
| html5lib                   | 63.6 ms                                                | 66.9 ms: 1.05x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.00 us: 1.06x slower                                                 |
| float                      | 80.8 ms                                                | 85.3 ms: 1.06x slower                                                 |
| regex_dna                  | 168 ms                                                 | 178 ms: 1.06x slower                                                  |
| json                       | 5.02 ms                                                | 5.36 ms: 1.07x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.60 ms: 1.07x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.69 ms: 1.07x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                 |
| sympy_str                  | 292 ms                                                 | 314 ms: 1.08x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 239 us: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.09x slower                                                  |
| logging_format             | 7.35 us                                                | 8.01 us: 1.09x slower                                                 |
| nqueens                    | 80.1 ms                                                | 87.4 ms: 1.09x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 817 ms: 1.10x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 342 us: 1.11x slower                                                  |
| pidigits                   | 184 ms                                                 | 205 ms: 1.11x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.69 sec: 1.12x slower                                                |
| 2to3                       | 264 ms                                                 | 295 ms: 1.12x slower                                                  |
| sympy_expand               | 468 ms                                                 | 526 ms: 1.12x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.97 sec: 1.13x slower                                                |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.71 sec: 1.13x slower                                                |
| json_loads                 | 26.5 us                                                | 30.3 us: 1.14x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.15x slower                                                  |
| thrift                     | 791 us                                                 | 909 us: 1.15x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 78.9 ms: 1.15x slower                                                 |
| pickle_list                | 4.77 us                                                | 5.51 us: 1.16x slower                                                 |
| richards_super             | 51.9 ms                                                | 60.0 ms: 1.16x slower                                                 |
| django_template            | 34.7 ms                                                | 40.4 ms: 1.17x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 89.7 ms: 1.17x slower                                                 |
| richards                   | 45.9 ms                                                | 54.0 ms: 1.18x slower                                                 |
| regex_compile              | 142 ms                                                 | 169 ms: 1.19x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.20x slower                                                  |
| pickle                     | 10.9 us                                                | 13.1 us: 1.20x slower                                                 |
| meteor_contest             | 104 ms                                                 | 125 ms: 1.21x slower                                                  |
| unpickle                   | 14.1 us                                                | 17.2 us: 1.22x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 13.3 ms: 1.23x slower                                                 |
| fannkuch                   | 372 ms                                                 | 465 ms: 1.25x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.50 ms: 1.25x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.38 ms: 1.27x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 75.0 ms: 1.27x slower                                                 |
| unpickle_list              | 4.67 us                                                | 5.96 us: 1.28x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.32 ms: 1.30x slower                                                 |
| nbody                      | 89.3 ms                                                | 127 ms: 1.42x slower                                                  |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.50 ms: 1.59x slower                                                 |
| coverage                   | 71.4 ms                                                | 114 ms: 1.60x slower                                                  |
| telco                      | 6.53 ms                                                | 175 ms: 26.86x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                          |

Benchmark hidden because not significant (2): logging_silent, coroutines
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260719-3.16.0a0-c08c89a-NOGIL/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.042x slower

# HPT report

- Reliability score: 93.15% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x