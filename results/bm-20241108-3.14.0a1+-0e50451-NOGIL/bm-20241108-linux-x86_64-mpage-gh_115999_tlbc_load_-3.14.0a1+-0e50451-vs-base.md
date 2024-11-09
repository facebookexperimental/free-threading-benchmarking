# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: 0e50451
- commit date: 2024-11-08
- overall geometric mean: 1.03x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 4.74 sec                                                               | 4.56 sec: 1.04x faster                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark       | bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_tcp_ssl | 3.27 sec                                                               | 3.21 sec: 1.02x faster                                                |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (4): asyncio_tcp, coroutines, asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): float, nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.89 ms                                                                | 5.14 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (3): regex_dna, regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|--------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python | 889 us                                                                 | 759 us: 1.17x faster                                                  |
| tomli_loads        | 4.15 sec                                                               | 4.03 sec: 1.03x faster                                                |
| unpickle_list      | 7.92 us                                                                | 8.36 us: 1.06x slower                                                 |
| pickle             | 15.6 us                                                                | 17.4 us: 1.12x slower                                                 |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (10): xml_etree_generate, pickle_dict, pickle_list, json_dumps, unpickle_pure_python, xml_etree_process, unpickle, xml_etree_parse, xml_etree_iterparse, json_loads

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 124 ms                                                                 | 109 ms: 1.14x faster                                                  |
| django_template | 83.8 ms                                                                | 75.9 ms: 1.10x faster                                                 |
| genshi_text     | 53.5 ms                                                                | 50.7 ms: 1.05x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                | bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|--------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| sqlglot_optimize         | 135 ms                                                                 | 112 ms: 1.20x faster                                                  |
| meteor_contest           | 216 ms                                                                 | 182 ms: 1.19x faster                                                  |
| pickle_pure_python       | 889 us                                                                 | 759 us: 1.17x faster                                                  |
| genshi_xml               | 124 ms                                                                 | 109 ms: 1.14x faster                                                  |
| sqlglot_parse            | 4.31 ms                                                                | 3.79 ms: 1.14x faster                                                 |
| gc_traversal             | 4.62 ms                                                                | 4.09 ms: 1.13x faster                                                 |
| scimark_lu               | 299 ms                                                                 | 265 ms: 1.13x faster                                                  |
| unpack_sequence          | 213 ns                                                                 | 190 ns: 1.12x faster                                                  |
| pprint_safe_repr         | 1.69 sec                                                               | 1.51 sec: 1.12x faster                                                |
| hexiom                   | 17.3 ms                                                                | 15.5 ms: 1.12x faster                                                 |
| deepcopy_memo            | 72.2 us                                                                | 64.9 us: 1.11x faster                                                 |
| richards                 | 112 ms                                                                 | 101 ms: 1.11x faster                                                  |
| json                     | 8.20 ms                                                                | 7.43 ms: 1.10x faster                                                 |
| sympy_integrate          | 47.0 ms                                                                | 42.6 ms: 1.10x faster                                                 |
| django_template          | 83.8 ms                                                                | 75.9 ms: 1.10x faster                                                 |
| pprint_pformat           | 3.35 sec                                                               | 3.04 sec: 1.10x faster                                                |
| bench_mp_pool            | 70.6 ms                                                                | 64.3 ms: 1.10x faster                                                 |
| sqlglot_normalize        | 227 ms                                                                 | 207 ms: 1.09x faster                                                  |
| pathlib                  | 37.1 ms                                                                | 34.0 ms: 1.09x faster                                                 |
| deepcopy                 | 560 us                                                                 | 517 us: 1.08x faster                                                  |
| pylint                   | 591 ms                                                                 | 547 ms: 1.08x faster                                                  |
| sympy_str                | 677 ms                                                                 | 630 ms: 1.07x faster                                                  |
| typing_runtime_protocols | 340 us                                                                 | 318 us: 1.07x faster                                                  |
| sympy_expand             | 1.29 sec                                                               | 1.20 sec: 1.07x faster                                                |
| sqlite_synth             | 4.36 us                                                                | 4.12 us: 1.06x faster                                                 |
| genshi_text              | 53.5 ms                                                                | 50.7 ms: 1.05x faster                                                 |
| deepcopy_reduce          | 5.36 us                                                                | 5.15 us: 1.04x faster                                                 |
| docutils                 | 4.74 sec                                                               | 4.56 sec: 1.04x faster                                                |
| tomli_loads              | 4.15 sec                                                               | 4.03 sec: 1.03x faster                                                |
| asyncio_tcp_ssl          | 3.27 sec                                                               | 3.21 sec: 1.02x faster                                                |
| regex_effbot             | 4.89 ms                                                                | 5.14 ms: 1.05x slower                                                 |
| unpickle_list            | 7.92 us                                                                | 8.36 us: 1.06x slower                                                 |
| spectral_norm            | 215 ms                                                                 | 228 ms: 1.06x slower                                                  |
| pickle                   | 15.6 us                                                                | 17.4 us: 1.12x slower                                                 |
| scimark_sparse_mat_mult  | 8.51 ms                                                                | 9.71 ms: 1.14x slower                                                 |
| Geometric mean           | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (53): chaos, xml_etree_generate, generators, regex_dna, coverage, python_startup_no_site, pickle_dict, telco, bench_thread_pool, asyncio_tcp, pickle_list, comprehensions, json_dumps, scimark_fft, coroutines, thrift, deltablue, 2to3, pyflate, scimark_sor, float, unpickle_pure_python, scimark_monte_carlo, xml_etree_process, sympy_sum, fannkuch, crypto_pyaes, go, unpickle, xml_etree_parse, logging_simple, asyncio_websockets, logging_format, dulwich_log, raytrace, mako, nbody, xml_etree_iterparse, regex_compile, json_loads, bpe_tokeniser, regex_v8, logging_silent, nqueens, pycparser, mdp, sqlglot_transpile, async_generators, python_startup, pidigits, create_gc_cycles, html5lib, richards_super

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x