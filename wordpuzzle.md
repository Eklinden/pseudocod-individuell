START

FUNCTION named words
DISPLAY please enter starting word
INPUT word saved 'startword'
DISPLAY please enter end word
INPUT word saved 'endword'

CALCULATE number of letters in startword saved as lettersone
CALCULATE number of letters in startword saved as letterstwo

IF lettersone AND letterstwo is equal
OUTPUT 'lettersone'
       'startword'
       'endword'
ELSE
CALL FUNCTION named words
ENDFUNCTION

FUNCTION named letternumber
DISPLAY Choose what letter to change, 1 = first letter and so on
INPUT number saved as 'change'
IF change is between 1 and 'lettersone'
OUTPUT 'change'
ELSE 
CALL FUNCTION named letternumber
ENDFUNCTION

FUNCTION named letter
DISPLAY Now type what letter to replace it with
INPUT word saved as 'letter'
DISPLAY check if the new word fits. press 1 for yes, 2 for no
INPUT number saved as 'check'
IF 'check' equals 1
OUTPUT 'letter'
ELSEIF check equals 2
CALL FUNCTION named letter
ENDFUNCTION

FUNCTION named wordpuzzle
DISPLAY Please open dictionary.com to play
CALL FUNCTION named words

LOOP untill startword AND endword is equal
CALL FUNCTION named letternumber
CALL FUNCTION named letter
CALCULATE replace the 'change' letter in startword with 'letter'
CALCULATE add 1 to 'tries'
ENDLOOP

DISPLAY YAAAAY YOU WON! it only took 'tries' changes
ENDFUNCTION

CALL FUNCTION named wordpuzzle

END