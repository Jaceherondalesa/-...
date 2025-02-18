respuesta) {
            const correo = "emmanuel07salinas@gmail.com";
            const asunto = "Respuesta del cuestionario";
            const cuerpo = `La respuesta fue: ${respuesta}`;

            // Usar Formspree para enviar el correo
            fetch(url, {
                method: "POST",
                headers: {
                    "Content-Type": "application/json",
                },
                body: JSON.stringify({
                    email: correo,
                    subject: asunto,
                    message: cuerpo,
                }),
            })
            .then(response => {
                if (!response.ok) {
                    console.error("Error al enviar la respuesta.");
                }
            })
            .catch(error => {
                console.error("Error:", error);
            });
        }
    </script>

</body>
</html>
