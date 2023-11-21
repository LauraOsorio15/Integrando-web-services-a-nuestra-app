# Integrando-web-services-a-nuestra-app
// Aquí iría la lógica para cargar las fotos recientes del usuario principal y asignar usuarios.

// Ejemplo de carga de fotos (simulado):
function loadTimeline(userId) {
    // Aquí cargarías las fotos recientes del usuario con el ID proporcionado.
    // Puedes usar AJAX, Fetch API u otras técnicas para obtener los datos del servidor.
    console.log(`Cargando fotos del usuario ${userId}...`);
}

// Ejemplo de asignación de usuario principal (simulado):
function assignUser(userId) {
    // Aquí implementarías la lógica para asignar el usuario principal.
    console.log(`Usuario principal asignado: ${userId}`);
}

// Ejemplo de uso:
document.addEventListener('DOMContentLoaded', function() {
    // Cargar fotos del usuario principal al cargar la página (puedes obtener el ID del usuario de tu sistema).
    const principalUserId = '123';
    loadTimeline(principalUserId);
    
    // Evento de clic en el enlace "Asignar Usuario Principal".
    document.querySelector('nav a[href="#"]').addEventListener('click', function() {
        // Puedes mostrar la pantalla de asignación de usuario aquí.
        const newPrincipalUserId = prompt('Ingrese el nuevo usuario principal:');
        if (newPrincipalUserId) {
            assignUser(newPrincipalUserId);
            loadTimeline(newPrincipalUserId); // Recargar fotos del nuevo usuario principal.
        }
    });
});
