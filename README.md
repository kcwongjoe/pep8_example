#! /usr/bin/env python
# -*- coding: utf-8 -*-
"""
Example of common PEP 8 conventions.

- 4 spaces per indentation level
- Module and package names should be short, lowercase, and use underscores
"""

# Order of imports

__all__ = ["send_money_to_wife", "FamilyHarmonySimulator"]
__version__ = "0.1"
__author__ = "Wife Lover"

# Standard library imports
import os

# Third-party imports
import pandas as pd

# Local application imports
from my_family import wife_and_husband

FAMILY_HARMONY_DEFAULT_SCORE = 0


# 2 blank lines -> between top-level functions/classes
# 1 blank line  -> between methods inside a class
def send_money_to_wife(family_harmony_score: int, amount_in_pound: int) -> int:
    """
	Update the family harmony score based on the amount sent.
	"""

    family_harmony_score = family_harmony_score + (amount_in_pound * 100)
    return family_harmony_score  # At least two spaces before inline comment


class FamilyHarmonySimulator:
    """Simulator for family harmony."""

    def __init__(self, handsome_husband: bool, husband_likes_cooking = False,
        husband_likes_doing_housework: bool = False, have_children: bool = False,
    ) -> None:

        self.family_harmony_score = FAMILY_HARMONY_DEFAULT_SCORE

        if (
            handsome_husband
            and husband_likes_cooking
            and husband_likes_doing_housework
        ):
            self.family_harmony_score = self.family_harmony_score + 100000
            shopping_list = [
                'oyster', 'oyster', 'oyster',
                'oyster', 'oyster', 'oyster',
            ]

        if have_children:
            self.family_harmony_score = self.family_harmony_score - 50000
            children = {
                'name': 'John',
                'naughty': False,
            }
            children["naughty"] = True

    def show_love_to_wife(self, amount_in_pound: int) -> None:
        """Increase harmony score by sending money to wife."""

		# PEP 257 A blank line after the docstring
        self.family_harmony_score = send_money_to_wife(
            self.family_harmony_score,
            amount_in_pound=amount_in_pound,
        )
# New line at the end of file
