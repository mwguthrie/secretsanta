# secretsanta
Secret Santa pairing and emailing script in Python. 

First, `pairing.py` takes a .csv file where the first row contains column headers (ignored), the first column contains time stamps (ignored), and further columns contain the participants' name, housing pairs (ordered by integer, but could be any matching variable), and email address. It then generates a csv with these columns for 'givers' adjacent to columns for 'receivers,' such that:

1. a person doesn't have to give a gift to themselves;
2. a person doesn't receive a gift from the person they give a gift to; 
3. a person shouldn't give a gift to their partner; 
4. everyone gets one gift. 


Note that the approach is inelegant in that an index vector is 'shuffled,' then checked against conditions 1 through 4, and shuffled again until these conditions are true. 

Then, `sendemail.py` sends an email to each 'giver' with information about his 'receiver,' corresponding with the list generated in the previous script. Run with caution, as this sends an email to everyone upon running!  
