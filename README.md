# Ex4.1-Animal-Feeding-Phase1

## Aim:

To develop a animal feeding game-Phase-1 using unity.

## Algorithm:
Player Control:
Step 1:
Extract the package and in unity , asserts -> Import packages -> Custom packages and select the package. When we go to Assets folders we can see the course library which we extracted

Step 2:
If you want, drag a different material from Course Library > Materials onto the Ground object

Step 3:
Drag 1 Human, 3 Animals, and 1 Food object into the Hierarchy

Step 4:
Rename the character “Player”, then reposition the animals and food so you can see them

Step 5:
Adjust the XYZ scale of the food (2,2,2) so you can easily see it from above

Step 6:
In your Assets folder, create a “Scripts” folder, and a “PlayerController” script inside.Attach the script to the Player by dragging the c# file to the player and open in the inspector and check whether it is attached.

## Program:
## developed by : Thavanesh B
## register number : 212224040352

## player control 

Name:thavanesh b
Reg No:212224040352
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlayerController : MonoBehaviour
{
    public float horizontalInput;
    public float speed = 10.0f;
    public float xRange = 10f;
    public GameObject projectilePrefab;
    // Start is called before the first frame update
    void Start()
    {

    }

    // Update is called once per frame
    void Update()
    {
        if (transform.position.x < -xRange)
        {
            transform.position = new Vector3(-xRange, transform.position.y, transform.position.z);
        }
        if (transform.position.x > xRange)
        {
            transform.position = new Vector3(xRange, transform.position.y, transform.position.z);
        }
        horizontalInput = Input.GetAxis("Horizontal");
        transform.Translate(Vector3.right * horizontalInput * Time.deltaTime * speed);

        if (Input.GetKeyDown(KeyCode.Space))
        {
            Instantiate(projectilePrefab, transform.position, projectilePrefab.transform.rotation);
        }

    }
}

```
## moving forward :
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class MoveForward : MonoBehaviour
{
    public float speed = 40.0f;
    // Start is called before the first frame update
    void Start()
    {

    }

    // Update is called once per frame
    void Update()
    {
        transform.Translate(Vector3.forward * Time.deltaTime * speed);

    }
}
```


## Output:

<img width="1918" height="1137" alt="image" src="https://github.com/user-attachments/assets/c3395bc1-eed2-498a-8e26-1844d568a804" />


## Result:

Animal feeding game-Phase-1 using unity is developed successfully.
