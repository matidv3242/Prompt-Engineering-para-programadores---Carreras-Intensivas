import streamlit as st
import openai

# Configuración de la página
st.set_page_config(page_title="FitPlan IA", page_icon="💪", layout="centered")

# Header
st.markdown("""
    <div style='background-color:#2c3e50;padding:10px;border-radius:10px'>
    <h2 style='color:white;text-align:center;'>FitPlan IA</h2>
    <h4 style='color:white;text-align:center;'>Tu rutina personalizada con inteligencia artificial</h4>
    </div>
""", unsafe_allow_html=True)

st.markdown("---")

# Inputs del usuario
st.subheader("Genera tu rutina personalizada")
objetivo = st.selectbox("¿Cuál es tu objetivo principal?", ["Bajar de peso", "Tonificar", "Ganar masa muscular"])
nivel = st.selectbox("¿Cuál es tu nivel de entrenamiento?", ["Principiante", "Intermedio", "Avanzado"])
frecuencia = st.slider("¿Cuántos días por semana podés entrenar?", 1, 7, 3)

# Botón para generar rutina
if st.button("Generar rutina"):
    with st.spinner("Generando tu rutina con IA..."):
        prompt = f"""
        Actúa como un entrenador personal profesional. El usuario quiere una rutina de entrenamiento semanal personalizada. 
        Tiene el siguiente objetivo: {objetivo}. Su nivel de entrenamiento es: {nivel}. Puede entrenar {frecuencia} veces por semana. 
        Crea una rutina completa, explicando qué ejercicios debe hacer cada día, incluyendo repeticiones y recomendaciones básicas.
        """

        # Simulación de la respuesta (modo demo, sin API)
        rutina_demo = f"""
        **Lunes**: Sentadillas, flexiones, abdominales (3x15).\n
        **Miércoles**: Zancadas, remo con mochila, plancha (3x30s).\n
        **Viernes**: Saltos de tijera, abdominales oblicuos, burpees (3x12).\n
        ¡Recordá estirar al final y mantenerte hidratado!
        """
        
        st.markdown("### Tu rutina personalizada:")
        st.success(rutina_demo)

# Footer
st.markdown("---")
st.markdown("""
    <div style='text-align:center;font-size:12px;color:gray;'>
    Proyecto académico - Matías De Vas - 2025
    </div>
""", unsafe_allow_html=True)
