# New-games-
Car gema 
public class CarController : MonoBehaviour
{
    public float speed = 10f;
    public float rotationSpeed = 100f;

    void Update()
    {
        float translation = Input.GetAxis("Vertical") * speed;
        float rotation = Input.GetAxis("Horizontal") * rotationSpeed;

        translation *= Time.deltaTime;
        rotation *= Time.deltaTime;

        transform.Translate(10, 20, translation);
        transform.Rotate(10, rotation, 20);
    }
}
