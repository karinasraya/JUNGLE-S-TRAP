# JUNGGLE-S-TRAP

JUNGGLE'S TRAP is a game that use Breadth First Search (BFS) algorithm. This game has a story about a girl or boy that lost in junggle. Then he/she want to go out from junggle. But, in the junggle, there are so many high cliffs, and he/she can't passed the cliff. And the junggle consisting of 5 tier with different track. So, you should help her/him to go out from that junggle.

#

Breadth-first search (BFS) is an algorithm for traversing or searching tree or graph data structures. It starts at the tree root (or some arbitrary node of a graph, sometimes referred to as a 'search key'), and explores all of the neighbor nodes at the present depth prior to moving on to the nodes at the next depth level.

It uses the opposite strategy as depth-first search, which instead explores the highest-depth nodes first before being forced to backtrack and expand shallower nodes.

*The source code for BFS :*

        vector<bool> visited(nodes*nodes, false);
        vector<int> distance(nodes*nodes, 0);
        queue <int> Q;
        distance[a] = 0;
        Q.push(a);
        visited[a] = true;
        
        while (!Q.empty())
        {
            int x = Q.front();
            Q.pop();
            	for (int i=0; i<adj[x].size(); i++)
            	{
                	if (visited[adj[x][i]])
                    	continue;
                	
			distance[adj[x][i]] = distance[x] + 1;
                	Q.push(adj[x][i]);
                	visited[adj[x][i]] = 1;
            	}
        }
        return distance[b];
