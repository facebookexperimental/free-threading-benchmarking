# Results vs. 3.12.6

- fork: python
- ref: d0bfff47fb2aea9272b5
- machine: linux-x86_64
- commit hash: d0bfff4
- commit date: 2024-10-21
- overall geometric mean: 1.55x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.39x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 414 ms: 1.57x slower                                                   |
| docutils       | 2.64 sec                                               | 3.33 sec: 1.26x slower                                                 |
| html5lib       | 63.6 ms                                                | 103 ms: 1.62x slower                                                   |
| tornado_http   | 119 ms                                                 | 163 ms: 1.37x slower                                                   |
| Geometric mean | (ref)                                                  | 1.45x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 517 ms                                                 | 519 ms: 1.00x slower                                                   |
| asyncio_tcp        | 519 ms                                                 | 580 ms: 1.12x slower                                                   |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.72 sec: 1.14x slower                                                 |
| async_generators   | 384 ms                                                 | 496 ms: 1.29x slower                                                   |
| coroutines         | 23.9 ms                                                | 31.9 ms: 1.33x slower                                                  |
| Geometric mean     | (ref)                                                  | 1.17x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 187 ms: 1.01x slower                                                   |
| float          | 80.8 ms                                                | 155 ms: 1.91x slower                                                   |
| nbody          | 89.3 ms                                                | 226 ms: 2.53x slower                                                   |
| Geometric mean | (ref)                                                  | 1.70x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.13 ms: 1.01x faster                                                  |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| regex_v8       | 20.6 ms                                                | 25.9 ms: 1.26x slower                                                  |
| regex_compile  | 142 ms                                                 | 228 ms: 1.60x slower                                                   |
| Geometric mean | (ref)                                                  | 1.21x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| pickle_dict          | 31.8 us                                                | 31.2 us: 1.02x faster                                                  |
| pickle_list          | 4.77 us                                                | 4.83 us: 1.01x slower                                                  |
| unpickle             | 14.1 us                                                | 14.5 us: 1.03x slower                                                  |
| unpickle_list        | 4.67 us                                                | 5.12 us: 1.10x slower                                                  |
| json_loads           | 26.5 us                                                | 29.4 us: 1.11x slower                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 109 ms: 1.13x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 113 ms: 1.32x slower                                                   |
| json_dumps           | 10.4 ms                                                | 15.5 ms: 1.50x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 3.30 sec: 1.57x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 92.6 ms: 1.57x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 425 us: 1.93x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 618 us: 2.01x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.26x slower                                                           |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.0 ms: 1.40x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 81.3 ms: 1.62x slower                                                  |
| genshi_text     | 22.8 ms                                                | 40.5 ms: 1.78x slower                                                  |
| django_template | 34.7 ms                                                | 64.8 ms: 1.87x slower                                                  |
| mako            | 11.0 ms                                                | 20.9 ms: 1.89x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.79x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.56 ms: 1.35x faster                                                  |
| xml_etree_parse          | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| pickle_dict              | 31.8 us                                                | 31.2 us: 1.02x faster                                                  |
| regex_effbot             | 3.17 ms                                                | 3.13 ms: 1.01x faster                                                  |
| asyncio_websockets       | 517 ms                                                 | 519 ms: 1.00x slower                                                   |
| create_gc_cycles         | 1.09 ms                                                | 1.10 ms: 1.01x slower                                                  |
| pickle_list              | 4.77 us                                                | 4.83 us: 1.01x slower                                                  |
| pidigits                 | 184 ms                                                 | 187 ms: 1.01x slower                                                   |
| pathlib                  | 21.5 ms                                                | 21.9 ms: 1.02x slower                                                  |
| unpickle                 | 14.1 us                                                | 14.5 us: 1.03x slower                                                  |
| json                     | 5.02 ms                                                | 5.42 ms: 1.08x slower                                                  |
| regex_dna                | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| unpickle_list            | 4.67 us                                                | 5.12 us: 1.10x slower                                                  |
| json_loads               | 26.5 us                                                | 29.4 us: 1.11x slower                                                  |
| sqlite_synth             | 2.20 us                                                | 2.46 us: 1.12x slower                                                  |
| asyncio_tcp              | 519 ms                                                 | 580 ms: 1.12x slower                                                   |
| xml_etree_iterparse      | 96.7 ms                                                | 109 ms: 1.13x slower                                                   |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.72 sec: 1.14x slower                                                 |
| deepcopy                 | 352 us                                                 | 436 us: 1.24x slower                                                   |
| regex_v8                 | 20.6 ms                                                | 25.9 ms: 1.26x slower                                                  |
| docutils                 | 2.64 sec                                               | 3.33 sec: 1.26x slower                                                 |
| async_generators         | 384 ms                                                 | 496 ms: 1.29x slower                                                   |
| dulwich_log              | 78.9 ms                                                | 102 ms: 1.30x slower                                                   |
| pylint                   | 319 ms                                                 | 417 ms: 1.31x slower                                                   |
| mdp                      | 2.42 sec                                               | 3.16 sec: 1.31x slower                                                 |
| xml_etree_generate       | 85.2 ms                                                | 113 ms: 1.32x slower                                                   |
| generators               | 32.2 ms                                                | 42.7 ms: 1.32x slower                                                  |
| coroutines               | 23.9 ms                                                | 31.9 ms: 1.33x slower                                                  |
| bpe_tokeniser            | 4.74 sec                                               | 6.32 sec: 1.33x slower                                                 |
| scimark_fft              | 342 ms                                                 | 459 ms: 1.34x slower                                                   |
| deepcopy_memo            | 40.3 us                                                | 54.3 us: 1.35x slower                                                  |
| meteor_contest           | 104 ms                                                 | 140 ms: 1.35x slower                                                   |
| tornado_http             | 119 ms                                                 | 163 ms: 1.37x slower                                                   |
| python_startup_no_site   | 7.16 ms                                                | 10.0 ms: 1.40x slower                                                  |
| coverage                 | 71.4 ms                                                | 103 ms: 1.44x slower                                                   |
| telco                    | 6.53 ms                                                | 9.41 ms: 1.44x slower                                                  |
| crypto_pyaes             | 76.6 ms                                                | 111 ms: 1.44x slower                                                   |
| pycparser                | 1.17 sec                                               | 1.70 sec: 1.46x slower                                                 |
| deepcopy_reduce          | 3.08 us                                                | 4.55 us: 1.48x slower                                                  |
| nqueens                  | 80.1 ms                                                | 119 ms: 1.49x slower                                                   |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 6.54 ms: 1.49x slower                                                  |
| json_dumps               | 10.4 ms                                                | 15.5 ms: 1.50x slower                                                  |
| typing_runtime_protocols | 163 us                                                 | 247 us: 1.51x slower                                                   |
| comprehensions           | 19.8 us                                                | 30.4 us: 1.53x slower                                                  |
| python_startup           | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                  |
| fannkuch                 | 372 ms                                                 | 582 ms: 1.56x slower                                                   |
| tomli_loads              | 2.11 sec                                               | 3.30 sec: 1.57x slower                                                 |
| 2to3                     | 264 ms                                                 | 414 ms: 1.57x slower                                                   |
| xml_etree_process        | 59.0 ms                                                | 92.6 ms: 1.57x slower                                                  |
| regex_compile            | 142 ms                                                 | 228 ms: 1.60x slower                                                   |
| sympy_integrate          | 20.5 ms                                                | 33.0 ms: 1.60x slower                                                  |
| thrift                   | 791 us                                                 | 1.27 ms: 1.61x slower                                                  |
| genshi_xml               | 50.2 ms                                                | 81.3 ms: 1.62x slower                                                  |
| html5lib                 | 63.6 ms                                                | 103 ms: 1.62x slower                                                   |
| spectral_norm            | 110 ms                                                 | 181 ms: 1.64x slower                                                   |
| sqlglot_normalize        | 107 ms                                                 | 180 ms: 1.69x slower                                                   |
| sqlglot_optimize         | 53.3 ms                                                | 90.4 ms: 1.70x slower                                                  |
| genshi_text              | 22.8 ms                                                | 40.5 ms: 1.78x slower                                                  |
| pyflate                  | 448 ms                                                 | 798 ms: 1.78x slower                                                   |
| pprint_safe_repr         | 743 ms                                                 | 1.34 sec: 1.81x slower                                                 |
| pprint_pformat           | 1.52 sec                                               | 2.77 sec: 1.82x slower                                                 |
| sympy_str                | 292 ms                                                 | 540 ms: 1.85x slower                                                   |
| logging_format           | 7.35 us                                                | 13.6 us: 1.86x slower                                                  |
| logging_simple           | 6.63 us                                                | 12.4 us: 1.86x slower                                                  |
| django_template          | 34.7 ms                                                | 64.8 ms: 1.87x slower                                                  |
| mako                     | 11.0 ms                                                | 20.9 ms: 1.89x slower                                                  |
| float                    | 80.8 ms                                                | 155 ms: 1.91x slower                                                   |
| unpickle_pure_python     | 221 us                                                 | 425 us: 1.93x slower                                                   |
| scimark_monte_carlo      | 68.4 ms                                                | 135 ms: 1.97x slower                                                   |
| richards                 | 45.9 ms                                                | 90.7 ms: 1.97x slower                                                  |
| sqlglot_transpile        | 1.67 ms                                                | 3.33 ms: 1.99x slower                                                  |
| logging_silent           | 109 ns                                                 | 217 ns: 1.99x slower                                                   |
| pickle_pure_python       | 308 us                                                 | 618 us: 2.01x slower                                                   |
| hexiom                   | 6.17 ms                                                | 12.6 ms: 2.04x slower                                                  |
| chaos                    | 62.8 ms                                                | 130 ms: 2.06x slower                                                   |
| richards_super           | 51.9 ms                                                | 108 ms: 2.09x slower                                                   |
| sqlglot_parse            | 1.36 ms                                                | 2.89 ms: 2.13x slower                                                  |
| scimark_lu               | 114 ms                                                 | 248 ms: 2.17x slower                                                   |
| raytrace                 | 299 ms                                                 | 650 ms: 2.17x slower                                                   |
| scimark_sor              | 130 ms                                                 | 283 ms: 2.18x slower                                                   |
| go                       | 139 ms                                                 | 305 ms: 2.19x slower                                                   |
| sympy_expand             | 468 ms                                                 | 1.05 sec: 2.25x slower                                                 |
| sympy_sum                | 166 ms                                                 | 381 ms: 2.29x slower                                                   |
| nbody                    | 89.3 ms                                                | 226 ms: 2.53x slower                                                   |
| deltablue                | 3.45 ms                                                | 9.23 ms: 2.68x slower                                                  |
| unpack_sequence          | 52.1 ns                                                | 145 ns: 2.78x slower                                                   |
| bench_thread_pool        | 941 us                                                 | 3.18 ms: 3.38x slower                                                  |
| bench_mp_pool            | 10.8 ms                                                | 70.6 ms: 6.54x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.55x slower                                                           |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.46x
- 95% likely to have a slowdown of 1.44x
- 99% likely to have a slowdown of 1.39x

# Memory
- memory change: 1.21x