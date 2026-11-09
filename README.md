# Reel Shelf

A personal catalogue of movies and TV series: recommendations, details, ratings from several platforms, where to stream (India by default), and your own lists (Plan to watch, Watching, Watched, Dropped, Favourites) with ratings, notes and episode progress.

It is a static site. It runs on GitHub Pages and saves your lists and uploaded posters back into this repo.

## Set up (about 10 minutes)

1. **Create the repo.** On GitHub, create a new repository (for example `reel-shelf`). Public is the simplest. Your lists will be visible to anyone who finds the repo; private repos need a paid plan to use Pages.
2. **Upload these files** to the repo root: `index.html`, `README.md`, `.nojekyll`, `data/shelf.json`, `posters/.gitkeep`. (Add file > Upload files; keep the folder structure.)
3. **Turn on Pages.** Repo Settings > Pages > Build and deployment > Deploy from a branch > `main` / `(root)` > Save. After a minute your site is at `https://<your-username>.github.io/<repo>/`.
4. **Get a TMDB key** (free): create an account at themoviedb.org, then Settings > API > request a key. Either the API key or the "API Read Access Token" works.
5. *(Optional)* **Get an OMDb key** (free) at omdbapi.com to add IMDb, Rotten Tomatoes and Metacritic ratings.
6. **Create a GitHub token.** GitHub Settings > Developer settings > Personal access tokens > Fine-grained tokens > Generate. Repository access: only this repo. Permissions: Repository > Contents > Read and write.
7. **Open your site > Settings**, paste the TMDB key, optional OMDb key, and the GitHub token (owner and repo are filled in automatically on github.io). Click **Save and test**.
8. Click **Fetch live data** > **Fetch missing**. Posters, streaming availability and ratings are filled in for every starter title. Titles that could not be matched can be fixed by opening them and choosing **Match on TMDB**.

Repeat step 7 on each device you use (phone, laptop). Your lists load from the repo automatically.

## Notes

- Keys and the token live only in your browser's local storage, not in the repo. Use a token limited to this one repo.
- Starter ratings and streaming info are approximate until a title is matched on TMDB.
- Without a token the site still works in read-only sync mode: it shows the lists committed in `data/shelf.json`, and edits stay in that browser.
- Uploaded posters are committed to `posters/`. Posters from TMDB are loaded directly from TMDB and take no repo space.

## Credits

This product uses the TMDB API but is not endorsed or certified by TMDB. Streaming availability data is provided by JustWatch via TMDB. Optional ratings come from OMDb.
