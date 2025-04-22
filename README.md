
# 🎯 Multimodal Classification: Audio + Image Fusion

Ce projet propose une solution de classification multimodale combinant des données **visuelles** (images) et **auditives** (audio), en exploitant les forces des réseaux CNN et LSTM, avec une stratégie de **fusion tardive** (late fusion) pour améliorer la précision de prédiction.

## 🚀 Objectifs

- Extraire des caractéristiques pertinentes d'images et d'audios.
- Construire deux modèles indépendants :
  - Un CNN basé sur ResNet50 pour la classification d’images.
  - Un LSTM basé sur les MFCC pour la classification d’audios.
- Fusionner les prédictions des deux modèles pour obtenir une meilleure performance.
## 📁 Structure

1. **Prétraitement des données**
   - Redimensionnement des images à 224x224, normalisation.
   - Extraction des MFCC à partir des fichiers audio.

2. **Extraction des caractéristiques**
   - 📷 Images : ResNet50 (2048 dimensions par image).
   - 🔊 Audio : MFCC .

3. **Modélisation**
   - CNN personnalisé pour les images.
   - LSTM avec Dropout pour l'audio.

4. **Fusion Tardive**
   - Pondération des prédictions CNN (α = 0.6) et LSTM (β = 0.4).
   - Fusion des classes prédictives pour une décision finale.

## 📊 Résultats

| Modèle       | Précision |
|--------------|-----------|
| CNN (Images) | 99.54%    |
| LSTM (Audio) | 84.24%    |
| Fusion       | **99.62%** ✅ |

## 📝 Conclusion

La fusion tardive a permis d'améliorer les performances globales du système. Ce projet démontre l’intérêt de combiner plusieurs modalités pour une meilleure compréhension des données complexes.
