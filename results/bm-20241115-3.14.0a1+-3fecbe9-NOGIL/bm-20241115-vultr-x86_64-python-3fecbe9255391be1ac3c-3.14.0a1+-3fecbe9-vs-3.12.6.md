# Results vs. 3.12.6

- fork: python
- ref: 3fecbe9255391be1ac3c
- machine: linux-x86_64
- commit hash: 3fecbe9
- commit date: 2024-11-15
- overall geometric mean: 1.54x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.39x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 415 ms: 1.58x slower                                                   |
| docutils       | 2.64 sec                                               | 3.39 sec: 1.28x slower                                                 |
| html5lib       | 63.6 ms                                                | 107 ms: 1.68x slower                                                   |
| Geometric mean | (ref)                                                  | 1.50x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 517 ms                                                 | 521 ms: 1.01x slower                                                   |
| asyncio_tcp        | 519 ms                                                 | 583 ms: 1.12x slower                                                   |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.82 sec: 1.21x slower                                                 |
| async_generators   | 384 ms                                                 | 497 ms: 1.29x slower                                                   |
| coroutines         | 23.9 ms                                                | 31.7 ms: 1.32x slower                                                  |
| Geometric mean     | (ref)                                                  | 1.19x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 183 ms: 1.01x faster                                                   |
| float          | 80.8 ms                                                | 152 ms: 1.88x slower                                                   |
| nbody          | 89.3 ms                                                | 198 ms: 2.21x slower                                                   |
| Geometric mean | (ref)                                                  | 1.60x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.98 ms: 1.06x faster                                                  |
| regex_dna      | 168 ms                                                 | 180 ms: 1.08x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.6 ms: 1.20x slower                                                  |
| regex_compile  | 142 ms                                                 | 227 ms: 1.60x slower                                                   |
| Geometric mean | (ref)                                                  | 1.18x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.05x faster                                                   |
| pickle_dict          | 31.8 us                                                | 32.5 us: 1.02x slower                                                  |
| unpickle             | 14.1 us                                                | 14.5 us: 1.03x slower                                                  |
| unpickle_list        | 4.67 us                                                | 4.94 us: 1.06x slower                                                  |
| pickle_list          | 4.77 us                                                | 5.11 us: 1.07x slower                                                  |
| json_loads           | 26.5 us                                                | 28.8 us: 1.08x slower                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 109 ms: 1.13x slower                                                   |
| pickle               | 10.9 us                                                | 12.7 us: 1.16x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 114 ms: 1.34x slower                                                   |
| json_dumps           | 10.4 ms                                                | 15.3 ms: 1.48x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 3.25 sec: 1.54x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 93.6 ms: 1.59x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 420 us: 1.90x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 618 us: 2.01x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.27x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.50x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 82.4 ms: 1.64x slower                                                  |
| genshi_text     | 22.8 ms                                                | 40.7 ms: 1.79x slower                                                  |
| django_template | 34.7 ms                                                | 65.4 ms: 1.89x slower                                                  |
| mako            | 11.0 ms                                                | 20.8 ms: 1.89x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.80x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.47 ms: 1.40x faster                                                  |
| regex_effbot             | 3.17 ms                                                | 2.98 ms: 1.06x faster                                                  |
| xml_etree_parse          | 139 ms                                                 | 133 ms: 1.05x faster                                                   |
| pidigits                 | 184 ms                                                 | 183 ms: 1.01x faster                                                   |
| asyncio_websockets       | 517 ms                                                 | 521 ms: 1.01x slower                                                   |
| pickle_dict              | 31.8 us                                                | 32.5 us: 1.02x slower                                                  |
| pathlib                  | 21.5 ms                                                | 22.1 ms: 1.03x slower                                                  |
| unpickle                 | 14.1 us                                                | 14.5 us: 1.03x slower                                                  |
| create_gc_cycles         | 1.09 ms                                                | 1.13 ms: 1.04x slower                                                  |
| json                     | 5.02 ms                                                | 5.30 ms: 1.05x slower                                                  |
| unpickle_list            | 4.67 us                                                | 4.94 us: 1.06x slower                                                  |
| pickle_list              | 4.77 us                                                | 5.11 us: 1.07x slower                                                  |
| regex_dna                | 168 ms                                                 | 180 ms: 1.08x slower                                                   |
| json_loads               | 26.5 us                                                | 28.8 us: 1.08x slower                                                  |
| sqlite_synth             | 2.20 us                                                | 2.47 us: 1.12x slower                                                  |
| asyncio_tcp              | 519 ms                                                 | 583 ms: 1.12x slower                                                   |
| xml_etree_iterparse      | 96.7 ms                                                | 109 ms: 1.13x slower                                                   |
| pickle                   | 10.9 us                                                | 12.7 us: 1.16x slower                                                  |
| regex_v8                 | 20.6 ms                                                | 24.6 ms: 1.20x slower                                                  |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.82 sec: 1.21x slower                                                 |
| scimark_fft              | 342 ms                                                 | 416 ms: 1.22x slower                                                   |
| deepcopy                 | 352 us                                                 | 435 us: 1.24x slower                                                   |
| generators               | 32.2 ms                                                | 41.1 ms: 1.27x slower                                                  |
| docutils                 | 2.64 sec                                               | 3.39 sec: 1.28x slower                                                 |
| bpe_tokeniser            | 4.74 sec                                               | 6.12 sec: 1.29x slower                                                 |
| async_generators         | 384 ms                                                 | 497 ms: 1.29x slower                                                   |
| pylint                   | 319 ms                                                 | 420 ms: 1.32x slower                                                   |
| coroutines               | 23.9 ms                                                | 31.7 ms: 1.32x slower                                                  |
| deepcopy_memo            | 40.3 us                                                | 53.6 us: 1.33x slower                                                  |
| meteor_contest           | 104 ms                                                 | 138 ms: 1.33x slower                                                   |
| dulwich_log              | 78.9 ms                                                | 105 ms: 1.33x slower                                                   |
| mdp                      | 2.42 sec                                               | 3.24 sec: 1.34x slower                                                 |
| xml_etree_generate       | 85.2 ms                                                | 114 ms: 1.34x slower                                                   |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 5.94 ms: 1.35x slower                                                  |
| crypto_pyaes             | 76.6 ms                                                | 108 ms: 1.41x slower                                                   |
| telco                    | 6.53 ms                                                | 9.23 ms: 1.41x slower                                                  |
| python_startup_no_site   | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                  |
| nqueens                  | 80.1 ms                                                | 116 ms: 1.45x slower                                                   |
| coverage                 | 71.4 ms                                                | 104 ms: 1.45x slower                                                   |
| spectral_norm            | 110 ms                                                 | 162 ms: 1.47x slower                                                   |
| json_dumps               | 10.4 ms                                                | 15.3 ms: 1.48x slower                                                  |
| deepcopy_reduce          | 3.08 us                                                | 4.57 us: 1.48x slower                                                  |
| pycparser                | 1.17 sec                                               | 1.75 sec: 1.50x slower                                                 |
| fannkuch                 | 372 ms                                                 | 564 ms: 1.51x slower                                                   |
| tomli_loads              | 2.11 sec                                               | 3.25 sec: 1.54x slower                                                 |
| comprehensions           | 19.8 us                                                | 30.8 us: 1.55x slower                                                  |
| typing_runtime_protocols | 163 us                                                 | 253 us: 1.55x slower                                                   |
| 2to3                     | 264 ms                                                 | 415 ms: 1.58x slower                                                   |
| python_startup           | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                  |
| xml_etree_process        | 59.0 ms                                                | 93.6 ms: 1.59x slower                                                  |
| regex_compile            | 142 ms                                                 | 227 ms: 1.60x slower                                                   |
| thrift                   | 791 us                                                 | 1.26 ms: 1.60x slower                                                  |
| sympy_integrate          | 20.5 ms                                                | 33.2 ms: 1.62x slower                                                  |
| genshi_xml               | 50.2 ms                                                | 82.4 ms: 1.64x slower                                                  |
| html5lib                 | 63.6 ms                                                | 107 ms: 1.68x slower                                                   |
| sqlglot_optimize         | 53.3 ms                                                | 91.4 ms: 1.72x slower                                                  |
| pyflate                  | 448 ms                                                 | 772 ms: 1.72x slower                                                   |
| sqlglot_normalize        | 107 ms                                                 | 184 ms: 1.73x slower                                                   |
| genshi_text              | 22.8 ms                                                | 40.7 ms: 1.79x slower                                                  |
| pprint_safe_repr         | 743 ms                                                 | 1.34 sec: 1.80x slower                                                 |
| pprint_pformat           | 1.52 sec                                               | 2.75 sec: 1.81x slower                                                 |
| scimark_monte_carlo      | 68.4 ms                                                | 126 ms: 1.84x slower                                                   |
| logging_simple           | 6.63 us                                                | 12.3 us: 1.85x slower                                                  |
| sympy_str                | 292 ms                                                 | 541 ms: 1.86x slower                                                   |
| logging_format           | 7.35 us                                                | 13.7 us: 1.86x slower                                                  |
| float                    | 80.8 ms                                                | 152 ms: 1.88x slower                                                   |
| django_template          | 34.7 ms                                                | 65.4 ms: 1.89x slower                                                  |
| mako                     | 11.0 ms                                                | 20.8 ms: 1.89x slower                                                  |
| unpickle_pure_python     | 221 us                                                 | 420 us: 1.90x slower                                                   |
| chaos                    | 62.8 ms                                                | 122 ms: 1.94x slower                                                   |
| logging_silent           | 109 ns                                                 | 213 ns: 1.95x slower                                                   |
| sqlglot_transpile        | 1.67 ms                                                | 3.35 ms: 2.00x slower                                                  |
| pickle_pure_python       | 308 us                                                 | 618 us: 2.01x slower                                                   |
| hexiom                   | 6.17 ms                                                | 12.5 ms: 2.03x slower                                                  |
| richards                 | 45.9 ms                                                | 93.2 ms: 2.03x slower                                                  |
| raytrace                 | 299 ms                                                 | 621 ms: 2.08x slower                                                   |
| scimark_sor              | 130 ms                                                 | 270 ms: 2.08x slower                                                   |
| richards_super           | 51.9 ms                                                | 109 ms: 2.09x slower                                                   |
| go                       | 139 ms                                                 | 295 ms: 2.12x slower                                                   |
| sqlglot_parse            | 1.36 ms                                                | 2.90 ms: 2.14x slower                                                  |
| scimark_lu               | 114 ms                                                 | 247 ms: 2.16x slower                                                   |
| nbody                    | 89.3 ms                                                | 198 ms: 2.21x slower                                                   |
| sympy_expand             | 468 ms                                                 | 1.06 sec: 2.27x slower                                                 |
| sympy_sum                | 166 ms                                                 | 381 ms: 2.29x slower                                                   |
| deltablue                | 3.45 ms                                                | 9.08 ms: 2.64x slower                                                  |
| unpack_sequence          | 52.1 ns                                                | 144 ns: 2.77x slower                                                   |
| bench_thread_pool        | 941 us                                                 | 3.49 ms: 3.71x slower                                                  |
| bench_mp_pool            | 10.8 ms                                                | 72.5 ms: 6.72x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.54x slower                                                           |
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.46x
- 95% likely to have a slowdown of 1.44x
- 99% likely to have a slowdown of 1.39x

# Memory
- memory change: 1.23x