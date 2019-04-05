# Copyright 2019 the V8 project authors. All rights reserved.
# Use of this source code is governed by a BSD-style license that can be
# found in the LICENSE file.

vars = {
  'binaryen_url': 'https://chromium.googlesource.com/external/github.com/WebAssembly/binaryen',
  'emscripten_url': 'https://chromium.googlesource.com/external/github.com/emscripten-core/emscripten',
  'fastcomp_url': 'https://chromium.googlesource.com/external/github.com/emscripten-core/emscripten-fastcomp',
  'fastcomp_clang_url': 'https://chromium.googlesource.com/external/github.com/emscripten-core/emscripten-fastcomp-clang',
  'llvm_project_url': 'https://github.com/llvm/llvm-project',
  'wabt_url': 'https://chromium.googlesource.com/external/github.com/WebAssembly/wabt',
  'waterfall_url': 'https://chromium.googlesource.com/external/github.com/WebAssembly/waterfall',
  # TODO: clang, v8 for testing, Gcc for torture tests, llvm test-suite

  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling binaryen
  # and whatever else without interference from each other.
  'binaryen_revision': '2129cef6acbbe4acd5fd675fbb00c329e2220a40',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling emscripten
  # and whatever else without interference from each other.
  'emscripten_revision': '941bbc6b9b35d3124f17d2503d7a32cc81032dac',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling fastcomp
  # and whatever else without interference from each other.
  'fastcomp_revision': '55fe180b3a624c5a7c31dc52ed7af095c5d4fef5',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling fastcomp_clang
  # and whatever else without interference from each other.
  'fastcomp_clang_revision': 'c498993ea75111f013b9fd7bda23eec40bff2970',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling llvm_project
  # and whatever else without interference from each other.
  'llvm_project_revision': '40442658db9461ab86bf33d7889689482a27c874',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling wabt
  # and whatever else without interference from each other.
  'wabt_revision': 'a927578d466838b6dacfdd30c2aebc891bcf594e',
  # Three lines of non-changing comments so that
  # the commit queue can handle CLs rolling waterfall
  # and whatever else without interference from each other.
  'waterfall_revision': '8a69fd9644646c7a63cbdcdbd175cd44036f7b12',
}

deps = {
  # TODO: refactor waterfall script such that we don't have to use the hardcoded work dir.
  'waterfall/src/work/binaryen': Var('binaryen_url') + '@' + Var('binaryen_revision'),
  'waterfall/src/work/emscripten': Var('emscripten_url') + '@' + Var('emscripten_revision'),
  'waterfall/src/work/emscripten-fastcomp': Var('fastcomp_url') + '@' + Var('fastcomp_revision'),
  'waterfall/src/work/emscripten-fastcomp/tools/clang': Var('fastcomp_clang_url') + '@' + Var('fastcomp_clang_revision'),
  'waterfall/src/work/llvm-project': Var('llvm_project_url') + '@' + Var('llvm_project_revision'),
  'waterfall/src/work/wabt': Var('wabt_url') + '@' + Var('wabt_revision'),
  'waterfall': Var('waterfall_url') + '@' + Var('waterfall_revision'),
}