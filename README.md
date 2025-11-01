###Research Mapper

A C++ data structures and algorithms project that builds a research publication database over authors, articles, and their relationships to enable efficient search, analytics, and collaboration queries[2].

### Features
- Total number of articles published by an author[2].
- Publications per year for a given author[2].
- Number of coauthors per publication of an author[2].
- Papers count by an author’s position (e.g., first author, coauthor)[2].
- Journal names for each article by an author[2].
- Authors at distance d from a given author[2].
- Check if two authors have worked together[2].
- List all coauthors of a given author[2].
- Count of coauthored articles between two authors[2].
- List all article titles by an author[2].
- List all author names in the database[2].

### Data structures
- AVL Trees: used where fast search was required, providing balanced-tree lookups with typical $$O(\log n)$$ operations[2][3].
- Graph: author collaboration network to support connectivity and distance-based queries[2].
- Linked Lists: used for constant-time insertions $$O(1)$$ in adjacency and article/author lists[2].
- Arrays: used for fixed-size or indexed collections where direct access is needed[2].

### Data model
- Articles are stored in an AVL tree; each article node maintains a linked list of its authors[2].
- Authors are stored in an AVL tree; each author maintains a linked list of their articles[2].
- Each author also maintains a year-wise AVL tree, where each year node holds a linked list of that year’s articles[2].
- An author graph captures coauthorship relations to power collaboration and distance queries[2].

### Dataset
- Input dataset is provided in data.csv and contains rows representing articles, their authors, and related metadata used to populate the structures at startup[2].


### Project structure
- r-mapper.cpp — main program entry point and implementation[2].
- data.csv — dataset of articles, authors, and relationships consumed by the program[2].
- README.md — project documentation[2].

### Why these structures
- Linked Lists provide $$O(1)$$ insertions for building per-node collections like author lists per article and article lists per author[2].
- AVL Trees maintain balance to keep search, insert, and delete near $$O(\log n)$$, improving performance over unbalanced BSTs for query-heavy operations[2][3].
- The author Graph supports collaboration queries such as discovering coauthors and enumerating authors at a given distance d in the network[2].

### How to run (quick)
- Compile r-mapper.cpp and ensure data.csv is present in the working directory, then run the generated executable to interact with the menu and query functionalities[2][5].

