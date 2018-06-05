# Robot-Navigation
Small, but fun project showing how A* search works that I implemented while studying for Artificial Intelligence Nanodegree 
at Udacity

The following gif shows how A* search works.
The problem is as follows:
Given a 2D plane with some polygon obstacles navigate from Start point to Destination point in shortest possible path.
![ScreenShot](/screenShots/robotNav.gif)

The problem is solved in the following manner:
The original search space is infinite (one can move in any possible direction), however by triangle inequality it is easy to see
that only next steps that go through the polygon vertices need to be considered. This observation reduces the directions that needs
to be evaluated to all the pairs of lines between accessible vertices plus lines from start and to destination nodes.
The heuristics used in the search is (Distance travelled + Distance to destination) Note that leads to search front moving in the
right direction instead of exhaustively evaluating all possible paths.
