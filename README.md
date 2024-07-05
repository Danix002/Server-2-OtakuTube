# Server-2-OtakuTube

Welcome to Server-2-OtakuTube, a Flask-based API server that helps you find and search for anime information. This server uses the `animeworld` library to fetch anime data and provides several endpoints to interact with the anime database.

## Features

- **Home Route**: Provides information about available routes.
- **Get Anime**: Fetches anime details based on the anime name.
- **Get Anime Not in AnimeWorld**: Lists anime starting with a specific letter that are not in AnimeWorld.
- **Search Anime**: Searches for anime by a query string.

## Installation

1. **Clone the repository**:

2. **Create a virtual python environment and activate it**:

3. **Install the dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Run the Flask server**:
    ```bash
    python AnimeInformation.py
    ```

2. **Access the home route**:
    ```http
    GET http://0.0.0.0:5000/
    ```
    This will provide a list of available routes.

3. **Get Anime details**:
    ```http
    GET http://0.0.0.0:5000/anime/<anime_name>
    ```
    Replace `<anime_name>` with the name of the anime you want to search.

4. **Get Anime Not in AnimeWorld**:
    ```http
    GET http://0.0.0.0:5000/anime_not_in_animeworld/<letter>
    ```
    Replace `<letter>` with the starting letter of anime names you want to search.

5. **Search Anime**:
    ```http
    GET http://0.0.0.0:5000/search_anime/<query>
    ```
    Replace `<query>` with the query string you want to search.

## API Endpoints

### Home Route

- **URL**: `/`
- **Method**: `GET`
- **Description**: Returns a JSON object with a welcome message and available routes.

### Get Anime

- **URL**: `/anime/<string:name>`
- **Method**: `GET`
- **Description**: Fetches details of an anime by name.
- **Parameters**:
    - `name` (string): The name of the anime to search for.

### Get Anime Not in AnimeWorld

- **URL**: `/anime_not_in_animeworld/<string:letter>`
- **Method**: `GET`
- **Description**: Lists anime starting with a specific letter that are not in AnimeWorld.
- **Parameters**:
    - `letter` (string): The starting letter of anime names to search.

### Search Anime

- **URL**: `/search_anime/<string:query>`
- **Method**: `GET`
- **Description**: Searches for anime by a query string.
- **Parameters**:
    - `query` (string): The query string to search for.

## Contribution

Feel free to fork this repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## Contact

For any questions or inquiries, please contact [daniela.adelina94@gmail.com](mailto:daniela.adelina94@gmail.com).

---

Happy coding!
