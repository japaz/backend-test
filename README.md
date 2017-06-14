# Requisites

- Ruby 2.2 or 2.3
- Bundler >= 1.14
- PostgreSQL >= 9.5

# Running

1. `setup.sh`
2. `bundle exec rails s`
3.  Open http://localhost:3000

# For docker
1. `setup_docker.sh`
2.  Open http://localhost:3000

# Challenges

_Please note that output doesn't have to match exactly the previous examples (seed has some randomness)._

1. We want a list of users and group belonging. Display all users, their crypted names, the amount of groups that they belong to, and the name of the groups, sorted by the amount of groups. You should do this with ActiveRecord, but it should trigger as few queries as possible. Example output:

```
Eva - 20VD6w7LkMKOA - 0 - []
Daphne - 20Rz52sSo/wpo - 2 - ["Frontend", "Madrid"]
Charles - 20sn5SsIlkS8E - 3 - ["Product", "Backend", "Madrid"]
Bob - 20H3bGo1QH5VQ - 3 - ["Leads", "Engine", "Madrid"]
Alice - 20EPxrR6s1g7I - 3 - ["Product", "Leads", "Madrid"]
```

2. There's a competition within groups to be the one with more mapviews. Display a list of the mapviews of every user within their groups, sorted by group and mapviews (desc). This can be accomplished with a single SQL query. Example output:

```
Backend, Charles, 1233303
Engine, Bob, 1225498
Frontend, Daphne, 1279748
Leads, Alice, 1249250
Leads, Bob, 1225498
Madrid, Daphne, 1279748
Madrid, Alice, 1249250
Madrid, Charles, 1233303
Madrid, Bob, 1225498
Product, Alice, 1249250
Product, Charles, 1233303
```

3. Extra ball: continuing from the previous task, for each group, we want to know the percentage of mapviews generated by each group member. One SQL query is all you need.

```
 group   |  name   |  views  | percent_of_group_views
----------+---------+---------+-----------------------
 Backend  | Charles | 1211037 | 100.00% 
 Engine   | Bob     | 1223563 | 100.00%
 Frontend | Daphne  | 1264795 | 100.00%
 Leads    | Alice   | 1251522 | 50.56%
 Leads    | Bob     | 1223563 | 49.44%
 Madrid   | Daphne  | 1264795 | 25.55%
 Madrid   | Alice   | 1251522 | 25.28%
 Madrid   | Bob     | 1223563 | 24.71%
 Madrid   | Charles | 1211037 | 24.46%
 Product  | Alice   | 1251522 | 50.82%
 Product  | Charles | 1211037 | 49.18%
 ```

# Submission

Send your solution to [CARTO Backend position](https://boards.greenhouse.io/cartodb/jobs/726194#.WT6AaRPyjUI). Please, don't send PRs, as we want to keep your solutions separated from the challenge. Fork it to your Github profile and send us the link to the diff of your solution.
