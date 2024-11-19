# Results vs. 3.12.6

- fork: python
- ref: 29cbcbd73bbfd8c953c0
- machine: linux-x86_64
- commit hash: 29cbcbd
- commit date: 2024-11-19
- overall geometric mean: 1.55x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.39x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 419 ms: 1.59x slower                                                   |
| docutils       | 2.64 sec                                               | 3.37 sec: 1.28x slower                                                 |
| html5lib       | 63.6 ms                                                | 105 ms: 1.65x slower                                                   |
| Geometric mean | (ref)                                                  | 1.50x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| asyncio_tcp        | 519 ms                                                 | 583 ms: 1.12x slower                                                   |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.83 sec: 1.21x slower                                                 |
| async_generators   | 384 ms                                                 | 496 ms: 1.29x slower                                                   |
| coroutines         | 23.9 ms                                                | 31.8 ms: 1.33x slower                                                  |
| Geometric mean     | (ref)                                                  | 1.19x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 183 ms: 1.00x faster                                                   |
| float          | 80.8 ms                                                | 154 ms: 1.91x slower                                                   |
| nbody          | 89.3 ms                                                | 208 ms: 2.33x slower                                                   |
| Geometric mean | (ref)                                                  | 1.64x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.12x faster                                                  |
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                  |
| regex_compile  | 142 ms                                                 | 233 ms: 1.63x slower                                                   |
| Geometric mean | (ref)                                                  | 1.18x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 134 ms: 1.03x faster                                                   |
| pickle_dict          | 31.8 us                                                | 32.5 us: 1.02x slower                                                  |
| unpickle             | 14.1 us                                                | 14.6 us: 1.04x slower                                                  |
| unpickle_list        | 4.67 us                                                | 5.01 us: 1.07x slower                                                  |
| pickle_list          | 4.77 us                                                | 5.11 us: 1.07x slower                                                  |
| json_loads           | 26.5 us                                                | 28.7 us: 1.08x slower                                                  |
| pickle               | 10.9 us                                                | 12.4 us: 1.14x slower                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 110 ms: 1.14x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 114 ms: 1.34x slower                                                   |
| json_dumps           | 10.4 ms                                                | 15.4 ms: 1.49x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 3.25 sec: 1.54x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 94.3 ms: 1.60x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 425 us: 1.93x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 624 us: 2.03x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.28x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.51x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 82.8 ms: 1.65x slower                                                  |
| genshi_text     | 22.8 ms                                                | 41.0 ms: 1.80x slower                                                  |
| django_template | 34.7 ms                                                | 65.7 ms: 1.90x slower                                                  |
| mako            | 11.0 ms                                                | 21.1 ms: 1.91x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.81x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.59 ms: 1.34x faster                                                  |
| regex_effbot             | 3.17 ms                                                | 2.84 ms: 1.12x faster                                                  |
| xml_etree_parse          | 139 ms                                                 | 134 ms: 1.03x faster                                                   |
| pidigits                 | 184 ms                                                 | 183 ms: 1.00x faster                                                   |
| asyncio_websockets       | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| pathlib                  | 21.5 ms                                                | 21.9 ms: 1.02x slower                                                  |
| pickle_dict              | 31.8 us                                                | 32.5 us: 1.02x slower                                                  |
| create_gc_cycles         | 1.09 ms                                                | 1.13 ms: 1.03x slower                                                  |
| unpickle                 | 14.1 us                                                | 14.6 us: 1.04x slower                                                  |
| json                     | 5.02 ms                                                | 5.31 ms: 1.06x slower                                                  |
| unpickle_list            | 4.67 us                                                | 5.01 us: 1.07x slower                                                  |
| pickle_list              | 4.77 us                                                | 5.11 us: 1.07x slower                                                  |
| json_loads               | 26.5 us                                                | 28.7 us: 1.08x slower                                                  |
| regex_dna                | 168 ms                                                 | 186 ms: 1.11x slower                                                   |
| sqlite_synth             | 2.20 us                                                | 2.45 us: 1.11x slower                                                  |
| asyncio_tcp              | 519 ms                                                 | 583 ms: 1.12x slower                                                   |
| pickle                   | 10.9 us                                                | 12.4 us: 1.14x slower                                                  |
| xml_etree_iterparse      | 96.7 ms                                                | 110 ms: 1.14x slower                                                   |
| regex_v8                 | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                  |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.83 sec: 1.21x slower                                                 |
| deepcopy                 | 352 us                                                 | 439 us: 1.25x slower                                                   |
| scimark_fft              | 342 ms                                                 | 431 ms: 1.26x slower                                                   |
| docutils                 | 2.64 sec                                               | 3.37 sec: 1.28x slower                                                 |
| generators               | 32.2 ms                                                | 41.2 ms: 1.28x slower                                                  |
| async_generators         | 384 ms                                                 | 496 ms: 1.29x slower                                                   |
| bpe_tokeniser            | 4.74 sec                                               | 6.13 sec: 1.29x slower                                                 |
| dulwich_log              | 78.9 ms                                                | 103 ms: 1.31x slower                                                   |
| mdp                      | 2.42 sec                                               | 3.18 sec: 1.31x slower                                                 |
| deepcopy_memo            | 40.3 us                                                | 53.3 us: 1.32x slower                                                  |
| pylint                   | 319 ms                                                 | 422 ms: 1.33x slower                                                   |
| coroutines               | 23.9 ms                                                | 31.8 ms: 1.33x slower                                                  |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 5.85 ms: 1.33x slower                                                  |
| xml_etree_generate       | 85.2 ms                                                | 114 ms: 1.34x slower                                                   |
| meteor_contest           | 104 ms                                                 | 141 ms: 1.36x slower                                                   |
| python_startup_no_site   | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                  |
| coverage                 | 71.4 ms                                                | 103 ms: 1.44x slower                                                   |
| crypto_pyaes             | 76.6 ms                                                | 110 ms: 1.44x slower                                                   |
| telco                    | 6.53 ms                                                | 9.47 ms: 1.45x slower                                                  |
| nqueens                  | 80.1 ms                                                | 116 ms: 1.45x slower                                                   |
| pycparser                | 1.17 sec                                               | 1.72 sec: 1.47x slower                                                 |
| json_dumps               | 10.4 ms                                                | 15.4 ms: 1.49x slower                                                  |
| deepcopy_reduce          | 3.08 us                                                | 4.60 us: 1.49x slower                                                  |
| fannkuch                 | 372 ms                                                 | 563 ms: 1.51x slower                                                   |
| spectral_norm            | 110 ms                                                 | 167 ms: 1.52x slower                                                   |
| typing_runtime_protocols | 163 us                                                 | 249 us: 1.52x slower                                                   |
| tomli_loads              | 2.11 sec                                               | 3.25 sec: 1.54x slower                                                 |
| comprehensions           | 19.8 us                                                | 31.1 us: 1.57x slower                                                  |
| python_startup           | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                  |
| 2to3                     | 264 ms                                                 | 419 ms: 1.59x slower                                                   |
| xml_etree_process        | 59.0 ms                                                | 94.3 ms: 1.60x slower                                                  |
| sympy_integrate          | 20.5 ms                                                | 33.3 ms: 1.62x slower                                                  |
| thrift                   | 791 us                                                 | 1.29 ms: 1.63x slower                                                  |
| regex_compile            | 142 ms                                                 | 233 ms: 1.63x slower                                                   |
| genshi_xml               | 50.2 ms                                                | 82.8 ms: 1.65x slower                                                  |
| html5lib                 | 63.6 ms                                                | 105 ms: 1.65x slower                                                   |
| sqlglot_normalize        | 107 ms                                                 | 183 ms: 1.72x slower                                                   |
| sqlglot_optimize         | 53.3 ms                                                | 91.6 ms: 1.72x slower                                                  |
| pyflate                  | 448 ms                                                 | 785 ms: 1.75x slower                                                   |
| genshi_text              | 22.8 ms                                                | 41.0 ms: 1.80x slower                                                  |
| pprint_safe_repr         | 743 ms                                                 | 1.34 sec: 1.80x slower                                                 |
| pprint_pformat           | 1.52 sec                                               | 2.77 sec: 1.82x slower                                                 |
| logging_simple           | 6.63 us                                                | 12.1 us: 1.82x slower                                                  |
| logging_format           | 7.35 us                                                | 13.5 us: 1.83x slower                                                  |
| sympy_str                | 292 ms                                                 | 544 ms: 1.87x slower                                                   |
| django_template          | 34.7 ms                                                | 65.7 ms: 1.90x slower                                                  |
| scimark_monte_carlo      | 68.4 ms                                                | 130 ms: 1.90x slower                                                   |
| float                    | 80.8 ms                                                | 154 ms: 1.91x slower                                                   |
| mako                     | 11.0 ms                                                | 21.1 ms: 1.91x slower                                                  |
| unpickle_pure_python     | 221 us                                                 | 425 us: 1.93x slower                                                   |
| chaos                    | 62.8 ms                                                | 124 ms: 1.97x slower                                                   |
| logging_silent           | 109 ns                                                 | 217 ns: 2.00x slower                                                   |
| richards                 | 45.9 ms                                                | 91.8 ms: 2.00x slower                                                  |
| sqlglot_transpile        | 1.67 ms                                                | 3.37 ms: 2.02x slower                                                  |
| pickle_pure_python       | 308 us                                                 | 624 us: 2.03x slower                                                   |
| hexiom                   | 6.17 ms                                                | 12.7 ms: 2.05x slower                                                  |
| scimark_sor              | 130 ms                                                 | 273 ms: 2.11x slower                                                   |
| richards_super           | 51.9 ms                                                | 110 ms: 2.12x slower                                                   |
| raytrace                 | 299 ms                                                 | 644 ms: 2.15x slower                                                   |
| sqlglot_parse            | 1.36 ms                                                | 2.95 ms: 2.18x slower                                                  |
| go                       | 139 ms                                                 | 306 ms: 2.20x slower                                                   |
| scimark_lu               | 114 ms                                                 | 254 ms: 2.22x slower                                                   |
| sympy_expand             | 468 ms                                                 | 1.06 sec: 2.27x slower                                                 |
| sympy_sum                | 166 ms                                                 | 382 ms: 2.30x slower                                                   |
| nbody                    | 89.3 ms                                                | 208 ms: 2.33x slower                                                   |
| deltablue                | 3.45 ms                                                | 9.27 ms: 2.69x slower                                                  |
| unpack_sequence          | 52.1 ns                                                | 150 ns: 2.89x slower                                                   |
| bench_thread_pool        | 941 us                                                 | 3.51 ms: 3.72x slower                                                  |
| bench_mp_pool            | 10.8 ms                                                | 72.7 ms: 6.73x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.55x slower                                                           |
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.46x
- 95% likely to have a slowdown of 1.44x
- 99% likely to have a slowdown of 1.39x

# Memory
- memory change: 1.23x