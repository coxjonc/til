Sometimes it's necessary to split a list into sublists on a given value. This can especially come in handy when scraping websites. Imagine you have a list of authors' names ['Dalton', 'Trumbo', 'and', 'Truman', 'Capote'] and want to turn each name into its own list. 

It would be trivial to do this with a for loop, but you can also do it with a simple list comprehension that makes use of the `itertools.groupby` function. Here's how: 

    >>>from itertools import groupby

    >>>names = ['Fred', 'Astaire', 'and', 'Ginger', 'Rogers']

    >>>split_on_and = [list(g) for k,g in groupby(names, lambda x:x == 'and') if not k]

    >>>print split_on_and
    [['Fred', 'Astaire'], ['Ginger', 'Rogers']]
