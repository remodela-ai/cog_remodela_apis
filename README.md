#  Indoor Design APIs

## Overview

The **Indoor Design API** offers advanced machine learning solutions tailored to interior design needs. Using sophisticated computer vision, this API provides tools for scaling, staging, and spatial analysis to enhance layout planning, object recognition, and design coherence in indoor spaces. Developed as part of the **Google for Startups** programme, these tools are perfect for designers, architects, and developers looking to integrate AI-driven design intelligence into their applications.

---

## Key Features

- **Virtual Staging**: Manipulate scenes by changing materials, objects, and layouts with precision.
- **Spatial Scaling**: Accurately calculate room dimensions based on reference objects and layout arrangements.
- **Object Recognition**: Identify objects within a space and generate masks for enhanced design flexibility.
- **Style Transfer**: Apply artistic styles to furniture and decor to customise room aesthetics.
- **Panoptic Masking**: Segment objects, people, and backgrounds for comprehensive space analysis.

---

## Models

Our API integrates multiple models to offer a range of capabilities for interior design use cases:

### Virtual Staging
- **_remodela-ai / virtual_staging_i** – Stage initial room designs with foundational object manipulation.
- **_remodela-ai / virtual_staging_ii** – Provides advanced scene staging, including material and object transitions.
- **_remodela-ai / virtual_staging_iii** – Enhanced virtual staging for multi-object setups in various lighting.

### Spatial Scaling
- **_remodela-ai / scaling-model-v1** – Interior decoration space scaling, ideal for layout estimation.
- **_remodela-ai / scaling-model-v2** – Improved scaling with higher accuracy in object-based reference scaling.
- **_remodela-ai / scaling-model-v3** – Latest model providing optimised space scaling for complex indoor layouts.

### Object Recognition & Masking
- **_remodela-ai / recognize-anything** – Object recognition to identify various indoor items.
- **_remodela-ai / object-masks** – Generates object-specific masks for layered scene editing.
- **_remodela-ai / panoptic-masks** – Combines object, person, and background masking for seamless integration.

### Style Transfer
- **_remodela-ai / style-transfer-i** – High-resolution style transfer with over 1,000 unique runs.
- **_remodela-ai / style-transfer-ii** – Enhanced style customisation and compatibility for furniture and decor items.

---

## Getting Started

### Requirements

- **API Key**: Obtain an API key through the [Houdini Exe platform](https://houdiniexample.com/signup).
- **Compatibility**: Supports modern web and mobile applications with JSON-based request-response interactions.

### Installation

#### Node.js

```bash
npm install houdini-exe-design-api
```

#### Python

```bash
pip install houdini-exe-design-api
```

### Authentication

Include your API key with each request, either as a query parameter or in the request header.

---

## API Endpoints

### 1. Virtual Staging

*Transform indoor scenes by modifying objects, materials, and spatial layouts.*

**Endpoint**: `/v1/stage`

**Request Example**:

```json
POST /v1/stage
{
    "image_url": "https://example.com/room.jpg",
    "model": "virtual_staging_ii"
}
```

**Response Example**:

```json
{
    "status": "success",
    "staged_image": "https://example.com/staged_room.jpg"
}
```

### 2. Spatial Scaling

*Estimate room dimensions based on layout and reference objects.*

**Endpoint**: `/v1/scale`

**Request Example**:

```json
POST /v1/scale
{
    "image_url": "https://example.com/room.jpg",
    "model": "scaling-model-v2"
}
```

**Response Example**:

```json
{
    "dimensions": {
        "width": 5.2,
        "height": 3.1,
        "depth": 4.0
    }
}
```

### 3. Object Recognition & Masking

*Identify and segment objects within a room for enhanced design manipulation.*

**Endpoint**: `/v1/recognize`

**Request Example**:

```json
POST /v1/recognize
{
    "image_url": "https://example.com/room.jpg",
    "model": "recognize-anything"
}
```

**Response Example**:

```json
{
    "objects": [
        {"name": "sofa", "coordinates": [120, 200]},
        {"name": "table", "coordinates": [400, 300]}
    ]
}
```

---

## Support

For help or feedback, contact our support team at support@houdiniexample.com, or view our complete [API documentation](https://houdiniexample.com/docs).
