# leadflow-ai

**Système de qualification et d’activation de leads basé sur l’IA**

Ce projet présente un workflow IA permettant de transformer des leads entrants en décisions structurées, priorisées et actionnables.

---

## Objectif

Automatiser partiellement la qualification des leads tout en conservant :

- des sorties structurées et exploitables  
- un contrôle humain sur les décisions critiques  
- une gestion des entrées non fiables (sécurité)  

---

## Pipeline

```
ingestion → sécurité → analyse LLM → scoring → décision → réponse → activation
```


- **ingestion** : formulaires, CRM, LinkedIn, CSV  
- **sécurité** : détection d’injection de prompt, nettoyage  
- **analyse** : extraction de l’intention et des besoins  
- **scoring** : priorisation des leads (A / B / C / revue manuelle)  
- **réponse** : génération d’emails personnalisés  
- **activation** : simulation CRM et actions commerciales  

---

## Fonctionnalités principales

- analyse de leads via LLM  
- prompting structuré + validation JSON (Pydantic)  
- scoring déterministe et explicable  
- génération de réponses personnalisées  
- couche de sécurité (entrées non fiables, prompt injection)  
- traitement batch et export des résultats  

---

## Sécurité et robustesse

Le système considère tous les messages comme des entrées non fiables et intègre :

- détection des injections de prompt  
- validation des sorties  
- blocage de l’automatisation en cas de risque  
- routage vers revue humaine  

---

## Cas d’usage

- qualification de leads entrants  
- automatisation de la prospection  
- priorisation commerciale  
- structuration des flux CRM  

---

## Intégration (exemples)

- Make / n8n (orchestration)  
- OpenAI API (analyse et génération)  
- Airtable / HubSpot / Pipedrive (CRM)  
- Gmail / Slack (notifications et actions)  

---

## Impact métier

- réduction du temps de qualification manuelle  
- amélioration de la réactivité commerciale  
- standardisation des décisions  
- personnalisation à grande échelle  
- réduction des risques liés à l’automatisation  

---

## Notebook

Le système est démontré dans un notebook Colab :

👉 voir le notebook principal du projet

---

## Positionnement

Ce projet ne se limite pas à un usage de LLM.

Il illustre la conception d’un **système décisionnel basé sur l’IA**, intégrant :

- logique métier  
- sécurité  
- automatisation  
- capacité d’intégration en production  

---

## Licence

MIT

