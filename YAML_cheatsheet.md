# YAML cheat sheet
# Reference: https://www.youtube.com/watch?v=cdLNKUoMc6c

# object
person:

  # string value. single/double quotes
  # anchoring
  name: &name "daniel" # anchor name doesn't have to be the same as key name
  occupation: 'student'

  # integer value
  # type casting
  age: !!float 18 # 18.0
  gpa: !!str 3.5 # "3.5"

  # exponential form
  fav_num: 1e+10

  # boolean
  male: true

  # dates (ISO 8601)
  birthday: 2001-01-23 10:00:00

  # null value
  flaws: null

  # list of items
  hobbies: 
    - hiking
    - coding
    - movies
    - riding bike

  # another way to create lists
  movies: ['Dark Knight', "Good Will Hunting"]

  # store list of objects
  friends:
  - name: "steph"
    age: 22
  - {name: 'Adam', age: 22}
  -
    name: "joe"
    age: 23

  # long text. newline will be removed
  description: >
    Labore officia laborum Lorem culpa excepteur anim et. 
    Eiusmod non quis qui tempor ea proident consectetur eiusmod 
    ipsum. Enim consequat proident nisi nostrud ea occaecat 
    fugiat tempor in aliquip irure do minim. Sit esse non 
    laborum et. Minim sit non Lorem esse et quis labore 
    reprehenderit veniam minim. Consequat consequat amet enim 
    magna ea veniam fugiat nulla anim reprehenderit qui irure. 
    Qui aliqua irure sit cupidatat aute commodo cillum id.

  # verbatim. format will be preserved
  signature: |
    Aiman
    PHHM Organization
    email - hejes@gmail.com

  # anchoring. value will refer to anchor &ANCHOR
  id: *name # "daniel"

  # anchoring key-value object
  base: &base
    var1: 'value1'
  foo:
    <<: *base # expands to    var1: 'value1'
    val2: 'value2'
