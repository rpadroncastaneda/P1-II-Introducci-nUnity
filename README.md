# Práctica 1: Escena 3D Básica en Unity

## Descripción

Esta práctica consiste en crear una escena 3D básica en Unity utilizando únicamente el editor de escenas. Se han incluido:

- Terreno con texturas importadas de assets externos
- Rocas decorativas importadas de assets del terreno (tag: `Decorative`)
- Cubo y cápsula con materiales propios (tag: `Decorative`)
- Personaje principal en tercera persona (Starter Assets Third Person, tag: `Player`)

## Ejecución

A continuación se muestra un video de la ejecución de la escena (simulando un gif):



![Gif](Gif.gif)

## Script

Pega aquí el código C# que imprime en consola la etiqueta y posición de cada objeto:

```csharp
using UnityEngine;

public class ShowTagsAndPositions : MonoBehaviour
{
  void Start()
  {
    GameObject[] allObjects = FindObjectsOfType<GameObject>();
    foreach (GameObject obj in allObjects)
    {
      if (obj.activeInHierarchy && obj.tag != "Untagged")
      {
        Debug.Log(
          $"Objeto: {obj.name} | Tag: {obj.tag} | Posición: {obj.transform.position}"
        );
      }
    }
  }
}
```

## Tags y objetos agregados

- **Terreno:** Texturas importadas, tag `Decorative`
- **Rocas:** Importadas de assets del terreno, tag `Decorative`
- **Cubo y cápsula:** Materiales propios, tag `Decorative`
- **Personaje principal:** Prefab Third Person, tag `Player`

Las tags permiten identificar fácilmente el propósito de cada objeto en la escena.

## Recursos utilizados

- Starter Assets Third Person
- Asset Store para texturas y rocas
