1. expectation: add:/addAll:
   `col := OrderedCollection new. col ad`
   alp = nothing
   uni = add:/addAll: 1-2 position
   big = nothing

2. expectation: ifTrue:/ifFalse:
   
   `something := 1. (something = 1) if`
   
   apl = nothing
uni = ifTrue: 1 position followed by ifTrue:ifFalse & ifFalse:
   big = ifTrue: 5 position

   **from here onwards fixed bigram**
   
   `something := 1. (something = 1) ifT`
apl = ifTrue: 2 position
   uni = ifTrue: 1 position
big = ifTrue: 3 position
   
3. TokenProcessing>>returnProcessedData
   `self re`
   apl = readFile 3 position
   uni = nothing
   big = rejectInvalidTokens/replaceWithPlaceholders/readFile 7-8-9 position

4. TokenProcessing>>replaceWithPlaceholders
   `to`

   alp = tokenTypes/tokens (order unideal)
   uni =tokens/tokenTypes
   big = tokens/tokenTypes the only two available (temp var, as should be)

5. `UnigramTableCreator ne`
   apl = new/new: 2-3 pos
   uni = new/new: 1-2 pos
   big = new:/new 4-8 pos

6. creating method initialize
   `ini`
   apl = init 1 pos
   uni = initialize 1 pos
   big = nothing

7. in a test method
   `self as`

   alp = nothing
   uni = assert: assert:equals: 1-2 pos
   big = assert: equals: 1 pos

8. CompletionEvaluation>>averageSuccessRatio
   `countSuccess do: [ :each | su(cursor) ]`

   alp = sumA,sumS, super
   uni = super,sumA,sumS (2-3 are temps)
   big = super,sumA,sumS (2-3 are temps)

9. `RBScanner sc`
   alp = scanTokenObjects:/scanTokens:
   uni = scanTokenObjects:/scanTokens:
   big = scanTokens:/scanTokenObjects:

10. UnigramTableCreator>>writeToFile
    `(NeoCSVWriter on: stream)
                    nextPut: #(key value);
    					ne`

    alp = nothing
    uni = nextPutAll:/nextPut: 2-3 pos

    big = next 1 pos but less relevant