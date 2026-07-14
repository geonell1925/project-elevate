# Reflection 

Mission 3 marked the point where I began thinking like an Identity Engineer rather than simply supporting Microsoft 365 users.

One of the biggest lessons I learned was to separate authentication from authorization. Before this mission, I often viewed identity issues as login problems. I now understand that successful authentication does not necessarily mean a user has the correct permissions inside an application. Microsoft Entra ID authenticates the identity and issues a security token containing claims, while the Enterprise Application evaluates those claims to determine authorization.

The hotel analogy helped me visualize the identity flow. Microsoft Entra acts as the trusted receptionist that verifies the guest and issues a key card. The key card represents the security token, while the information printed on it represents the claims. Individual areas of the hotel, such as the executive lounge or gym, do not contact the receptionist every time the guest arrives. Instead, they trust the information contained within the key card when deciding whether access should be granted.

This mission also reinforced the importance of following a structured troubleshooting methodology. Rather than immediately checking random settings, I learned to first determine whether authentication or authorization is failing. That distinction allows investigations to become more focused and efficient.

Another important lesson was understanding token lifetime. Changes to group membership or roles may not immediately affect users with active sessions because applications continue trusting existing valid tokens until they expire or are revoked. This explained why removing a user from an administrative group does not always produce an immediate change in application access.

Overall, Mission 3 strengthened both my technical understanding and my engineering mindset. Instead of memorizing identity concepts, I now understand the relationship between authentication, tokens, claims, federation, Enterprise Applications, and authorization. More importantly, I learned to reason through identity problems using evidence and structured troubleshooting rather than assumptions.
