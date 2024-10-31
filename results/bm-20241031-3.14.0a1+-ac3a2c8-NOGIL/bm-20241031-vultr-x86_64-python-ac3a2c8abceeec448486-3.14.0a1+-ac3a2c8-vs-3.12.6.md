# Results vs. 3.12.6

- fork: python
- ref: ac3a2c8abceeec448486
- machine: linux-x86_64
- commit hash: ac3a2c8
- commit date: 2024-10-31
- overall geometric mean: 1.55x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.39x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 413 ms: 1.57x slower                                                   |
| docutils       | 2.64 sec                                               | 3.37 sec: 1.28x slower                                                 |
| html5lib       | 63.6 ms                                                | 106 ms: 1.67x slower                                                   |
| tornado_http   | 119 ms                                                 | 162 ms: 1.36x slower                                                   |
| Geometric mean | (ref)                                                  | 1.46x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp      | 519 ms                                                 | 580 ms: 1.12x slower                                                   |
| asyncio_tcp_ssl  | 1.51 sec                                               | 1.80 sec: 1.19x slower                                                 |
| async_generators | 384 ms                                                 | 500 ms: 1.30x slower                                                   |
| coroutines       | 23.9 ms                                                | 32.3 ms: 1.35x slower                                                  |
| Geometric mean   | (ref)                                                  | 1.19x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                   |
| float          | 80.8 ms                                                | 154 ms: 1.90x slower                                                   |
| nbody          | 89.3 ms                                                | 219 ms: 2.46x slower                                                   |
| Geometric mean | (ref)                                                  | 1.68x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                                   |
| regex_v8       | 20.6 ms                                                | 25.3 ms: 1.23x slower                                                  |
| regex_compile  | 142 ms                                                 | 228 ms: 1.60x slower                                                   |
| Geometric mean | (ref)                                                  | 1.22x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                   |
| pickle_dict          | 31.8 us                                                | 31.2 us: 1.02x faster                                                  |
| pickle               | 10.9 us                                                | 10.8 us: 1.02x faster                                                  |
| unpickle             | 14.1 us                                                | 14.8 us: 1.05x slower                                                  |
| unpickle_list        | 4.67 us                                                | 5.04 us: 1.08x slower                                                  |
| json_loads           | 26.5 us                                                | 29.8 us: 1.12x slower                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 111 ms: 1.14x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 113 ms: 1.33x slower                                                   |
| json_dumps           | 10.4 ms                                                | 15.1 ms: 1.46x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 3.30 sec: 1.56x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 93.5 ms: 1.59x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 427 us: 1.94x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 620 us: 2.01x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.26x slower                                                           |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.1 ms: 1.41x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.48x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 82.4 ms: 1.64x slower                                                  |
| genshi_text     | 22.8 ms                                                | 40.4 ms: 1.77x slower                                                  |
| django_template | 34.7 ms                                                | 64.9 ms: 1.87x slower                                                  |
| mako            | 11.0 ms                                                | 21.1 ms: 1.92x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.80x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.44 ms: 1.42x faster                                                  |
| xml_etree_parse          | 139 ms                                                 | 133 ms: 1.04x faster                                                   |
| pickle_dict              | 31.8 us                                                | 31.2 us: 1.02x faster                                                  |
| pickle                   | 10.9 us                                                | 10.8 us: 1.02x faster                                                  |
| pidigits                 | 184 ms                                                 | 186 ms: 1.01x slower                                                   |
| create_gc_cycles         | 1.09 ms                                                | 1.11 ms: 1.01x slower                                                  |
| pathlib                  | 21.5 ms                                                | 22.0 ms: 1.02x slower                                                  |
| unpickle                 | 14.1 us                                                | 14.8 us: 1.05x slower                                                  |
| unpickle_list            | 4.67 us                                                | 5.04 us: 1.08x slower                                                  |
| json                     | 5.02 ms                                                | 5.51 ms: 1.10x slower                                                  |
| regex_dna                | 168 ms                                                 | 186 ms: 1.11x slower                                                   |
| asyncio_tcp              | 519 ms                                                 | 580 ms: 1.12x slower                                                   |
| sqlite_synth             | 2.20 us                                                | 2.47 us: 1.12x slower                                                  |
| json_loads               | 26.5 us                                                | 29.8 us: 1.12x slower                                                  |
| xml_etree_iterparse      | 96.7 ms                                                | 111 ms: 1.14x slower                                                   |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.80 sec: 1.19x slower                                                 |
| regex_v8                 | 20.6 ms                                                | 25.3 ms: 1.23x slower                                                  |
| deepcopy                 | 352 us                                                 | 438 us: 1.24x slower                                                   |
| mdp                      | 2.42 sec                                               | 3.08 sec: 1.27x slower                                                 |
| docutils                 | 2.64 sec                                               | 3.37 sec: 1.28x slower                                                 |
| async_generators         | 384 ms                                                 | 500 ms: 1.30x slower                                                   |
| dulwich_log              | 78.9 ms                                                | 104 ms: 1.31x slower                                                   |
| pylint                   | 319 ms                                                 | 419 ms: 1.32x slower                                                   |
| scimark_fft              | 342 ms                                                 | 452 ms: 1.32x slower                                                   |
| xml_etree_generate       | 85.2 ms                                                | 113 ms: 1.33x slower                                                   |
| generators               | 32.2 ms                                                | 42.8 ms: 1.33x slower                                                  |
| bpe_tokeniser            | 4.74 sec                                               | 6.32 sec: 1.33x slower                                                 |
| meteor_contest           | 104 ms                                                 | 138 ms: 1.34x slower                                                   |
| deepcopy_memo            | 40.3 us                                                | 54.3 us: 1.35x slower                                                  |
| coroutines               | 23.9 ms                                                | 32.3 ms: 1.35x slower                                                  |
| tornado_http             | 119 ms                                                 | 162 ms: 1.36x slower                                                   |
| python_startup_no_site   | 7.16 ms                                                | 10.1 ms: 1.41x slower                                                  |
| crypto_pyaes             | 76.6 ms                                                | 109 ms: 1.43x slower                                                   |
| coverage                 | 71.4 ms                                                | 102 ms: 1.43x slower                                                   |
| telco                    | 6.53 ms                                                | 9.50 ms: 1.46x slower                                                  |
| pycparser                | 1.17 sec                                               | 1.70 sec: 1.46x slower                                                 |
| json_dumps               | 10.4 ms                                                | 15.1 ms: 1.46x slower                                                  |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 6.45 ms: 1.47x slower                                                  |
| deepcopy_reduce          | 3.08 us                                                | 4.59 us: 1.49x slower                                                  |
| nqueens                  | 80.1 ms                                                | 120 ms: 1.49x slower                                                   |
| fannkuch                 | 372 ms                                                 | 576 ms: 1.55x slower                                                   |
| python_startup           | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                  |
| typing_runtime_protocols | 163 us                                                 | 254 us: 1.56x slower                                                   |
| comprehensions           | 19.8 us                                                | 31.0 us: 1.56x slower                                                  |
| tomli_loads              | 2.11 sec                                               | 3.30 sec: 1.56x slower                                                 |
| 2to3                     | 264 ms                                                 | 413 ms: 1.57x slower                                                   |
| xml_etree_process        | 59.0 ms                                                | 93.5 ms: 1.59x slower                                                  |
| thrift                   | 791 us                                                 | 1.26 ms: 1.60x slower                                                  |
| spectral_norm            | 110 ms                                                 | 176 ms: 1.60x slower                                                   |
| regex_compile            | 142 ms                                                 | 228 ms: 1.60x slower                                                   |
| sympy_integrate          | 20.5 ms                                                | 33.0 ms: 1.61x slower                                                  |
| genshi_xml               | 50.2 ms                                                | 82.4 ms: 1.64x slower                                                  |
| html5lib                 | 63.6 ms                                                | 106 ms: 1.67x slower                                                   |
| sqlglot_normalize        | 107 ms                                                 | 181 ms: 1.70x slower                                                   |
| sqlglot_optimize         | 53.3 ms                                                | 91.6 ms: 1.72x slower                                                  |
| pyflate                  | 448 ms                                                 | 790 ms: 1.76x slower                                                   |
| genshi_text              | 22.8 ms                                                | 40.4 ms: 1.77x slower                                                  |
| pprint_safe_repr         | 743 ms                                                 | 1.35 sec: 1.82x slower                                                 |
| pprint_pformat           | 1.52 sec                                               | 2.81 sec: 1.85x slower                                                 |
| sympy_str                | 292 ms                                                 | 540 ms: 1.85x slower                                                   |
| logging_format           | 7.35 us                                                | 13.7 us: 1.86x slower                                                  |
| logging_simple           | 6.63 us                                                | 12.4 us: 1.87x slower                                                  |
| django_template          | 34.7 ms                                                | 64.9 ms: 1.87x slower                                                  |
| float                    | 80.8 ms                                                | 154 ms: 1.90x slower                                                   |
| scimark_monte_carlo      | 68.4 ms                                                | 131 ms: 1.92x slower                                                   |
| mako                     | 11.0 ms                                                | 21.1 ms: 1.92x slower                                                  |
| unpickle_pure_python     | 221 us                                                 | 427 us: 1.94x slower                                                   |
| richards                 | 45.9 ms                                                | 89.7 ms: 1.95x slower                                                  |
| sqlglot_transpile        | 1.67 ms                                                | 3.31 ms: 1.98x slower                                                  |
| logging_silent           | 109 ns                                                 | 217 ns: 1.99x slower                                                   |
| pickle_pure_python       | 308 us                                                 | 620 us: 2.01x slower                                                   |
| hexiom                   | 6.17 ms                                                | 12.6 ms: 2.04x slower                                                  |
| chaos                    | 62.8 ms                                                | 129 ms: 2.05x slower                                                   |
| richards_super           | 51.9 ms                                                | 110 ms: 2.12x slower                                                   |
| sqlglot_parse            | 1.36 ms                                                | 2.90 ms: 2.14x slower                                                  |
| go                       | 139 ms                                                 | 299 ms: 2.15x slower                                                   |
| raytrace                 | 299 ms                                                 | 650 ms: 2.17x slower                                                   |
| scimark_sor              | 130 ms                                                 | 283 ms: 2.18x slower                                                   |
| scimark_lu               | 114 ms                                                 | 252 ms: 2.21x slower                                                   |
| sympy_expand             | 468 ms                                                 | 1.06 sec: 2.26x slower                                                 |
| sympy_sum                | 166 ms                                                 | 382 ms: 2.30x slower                                                   |
| nbody                    | 89.3 ms                                                | 219 ms: 2.46x slower                                                   |
| deltablue                | 3.45 ms                                                | 9.25 ms: 2.68x slower                                                  |
| unpack_sequence          | 52.1 ns                                                | 144 ns: 2.77x slower                                                   |
| bench_thread_pool        | 941 us                                                 | 3.19 ms: 3.38x slower                                                  |
| bench_mp_pool            | 10.8 ms                                                | 70.8 ms: 6.55x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.55x slower                                                           |

Benchmark hidden because not significant (3): pickle_list, regex_effbot, asyncio_websockets
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.46x
- 95% likely to have a slowdown of 1.44x
- 99% likely to have a slowdown of 1.39x

# Memory
- memory change: 1.21x