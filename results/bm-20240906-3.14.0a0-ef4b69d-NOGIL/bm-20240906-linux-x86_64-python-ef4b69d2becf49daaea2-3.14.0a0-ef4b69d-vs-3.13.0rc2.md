# Results vs. 3.13.0rc2

- fork: python
- ref: ef4b69d2becf49daaea2
- machine: linux-x86_64
- commit hash: ef4b69d
- commit date: 2024-09-06
- overall geometric mean: 1.45x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.32x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 719 ms: 1.62x slower                                                  |
| docutils       | 4.01 sec                                                     | 4.96 sec: 1.24x slower                                                |
| html5lib       | 92.6 ms                                                      | 139 ms: 1.50x slower                                                  |
| tornado_http   | 251 ms                                                       | 350 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                        | 1.43x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|-------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg        | 1.40 sec                                                     | 1.17 sec: 1.19x faster                                                |
| async_tree_memoization  | 709 ms                                                       | 747 ms: 1.05x slower                                                  |
| async_tree_none         | 572 ms                                                       | 610 ms: 1.07x slower                                                  |
| async_tree_cpu_io_mixed | 889 ms                                                       | 952 ms: 1.07x slower                                                  |
| asyncio_tcp_ssl         | 2.77 sec                                                     | 3.56 sec: 1.28x slower                                                |
| asyncio_tcp             | 948 ms                                                       | 1.22 sec: 1.28x slower                                                |
| async_generators        | 567 ms                                                       | 734 ms: 1.29x slower                                                  |
| coroutines              | 30.9 ms                                                      | 41.7 ms: 1.35x slower                                                 |
| Geometric mean          | (ref)                                                        | 1.08x slower                                                          |

Benchmark hidden because not significant (5): async_tree_io, asyncio_websockets, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 116 ms                                                       | 204 ms: 1.76x slower                                                  |
| nbody          | 119 ms                                                       | 300 ms: 2.53x slower                                                  |
| Geometric mean | (ref)                                                        | 1.64x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 294 ms: 1.04x slower                                                  |
| regex_v8       | 32.8 ms                                                      | 37.7 ms: 1.15x slower                                                 |
| regex_compile  | 182 ms                                                       | 284 ms: 1.56x slower                                                  |
| Geometric mean | (ref)                                                        | 1.18x slower                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 47.2 us                                                      | 40.9 us: 1.15x faster                                                 |
| xml_etree_parse      | 231 ms                                                       | 215 ms: 1.08x faster                                                  |
| unpickle             | 20.5 us                                                      | 21.8 us: 1.06x slower                                                 |
| unpickle_list        | 6.68 us                                                      | 7.20 us: 1.08x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 18.1 ms: 1.28x slower                                                 |
| json_loads           | 34.3 us                                                      | 44.0 us: 1.28x slower                                                 |
| xml_etree_generate   | 122 ms                                                       | 163 ms: 1.33x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 128 ms: 1.49x slower                                                  |
| tomli_loads          | 2.78 sec                                                     | 4.30 sec: 1.55x slower                                                |
| unpickle_pure_python | 290 us                                                       | 550 us: 1.89x slower                                                  |
| pickle_pure_python   | 416 us                                                       | 870 us: 2.09x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.23x slower                                                          |

Benchmark hidden because not significant (3): pickle_list, xml_etree_iterparse, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 21.5 ms: 1.40x slower                                                 |
| python_startup         | 22.4 ms                                                      | 32.8 ms: 1.47x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.43x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 55.1 ms: 1.74x slower                                                 |
| genshi_xml      | 72.1 ms                                                      | 129 ms: 1.80x slower                                                  |
| mako            | 15.9 ms                                                      | 30.1 ms: 1.89x slower                                                 |
| django_template | 44.3 ms                                                      | 85.9 ms: 1.94x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.84x slower                                                          |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|--------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal             | 5.70 ms                                                      | 4.60 ms: 1.24x faster                                                 |
| async_tree_io_tg         | 1.40 sec                                                     | 1.17 sec: 1.19x faster                                                |
| pickle_dict              | 47.2 us                                                      | 40.9 us: 1.15x faster                                                 |
| create_gc_cycles         | 2.41 ms                                                      | 2.12 ms: 1.14x faster                                                 |
| xml_etree_parse          | 231 ms                                                       | 215 ms: 1.08x faster                                                  |
| regex_dna                | 282 ms                                                       | 294 ms: 1.04x slower                                                  |
| async_tree_memoization   | 709 ms                                                       | 747 ms: 1.05x slower                                                  |
| unpickle                 | 20.5 us                                                      | 21.8 us: 1.06x slower                                                 |
| async_tree_none          | 572 ms                                                       | 610 ms: 1.07x slower                                                  |
| async_tree_cpu_io_mixed  | 889 ms                                                       | 952 ms: 1.07x slower                                                  |
| unpickle_list            | 6.68 us                                                      | 7.20 us: 1.08x slower                                                 |
| deepcopy                 | 498 us                                                       | 568 us: 1.14x slower                                                  |
| regex_v8                 | 32.8 ms                                                      | 37.7 ms: 1.15x slower                                                 |
| sqlite_synth             | 3.99 us                                                      | 4.60 us: 1.15x slower                                                 |
| telco                    | 12.2 ms                                                      | 14.7 ms: 1.21x slower                                                 |
| docutils                 | 4.01 sec                                                     | 4.96 sec: 1.24x slower                                                |
| json                     | 6.51 ms                                                      | 8.10 ms: 1.24x slower                                                 |
| pathlib                  | 29.9 ms                                                      | 37.2 ms: 1.25x slower                                                 |
| json_dumps               | 14.1 ms                                                      | 18.1 ms: 1.28x slower                                                 |
| bench_mp_pool            | 18.7 ms                                                      | 24.0 ms: 1.28x slower                                                 |
| json_loads               | 34.3 us                                                      | 44.0 us: 1.28x slower                                                 |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.56 sec: 1.28x slower                                                |
| asyncio_tcp              | 948 ms                                                       | 1.22 sec: 1.28x slower                                                |
| async_generators         | 567 ms                                                       | 734 ms: 1.29x slower                                                  |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 8.80 ms: 1.30x slower                                                 |
| meteor_contest           | 150 ms                                                       | 199 ms: 1.32x slower                                                  |
| pylint                   | 470 ms                                                       | 625 ms: 1.33x slower                                                  |
| xml_etree_generate       | 122 ms                                                       | 163 ms: 1.33x slower                                                  |
| deepcopy_memo            | 50.1 us                                                      | 67.4 us: 1.35x slower                                                 |
| coroutines               | 30.9 ms                                                      | 41.7 ms: 1.35x slower                                                 |
| generators               | 40.0 ms                                                      | 54.6 ms: 1.36x slower                                                 |
| mdp                      | 3.80 sec                                                     | 5.18 sec: 1.36x slower                                                |
| scimark_fft              | 473 ms                                                       | 652 ms: 1.38x slower                                                  |
| pycparser                | 1.57 sec                                                     | 2.18 sec: 1.39x slower                                                |
| tornado_http             | 251 ms                                                       | 350 ms: 1.39x slower                                                  |
| python_startup_no_site   | 15.3 ms                                                      | 21.5 ms: 1.40x slower                                                 |
| deepcopy_reduce          | 4.10 us                                                      | 5.97 us: 1.46x slower                                                 |
| coverage                 | 107 ms                                                       | 157 ms: 1.46x slower                                                  |
| python_startup           | 22.4 ms                                                      | 32.8 ms: 1.47x slower                                                 |
| xml_etree_process        | 85.9 ms                                                      | 128 ms: 1.49x slower                                                  |
| html5lib                 | 92.6 ms                                                      | 139 ms: 1.50x slower                                                  |
| fannkuch                 | 547 ms                                                       | 831 ms: 1.52x slower                                                  |
| tomli_loads              | 2.78 sec                                                     | 4.30 sec: 1.55x slower                                                |
| thrift                   | 1.10 ms                                                      | 1.70 ms: 1.55x slower                                                 |
| crypto_pyaes             | 100 ms                                                       | 156 ms: 1.56x slower                                                  |
| nqueens                  | 112 ms                                                       | 174 ms: 1.56x slower                                                  |
| regex_compile            | 182 ms                                                       | 284 ms: 1.56x slower                                                  |
| typing_runtime_protocols | 226 us                                                       | 353 us: 1.56x slower                                                  |
| spectral_norm            | 157 ms                                                       | 249 ms: 1.59x slower                                                  |
| sympy_integrate          | 30.2 ms                                                      | 48.3 ms: 1.60x slower                                                 |
| 2to3                     | 445 ms                                                       | 719 ms: 1.62x slower                                                  |
| pyflate                  | 664 ms                                                       | 1.08 sec: 1.62x slower                                                |
| dulwich_log              | 93.7 ms                                                      | 152 ms: 1.62x slower                                                  |
| bpe_tokeniser            | 6.28 sec                                                     | 10.2 sec: 1.63x slower                                                |
| logging_format           | 9.24 us                                                      | 15.5 us: 1.68x slower                                                 |
| comprehensions           | 22.2 us                                                      | 37.3 us: 1.68x slower                                                 |
| richards_super           | 73.2 ms                                                      | 123 ms: 1.68x slower                                                  |
| pprint_safe_repr         | 987 ms                                                       | 1.68 sec: 1.70x slower                                                |
| sqlglot_normalize        | 140 ms                                                       | 240 ms: 1.72x slower                                                  |
| sqlglot_optimize         | 74.7 ms                                                      | 130 ms: 1.74x slower                                                  |
| genshi_text              | 31.7 ms                                                      | 55.1 ms: 1.74x slower                                                 |
| richards                 | 65.5 ms                                                      | 114 ms: 1.75x slower                                                  |
| float                    | 116 ms                                                       | 204 ms: 1.76x slower                                                  |
| scimark_monte_carlo      | 90.6 ms                                                      | 160 ms: 1.77x slower                                                  |
| pprint_pformat           | 1.94 sec                                                     | 3.48 sec: 1.79x slower                                                |
| genshi_xml               | 72.1 ms                                                      | 129 ms: 1.80x slower                                                  |
| sympy_str                | 379 ms                                                       | 696 ms: 1.84x slower                                                  |
| mako                     | 15.9 ms                                                      | 30.1 ms: 1.89x slower                                                 |
| bench_thread_pool        | 2.89 ms                                                      | 5.45 ms: 1.89x slower                                                 |
| go                       | 191 ms                                                       | 361 ms: 1.89x slower                                                  |
| unpickle_pure_python     | 290 us                                                       | 550 us: 1.89x slower                                                  |
| scimark_sor              | 179 ms                                                       | 340 ms: 1.90x slower                                                  |
| django_template          | 44.3 ms                                                      | 85.9 ms: 1.94x slower                                                 |
| logging_silent           | 130 ns                                                       | 260 ns: 2.00x slower                                                  |
| sqlglot_transpile        | 2.20 ms                                                      | 4.43 ms: 2.02x slower                                                 |
| hexiom                   | 8.11 ms                                                      | 16.4 ms: 2.02x slower                                                 |
| logging_simple           | 8.56 us                                                      | 17.7 us: 2.07x slower                                                 |
| scimark_lu               | 146 ms                                                       | 305 ms: 2.08x slower                                                  |
| pickle_pure_python       | 416 us                                                       | 870 us: 2.09x slower                                                  |
| chaos                    | 83.6 ms                                                      | 176 ms: 2.11x slower                                                  |
| sqlglot_parse            | 1.76 ms                                                      | 3.72 ms: 2.12x slower                                                 |
| raytrace                 | 344 ms                                                       | 751 ms: 2.18x slower                                                  |
| sympy_expand             | 601 ms                                                       | 1.33 sec: 2.22x slower                                                |
| sympy_sum                | 210 ms                                                       | 492 ms: 2.34x slower                                                  |
| unpack_sequence          | 74.3 ns                                                      | 180 ns: 2.42x slower                                                  |
| nbody                    | 119 ms                                                       | 300 ms: 2.53x slower                                                  |
| deltablue                | 4.44 ms                                                      | 11.3 ms: 2.56x slower                                                 |
| Geometric mean           | (ref)                                                        | 1.45x slower                                                          |

Benchmark hidden because not significant (10): pickle_list, xml_etree_iterparse, async_tree_io, asyncio_websockets, async_tree_memoization_tg, pidigits, async_tree_cpu_io_mixed_tg, pickle, async_tree_none_tg, regex_effbot
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.36x
- 95% likely to have a slowdown of 1.36x
- 99% likely to have a slowdown of 1.32x

# Memory
- memory change: 1.15x