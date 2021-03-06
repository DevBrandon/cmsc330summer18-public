# Discussion 2: There Will Be Cake
Due: Tuesday June 5th at 11:59:59PM

Points: 50P/50R/0S

## Introduction
Welcome to Aperture Science's Enrichment Center, a facility dedicated
to testing Aperture's products. Due to significant budget cuts, Aperture
has mandated that all employees must participate in enrichment center testing.
Unfortunately, employee records have been corrupted and tests may not
begin until they have been properly sanitized.

You will write the `ApertureScheduler` class in `scheduler.rb` to ensure
testing may resume. Here are the methods of this class.

### `sanitize(records : Array) -> Array`
The `records` parameter is an array of comma-separated strings each
representing an employee record. You must return all the entries of
the array that are not corrupted. A valid element of record is of
the form: `<ID>,<NAME>,<HOMETOWN>,<DOB>,<EMAIL>`.

* `<ID>` is a 2-digit to 5-digit number.
* `<NAME>` consists of two capitalized alphabetic words separated by a single space.
* `<HOMETOWN>` is a capitalized alphabetic word.
* `<DOB>` is a date in `MM-DD-YYYY` format.
* `<EMAIL>` is an alphanumeric string followed by "@", another alphanumeric string, a ".", and then three alphabetic characters.

Here are examples of valid records:

* `10,Cave Johnson,Chicago,12-15-1901,lemons@aperturescience.com`
* `730,Caroline McLain,Portland,01-17-1930,potato@aperturescience.com`
* `54388,Doug Rattmann,Atlanta,05-20-1950,beans@gmail.com`

### `schedule(records : Array) -> Array`
The `records` parameter is the same as the above, a list of potentially
corrupt employee records. You must return all the non-corrupt entries
in the array, but modifying the format slightly.

1. Sort the entries of the output lexicographically by last name.
2. Modify the names to be last name then first name order.
2. Change the date of birth format to `YYYY-MM-DD`.

## Submission
You should submit a file `scheduler.rb` containing your solution. You may submit other files, but they will be ignored during grading. We will run your solution against MiniTest test units, just as in the provided public test file.

Be sure to follow the description exactly! Your solution will be graded automatically, so any deviation from the specification will result in lost points.
