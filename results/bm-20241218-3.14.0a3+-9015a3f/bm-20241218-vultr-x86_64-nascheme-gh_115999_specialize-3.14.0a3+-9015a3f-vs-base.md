# Results vs. base

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 9015a3f
- commit date: 2024-12-18
- overall geometric mean: 1.000x slower
- HPT reliability: 87.03%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 256 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_generators | 353 ms                                                                 | 352 ms: 1.00x faster                                                     |
| async_tree_io    | 621 ms                                                                 | 630 ms: 1.01x slower                                                     |
| coroutines       | 21.8 ms                                                                | 22.2 ms: 1.02x slower                                                    |
| Geometric mean   | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (8): async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_none, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 222 ms                                                                 | 222 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 24.1 ms                                                                | 23.2 ms: 1.04x faster                                                    |
| regex_effbot   | 2.82 ms                                                                | 2.73 ms: 1.03x faster                                                    |
| regex_dna      | 173 ms                                                                 | 169 ms: 1.03x faster                                                     |
| regex_compile  | 126 ms                                                                 | 127 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_process    | 58.7 ms                                                                | 57.8 ms: 1.01x faster                                                    |
| json_dumps           | 11.4 ms                                                                | 11.3 ms: 1.01x faster                                                    |
| xml_etree_generate   | 84.1 ms                                                                | 83.2 ms: 1.01x faster                                                    |
| json_loads           | 26.3 us                                                                | 26.0 us: 1.01x faster                                                    |
| tomli_loads          | 1.97 sec                                                               | 1.96 sec: 1.01x faster                                                   |
| xml_etree_iterparse  | 90.6 ms                                                                | 90.1 ms: 1.01x faster                                                    |
| unpickle_pure_python | 211 us                                                                 | 212 us: 1.00x slower                                                     |
| pickle_pure_python   | 313 us                                                                 | 317 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.50 ms                                                                | 7.49 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 11.7 ms                                                                | 11.5 ms: 1.01x faster                                                    |
| genshi_text     | 21.6 ms                                                                | 21.4 ms: 1.01x faster                                                    |
| genshi_xml      | 49.8 ms                                                                | 49.3 ms: 1.01x faster                                                    |
| django_template | 35.1 ms                                                                | 34.9 ms: 1.01x faster                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|--------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8                 | 24.1 ms                                                                | 23.2 ms: 1.04x faster                                                    |
| regex_effbot             | 2.82 ms                                                                | 2.73 ms: 1.03x faster                                                    |
| regex_dna                | 173 ms                                                                 | 169 ms: 1.03x faster                                                     |
| richards                 | 44.4 ms                                                                | 43.5 ms: 1.02x faster                                                    |
| meteor_contest           | 100 ms                                                                 | 98.2 ms: 1.02x faster                                                    |
| sqlite_synth             | 2.25 us                                                                | 2.21 us: 1.02x faster                                                    |
| typing_runtime_protocols | 156 us                                                                 | 153 us: 1.02x faster                                                     |
| xml_etree_process        | 58.7 ms                                                                | 57.8 ms: 1.01x faster                                                    |
| deepcopy_reduce          | 2.58 us                                                                | 2.54 us: 1.01x faster                                                    |
| mako                     | 11.7 ms                                                                | 11.5 ms: 1.01x faster                                                    |
| crypto_pyaes             | 67.3 ms                                                                | 66.4 ms: 1.01x faster                                                    |
| json_dumps               | 11.4 ms                                                                | 11.3 ms: 1.01x faster                                                    |
| xml_etree_generate       | 84.1 ms                                                                | 83.2 ms: 1.01x faster                                                    |
| json_loads               | 26.3 us                                                                | 26.0 us: 1.01x faster                                                    |
| deepcopy_memo            | 29.6 us                                                                | 29.3 us: 1.01x faster                                                    |
| genshi_text              | 21.6 ms                                                                | 21.4 ms: 1.01x faster                                                    |
| generators               | 27.0 ms                                                                | 26.8 ms: 1.01x faster                                                    |
| genshi_xml               | 49.8 ms                                                                | 49.3 ms: 1.01x faster                                                    |
| richards_super           | 50.3 ms                                                                | 49.9 ms: 1.01x faster                                                    |
| bench_mp_pool            | 89.3 ms                                                                | 88.5 ms: 1.01x faster                                                    |
| pyflate                  | 424 ms                                                                 | 420 ms: 1.01x faster                                                     |
| logging_silent           | 104 ns                                                                 | 103 ns: 1.01x faster                                                     |
| many_optionals           | 1.03 ms                                                                | 1.02 ms: 1.01x faster                                                    |
| deltablue                | 3.15 ms                                                                | 3.13 ms: 1.01x faster                                                    |
| django_template          | 35.1 ms                                                                | 34.9 ms: 1.01x faster                                                    |
| tomli_loads              | 1.97 sec                                                               | 1.96 sec: 1.01x faster                                                   |
| chaos                    | 57.5 ms                                                                | 57.2 ms: 1.01x faster                                                    |
| hexiom                   | 5.80 ms                                                                | 5.77 ms: 1.01x faster                                                    |
| scimark_monte_carlo      | 62.9 ms                                                                | 62.5 ms: 1.01x faster                                                    |
| xml_etree_iterparse      | 90.6 ms                                                                | 90.1 ms: 1.01x faster                                                    |
| async_generators         | 353 ms                                                                 | 352 ms: 1.00x faster                                                     |
| python_startup_no_site   | 7.50 ms                                                                | 7.49 ms: 1.00x faster                                                    |
| bpe_tokeniser            | 4.25 sec                                                               | 4.25 sec: 1.00x faster                                                   |
| pidigits                 | 222 ms                                                                 | 222 ms: 1.00x slower                                                     |
| sympy_integrate          | 19.7 ms                                                                | 19.8 ms: 1.00x slower                                                    |
| bench_thread_pool        | 1.03 ms                                                                | 1.03 ms: 1.00x slower                                                    |
| sqlglot_normalize        | 103 ms                                                                 | 103 ms: 1.00x slower                                                     |
| unpickle_pure_python     | 211 us                                                                 | 212 us: 1.00x slower                                                     |
| 2to3                     | 255 ms                                                                 | 256 ms: 1.00x slower                                                     |
| sqlglot_optimize         | 51.9 ms                                                                | 52.1 ms: 1.00x slower                                                    |
| sqlglot_transpile        | 1.56 ms                                                                | 1.57 ms: 1.00x slower                                                    |
| deepcopy                 | 253 us                                                                 | 254 us: 1.01x slower                                                     |
| connected_components     | 399 ms                                                                 | 401 ms: 1.01x slower                                                     |
| go                       | 115 ms                                                                 | 116 ms: 1.01x slower                                                     |
| scimark_fft              | 309 ms                                                                 | 311 ms: 1.01x slower                                                     |
| regex_compile            | 126 ms                                                                 | 127 ms: 1.01x slower                                                     |
| nqueens                  | 77.1 ms                                                                | 77.7 ms: 1.01x slower                                                    |
| subparsers               | 21.7 ms                                                                | 21.9 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult  | 4.18 ms                                                                | 4.22 ms: 1.01x slower                                                    |
| sqlglot_parse            | 1.25 ms                                                                | 1.26 ms: 1.01x slower                                                    |
| spectral_norm            | 98.0 ms                                                                | 99.0 ms: 1.01x slower                                                    |
| pprint_safe_repr         | 702 ms                                                                 | 710 ms: 1.01x slower                                                     |
| pprint_pformat           | 1.45 sec                                                               | 1.46 sec: 1.01x slower                                                   |
| pickle_pure_python       | 313 us                                                                 | 317 us: 1.01x slower                                                     |
| sympy_str                | 270 ms                                                                 | 273 ms: 1.01x slower                                                     |
| comprehensions           | 16.9 us                                                                | 17.1 us: 1.01x slower                                                    |
| pycparser                | 1.11 sec                                                               | 1.12 sec: 1.01x slower                                                   |
| thrift                   | 736 us                                                                 | 746 us: 1.01x slower                                                     |
| async_tree_io            | 621 ms                                                                 | 630 ms: 1.01x slower                                                     |
| logging_format           | 6.79 us                                                                | 6.90 us: 1.02x slower                                                    |
| coroutines               | 21.8 ms                                                                | 22.2 ms: 1.02x slower                                                    |
| sqlalchemy_declarative   | 125 ms                                                                 | 128 ms: 1.02x slower                                                     |
| sqlalchemy_imperative    | 18.9 ms                                                                | 19.4 ms: 1.03x slower                                                    |
| logging_simple           | 6.04 us                                                                | 6.20 us: 1.03x slower                                                    |
| scimark_sor              | 123 ms                                                                 | 128 ms: 1.03x slower                                                     |
| mdp                      | 2.32 sec                                                               | 2.44 sec: 1.05x slower                                                   |
| Geometric mean           | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (29): json, nbody, k_core, async_tree_memoization, scimark_lu, async_tree_memoization_tg, gc_traversal, async_tree_none_tg, sympy_sum, xml_etree_parse, dulwich_log, pathlib, create_gc_cycles, asyncio_websockets, python_startup, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, fannkuch, raytrace, telco, sphinx, coverage, async_tree_none, docutils, async_tree_io_tg, pylint, shortest_path, sympy_expand, float

- Geometric mean (including insignificant results): 1.000x slower

# HPT report

- Reliability score: 87.03% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x