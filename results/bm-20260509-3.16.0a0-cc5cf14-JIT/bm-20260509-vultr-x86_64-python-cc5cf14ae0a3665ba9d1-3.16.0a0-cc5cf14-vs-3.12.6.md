# Results vs. 3.12.6

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: linux-x86_64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.154x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.64 sec                                               | 2.51 sec: 1.05x faster                                                |
| html5lib       | 63.6 ms                                                | 65.9 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 343 ms: 1.63x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 689 ms: 1.57x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 288 ms: 1.55x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 728 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 520 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 533 ms: 1.36x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 441 ms: 1.18x faster                                                  |
| async_generators           | 384 ms                                                 | 354 ms: 1.08x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.45 sec: 1.04x faster                                                |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.32x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 57.2 ms: 1.41x faster                                                 |
| nbody          | 89.3 ms                                                | 64.3 ms: 1.39x faster                                                 |
| pidigits       | 184 ms                                                 | 184 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                  | 1.25x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.4 ms: 1.04x slower                                                 |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.80 sec: 1.17x faster                                                |
| unpickle_pure_python | 221 us                                                 | 189 us: 1.17x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.25 ms: 1.12x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 87.3 ms: 1.11x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 279 us: 1.10x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 57.1 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 83.5 ms: 1.02x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 143 ms: 1.03x slower                                                  |
| json_loads           | 26.5 us                                                | 27.4 us: 1.03x slower                                                 |
| pickle_list          | 4.77 us                                                | 5.03 us: 1.05x slower                                                 |
| unpickle             | 14.1 us                                                | 15.1 us: 1.07x slower                                                 |
| pickle_dict          | 31.8 us                                                | 34.3 us: 1.08x slower                                                 |
| unpickle_list        | 4.67 us                                                | 5.22 us: 1.12x slower                                                 |
| pickle               | 10.9 us                                                | 12.9 us: 1.18x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.0 ms                                                | 10.5 ms: 1.05x faster                                                 |
| django_template | 34.7 ms                                                | 41.3 ms: 1.19x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 115 ms: 2.78x faster                                                  |
| richards_super             | 51.9 ms                                                | 21.4 ms: 2.42x faster                                                 |
| richards                   | 45.9 ms                                                | 19.0 ms: 2.42x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.24 sec: 1.95x faster                                                |
| deepcopy_memo              | 40.3 us                                                | 23.2 us: 1.74x faster                                                 |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                                  |
| scimark_sor                | 130 ms                                                 | 78.9 ms: 1.64x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 343 ms: 1.63x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 689 ms: 1.57x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                                  |
| spectral_norm              | 110 ms                                                 | 71.0 ms: 1.55x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 288 ms: 1.55x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 728 ms: 1.52x faster                                                  |
| deepcopy                   | 352 us                                                 | 244 us: 1.44x faster                                                  |
| float                      | 80.8 ms                                                | 57.2 ms: 1.41x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 81.5 ms: 1.40x faster                                                 |
| nbody                      | 89.3 ms                                                | 64.3 ms: 1.39x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 520 ms: 1.38x faster                                                  |
| go                         | 139 ms                                                 | 102 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 533 ms: 1.36x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.0 us: 1.32x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 52.2 ms: 1.31x faster                                                 |
| scimark_fft                | 342 ms                                                 | 261 ms: 1.31x faster                                                  |
| chaos                      | 62.8 ms                                                | 49.0 ms: 1.28x faster                                                 |
| pyflate                    | 448 ms                                                 | 352 ms: 1.27x faster                                                  |
| deltablue                  | 3.45 ms                                                | 2.72 ms: 1.27x faster                                                 |
| pathlib                    | 21.5 ms                                                | 17.1 ms: 1.26x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.42 us: 1.22x faster                                                 |
| nqueens                    | 80.1 ms                                                | 65.7 ms: 1.22x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 3.97 sec: 1.19x faster                                                |
| logging_format             | 7.35 us                                                | 6.22 us: 1.18x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.29 sec: 1.18x faster                                                |
| asyncio_tcp                | 519 ms                                                 | 441 ms: 1.18x faster                                                  |
| raytrace                   | 299 ms                                                 | 255 ms: 1.17x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 633 ms: 1.17x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.63 us: 1.17x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 65.4 ms: 1.17x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.80 sec: 1.17x faster                                                |
| unpickle_pure_python       | 221 us                                                 | 189 us: 1.17x faster                                                  |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                                  |
| fannkuch                   | 372 ms                                                 | 331 ms: 1.12x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.25 ms: 1.12x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.3 ms: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.3 ms: 1.11x faster                                                 |
| generators                 | 32.2 ms                                                | 29.2 ms: 1.11x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 279 us: 1.10x faster                                                  |
| logging_silent             | 109 ns                                                 | 100 ns: 1.09x faster                                                  |
| async_generators           | 384 ms                                                 | 354 ms: 1.08x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.69 ms: 1.08x faster                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.06 ms: 1.08x faster                                                 |
| meteor_contest             | 104 ms                                                 | 95.7 ms: 1.08x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 152 us: 1.08x faster                                                  |
| mako                       | 11.0 ms                                                | 10.5 ms: 1.05x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.51 sec: 1.05x faster                                                |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.45 sec: 1.04x faster                                                |
| sqlite_synth               | 2.20 us                                                | 2.12 us: 1.04x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 57.1 ms: 1.03x faster                                                 |
| json                       | 5.02 ms                                                | 4.91 ms: 1.02x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 83.5 ms: 1.02x faster                                                 |
| sympy_expand               | 468 ms                                                 | 464 ms: 1.01x faster                                                  |
| sympy_str                  | 292 ms                                                 | 289 ms: 1.01x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 165 ms: 1.01x faster                                                  |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x slower                                                  |
| thrift                     | 791 us                                                 | 809 us: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                 |
| xml_etree_parse            | 139 ms                                                 | 143 ms: 1.03x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.4 us: 1.03x slower                                                 |
| html5lib                   | 63.6 ms                                                | 65.9 ms: 1.04x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.4 ms: 1.04x slower                                                 |
| pycparser                  | 1.17 sec                                               | 1.22 sec: 1.04x slower                                                |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                  |
| pickle_list                | 4.77 us                                                | 5.03 us: 1.05x slower                                                 |
| unpickle                   | 14.1 us                                                | 15.1 us: 1.07x slower                                                 |
| pickle_dict                | 31.8 us                                                | 34.3 us: 1.08x slower                                                 |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                                  |
| unpickle_list              | 4.67 us                                                | 5.22 us: 1.12x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 3.87 ms: 1.12x slower                                                 |
| coverage                   | 71.4 ms                                                | 82.7 ms: 1.16x slower                                                 |
| pickle                     | 10.9 us                                                | 12.9 us: 1.18x slower                                                 |
| django_template            | 34.7 ms                                                | 41.3 ms: 1.19x slower                                                 |
| unpack_sequence            | 52.1 ns                                                | 64.8 ns: 1.25x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.33 ms: 1.42x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.67x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 203 ms: 18.75x slower                                                 |
| telco                      | 6.53 ms                                                | 137 ms: 20.92x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                          |
Ignored benchmarks (18) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260509-3.16.0a0-cc5cf14-JIT/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.154x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.22x