START

FUNCTION named total
INPUT number saved as money
INPUT number saved as dricks
CACULATE +1 to dricks
CALCULATE dricks * money saved as sum
OUTPUT sum
ENDFUNCTION

FUNCTION named people
INPUT number saved as split
OUTPUT split
ENDFUNCTION

FUNCTION named display
DISPLAY Varje person ska betala price kr

FUNCTION named splitthenota
CALL FUNCTION named total
CALL FUNCTION named people
CALCULATE sum / split saved as price
OUTPUT price
CALL FUNCTION named display
ENDFUNCTION

CALL FUNCTION named splitthenota
END