Derive a relational model from each of the ERDs below. 

## Practice #1

```
erdiagram courses
notation=crowsfoot

entity Students {
    id key
    name 
}

entity Courses { 
    number key
    title
}

relationship enrolls_in {
    Students[0..N] -> Courses[0..N]
}
```

![pic1.png](pics/pic1.png)

## Practice #2

```
erdiagram buildings
notation=crowsfoot

entity Buildings {
    name key
    address
}

weak entity Rooms { 
    floor partial-key
    number partial-key
}

weak relationship has {
    Buildings[1] -> Rooms[0..N]
}
```

![pic2.png](pics/pic2.png)

## Practice #3

```
erdiagram candidates
notation=crowsfoot

entity Candidates {
    ssn key
    name 
}

entity JobPositions { 
    number key 
    title 
    department 
}

relationship applies_for {
    Candidates[0..N] -> JobPositions[0..N]
}
```

![pic3.png](pics/pic3.png)

## Practice #4

```
erdiagram buildings
notation=crowsfoot

entity Employees {
    ssn key 
    name 
}

entity Projects { 
    number key 
    title 
}

relationship works_in {
    Employees[0..N] -> Projects[0..N]
    hours
}
```

![pic4.png](pics/pic4.png)

![pic5.png](pics/pic5.png)

## Practice #5

```
erdiagram shippings
notation=crowsfoot

entity Shippings {
    order_number key 
    address
}

weak entity Items { 
    seq_number partial-key
    description 
}

weak relationship has { 
    Shippings[1] -> Items[0..N]
}
```

![pic6.png](pics/pic6.png)


