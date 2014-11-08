
# Code Schule

##Some Turtle graphics

	clear
	fd 100
	lt 90
	fd 100
	rt 90
	fd 20


##Sequence – let’s do things one after another



	s [fd 100, lt 90]



##Repeat – let’s do the same thing for multiple times (change the value after r)


	r 4 (s [fd 100, lt 90])

##Functions – let’s teach the computer

	let step = s [fd 100, lt 90]
	let square = r 4 step
	square

##Parameters in functions – let’s do the same but with different values

	let circle radius = repeat 45 (s [fd radius, lt 8])
	circle 2
	circle 4

##Recursion – functions that repeat themselves

	let spiral x = if x == 0 then fd 0 else s [fd x/10, rt 10, spiral (x - 1)]
	spiral 100

# More examples

##Draw a house

	lt 90
	fd 100
	rt 90
	fd 100
	rt 45
	fd 71
	rt 90
	fd 71
	rt 135
	fd 100
	lt 135
	fd 142
	lt 135
	fd 100
	lt 135
	fd 142

##Now let’s draw the house again


	let house = s [	lt 90, fd 100, rt 90, fd 100, rt 45, fd 71, rt 90, fd 71, rt 135, fd 100, lt 135, fd 142, lt 135, fd 100, lt 135, fd 142]


##Draw a flower

	let curl x = if x == 0 then fd 0 else s [fd x/10, rt 10, curl (x - 1)]
	let flower = r 6 (curl 102)
	flower

More?

http://eraseallkittens.com/

http://scratch.mit.edu/