# Changelog

* The following workspace dependencies were updated
  * dependencies
    * co-circom-snarks bumped from 0.1.1 to 0.1.2
    * mpc-core bumped from 0.4.0 to 0.5.0

## [0.6.1](https://github.com/TaceoLabs/co-snarks/compare/co-plonk-v0.6.0...co-plonk-v0.6.1) (2025-04-03)


### Dependencies

* The following workspace dependencies were updated
  * dependencies
    * circom-types bumped from 0.8.0 to 0.9.0
    * co-circom-snarks bumped from 0.4.0 to 0.5.0
    * mpc-net bumped from 0.3.0 to 0.4.0
    * mpc-core bumped from 0.8.0 to 0.9.0

## [0.6.0](https://github.com/Taceolabs/co-snarks/compare/co-plonk-v0.5.0...co-plonk-v0.6.0) (2025-02-20)


### ⚠ BREAKING CHANGES

* ark to 0.5.0, co-noir witext works with 1.0.0-beta.2
* a lot of APIs and types changed
* a lot of APIs and types changed

### Features

* ark to 0.5.0, co-noir witext works with 1.0.0-beta.2 ([8a466df](https://github.com/Taceolabs/co-snarks/commit/8a466dffde68d64bed8265e1336e454559898602))


### Code Refactoring

* co-circom lib usability improvents, added lib usage examples ([5768011](https://github.com/Taceolabs/co-snarks/commit/576801192076a27c75cd07fe1ec62244700bb934))
* co-noir lib usability improvents, added lib usage examples ([18e644e](https://github.com/Taceolabs/co-snarks/commit/18e644ecdf18419fb9b4a071562210c5b0eee0a7))


### Dependencies

* The following workspace dependencies were updated
  * dependencies
    * circom-types bumped from 0.7.0 to 0.8.0
    * co-circom-snarks bumped from 0.3.0 to 0.4.0
    * mpc-net bumped from 0.2.1 to 0.3.0
    * mpc-core bumped from 0.7.0 to 0.8.0

## [0.5.0](https://github.com/TaceoLabs/co-snarks/compare/co-plonk-v0.4.0...co-plonk-v0.5.0) (2024-12-16)


### ⚠ BREAKING CHANGES

* Now the verify impls from groth16/plonk circom return an error indicating whether it was a success or not
* changed the traits for circom bridge. Also modified the from_reader impl for the two Zkeys
* Removes the zkey in the said function signature. We needed it earlier because we had to know domain size, which we now no longer need.
* the prover for Groth16/Plonk now expects an Arc<ZKey>. Cleaner than having multiple Arcs in ZKey
* now uses new mpc-core and forked networking but NO rayon

### Features

* now can specify whether we want curve checks during zkey deser ([e1c03f3](https://github.com/TaceoLabs/co-snarks/commit/e1c03f3ba979bface5ea79062d95ffc088fdfda0))
* prepare functions for compressed rep3 sharing ([55bef10](https://github.com/TaceoLabs/co-snarks/commit/55bef10313378e8ca14f2f22f312c84462a92a7e))
* refactor to use new mpc-core ([43da344](https://github.com/TaceoLabs/co-snarks/commit/43da344be00f00a46849508cea1d279cf29a95b2))


### Bug Fixes

* added a check during groth16 prover for public inputs ([76466eb](https://github.com/TaceoLabs/co-snarks/commit/76466eb2d662efa4d5061e53e09470740763c77f))


### Code Refactoring

* prove for circom now expect Arc&lt;ZKey&gt; ([c2ac465](https://github.com/TaceoLabs/co-snarks/commit/c2ac465ebf6f3a28b902d9f0489e3f57c0843d7f))
* Removed ark_relations deps. Also changed verify impls to not return bool but a common error ([b4f4bf1](https://github.com/TaceoLabs/co-snarks/commit/b4f4bf16beaa83108bc2ae6c6f972ab4e4da4473))
* with_network_config for ShamirGroth16 doesn't need zkey anymore ([2052d89](https://github.com/TaceoLabs/co-snarks/commit/2052d89cc4abb531702886daf70c47ee3b1ecf1a))


### Dependencies

* The following workspace dependencies were updated
  * dependencies
    * circom-types bumped from 0.6.0 to 0.7.0
    * co-circom-snarks bumped from 0.2.0 to 0.3.0
    * mpc-net bumped from 0.2.0 to 0.2.1
    * mpc-core bumped from 0.6.0 to 0.7.0

## [0.4.0](https://github.com/TaceoLabs/co-snarks/compare/co-plonk-v0.3.1...co-plonk-v0.4.0) (2024-11-12)


### ⚠ BREAKING CHANGES

* the prover for Groth16/Plonk now expects an Arc<ZKey>. Cleaner than having multiple Arcs in ZKey
* now uses new mpc-core and forked networking but NO rayon

### Features

* prepare functions for compressed rep3 sharing ([55bef10](https://github.com/TaceoLabs/co-snarks/commit/55bef10313378e8ca14f2f22f312c84462a92a7e))
* refactor to use new mpc-core ([43da344](https://github.com/TaceoLabs/co-snarks/commit/43da344be00f00a46849508cea1d279cf29a95b2))


### Code Refactoring

* prove for circom now expect Arc&lt;ZKey&gt; ([c2ac465](https://github.com/TaceoLabs/co-snarks/commit/c2ac465ebf6f3a28b902d9f0489e3f57c0843d7f))


### Dependencies

* The following workspace dependencies were updated
  * dependencies
    * circom-types bumped from 0.5.0 to 0.6.0
    * co-circom-snarks bumped from 0.1.2 to 0.2.0
    * mpc-net bumped from 0.1.2 to 0.2.0
    * mpc-core bumped from 0.5.0 to 0.6.0

## [0.3.0](https://github.com/TaceoLabs/collaborative-circom/compare/co-plonk-v0.2.0...co-plonk-v0.3.0) (2024-08-21)


### ⚠ BREAKING CHANGES

* we fixed a bug, where the (i)ffts for bls12_381 had a different permutation than from snarkjs. We removed our band-aid fix (FFTPostProcessing). Therfore, it is a breaking change.

### Bug Fixes

* fixes the bls12_381 permutation from arkworks ([f100615](https://github.com/TaceoLabs/collaborative-circom/commit/f100615790c51227d89e886ee6977367e4d5a1ce))


### Dependencies

* The following workspace dependencies were updated
  * dependencies
    * circom-types bumped from 0.4.0 to 0.5.0
    * co-circom-snarks bumped from 0.1.0 to 0.1.1
    * mpc-core bumped from 0.3.0 to 0.4.0

## [0.2.0](https://github.com/TaceoLabs/collaborative-circom/compare/co-plonk-v0.1.0...co-plonk-v0.2.0) (2024-08-14)


### ⚠ BREAKING CHANGES

* We renamed all crate names from collaborative-* to co-* for brevity, and also shortened `Collaborative` to `Co` in many types.

### Code Refactoring

* renamed crates to co-* ([#161](https://github.com/TaceoLabs/collaborative-circom/issues/161)) ([37f3493](https://github.com/TaceoLabs/collaborative-circom/commit/37f3493b25e41b43bbc8a89e281ae2dcb4b95484))

## 0.1.0 (2024-08-14)


### ⚠ BREAKING CHANGES

* to unify Groth16 and PLONK we now take the zkey as ref in PLONK when calling prove
* moved common code for PLONK and Groth16 into separate crate. Most notably the SharedWitness and SharedInput
* PLONK uses the witness struct, therefore we moved it from Groth16 to one level higher
* we hide the modules defining the zkey, proof, vk, and witness and use pub use the re-export them
* the verifier (and the arkwork dep) is now hidden behind the "verifier" feature. Also we refactored some stuff in Groth16 to mirror PLONK.

### Features

* plonk support ([9b65797](https://github.com/TaceoLabs/collaborative-circom/commit/9b6579724f6f5ba4fc6af8a98d386b96818dc08b))


### Code Refactoring

* added new crate co-circom-snarks ([ea3190f](https://github.com/TaceoLabs/collaborative-circom/commit/ea3190f4d731893e6fcce71976c32b3bbac6b89b))
* Added verifier feature for Groth16 ([489614c](https://github.com/TaceoLabs/collaborative-circom/commit/489614cf9242f63c9f9914aaf0b6cc6555deab4c))
* move the groth16 circom types ([fabc5e7](https://github.com/TaceoLabs/collaborative-circom/commit/fabc5e72343f08eea96efde4556dffac60d954cb))
* moved the witness struct ([9cee70b](https://github.com/TaceoLabs/collaborative-circom/commit/9cee70bc58f1980035d02e46e6ea9082a3368182))
* PLONK now takes zkey as ref for prove ([6f613e6](https://github.com/TaceoLabs/collaborative-circom/commit/6f613e6feffece37435da3960afa4d017fe4baa0))


### Dependencies

* The following workspace dependencies were updated
  * dependencies
    * circom-types bumped from 0.3.0 to 0.4.0
    * mpc-core bumped from 0.2.1 to 0.3.0
