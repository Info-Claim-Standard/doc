As we implement info triples and start building computer supported collaborative software,
we face the dilemma that theory meets reality.
Our info triples can no longer be perceived as atoms of knowledge, since there are now a software user involved in the creation process.
This user may or may not be telling the truth.
Hence, in the context of computer supported collaborative work, what we earlier called knowledge we now call a claim.
The info claim is an implementation of this concept.
We take the info triple as presented in the info table and add some extra fields to enable multiuser collaboration. 

| claimid | user | signature | id3 | id1 | id2 |

In short we uses SHA-256 hashes for the info triple identifier 1 and 2.
Then concatenate the two hashes and make a hash of that for id3.
This identifier is then signed with the users private key and the signature is added.
The users public key is added so that the signature can be proven valid.
All the fields created so far are then concatenated and a hash of that will be the claim identifier.
In order to prove the time at which the claim was created the claim identifier can, for example, be added to a blockchain.

