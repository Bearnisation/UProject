//using System.Collections;
using UnityEngine;

public class woopwoop : MonoBehaviour {

	//private Vector3 transform.position;
	public int Speed;
	private float Delay;
    private Vector3 NextPos;
	void Start () {
		//transform.position = transform.position;
        NextPos = transform.position;
    }

	void Update () {
		Delay = Speed * 500000;

		print(transform.position);

            if (Input.GetKeyDown("d"))
        {

            NextPos = transform.position + transform.right;
           
            
        }

        if (Input.GetKeyDown("w"))
        {
     
      
            NextPos = transform.position + transform.up;
        }

        if (Input.GetKeyDown("a"))
        {

            NextPos = transform.position - transform.right;
        }

        if (Input.GetKeyDown("s"))
        {

       
            NextPos = transform.position - transform.up;
        }
        transform.position = Vector3.Lerp(transform.position, NextPos,0.05F);
         

        
    }
}
