# Rasa Support Agent — MVP (FR/EN)

Agent IA de support client basé sur **Rasa Open Source 3.x**.
Fonctions : horaires, adresse, menu/allergènes (ex.), statut de commande simple, transfert vers humain.

## Démarrage rapide
python -m venv .venv
# Windows: .venv\Scripts\activate | macOS/Linux: source .venv/bin/activate
pip install --upgrade pip
pip install rasa==3.6.* rasa-sdk==3.6.*
rasa train
rasa shell
# REST (optionnel): rasa run --enable-api

## Structure
- config.yml, domain.yml
- data/nlu.yml, data/rules.yml, data/stories.yml
- actions/actions.py (logique métier)
- endpoints.yml

## Licence / usage
Dépôt **privé** pour l’instant. Ne pas commiter de secrets (mots de passe, clés API). 
# Exemple de variables locales (ne pas commiter le vrai .env)
CRM_API_KEY=
SUPPORT_EMAIL=support@example.com
ACTION_SERVER_URL=http://localhost:5055/webhook
.venv/
.env
__pycache__/
.rasa/
*.log

