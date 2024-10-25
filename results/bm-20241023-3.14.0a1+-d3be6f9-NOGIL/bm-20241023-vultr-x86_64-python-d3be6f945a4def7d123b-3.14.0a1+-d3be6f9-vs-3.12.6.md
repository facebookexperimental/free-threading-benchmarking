# Results vs. 3.12.6

- fork: python
- ref: d3be6f945a4def7d123b
- machine: linux-x86_64
- commit hash: d3be6f9
- commit date: 2024-10-23
- overall geometric mean: 1.55x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.39x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 414 ms: 1.57x slower                                                   |
| docutils       | 2.64 sec                                               | 3.34 sec: 1.27x slower                                                 |
| html5lib       | 63.6 ms                                                | 103 ms: 1.62x slower                                                   |
| tornado_http   | 119 ms                                                 | 162 ms: 1.36x slower                                                   |
| Geometric mean | (ref)                                                  | 1.45x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9 |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| asyncio_tcp        | 519 ms                                                 | 582 ms: 1.12x slower                                                   |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.78 sec: 1.18x slower                                                 |
| async_generators   | 384 ms                                                 | 495 ms: 1.29x slower                                                   |
| coroutines         | 23.9 ms                                                | 32.0 ms: 1.34x slower                                                  |
| Geometric mean     | (ref)                                                  | 1.18x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                   |
| float          | 80.8 ms                                                | 153 ms: 1.89x slower                                                   |
| nbody          | 89.3 ms                                                | 219 ms: 2.45x slower                                                   |
| Geometric mean | (ref)                                                  | 1.67x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.07 ms: 1.03x faster                                                  |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                   |
| regex_v8       | 20.6 ms                                                | 26.2 ms: 1.27x slower                                                  |
| regex_compile  | 142 ms                                                 | 228 ms: 1.60x slower                                                   |
| Geometric mean | (ref)                                                  | 1.21x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                   |
| pickle_list          | 4.77 us                                                | 4.74 us: 1.01x faster                                                  |
| unpickle             | 14.1 us                                                | 14.6 us: 1.04x slower                                                  |
| pickle_dict          | 31.8 us                                                | 33.4 us: 1.05x slower                                                  |
| pickle               | 10.9 us                                                | 11.5 us: 1.05x slower                                                  |
| unpickle_list        | 4.67 us                                                | 5.10 us: 1.09x slower                                                  |
| json_loads           | 26.5 us                                                | 30.0 us: 1.13x slower                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 109 ms: 1.13x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 113 ms: 1.32x slower                                                   |
| json_dumps           | 10.4 ms                                                | 15.3 ms: 1.47x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 3.26 sec: 1.55x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 93.0 ms: 1.58x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 419 us: 1.90x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 608 us: 1.98x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.27x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.1 ms: 1.41x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.56x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.48x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 82.5 ms: 1.64x slower                                                  |
| genshi_text     | 22.8 ms                                                | 40.8 ms: 1.79x slower                                                  |
| mako            | 11.0 ms                                                | 20.7 ms: 1.88x slower                                                  |
| django_template | 34.7 ms                                                | 65.6 ms: 1.89x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.80x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.48 ms: 1.39x faster                                                  |
| xml_etree_parse          | 139 ms                                                 | 133 ms: 1.04x faster                                                   |
| regex_effbot             | 3.17 ms                                                | 3.07 ms: 1.03x faster                                                  |
| pickle_list              | 4.77 us                                                | 4.74 us: 1.01x faster                                                  |
| asyncio_websockets       | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| pidigits                 | 184 ms                                                 | 186 ms: 1.01x slower                                                   |
| pathlib                  | 21.5 ms                                                | 22.0 ms: 1.02x slower                                                  |
| create_gc_cycles         | 1.09 ms                                                | 1.13 ms: 1.04x slower                                                  |
| unpickle                 | 14.1 us                                                | 14.6 us: 1.04x slower                                                  |
| pickle_dict              | 31.8 us                                                | 33.4 us: 1.05x slower                                                  |
| pickle                   | 10.9 us                                                | 11.5 us: 1.05x slower                                                  |
| json                     | 5.02 ms                                                | 5.46 ms: 1.09x slower                                                  |
| unpickle_list            | 4.67 us                                                | 5.10 us: 1.09x slower                                                  |
| regex_dna                | 168 ms                                                 | 183 ms: 1.09x slower                                                   |
| asyncio_tcp              | 519 ms                                                 | 582 ms: 1.12x slower                                                   |
| sqlite_synth             | 2.20 us                                                | 2.49 us: 1.13x slower                                                  |
| json_loads               | 26.5 us                                                | 30.0 us: 1.13x slower                                                  |
| xml_etree_iterparse      | 96.7 ms                                                | 109 ms: 1.13x slower                                                   |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.78 sec: 1.18x slower                                                 |
| deepcopy                 | 352 us                                                 | 434 us: 1.23x slower                                                   |
| docutils                 | 2.64 sec                                               | 3.34 sec: 1.27x slower                                                 |
| mdp                      | 2.42 sec                                               | 3.06 sec: 1.27x slower                                                 |
| regex_v8                 | 20.6 ms                                                | 26.2 ms: 1.27x slower                                                  |
| async_generators         | 384 ms                                                 | 495 ms: 1.29x slower                                                   |
| dulwich_log              | 78.9 ms                                                | 103 ms: 1.31x slower                                                   |
| meteor_contest           | 104 ms                                                 | 136 ms: 1.31x slower                                                   |
| pylint                   | 319 ms                                                 | 418 ms: 1.31x slower                                                   |
| bpe_tokeniser            | 4.74 sec                                               | 6.24 sec: 1.32x slower                                                 |
| xml_etree_generate       | 85.2 ms                                                | 113 ms: 1.32x slower                                                   |
| scimark_fft              | 342 ms                                                 | 453 ms: 1.33x slower                                                   |
| coroutines               | 23.9 ms                                                | 32.0 ms: 1.34x slower                                                  |
| deepcopy_memo            | 40.3 us                                                | 53.8 us: 1.34x slower                                                  |
| generators               | 32.2 ms                                                | 43.7 ms: 1.35x slower                                                  |
| tornado_http             | 119 ms                                                 | 162 ms: 1.36x slower                                                   |
| python_startup_no_site   | 7.16 ms                                                | 10.1 ms: 1.41x slower                                                  |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 6.23 ms: 1.42x slower                                                  |
| telco                    | 6.53 ms                                                | 9.33 ms: 1.43x slower                                                  |
| crypto_pyaes             | 76.6 ms                                                | 110 ms: 1.44x slower                                                   |
| coverage                 | 71.4 ms                                                | 103 ms: 1.45x slower                                                   |
| pycparser                | 1.17 sec                                               | 1.70 sec: 1.45x slower                                                 |
| json_dumps               | 10.4 ms                                                | 15.3 ms: 1.47x slower                                                  |
| deepcopy_reduce          | 3.08 us                                                | 4.54 us: 1.47x slower                                                  |
| nqueens                  | 80.1 ms                                                | 119 ms: 1.49x slower                                                   |
| typing_runtime_protocols | 163 us                                                 | 248 us: 1.52x slower                                                   |
| fannkuch                 | 372 ms                                                 | 572 ms: 1.54x slower                                                   |
| tomli_loads              | 2.11 sec                                               | 3.26 sec: 1.55x slower                                                 |
| python_startup           | 9.93 ms                                                | 15.4 ms: 1.56x slower                                                  |
| comprehensions           | 19.8 us                                                | 30.9 us: 1.56x slower                                                  |
| 2to3                     | 264 ms                                                 | 414 ms: 1.57x slower                                                   |
| xml_etree_process        | 59.0 ms                                                | 93.0 ms: 1.58x slower                                                  |
| spectral_norm            | 110 ms                                                 | 175 ms: 1.59x slower                                                   |
| sympy_integrate          | 20.5 ms                                                | 32.8 ms: 1.60x slower                                                  |
| regex_compile            | 142 ms                                                 | 228 ms: 1.60x slower                                                   |
| thrift                   | 791 us                                                 | 1.27 ms: 1.60x slower                                                  |
| html5lib                 | 63.6 ms                                                | 103 ms: 1.62x slower                                                   |
| genshi_xml               | 50.2 ms                                                | 82.5 ms: 1.64x slower                                                  |
| sqlglot_normalize        | 107 ms                                                 | 182 ms: 1.71x slower                                                   |
| sqlglot_optimize         | 53.3 ms                                                | 91.3 ms: 1.71x slower                                                  |
| pyflate                  | 448 ms                                                 | 794 ms: 1.77x slower                                                   |
| genshi_text              | 22.8 ms                                                | 40.8 ms: 1.79x slower                                                  |
| pprint_safe_repr         | 743 ms                                                 | 1.34 sec: 1.81x slower                                                 |
| pprint_pformat           | 1.52 sec                                               | 2.78 sec: 1.83x slower                                                 |
| sympy_str                | 292 ms                                                 | 538 ms: 1.84x slower                                                   |
| logging_format           | 7.35 us                                                | 13.7 us: 1.87x slower                                                  |
| mako                     | 11.0 ms                                                | 20.7 ms: 1.88x slower                                                  |
| logging_simple           | 6.63 us                                                | 12.5 us: 1.88x slower                                                  |
| float                    | 80.8 ms                                                | 153 ms: 1.89x slower                                                   |
| django_template          | 34.7 ms                                                | 65.6 ms: 1.89x slower                                                  |
| unpickle_pure_python     | 221 us                                                 | 419 us: 1.90x slower                                                   |
| scimark_monte_carlo      | 68.4 ms                                                | 133 ms: 1.94x slower                                                   |
| pickle_pure_python       | 308 us                                                 | 608 us: 1.98x slower                                                   |
| logging_silent           | 109 ns                                                 | 216 ns: 1.98x slower                                                   |
| richards                 | 45.9 ms                                                | 91.3 ms: 1.99x slower                                                  |
| sqlglot_transpile        | 1.67 ms                                                | 3.33 ms: 1.99x slower                                                  |
| hexiom                   | 6.17 ms                                                | 12.5 ms: 2.03x slower                                                  |
| chaos                    | 62.8 ms                                                | 130 ms: 2.07x slower                                                   |
| richards_super           | 51.9 ms                                                | 110 ms: 2.12x slower                                                   |
| sqlglot_parse            | 1.36 ms                                                | 2.89 ms: 2.13x slower                                                  |
| scimark_sor              | 130 ms                                                 | 281 ms: 2.16x slower                                                   |
| scimark_lu               | 114 ms                                                 | 248 ms: 2.17x slower                                                   |
| raytrace                 | 299 ms                                                 | 650 ms: 2.17x slower                                                   |
| go                       | 139 ms                                                 | 305 ms: 2.19x slower                                                   |
| sympy_expand             | 468 ms                                                 | 1.05 sec: 2.25x slower                                                 |
| sympy_sum                | 166 ms                                                 | 382 ms: 2.30x slower                                                   |
| nbody                    | 89.3 ms                                                | 219 ms: 2.45x slower                                                   |
| unpack_sequence          | 52.1 ns                                                | 136 ns: 2.61x slower                                                   |
| deltablue                | 3.45 ms                                                | 9.30 ms: 2.70x slower                                                  |
| bench_thread_pool        | 941 us                                                 | 3.18 ms: 3.38x slower                                                  |
| bench_mp_pool            | 10.8 ms                                                | 70.8 ms: 6.56x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.55x slower                                                           |
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.45x
- 95% likely to have a slowdown of 1.44x
- 99% likely to have a slowdown of 1.39x

# Memory
- memory change: 1.21x