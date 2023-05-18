- 👋 Hi, I’m @lletsgorilla
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
lletsgorilla/lletsgorilla is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
public class ZoomObject : MonoBehaviour
{
    public float zoomSpeed = 2f; // 확대 속도
    public float maxZoom = 5f; // 최대 확대 배율

    private bool isZoomedIn = false; // 확대 여부
    private Vector3 originalScale; // 오브젝트 원래

    public class ZoomObject : MonoBehaviour
    {
        public float zoomSpeed = 2f; // 확대 속도
        public float maxZoom = 5f; // 최대 확대 배율

        private bool isZoomedIn = false; // 확대 여부
        private Vector3 originalScale; // 오브젝트 원래 크기

        private void Start()
        {
            originalScale = transform.localScale;
        }

        public void Zoom()
        {
            if (isZoomedIn)
            {
                // 오브젝트 축소
                transform.localScale = originalScale;
                isZoomedIn = false;
            }
            else
            {
                // 오브젝트 확대
                transform.localScale *= maxZoom;
                isZoomedIn = true;
            }
        }
    }
