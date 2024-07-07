# CryptographyEngineering-AttacksonHashFunctions
AttacksOnHashFunctions

 
CA3 - Attacks on Hash Functions

Question 2

(a) Compute the following hash function h:

h = 7 + ∑_{i=1}^k (m_i)^2 mod 251
for a 4-byte message M:

M = {m_1, m_2, m_3, m_4} = {128, 252, 33, 19}
Answer: 
7 + ((128*128) + (252*252) + (33*33) + (19*19)) % 251 = 21

(b) Check if the hash function is:
• Second pre-image resistant (strong collision resistant)
Strong collision resistance can be defined as,
It is infeasible to find any x, y such that 
H(y) = H(x)

• Pre-image resistant (weak collision resistant)
Weak collision resistance can be defined as,
If x is given, it is infeasible to find y such that
H(y) = H(x)
Always the answer will be under 251 + 7, so definitely there will be collisions. 

(c) Show counter examples for any property that is not satisfied in above part (b).
• Examples for Strong collision resistance,

194	[27, 26, 3, 167], [227, 128, 63, 200]
161	[13, 94, 215, 12], [180, 58, 235, 23]
59	[172, 36, 137, 193], [146, 125, 69, 4]
178	[127, 50, 88, 135], [20, 212, 7, 186]
199	[110, 113, 240, 157], [83, 171, 131, 149]
169	[191, 183, 175, 59], [208, 188, 245, 9]
246	[52, 39, 18, 31], [57, 158, 206, 11]
53	[127, 153, 173, 68], [70, 17, 30, 105]
171	[170, 252, 81, 131], [174, 111, 143, 118]
38	[217, 12, 121, 144], [98, 36, 46, 148]

• Examples for Weak collision resistance,
[12, 234, 133, 173] = 117,
[1, 1, 4, 43]
[1, 1, 4, 208]
[1, 1, 5, 121]
[1, 1, 5, 130]
[1, 1, 9, 23]
[1, 1, 9, 228]
[1, 1, 16, 75]
[1, 1, 16, 176]
 

[148, 147, 182, 203] = 134
counter examples,
[1, 1, 1, 56]
[1, 1, 1, 195]
[1, 1, 2, 11]
[1, 1, 2, 240]
[1, 1, 5, 10]
[1, 1, 5, 241]
[1, 1, 6, 66]
[1, 1, 6, 185]

[44, 87, 173, 34] = 186
counter examples,
[1, 1, 2, 115]
[1, 1, 2, 136]
[1, 1, 4, 101]
[1, 1, 4, 150]
[1, 1, 5, 34]
[1, 1, 5, 217]
[1, 1, 8, 102]
[1, 1, 8, 149]



[54, 12, 43, 75] = 250
counter examples,
[1, 1, 1, 95]
[1, 1, 1, 156]
[1, 1, 2, 57]
[1, 1, 2, 194]
[1, 1, 3, 105]
[1, 1, 3, 146]
[1, 1, 4, 15]
[1, 1, 4, 236]

[45, 82, 124, 253] = 40 
counter examples,
[1, 1, 2, 23]
[1, 1, 2, 228]
[1, 1, 3, 111]
[1, 1, 3, 140]
[1, 1, 4, 39]
[1, 1, 4, 212]
[1, 1, 7, 22]
[1, 1, 7, 229] 
