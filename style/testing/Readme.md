# Testing

* Prefer `eq` to `==` in RSpec.
* Separate setup, excercise, verification, and teardown phases with newlines. [[sample]](https://github.com/qontak-dev/guides/blob/master/style/testing/four_phase_test.md)

# Factories

* Order factories.rb contents: sequences, traits, factory definitions.
* Order factory attributes: implicit attributes, explicit attributes, child factory definitions. Each section's attributes are alphabetical.
* Order factory definitions alphabetically by factory name.
* Use one factories.rb file per project.


Unit Tests
----------

[Sample](unit_test_spec.rb)

* Don't prefix `it` block descriptions with `should`. Use [Imperative mood]
  instead (Kalimat Bentuk Command / Perintah).
* Use `subject` blocks to define objects for use in one-line specs.
  [Example][subject for one-liners example].
* Put one-liner specs at the beginning of the outer `describe` blocks.
* Use `.method` to describe class methods and `#method` to describe instance
  methods.
* Use `context` to describe testing preconditions.
* Use `describe '#method_name'` to group tests by method-under-test
* Use a single, top-level `describe ClassName` block.
* Order validation, association, and method tests in the same order that they
  appear in the class.

[Imperative mood]: http://en.wikipedia.org/wiki/Imperative_mood
[subject for one-liners example]: unit_test_spec.rb#6
