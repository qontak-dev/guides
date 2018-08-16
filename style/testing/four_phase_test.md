# Four Phase Test

Following this article https://robots.thoughtbot.com/four-phase-test,
there are four distinct phases of the test. They are executed sequentially.

```
test do
   setup
   exercise
   verify
   teardown 
end
```

```ruby
RSpec.describe Person do
  describe "#full_name_with_middle_initial" do
    it "concatenate first name, with middle initial" do
      satya = Person.new(first_name: "Vinsensius", middle_name: "Satya", last_name: "Widhiasmara")
      
      satya.save
 
      expect(satya.full_name_width_middle_initial).to eq("Vinsensius S Widhiasmara")
    end
  end
end
```

### Setup
During setup, the system under test (usually a class, object, or method) is set up.
```ruby
satya = Person.new(first_name: "Vinsensius", middle_name: "Satya", last_name: "Widhiasmara")
```

### Excercise
During exercise, the system under test is executed.
```ruby
satya.save
```

### Verify
During verification, the result of the exercise is verified against the developer’s expectations.
```ruby
expect(satya.full_name_width_middle_initial).to eq("Vinsensius S Widhiasmara")
```

### Teardown
During teardown, the system under test is reset to its pre-setup state.
This is usually handled implicitly by the language (releasing memory) or test framework (running inside a database transaction).
