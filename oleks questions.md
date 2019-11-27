decide those things:
1. абсолютний мінімум роботи, який має бути зроблений.
2. які цілі, що маю досягнути.
3. яка має бути робота в кінцевому підсумку.


відповідь про фаро під час захисту : наукові висновки не обмежується фаро, можна екстраполювати на інші технології. бо я шарю принципи, бо ніхто не знає, як юзати н-грами для коду, всі знають що можна, але я з'ясую, які підводні камені і тд.


яка гранулярність токенів - цілий токен чи слова (aka ordered collection як 2 слова), functional vs semantic.


чи треба нам smoothing, наскільки тренування модель на тексті відрізняється на коді, бо там інша повторюваність, можливо в коді нема сенсу це робити.


як на практиці зараз роблять код комплішн в інших IDE (what do other IDEs already use for code completion, any that use ngram models? -- related work section basically).


research questions:
- how is applying the ngram approach to source code different from regular text? what's the best way to approach it?
- is applying ngrams to source code actually beneficial? is it better than what already existed in pharo?
- (potentially) figure out a way to compare accuracies of completion sorting strategies?


#### oleks' ideas for research questions
RQ1: Can we improve code completion in Pharo by sorting candidate completions with an n-gram language model?
RQ2: Can we build a tool based on a trained n-gram model that would propose completion fast enough to be used in an IDE? (user can not wait 30 seconds for a completion to appear)
RQ3: How can we numerically evaluate the results of code completion produced by different completion strategies?
------------
RQ4: How is source code different from natural human languages (English, French) in the context of building statistical language models? Can we effectively model source code with n-gram language models that were designed for natural language? How different is the process of training those models on source code (preprocessing steps, vocabulary size, repetitiveness, predictability, etc.)?

Я раджу зосередитись на питаннях 1-3.
Це виглядає як хороша основа для бакалаврської роботи і для статті.
Питання 4 бонусне. Це просто food for thought.
