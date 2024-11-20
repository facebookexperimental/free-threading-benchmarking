# Results vs. 3.12.6

- fork: python
- ref: c9b399fbdb01584dcfff
- machine: linux-x86_64
- commit hash: c9b399f
- commit date: 2024-11-19
- overall geometric mean: 1.41x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.31x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 648 ms: 1.42x slower                                                   |
| docutils       | 4.00 sec                                               | 4.60 sec: 1.15x slower                                                 |
| html5lib       | 88.9 ms                                                | 147 ms: 1.65x slower                                                   |
| Geometric mean | (ref)                                                  | 1.39x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp      | 923 ms                                                 | 1.03 sec: 1.12x slower                                                 |
| asyncio_tcp_ssl  | 2.81 sec                                               | 3.21 sec: 1.14x slower                                                 |
| async_generators | 589 ms                                                 | 679 ms: 1.15x slower                                                   |
| coroutines       | 29.5 ms                                                | 40.9 ms: 1.38x slower                                                  |
| Geometric mean   | (ref)                                                  | 1.15x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 201 ms: 1.64x slower                                                   |
| nbody          | 119 ms                                                 | 257 ms: 2.16x slower                                                   |
| Geometric mean | (ref)                                                  | 1.52x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.58 ms: 1.12x faster                                                  |
| regex_v8       | 32.5 ms                                                | 36.3 ms: 1.12x slower                                                  |
| regex_compile  | 187 ms                                                 | 287 ms: 1.54x slower                                                   |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 212 ms: 1.14x faster                                                   |
| pickle_dict          | 52.7 us                                                | 46.5 us: 1.13x faster                                                  |
| json_loads           | 37.9 us                                                | 40.7 us: 1.07x slower                                                  |
| unpickle_list        | 6.83 us                                                | 7.70 us: 1.13x slower                                                  |
| xml_etree_generate   | 127 ms                                                 | 164 ms: 1.29x slower                                                   |
| json_dumps           | 14.3 ms                                                | 19.5 ms: 1.36x slower                                                  |
| tomli_loads          | 2.88 sec                                               | 4.09 sec: 1.42x slower                                                 |
| xml_etree_process    | 83.7 ms                                                | 126 ms: 1.50x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 524 us: 1.75x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 776 us: 1.78x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.18x slower                                                           |

Benchmark hidden because not significant (4): pickle, pickle_list, xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 18.8 ms: 1.07x slower                                                  |
| python_startup         | 23.7 ms                                                | 29.5 ms: 1.24x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 112 ms: 1.66x slower                                                   |
| genshi_text     | 30.2 ms                                                | 50.2 ms: 1.66x slower                                                  |
| django_template | 44.9 ms                                                | 79.0 ms: 1.76x slower                                                  |
| mako            | 15.7 ms                                                | 30.4 ms: 1.93x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.75x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 5.86 ms                                                | 4.04 ms: 1.45x faster                                                  |
| xml_etree_parse          | 241 ms                                                 | 212 ms: 1.14x faster                                                   |
| pickle_dict              | 52.7 us                                                | 46.5 us: 1.13x faster                                                  |
| regex_effbot             | 5.13 ms                                                | 4.58 ms: 1.12x faster                                                  |
| create_gc_cycles         | 1.94 ms                                                | 1.83 ms: 1.06x faster                                                  |
| sqlite_synth             | 3.87 us                                                | 4.11 us: 1.06x slower                                                  |
| python_startup_no_site   | 17.6 ms                                                | 18.8 ms: 1.07x slower                                                  |
| json_loads               | 37.9 us                                                | 40.7 us: 1.07x slower                                                  |
| scimark_fft              | 500 ms                                                 | 545 ms: 1.09x slower                                                   |
| pathlib                  | 31.6 ms                                                | 34.6 ms: 1.10x slower                                                  |
| json                     | 6.85 ms                                                | 7.53 ms: 1.10x slower                                                  |
| regex_v8                 | 32.5 ms                                                | 36.3 ms: 1.12x slower                                                  |
| asyncio_tcp              | 923 ms                                                 | 1.03 sec: 1.12x slower                                                 |
| unpickle_list            | 6.83 us                                                | 7.70 us: 1.13x slower                                                  |
| asyncio_tcp_ssl          | 2.81 sec                                               | 3.21 sec: 1.14x slower                                                 |
| docutils                 | 4.00 sec                                               | 4.60 sec: 1.15x slower                                                 |
| async_generators         | 589 ms                                                 | 679 ms: 1.15x slower                                                   |
| pycparser                | 1.79 sec                                               | 2.13 sec: 1.19x slower                                                 |
| deepcopy                 | 468 us                                                 | 564 us: 1.21x slower                                                   |
| mdp                      | 3.97 sec                                               | 4.79 sec: 1.21x slower                                                 |
| python_startup           | 23.7 ms                                                | 29.5 ms: 1.24x slower                                                  |
| scimark_sparse_mat_mult  | 6.70 ms                                                | 8.36 ms: 1.25x slower                                                  |
| pylint                   | 465 ms                                                 | 589 ms: 1.27x slower                                                   |
| xml_etree_generate       | 127 ms                                                 | 164 ms: 1.29x slower                                                   |
| dulwich_log              | 100 ms                                                 | 130 ms: 1.30x slower                                                   |
| generators               | 41.1 ms                                                | 53.5 ms: 1.30x slower                                                  |
| meteor_contest           | 146 ms                                                 | 191 ms: 1.30x slower                                                   |
| nqueens                  | 117 ms                                                 | 153 ms: 1.31x slower                                                   |
| comprehensions           | 27.1 us                                                | 35.7 us: 1.32x slower                                                  |
| bpe_tokeniser            | 6.59 sec                                               | 8.77 sec: 1.33x slower                                                 |
| deepcopy_memo            | 52.4 us                                                | 69.9 us: 1.33x slower                                                  |
| spectral_norm            | 156 ms                                                 | 209 ms: 1.34x slower                                                   |
| crypto_pyaes             | 107 ms                                                 | 146 ms: 1.36x slower                                                   |
| json_dumps               | 14.3 ms                                                | 19.5 ms: 1.36x slower                                                  |
| telco                    | 9.59 ms                                                | 13.1 ms: 1.37x slower                                                  |
| coroutines               | 29.5 ms                                                | 40.9 ms: 1.38x slower                                                  |
| fannkuch                 | 540 ms                                                 | 759 ms: 1.40x slower                                                   |
| tomli_loads              | 2.88 sec                                               | 4.09 sec: 1.42x slower                                                 |
| 2to3                     | 456 ms                                                 | 648 ms: 1.42x slower                                                   |
| deepcopy_reduce          | 4.04 us                                                | 5.74 us: 1.42x slower                                                  |
| pyflate                  | 727 ms                                                 | 1.04 sec: 1.43x slower                                                 |
| sympy_integrate          | 29.8 ms                                                | 43.3 ms: 1.46x slower                                                  |
| sqlglot_normalize        | 157 ms                                                 | 232 ms: 1.48x slower                                                   |
| xml_etree_process        | 83.7 ms                                                | 126 ms: 1.50x slower                                                   |
| coverage                 | 95.4 ms                                                | 147 ms: 1.54x slower                                                   |
| regex_compile            | 187 ms                                                 | 287 ms: 1.54x slower                                                   |
| sqlglot_optimize         | 76.0 ms                                                | 117 ms: 1.54x slower                                                   |
| thrift                   | 1.06 ms                                                | 1.65 ms: 1.56x slower                                                  |
| typing_runtime_protocols | 224 us                                                 | 353 us: 1.57x slower                                                   |
| logging_simple           | 9.45 us                                                | 15.1 us: 1.60x slower                                                  |
| scimark_monte_carlo      | 96.4 ms                                                | 154 ms: 1.60x slower                                                   |
| float                    | 123 ms                                                 | 201 ms: 1.64x slower                                                   |
| html5lib                 | 88.9 ms                                                | 147 ms: 1.65x slower                                                   |
| genshi_xml               | 67.6 ms                                                | 112 ms: 1.66x slower                                                   |
| genshi_text              | 30.2 ms                                                | 50.2 ms: 1.66x slower                                                  |
| pprint_safe_repr         | 967 ms                                                 | 1.64 sec: 1.70x slower                                                 |
| pprint_pformat           | 1.98 sec                                               | 3.37 sec: 1.70x slower                                                 |
| sympy_str                | 385 ms                                                 | 662 ms: 1.72x slower                                                   |
| logging_format           | 9.59 us                                                | 16.6 us: 1.73x slower                                                  |
| unpickle_pure_python     | 300 us                                                 | 524 us: 1.75x slower                                                   |
| django_template          | 44.9 ms                                                | 79.0 ms: 1.76x slower                                                  |
| richards_super           | 72.8 ms                                                | 128 ms: 1.76x slower                                                   |
| logging_silent           | 139 ns                                                 | 246 ns: 1.77x slower                                                   |
| richards                 | 60.3 ms                                                | 107 ms: 1.78x slower                                                   |
| pickle_pure_python       | 436 us                                                 | 776 us: 1.78x slower                                                   |
| chaos                    | 84.9 ms                                                | 153 ms: 1.80x slower                                                   |
| sqlglot_transpile        | 2.34 ms                                                | 4.23 ms: 1.81x slower                                                  |
| raytrace                 | 408 ms                                                 | 741 ms: 1.82x slower                                                   |
| scimark_lu               | 152 ms                                                 | 290 ms: 1.91x slower                                                   |
| mako                     | 15.7 ms                                                | 30.4 ms: 1.93x slower                                                  |
| go                       | 172 ms                                                 | 336 ms: 1.95x slower                                                   |
| hexiom                   | 8.27 ms                                                | 16.3 ms: 1.97x slower                                                  |
| scimark_sor              | 167 ms                                                 | 334 ms: 2.01x slower                                                   |
| sympy_expand             | 582 ms                                                 | 1.21 sec: 2.08x slower                                                 |
| sqlglot_parse            | 1.79 ms                                                | 3.82 ms: 2.14x slower                                                  |
| nbody                    | 119 ms                                                 | 257 ms: 2.16x slower                                                   |
| sympy_sum                | 222 ms                                                 | 482 ms: 2.17x slower                                                   |
| deltablue                | 4.27 ms                                                | 11.3 ms: 2.64x slower                                                  |
| bench_mp_pool            | 20.7 ms                                                | 63.7 ms: 3.08x slower                                                  |
| unpack_sequence          | 60.2 ns                                                | 209 ns: 3.47x slower                                                   |
| Geometric mean           | (ref)                                                  | 1.41x slower                                                           |

Benchmark hidden because not significant (8): pickle, bench_thread_pool, pickle_list, xml_etree_iterparse, asyncio_websockets, pidigits, unpickle, regex_dna
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.36x
- 95% likely to have a slowdown of 1.34x
- 99% likely to have a slowdown of 1.31x

# Memory
- memory change: 1.20x