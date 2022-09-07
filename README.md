Unity C# Helping Code Guides

Pathfiders Code Examples


```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.AI;


public class Pathfinding : MonoBehaviour
{
    public Transform[] points;
    private NavMeshAgent nav;
    private int destPoint;
    // Start is called before the first frame update
    void Start()
    {
         nav = GetComponent<NavMeshAgent>();
        
    }
    
    
    // Update is called once per frame
    void FixedUpdate()
    {
        if(!nav.pathPending && nav.remainingDistance < 0.5f)
        {
            GotoNextPoint();
        }
    }```
