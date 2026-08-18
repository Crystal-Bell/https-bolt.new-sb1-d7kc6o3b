{
  "material_id": "MAT_PET_002",
  "name": "Polyethylene Terephthalate (PET) 2-Liter Bottle",
  "category": "Rigid Polymer",
  "physical_properties": {
    "state": "Solid",
    "density_g_cm3": 1.38,
    "melting_point_celsius": 250,
    "tensile_strength_mpa": 55,
    "rigidity_index": 0.75,
    "waterproof": true,
    "buoyancy": "High"
  },
  "chemical_behavior": {
    "combustibility": "Moderate (releases toxic fumes if unventilated)",
    "reactive_agents": ["Strong bases", "Ketones"],
    "thermal_shrinkage_temp_celsius": 80
  },
  "utility_affordances": [
    "Fluid containment / Hydration vessel",
    "Structural casing / Sleeve housing",
    "Buoyancy module / Floatation collar",
    "Thermal chimney / Air ducting"
  ]
}# SYSTEM PROMPT: Debris-to-Design Vision Parser
> **Role:** Multimodal Upcycling Computer Vision Agent  
> **Input:** RGB Image Matrix (Kitchen, Yard, or Workshop clutter)  
> **Output Structured Data:** JSON Array of Detected Items with Material Vectors{
  "model": "vision-multimodal-engine-v4",
  "parameters": {
    "temperature": 0.1,
    "response_format": { "type": "json_object" }
  },
  "messages": [
    {
      "role": "system",
      "content": "Analyze the provided image of household or yard debris. Identify every physical item present. For each item, return a JSON object containing: item_name, estimated_quantity, material_composition, structural_state (rigid, flexible, shredded, liquid), and top 3 potential upcycling utility roles based on physical affordances."
    },
    {
      "role": "user",
      "content": [
        {
          "type": "image_url",
          "image_url": { "url": "data:image/jpeg;base64,{user_captured_image_bytes}" }
        }
      ]
    }
  ]
}# https-bolt.new-sb1-d7kc6o3b

"Analyze the uploaded image of household or industrial waste. Identify the primary material composition (e.g., HDPE plastic, corrugated cardboard, aluminum, steel hardware). Map the detected object to its nearest structural category, estimate its dimensional scale, and list three potential upcycled utility applications based on its material rigidity and form factor."
{
  "material_id": "hdpe_plastic_jug_gallon",
  "category": "Rigid Plastic",
  "tensile_strength": "Medium-Low",
  "load_bearing_capacity": "Non-structural / Enclosure or Panel",
  "cutting_tools_required": ["Utility Knife", "Tin Snips"],
  "joining_methods": ["Zip Ties", "Hot Glue", "Rivet Fasteners"],
  "common_sources": ["Milk jugs", "Laundry detergent containers"]
}
