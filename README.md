# ci-ncia-de-dados-com-mapa
import pandas as pd

df = pd.read_csv("Cidades.csv")

print(df)

import plotly.express as px

grafico = px.density_mapbox(df, lon="geolocation_lng", lat="geolocation_lat", z="quantidade", mapbox_style="open-street-map",
                            zoom=3, radius=10)
grafico.update_layout(margin={"r": 0, "t": 0, "b": 0, "l": 0})
grafico.show()
