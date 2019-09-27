# Advice Memo

To: ${ user}

From: Andrew Green

Date: ${ format_date(today())}


The following memo attempts to determine if 
% if like_cats:
our good friend 
% else:
evil cat-hater 
% endif
${user.name.first} who was born ${ user.birthdate}.  I wonder if he/she knows he/she was born on a ${format_date( user.birthdate, format='EEEE')}.  That is, he/she was born on ${format_date( user.birthdate, format='full')} 
We know that ${user.name.first} ${user.name.last}
% if like_cats:
likes cats and is therefore a good person and incapable of committing a crime.
% else:
likes dogs and is likely to have committed other horrible crimes.
% endif
% if eligible_aid:
Regardless, we are pleased that you are eligible for legal aid.
% else:
Regardless, it is unfortunate that you are not elgible for legal aid.
% endif
% if len(child_household) ==0:
You are childless and life is good.
% elif len(child_household) ==1:
You have one child named: ${child_household}.
% else:
You have more than one child.  The names of your children are: ${child_household}.
% endif
