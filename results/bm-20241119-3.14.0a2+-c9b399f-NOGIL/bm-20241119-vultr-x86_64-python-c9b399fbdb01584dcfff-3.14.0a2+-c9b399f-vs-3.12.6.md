# Results vs. 3.12.6

- fork: python
- ref: c9b399fbdb01584dcfff
- machine: linux-x86_64
- commit hash: c9b399f
- commit date: 2024-11-19
- overall geometric mean: 1.54x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.38x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 414 ms: 1.57x slower                                                   |
| docutils       | 2.64 sec                                               | 3.37 sec: 1.28x slower                                                 |
| html5lib       | 63.6 ms                                                | 106 ms: 1.67x slower                                                   |
| Geometric mean | (ref)                                                  | 1.50x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 517 ms                                                 | 519 ms: 1.00x slower                                                   |
| asyncio_tcp        | 519 ms                                                 | 584 ms: 1.13x slower                                                   |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.83 sec: 1.21x slower                                                 |
| coroutines         | 23.9 ms                                                | 31.1 ms: 1.30x slower                                                  |
| async_generators   | 384 ms                                                 | 504 ms: 1.31x slower                                                   |
| Geometric mean     | (ref)                                                  | 1.19x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 187 ms: 1.02x slower                                                   |
| float          | 80.8 ms                                                | 151 ms: 1.87x slower                                                   |
| nbody          | 89.3 ms                                                | 199 ms: 2.23x slower                                                   |
| Geometric mean | (ref)                                                  | 1.62x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                  |
| regex_dna      | 168 ms                                                 | 187 ms: 1.12x slower                                                   |
| regex_v8       | 20.6 ms                                                | 25.0 ms: 1.21x slower                                                  |
| regex_compile  | 142 ms                                                 | 228 ms: 1.60x slower                                                   |
| Geometric mean | (ref)                                                  | 1.18x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                   |
| pickle_dict          | 31.8 us                                                | 31.7 us: 1.00x faster                                                  |
| unpickle             | 14.1 us                                                | 15.0 us: 1.06x slower                                                  |
| json_loads           | 26.5 us                                                | 28.5 us: 1.07x slower                                                  |
| pickle_list          | 4.77 us                                                | 5.15 us: 1.08x slower                                                  |
| unpickle_list        | 4.67 us                                                | 5.09 us: 1.09x slower                                                  |
| pickle               | 10.9 us                                                | 12.0 us: 1.09x slower                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 110 ms: 1.13x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 114 ms: 1.33x slower                                                   |
| json_dumps           | 10.4 ms                                                | 15.4 ms: 1.49x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 3.21 sec: 1.52x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 93.8 ms: 1.59x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 427 us: 1.93x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 623 us: 2.02x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.27x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.50x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 82.8 ms: 1.65x slower                                                  |
| genshi_text     | 22.8 ms                                                | 40.8 ms: 1.79x slower                                                  |
| django_template | 34.7 ms                                                | 65.2 ms: 1.88x slower                                                  |
| mako            | 11.0 ms                                                | 21.0 ms: 1.91x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.80x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.39 ms: 1.45x faster                                                  |
| regex_effbot             | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                  |
| xml_etree_parse          | 139 ms                                                 | 133 ms: 1.04x faster                                                   |
| pickle_dict              | 31.8 us                                                | 31.7 us: 1.00x faster                                                  |
| asyncio_websockets       | 517 ms                                                 | 519 ms: 1.00x slower                                                   |
| pidigits                 | 184 ms                                                 | 187 ms: 1.02x slower                                                   |
| pathlib                  | 21.5 ms                                                | 22.1 ms: 1.02x slower                                                  |
| create_gc_cycles         | 1.09 ms                                                | 1.14 ms: 1.04x slower                                                  |
| json                     | 5.02 ms                                                | 5.30 ms: 1.05x slower                                                  |
| unpickle                 | 14.1 us                                                | 15.0 us: 1.06x slower                                                  |
| json_loads               | 26.5 us                                                | 28.5 us: 1.07x slower                                                  |
| pickle_list              | 4.77 us                                                | 5.15 us: 1.08x slower                                                  |
| unpickle_list            | 4.67 us                                                | 5.09 us: 1.09x slower                                                  |
| pickle                   | 10.9 us                                                | 12.0 us: 1.09x slower                                                  |
| sqlite_synth             | 2.20 us                                                | 2.45 us: 1.11x slower                                                  |
| regex_dna                | 168 ms                                                 | 187 ms: 1.12x slower                                                   |
| asyncio_tcp              | 519 ms                                                 | 584 ms: 1.13x slower                                                   |
| xml_etree_iterparse      | 96.7 ms                                                | 110 ms: 1.13x slower                                                   |
| scimark_fft              | 342 ms                                                 | 408 ms: 1.19x slower                                                   |
| regex_v8                 | 20.6 ms                                                | 25.0 ms: 1.21x slower                                                  |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.83 sec: 1.21x slower                                                 |
| deepcopy                 | 352 us                                                 | 436 us: 1.24x slower                                                   |
| mdp                      | 2.42 sec                                               | 3.06 sec: 1.26x slower                                                 |
| docutils                 | 2.64 sec                                               | 3.37 sec: 1.28x slower                                                 |
| generators               | 32.2 ms                                                | 41.5 ms: 1.29x slower                                                  |
| coroutines               | 23.9 ms                                                | 31.1 ms: 1.30x slower                                                  |
| bpe_tokeniser            | 4.74 sec                                               | 6.17 sec: 1.30x slower                                                 |
| async_generators         | 384 ms                                                 | 504 ms: 1.31x slower                                                   |
| dulwich_log              | 78.9 ms                                                | 104 ms: 1.32x slower                                                   |
| pylint                   | 319 ms                                                 | 422 ms: 1.33x slower                                                   |
| xml_etree_generate       | 85.2 ms                                                | 114 ms: 1.33x slower                                                   |
| deepcopy_memo            | 40.3 us                                                | 54.2 us: 1.35x slower                                                  |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 5.93 ms: 1.35x slower                                                  |
| meteor_contest           | 104 ms                                                 | 140 ms: 1.35x slower                                                   |
| crypto_pyaes             | 76.6 ms                                                | 108 ms: 1.41x slower                                                   |
| python_startup_no_site   | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| coverage                 | 71.4 ms                                                | 102 ms: 1.43x slower                                                   |
| spectral_norm            | 110 ms                                                 | 158 ms: 1.44x slower                                                   |
| nqueens                  | 80.1 ms                                                | 116 ms: 1.44x slower                                                   |
| pycparser                | 1.17 sec                                               | 1.71 sec: 1.46x slower                                                 |
| telco                    | 6.53 ms                                                | 9.58 ms: 1.47x slower                                                  |
| deepcopy_reduce          | 3.08 us                                                | 4.55 us: 1.48x slower                                                  |
| json_dumps               | 10.4 ms                                                | 15.4 ms: 1.49x slower                                                  |
| fannkuch                 | 372 ms                                                 | 563 ms: 1.51x slower                                                   |
| tomli_loads              | 2.11 sec                                               | 3.21 sec: 1.52x slower                                                 |
| typing_runtime_protocols | 163 us                                                 | 253 us: 1.55x slower                                                   |
| comprehensions           | 19.8 us                                                | 30.9 us: 1.56x slower                                                  |
| 2to3                     | 264 ms                                                 | 414 ms: 1.57x slower                                                   |
| python_startup           | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                  |
| xml_etree_process        | 59.0 ms                                                | 93.8 ms: 1.59x slower                                                  |
| regex_compile            | 142 ms                                                 | 228 ms: 1.60x slower                                                   |
| sympy_integrate          | 20.5 ms                                                | 33.2 ms: 1.61x slower                                                  |
| thrift                   | 791 us                                                 | 1.29 ms: 1.62x slower                                                  |
| genshi_xml               | 50.2 ms                                                | 82.8 ms: 1.65x slower                                                  |
| html5lib                 | 63.6 ms                                                | 106 ms: 1.67x slower                                                   |
| sqlglot_normalize        | 107 ms                                                 | 182 ms: 1.71x slower                                                   |
| sqlglot_optimize         | 53.3 ms                                                | 91.2 ms: 1.71x slower                                                  |
| pyflate                  | 448 ms                                                 | 778 ms: 1.74x slower                                                   |
| pprint_safe_repr         | 743 ms                                                 | 1.32 sec: 1.78x slower                                                 |
| genshi_text              | 22.8 ms                                                | 40.8 ms: 1.79x slower                                                  |
| pprint_pformat           | 1.52 sec                                               | 2.76 sec: 1.81x slower                                                 |
| scimark_monte_carlo      | 68.4 ms                                                | 125 ms: 1.83x slower                                                   |
| logging_simple           | 6.63 us                                                | 12.1 us: 1.83x slower                                                  |
| logging_format           | 7.35 us                                                | 13.6 us: 1.85x slower                                                  |
| sympy_str                | 292 ms                                                 | 541 ms: 1.85x slower                                                   |
| float                    | 80.8 ms                                                | 151 ms: 1.87x slower                                                   |
| django_template          | 34.7 ms                                                | 65.2 ms: 1.88x slower                                                  |
| mako                     | 11.0 ms                                                | 21.0 ms: 1.91x slower                                                  |
| unpickle_pure_python     | 221 us                                                 | 427 us: 1.93x slower                                                   |
| chaos                    | 62.8 ms                                                | 122 ms: 1.94x slower                                                   |
| logging_silent           | 109 ns                                                 | 213 ns: 1.95x slower                                                   |
| richards                 | 45.9 ms                                                | 89.7 ms: 1.95x slower                                                  |
| sqlglot_transpile        | 1.67 ms                                                | 3.30 ms: 1.97x slower                                                  |
| hexiom                   | 6.17 ms                                                | 12.5 ms: 2.02x slower                                                  |
| pickle_pure_python       | 308 us                                                 | 623 us: 2.02x slower                                                   |
| scimark_sor              | 130 ms                                                 | 271 ms: 2.09x slower                                                   |
| richards_super           | 51.9 ms                                                | 109 ms: 2.09x slower                                                   |
| sqlglot_parse            | 1.36 ms                                                | 2.85 ms: 2.10x slower                                                  |
| raytrace                 | 299 ms                                                 | 631 ms: 2.11x slower                                                   |
| go                       | 139 ms                                                 | 297 ms: 2.13x slower                                                   |
| scimark_lu               | 114 ms                                                 | 245 ms: 2.14x slower                                                   |
| nbody                    | 89.3 ms                                                | 199 ms: 2.23x slower                                                   |
| sympy_expand             | 468 ms                                                 | 1.06 sec: 2.26x slower                                                 |
| sympy_sum                | 166 ms                                                 | 381 ms: 2.30x slower                                                   |
| deltablue                | 3.45 ms                                                | 9.02 ms: 2.62x slower                                                  |
| unpack_sequence          | 52.1 ns                                                | 147 ns: 2.83x slower                                                   |
| bench_thread_pool        | 941 us                                                 | 3.49 ms: 3.71x slower                                                  |
| bench_mp_pool            | 10.8 ms                                                | 72.6 ms: 6.72x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.54x slower                                                           |
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.45x
- 95% likely to have a slowdown of 1.43x
- 99% likely to have a slowdown of 1.38x

# Memory
- memory change: 1.23x