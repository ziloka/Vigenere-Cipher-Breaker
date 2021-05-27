# Practical Cryptography's Vigenère cipher breaker in C++

This repository contains a C++ implementation of Practical Cryptography's <a href="http://practicalcryptography.com/cryptanalysis/stochastic-searching/cryptanalysis-vigenere-cipher-part-2/">Vigenère cipher breaker</a>, written in Python. Although very effective, Practical Cryptography's algorithm for breaking the Vigenère cipher runs very slowly as a Python program. I felt compelled to modify it, so that it would run faster. I initially tried to use Cython, but that did not result in any noticeable difference. I finally decided to rewrite the entire program in C++ (following the same underlying logic, but introducing some of my own modifications where I saw fit). The difference in speed is very significant, making it more suitable for brute-forcing key lengths.
