# Results vs. 3.12.6

- fork: python
- ref: 3fecbe9255391be1ac3c
- machine: linux-x86_64
- commit hash: 3fecbe9
- commit date: 2024-11-15
- overall geometric mean: 1.43x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.33x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 656 ms: 1.44x slower                                                   |
| docutils       | 4.00 sec                                               | 4.56 sec: 1.14x slower                                                 |
| html5lib       | 88.9 ms                                                | 135 ms: 1.52x slower                                                   |
| Geometric mean | (ref)                                                  | 1.36x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp      | 923 ms                                                 | 1.05 sec: 1.14x slower                                                 |
| asyncio_tcp_ssl  | 2.81 sec                                               | 3.33 sec: 1.18x slower                                                 |
| async_generators | 589 ms                                                 | 713 ms: 1.21x slower                                                   |
| coroutines       | 29.5 ms                                                | 39.9 ms: 1.35x slower                                                  |
| Geometric mean   | (ref)                                                  | 1.18x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 190 ms: 1.54x slower                                                   |
| nbody          | 119 ms                                                 | 250 ms: 2.10x slower                                                   |
| Geometric mean | (ref)                                                  | 1.47x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.78 ms: 1.07x faster                                                  |
| regex_dna      | 278 ms                                                 | 295 ms: 1.06x slower                                                   |
| regex_v8       | 32.5 ms                                                | 38.8 ms: 1.19x slower                                                  |
| regex_compile  | 187 ms                                                 | 290 ms: 1.55x slower                                                   |
| Geometric mean | (ref)                                                  | 1.16x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 43.2 us: 1.22x faster                                                  |
| xml_etree_parse      | 241 ms                                                 | 217 ms: 1.11x faster                                                   |
| xml_etree_iterparse  | 169 ms                                                 | 157 ms: 1.08x faster                                                   |
| unpickle             | 21.2 us                                                | 23.7 us: 1.11x slower                                                  |
| unpickle_list        | 6.83 us                                                | 7.71 us: 1.13x slower                                                  |
| xml_etree_generate   | 127 ms                                                 | 157 ms: 1.24x slower                                                   |
| json_dumps           | 14.3 ms                                                | 19.3 ms: 1.35x slower                                                  |
| tomli_loads          | 2.88 sec                                               | 4.11 sec: 1.42x slower                                                 |
| xml_etree_process    | 83.7 ms                                                | 129 ms: 1.54x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 761 us: 1.75x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 539 us: 1.80x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.18x slower                                                           |

Benchmark hidden because not significant (3): pickle_list, pickle, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 20.9 ms: 1.19x slower                                                  |
| python_startup         | 23.7 ms                                                | 30.8 ms: 1.30x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 111 ms: 1.64x slower                                                   |
| genshi_text     | 30.2 ms                                                | 53.0 ms: 1.76x slower                                                  |
| django_template | 44.9 ms                                                | 81.0 ms: 1.80x slower                                                  |
| mako            | 15.7 ms                                                | 30.9 ms: 1.97x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.79x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 5.86 ms                                                | 3.97 ms: 1.48x faster                                                  |
| pickle_dict              | 52.7 us                                                | 43.2 us: 1.22x faster                                                  |
| xml_etree_parse          | 241 ms                                                 | 217 ms: 1.11x faster                                                   |
| xml_etree_iterparse      | 169 ms                                                 | 157 ms: 1.08x faster                                                   |
| regex_effbot             | 5.13 ms                                                | 4.78 ms: 1.07x faster                                                  |
| create_gc_cycles         | 1.94 ms                                                | 1.85 ms: 1.05x faster                                                  |
| regex_dna                | 278 ms                                                 | 295 ms: 1.06x slower                                                   |
| json                     | 6.85 ms                                                | 7.26 ms: 1.06x slower                                                  |
| unpickle                 | 21.2 us                                                | 23.7 us: 1.11x slower                                                  |
| sqlite_synth             | 3.87 us                                                | 4.37 us: 1.13x slower                                                  |
| unpickle_list            | 6.83 us                                                | 7.71 us: 1.13x slower                                                  |
| asyncio_tcp              | 923 ms                                                 | 1.05 sec: 1.14x slower                                                 |
| docutils                 | 4.00 sec                                               | 4.56 sec: 1.14x slower                                                 |
| scimark_sparse_mat_mult  | 6.70 ms                                                | 7.79 ms: 1.16x slower                                                  |
| scimark_fft              | 500 ms                                                 | 590 ms: 1.18x slower                                                   |
| asyncio_tcp_ssl          | 2.81 sec                                               | 3.33 sec: 1.18x slower                                                 |
| pycparser                | 1.79 sec                                               | 2.13 sec: 1.19x slower                                                 |
| python_startup_no_site   | 17.6 ms                                                | 20.9 ms: 1.19x slower                                                  |
| regex_v8                 | 32.5 ms                                                | 38.8 ms: 1.19x slower                                                  |
| async_generators         | 589 ms                                                 | 713 ms: 1.21x slower                                                   |
| mdp                      | 3.97 sec                                               | 4.86 sec: 1.22x slower                                                 |
| xml_etree_generate       | 127 ms                                                 | 157 ms: 1.24x slower                                                   |
| deepcopy                 | 468 us                                                 | 582 us: 1.24x slower                                                   |
| deepcopy_memo            | 52.4 us                                                | 66.7 us: 1.27x slower                                                  |
| nqueens                  | 117 ms                                                 | 149 ms: 1.28x slower                                                   |
| python_startup           | 23.7 ms                                                | 30.8 ms: 1.30x slower                                                  |
| meteor_contest           | 146 ms                                                 | 190 ms: 1.30x slower                                                   |
| dulwich_log              | 100 ms                                                 | 133 ms: 1.32x slower                                                   |
| pylint                   | 465 ms                                                 | 616 ms: 1.33x slower                                                   |
| json_dumps               | 14.3 ms                                                | 19.3 ms: 1.35x slower                                                  |
| coroutines               | 29.5 ms                                                | 39.9 ms: 1.35x slower                                                  |
| sqlglot_normalize        | 157 ms                                                 | 214 ms: 1.36x slower                                                   |
| deepcopy_reduce          | 4.04 us                                                | 5.53 us: 1.37x slower                                                  |
| generators               | 41.1 ms                                                | 56.7 ms: 1.38x slower                                                  |
| crypto_pyaes             | 107 ms                                                 | 149 ms: 1.38x slower                                                   |
| fannkuch                 | 540 ms                                                 | 748 ms: 1.38x slower                                                   |
| bpe_tokeniser            | 6.59 sec                                               | 9.21 sec: 1.40x slower                                                 |
| comprehensions           | 27.1 us                                                | 38.5 us: 1.42x slower                                                  |
| tomli_loads              | 2.88 sec                                               | 4.11 sec: 1.42x slower                                                 |
| spectral_norm            | 156 ms                                                 | 222 ms: 1.43x slower                                                   |
| telco                    | 9.59 ms                                                | 13.8 ms: 1.44x slower                                                  |
| 2to3                     | 456 ms                                                 | 656 ms: 1.44x slower                                                   |
| pyflate                  | 727 ms                                                 | 1.04 sec: 1.44x slower                                                 |
| sympy_integrate          | 29.8 ms                                                | 44.8 ms: 1.51x slower                                                  |
| sqlglot_optimize         | 76.0 ms                                                | 115 ms: 1.52x slower                                                   |
| html5lib                 | 88.9 ms                                                | 135 ms: 1.52x slower                                                   |
| float                    | 123 ms                                                 | 190 ms: 1.54x slower                                                   |
| xml_etree_process        | 83.7 ms                                                | 129 ms: 1.54x slower                                                   |
| regex_compile            | 187 ms                                                 | 290 ms: 1.55x slower                                                   |
| scimark_monte_carlo      | 96.4 ms                                                | 150 ms: 1.56x slower                                                   |
| typing_runtime_protocols | 224 us                                                 | 351 us: 1.56x slower                                                   |
| coverage                 | 95.4 ms                                                | 150 ms: 1.58x slower                                                   |
| logging_simple           | 9.45 us                                                | 15.0 us: 1.59x slower                                                  |
| thrift                   | 1.06 ms                                                | 1.72 ms: 1.63x slower                                                  |
| genshi_xml               | 67.6 ms                                                | 111 ms: 1.64x slower                                                   |
| pprint_pformat           | 1.98 sec                                               | 3.34 sec: 1.69x slower                                                 |
| pprint_safe_repr         | 967 ms                                                 | 1.65 sec: 1.71x slower                                                 |
| pickle_pure_python       | 436 us                                                 | 761 us: 1.75x slower                                                   |
| richards_super           | 72.8 ms                                                | 127 ms: 1.75x slower                                                   |
| genshi_text              | 30.2 ms                                                | 53.0 ms: 1.76x slower                                                  |
| sympy_str                | 385 ms                                                 | 688 ms: 1.79x slower                                                   |
| unpickle_pure_python     | 300 us                                                 | 539 us: 1.80x slower                                                   |
| django_template          | 44.9 ms                                                | 81.0 ms: 1.80x slower                                                  |
| logging_silent           | 139 ns                                                 | 255 ns: 1.83x slower                                                   |
| chaos                    | 84.9 ms                                                | 156 ms: 1.84x slower                                                   |
| raytrace                 | 408 ms                                                 | 776 ms: 1.90x slower                                                   |
| logging_format           | 9.59 us                                                | 18.3 us: 1.90x slower                                                  |
| richards                 | 60.3 ms                                                | 115 ms: 1.91x slower                                                   |
| scimark_lu               | 152 ms                                                 | 290 ms: 1.91x slower                                                   |
| hexiom                   | 8.27 ms                                                | 15.8 ms: 1.91x slower                                                  |
| scimark_sor              | 167 ms                                                 | 327 ms: 1.97x slower                                                   |
| mako                     | 15.7 ms                                                | 30.9 ms: 1.97x slower                                                  |
| go                       | 172 ms                                                 | 353 ms: 2.05x slower                                                   |
| sqlglot_parse            | 1.79 ms                                                | 3.68 ms: 2.06x slower                                                  |
| sympy_sum                | 222 ms                                                 | 457 ms: 2.06x slower                                                   |
| sqlglot_transpile        | 2.34 ms                                                | 4.89 ms: 2.10x slower                                                  |
| nbody                    | 119 ms                                                 | 250 ms: 2.10x slower                                                   |
| sympy_expand             | 582 ms                                                 | 1.26 sec: 2.17x slower                                                 |
| deltablue                | 4.27 ms                                                | 11.6 ms: 2.71x slower                                                  |
| bench_mp_pool            | 20.7 ms                                                | 59.4 ms: 2.87x slower                                                  |
| unpack_sequence          | 60.2 ns                                                | 197 ns: 3.28x slower                                                   |
| Geometric mean           | (ref)                                                  | 1.43x slower                                                           |

Benchmark hidden because not significant (7): pickle_list, pickle, pidigits, pathlib, bench_thread_pool, asyncio_websockets, json_loads
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.40x
- 95% likely to have a slowdown of 1.38x
- 99% likely to have a slowdown of 1.33x

# Memory
- memory change: 1.20x