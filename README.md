```python
#! /usr/bin/env python
# -*- coding: utf-8 -*-
"""
4 spaces per indentation level. Maximum of 79 characters per line.
Module and packages names should be short, lower case with underscores.
"""

# Order of imports

__all__ = ['Do', 'you', 'love', 'your wife', '?']
__version__ = '0.1'
__author__ = 'Wife Lover'

import os # Standard library first

import pandas as pd # 3rd party libs

from my_family import wife_and_hushand # Local libs

FAMILY_HARMONY_DEFAULT_SCORE = 0


# top-level function and class definitions with two blank lines
def send_money_to_wife(family_harmony_score, amount_in_pound):
    """Calculate the hoarmony score based on how much money you sent"""
    family_harmony_score = family_harmony_score + (amount_in_pound * 100)
    return family_harmony_score  # at least 2 space before #


class FamilyHarmonySimulator:
    """Simulator for your family harmony
    """

    family_harmony_score = 0

    def __init__(self, handsome_husband : bool, husband_like_cooking=False,
                 man_like_doing_houseworks=False, have_children=False):

        self.family_harmony_score = FAMILY_HARMONY_DEFAULT_SCORE

        if handsome_husband and husband_like_cooking and \
           man_like_doing_houseworks:
            self.family_harmony_score = self.family_harmony_score + 1e5
            shopping_list = [
                'oyster', 'oyster', 'oyster',
                'oyster', 'oyster', 'oyster',
                ]

        if have_children:
            self.family_harmony_score = self.family_harmony_score - 5e4
            children = {'name': 'John',
                        'naughty': False}
            children['naughty'] = True

    # 1 line space for in-class function
    def send_money_to_wife(self, amount_in_pound):
        """If you love your wife, send as much as money you have.
        """
        self.family_harmony_score = send_money_to_wife(
            self.family_harmony_score, amount_in_pound)

# New line at the end of file
```