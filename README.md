# RedX-3D-Basic-Engine
This is Rage3DGL SRC BASED
ORIGINALLY TAKEN FROM "Søren Dreijer"

--SHADER EXAMPLE--
	colorOUT.rgb = saturate(dot(vLightVector, vNormal)) * tex2D(baseTexture, texCoords).rgb * fLightDiffuseColor;
	colorIN.rgb = saturate(dot(vLightVector, vNormal)) * tex2D(baseTexture, texCoords).rgb * fLightDiffuseColor;

--REFLECT_FP.GP--
{
  // Fetch reflected environment color
  float4 reflectedColor = texCUBE(environmentMap, R);
  // Fetch the decal base color
  float4 decalColor = tex2D(decalMap, texCoord);
  color = lerp(decalColor,reflectedColor, reflectivity);

}

 
