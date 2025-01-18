# Java Counter Race Condition

This repository demonstrates a race condition in a simple Java counter class and its solution.

## Description

The `Counter` class is designed to increment a counter. However, if multiple threads access the `increment()` method concurrently, a race condition can occur. This leads to incorrect results where the final counter value is less than expected.

## Bug

The original `Counter.java` demonstrates the race condition. When multiple threads attempt to increment the counter concurrently, the increment operation is not atomic, leading to lost updates.

## Solution

The solution, provided in `CounterFixed.java`, uses the `synchronized` keyword to make the `increment()` method thread-safe. This ensures that only one thread can access the method at a time, preventing the race condition and guaranteeing correct counter updates.