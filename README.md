# T-Shirt-Problem-Algorithm

Consider the following problem. An organizer of a running race wishes to purchase (at least) n identical T-shirts (same size) for participants. At a wholesale, T-shirts are packaged at different prices depending on the number of T-shirts in the package. The organizer can buy any number of packages of each size (size here is not the T-shirt size, it is the number of T-shirts in a package), as long as the total number is at least n. The organizer wishes to find the minimum total price of such a set of packages. The input is given as n and an array Packages[1..m], where each Package[i] has a positive integer field Package[i].size and a positive real field Package[i].price, giving the number of T-shirts in the package and the price of the package, respectively.

A recursive algorithm to solve this problem is:

BestPrice[n : positiveinteger, Packages[1..m] : array of pairs (size: integer, price: real).]
1. MinPrice ← inf;
2. For d=1 to m do:
3. begin;
4. IF Packages[d].size ≥ n THEN TempPrice ← Packages[d].price
5. ELSE TempPrice ← Packages[d].price + BestPrice(n − Packages[d].size, P ackages);
6. IF TempPrice < MinPrice THEN MinPrice ← TempPrice;
7. end;
8. Return MinPrice.
