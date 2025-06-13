# COFFEE WEBSITE

I've been learning how to make my code responsive across different devices lately. I came across one of my old projects from a HTML course I can't remember right now and decided to revamp it with some CSS.
I made the navbar responsive: for smaller screens we have a menu bar icon and for larger screen we have a top horizontal navigation. This is my first time making such a thing.

```
.top-nav ul {
  list-style-type: none;
  display: flex;
  position: fixed;
  top: 90px;
  right: -100%;
  background-color: var(--color);
  width: 100%;
  height: calc(100vh - 90px);
  flex-direction: column;
  justify-content: center;
  align-items: center;
  transition: all 0.3s;
}

.top-nav ul li {
  margin: 1.25em 0;
}

.top-nav a {
  color: var(--background-color);
  font-size: 1.25rem;
}

.top-nav a:hover,
.top-nav a:focus-visible,
.top-nav .active {
  color: var(--accent-color);
}

.checkbtn {
  font-size: 1.75rem;
  color: var(--background-color);
  cursor: pointer;
  display: block;
  order: 1;
  margin-right: 1.25em;
}

#check {
  display: none;
}

#check:checked ~ ul {
  right: 0;
}

@media only screen and (min-width: 768px) {
.checkbtn {
    display: none;
  }

  .top-nav ul {
    gap: 1.5em;
    position: unset;
    background-color: unset;
    flex-direction: row;
  }

  .top-nav a {
    border-radius: 2px;
    padding: 0.75em;
  }

  .top-nav a:focus-visible,
  .top-nav a:hover {
    background-color: var(--color);
    color: var(--background-color);
  }

  .top-nav .active {
    background-color: var(--accent-color);
    color: var(--background-color);
  }
}

```

I also made the article in the home page responsive: for larger screens every article is displayed in a 2-column grid and for smaller screens only 1-column.

```
@media only screen and (min-width: 768px) {
 section[class^="home"] article {
    grid-template-columns: 1fr 1fr;
  }
}
```

I'm still working on the cross-browser capabilities, but this should be solved in the near future.

I also hope to implement some javascript as I learn.

## TOOLS

- CSS grid
- flexbox

## CREDITS

- [HTML & CSS for Absolute Beginners: Introduction](https://www.youtube.com/watch?v=1L2YiWdaUDM&list=PL4-IK0AVhVjOJs_UjdQeyEZ_cmEV3uJvx&pp=0gcJCWMEOCosWNin)

- [How to Create Responsive Navigation Bar using HTML and CSS](https://www.youtube.com/watch?v=oLgtucwjVII&pp=ygUlY29kaW5nbmVwYWwgcmVzcG9uc2l2ZSBuYXZpZ2F0aW9uIGJhctIHCQneCQGHKiGM7w%3D%3D)
