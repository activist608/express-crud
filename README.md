# Rendu · CRUD Express

- `POST /citations` avec `{"texte":" ","auteur":"Ada"}` : réponse `400 Bad Request` avec un message JSON, car `texte` est vide après `trim()`.
- Après `DELETE /citations/1`, `GET /citations/1` renvoie `404 Not Found` avec `{"message":"Citation introuvable"}`.

`req.params.id` vient du segment correspondant à `:id` dans le chemin de l’URL, par exemple `"1"` dans `/citations/1`. `req.body` vient du corps de la requête ; ici, `express.json()` le lit lorsque la requête envoie du JSON avec `Content-Type: application/json`.
