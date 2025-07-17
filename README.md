# navttc-data-science-project

navttc-data-science-project 3 months course

---

# Final Report: Comprehensive Project Documentation

## Table of Contents

1. [Project Overview](#project-overview)
2. [Phase 1: Problem Definition & Data Collection](#phase-1-problem-definition--data-collection)
3. [Phase 2: Data Preprocessing & Exploration](#phase-2-data-preprocessing--exploration)
4. [Phase 3: Feature Engineering](#phase-3-feature-engineering)
5. [Phase 4: Model Selection & Training](#phase-4-model-selection--training)
6. [Phase 5: Model Evaluation](#phase-5-model-evaluation)
7. [Phase 6: Deployment](#phase-6-deployment)
8. [Phase 7: Results & Discussion](#phase-7-results--discussion)
9. [Phase 8: Conclusion & Future Work](#phase-8-conclusion--future-work)
10. [Appendix: Code & Resources](#appendix-code--resources)

---

## Project Overview

Provide a brief summary of the project, its objectives, and the problem statement. Include the motivation behind the project and its expected impact.

---

## Phase 1: Problem Definition & Data Collection

- **Problem Statement:** Clearly define the problem you are solving.
- **Objectives:** List the main goals of the project.
- **Data Sources:** Describe where and how the data was collected (e.g., public datasets, APIs, web scraping).
- **Data Description:** Summarize the data, including the number of samples, features, and target variable.

---

## Phase 2: Data Preprocessing & Exploration

- **Data Cleaning:** Describe steps taken to handle missing values, outliers, and inconsistencies.
- **Exploratory Data Analysis (EDA):** Summarize key findings from EDA, including visualizations and statistical summaries.
- **Insights:** Highlight important patterns or trends discovered.

---

## Phase 3: Feature Engineering

- **Feature Selection:** Explain how relevant features were selected.
- **Feature Creation:** Describe any new features created from existing data.
- **Dimensionality Reduction:** If applicable, discuss techniques used (e.g., PCA).

---

## Phase 4: Model Selection & Training

- **Model Candidates:** List the machine learning models considered.
- **Training Process:** Describe how models were trained, including data splits (train/test/validation).
- **Hyperparameter Tuning:** Summarize the tuning process and chosen parameters.

---

## Phase 5: Model Evaluation

- **Evaluation Metrics:** List and explain the metrics used (e.g., accuracy, precision, recall, F1-score, RMSE).
- **Results:** Present the performance of each model.
- **Model Selection:** Justify the final model choice based on results.

---

## Phase 6: Deployment

- **Deployment Strategy:** Describe how the model was deployed (e.g., web app, API, batch process).
- **Tools & Technologies:** List the tools and platforms used for deployment.
- **User Guide:** Provide instructions for using the deployed solution.

---

## Phase 7: Results & Discussion

- **Key Findings:** Summarize the main results.
- **Interpretation:** Discuss what the results mean in the context of the problem.
- **Limitations:** Note any limitations or challenges faced.

---

## Phase 8: Conclusion & Future Work

- **Conclusion:** Recap the project and its outcomes.
- **Future Work:** Suggest possible improvements or next steps.

---

## Appendix: Code & Resources

- **Code Repository:** Link to the codebase and important scripts.
- **References:** List any papers, articles, or resources used.
- **Acknowledgments:** Credit contributors and supporters.

---

# 📚 Code Documentation

## Packages Used

AdSnap Studio relies on the following main Python packages:

- **streamlit**: For building the interactive web application interface.
- **requests**: For making HTTP requests to Bria AI's APIs and other endpoints.
- **python-dotenv**: For loading environment variables (such as API keys) from a `.env` file.
- **Pillow (PIL)**: For image processing and manipulation.
- **python-magic**: For file type detection.
- **streamlit-drawable-canvas**: For enabling users to draw masks and annotations directly on images within the Streamlit app.
- **numpy**: For numerical operations, especially with image arrays.

## How AdSnap Studio Works

AdSnap Studio is a Streamlit-based application designed to help users generate professional product advertisements using Bria AI's advanced image generation and manipulation APIs. Here’s a high-level overview of its workflow:

1. **User Input**: Users can enter a product description (text prompt) or upload a product image.
2. **Configuration**: Users can configure options in the sidebar, such as:
   - Enhancing prompts with AI
   - Removing backgrounds
   - Adding realistic shadows
   - Creating lifestyle shots (placing products in context)
   - Adding call-to-action (CTA) text overlays
   - Adjusting advanced settings (background color, shadow intensity, etc.)
3. **Image Generation**:
   - The app calls Bria AI APIs to generate HD product images, create lifestyle shots, add shadows, or remove backgrounds based on user input and configuration.
   - Users can use a drawable canvas to mask areas for generative fill or erasure.
4. **Result Display**:
   - Generated images are displayed in the app.
   - Users can download the results directly.
5. **Session Management**:
   - The app uses Streamlit’s session state to manage API keys, generated images, and user settings across interactions.

## Main Components

- **app.py**: The main entry point, handling the UI, user interactions, and orchestrating calls to service functions.
- **services/**: Contains modules for each image manipulation feature (e.g., `packshot`, `lifestyle_shot`, `generative_fill`, etc.), each wrapping a Bria AI API endpoint.
- **components/sidebar.py**: Handles the sidebar configuration UI and collects user preferences.
- **workflows/**: Contains higher-level workflows that combine multiple services for more complex ad generation.

## Example Workflow

1. User uploads a product image and enters a description.
2. User selects "Create Packshot" and configures background color.
3. The app sends the image and options to the Bria API via the `create_packshot` service.
4. The processed image is returned and displayed for download.

## Environment Setup

- The app requires a `.env` file with your Bria API key:
  ```
  BRIA_API_KEY=your_api_key_here
  ```

## 📦 Packages, Libraries, and APIs Used

### Python Packages (with Versions)

- **streamlit==1.32.0**: Interactive web app framework for Python.
- **requests==2.31.0**: HTTP library for making API requests.
- **python-dotenv==1.0.1**: Loads environment variables from a `.env` file.
- **Pillow==10.2.0**: Python Imaging Library for image processing.
- **python-magic==0.4.27**: File type identification using libmagic.
- **streamlit-drawable-canvas**: Streamlit component for drawing on images (version as per PyPI/latest).
- **numpy**: Used for numerical operations and image array manipulation (version as per your environment).

### External APIs and Services

- **Bria AI APIs** (https://bria.ai):
  - `/v1/text-to-image/hd/{model_version}`: Generate HD product images from text prompts.
  - `/v1/product/packshot`: Create professional product packshots from images.
  - `/v1/product/shadow`: Add realistic shadows to product images.
  - `/v1/product/lifestyle_shot_by_text`: Generate lifestyle shots using text descriptions.
  - `/v1/product/lifestyle_shot_by_image`: Generate lifestyle shots using reference images.
  - `/v1/prompt_enhancer`: AI-powered prompt enhancement.
  - `/v1/gen_fill`: Generative fill for masked image areas.
  - `/v1/erase_foreground`: Remove or erase foreground elements from images.

> **Note:** All API endpoints require a valid Bria API key, which should be set in your `.env` file as `BRIA_API_KEY`.

---

# 📝 app.py — Main Application Script Documentation

## Overview

`app.py` is the main entry point for AdSnap Studio. It is responsible for initializing the Streamlit web interface, managing user sessions, and orchestrating all image generation and editing workflows by integrating with Bria AI APIs and internal service modules.

---

## Structure & Main Phases

### 1. Imports and Setup

- **Imports**: Loads essential libraries for UI (`streamlit`), environment management (`os`, `dotenv`), image processing (`PIL`, `numpy`), HTTP requests (`requests`), and custom services from the `services` module.
- **Page Configuration**: Sets up the Streamlit page (title, icon, layout).
- **Environment Variables**: Loads the Bria API key and other environment variables using `python-dotenv`.

### 2. Session State Initialization

- **Function:** `initialize_session_state()`
  - Initializes Streamlit's session state variables to persist user data and app state across interactions.
  - Example variables: `api_key`, `generated_images`, `current_image`, `pending_urls`, `edited_image`, `original_prompt`, `enhanced_prompt`.

### 3. Utility Functions

- **`download_image(url)`**: Downloads an image from a URL and returns it as bytes.
- **`apply_image_filter(image, filter_type)`**: Applies filters (Grayscale, Sepia, High Contrast, Blur) to an image using PIL.
- **`check_generated_images()`**: Checks if images at `pending_urls` are ready (HTTP 200) and updates the session state.
- **`auto_check_images(status_container)`**: Automatically checks for image completion a few times, updating the UI status.

### 4. Main Application Logic

- **Function:** `main()`
  - Builds the Streamlit UI and handles user interaction.
  - **Sidebar**: Lets users input their Bria API key.
  - **Tabs**: The app is organized into four main tabs:
    1. **Generate Image**: Generate product images from text prompts.
    2. **Lifestyle Shot**: Create lifestyle/contextual images from product images.
    3. **Generative Fill**: Inpaint or fill masked areas in images.
    4. **Erase Elements**: Remove unwanted elements from images.

---

## Detailed Functionality by Tab

### 1. 🎨 Generate Image Tab

- **Prompt Input**: Users enter a text prompt describing the desired product image.
- **Prompt Enhancement**: Option to enhance the prompt using Bria AI (`enhance_prompt`).
- **Image Generation**: Calls `generate_hd_image` service with the prompt and user settings (number of images, aspect ratio, style, etc.).
- **Result Display**: Shows generated images and allows download.

### 2. 🖼️ Lifestyle Shot Tab

- **Image Upload**: Users upload a product image.
- **Edit Options**: Choose between creating a packshot, adding a shadow, or generating a lifestyle shot.
- **Packshot**: Calls `create_packshot` service to generate a professional product image with a clean background.
- **Shadow**: Calls `add_shadow` service to add realistic shadows.
- **Lifestyle Shot**: Calls `lifestyle_shot_by_text` or `lifestyle_shot_by_image` to place the product in a contextual scene.

### 3. 🎨 Generative Fill Tab

- **Image Upload & Masking**: Users upload an image and draw a mask over the area to be filled.
- **Prompt Input**: Describe what should appear in the masked area.
- **Generative Fill**: Calls `generative_fill` service to inpaint the masked region using AI.
- **Result Display**: Shows the filled images and allows download.

### 4. 🎨 Erase Elements Tab

- **Image Upload & Masking**: Users upload an image and draw over elements to erase.
- **Erase Foreground**: Calls `erase_foreground` service to remove the selected elements and reconstruct the background.
- **Result Display**: Shows the edited images and allows download.

---

## Key Functions and Their Roles

- **`main()`**: Orchestrates the UI, tab navigation, and user interaction.
- **`initialize_session_state()`**: Ensures all necessary session variables are set.
- **`download_image(url)`**: Utility for fetching images from URLs.
- **`apply_image_filter(image, filter_type)`**: Applies visual effects to images.
- **`check_generated_images()` / `auto_check_images()`**: Manage asynchronous image generation and update the UI when results are ready.

---

## Example Code Snippet: Session State Initialization

```python
# In app.py
def initialize_session_state():
    if 'api_key' not in st.session_state:
        st.session_state.api_key = os.getenv('BRIA_API_KEY')
    if 'generated_images' not in st.session_state:
        st.session_state.generated_images = []
    # ... (other session variables)
```

---

## How to Extend or Modify

- To add new image editing features, implement a new service in the `services/` directory and add a corresponding UI section in `app.py`.
- To change the UI, modify the relevant tab or sidebar code in `main()`.

---

# 📖 In-Depth Codebase Documentation

This section provides a comprehensive overview of the entire AdSnap Studio codebase, describing the purpose and functionality of each file and module.

---

## 1. Main Application: `app.py`

- **Role:** Entry point for the Streamlit web app. Handles UI, session state, and orchestrates all workflows.
- **Key Functions:**
  - `main()`: Builds the UI, manages tab navigation, and user interaction.
  - `initialize_session_state()`: Sets up persistent session variables.
  - Utility functions for downloading images, applying filters, and checking image generation status.
- **Tabs:**
  - **Generate Image:** Text-to-image generation with prompt enhancement.
  - **Lifestyle Shot:** Product placement in contextual scenes, packshot, and shadow addition.
  - **Generative Fill:** Inpainting masked areas with AI.
  - **Erase Elements:** Remove unwanted elements from images.

---

## 2. Services: `services/`

These modules wrap Bria AI API endpoints and provide core image processing features.

- **`__init__.py`**: Exports all service functions for easy import.

- **`lifestyle_shot.py`**

  - `lifestyle_shot_by_text()`: Generates lifestyle images from a product image and scene description.
  - `lifestyle_shot_by_image()`: Generates lifestyle images using a reference image for context.
  - **API Endpoints:** `/v1/product/lifestyle_shot_by_text`, `/v1/product/lifestyle_shot_by_image`

- **`erase_foreground.py`**

  - `erase_foreground()`: Removes the foreground object from an image and reconstructs the background.
  - **API Endpoint:** `/v1/erase_foreground`

- **`generative_fill.py`**

  - `generative_fill()`: Fills masked areas in an image based on a text prompt (inpainting).
  - **API Endpoint:** `/v1/gen_fill`

- **`shadow.py`**

  - `add_shadow()`: Adds realistic or float shadows to product images.
  - **API Endpoint:** `/v1/product/shadow`

- **`packshot.py`**

  - `create_packshot()`: Generates a clean, professional product image (packshot) with optional background removal.
  - **API Endpoint:** `/v1/product/packshot`

- **`hd_image_generation.py`**

  - `generate_hd_image()`: Generates high-definition images from text prompts.
  - **API Endpoint:** `/v1/text-to-image/hd/{model_version}`

- **`prompt_enhancement.py`**
  - `enhance_prompt()`: Improves user prompts using Bria AI's prompt enhancement service.
  - **API Endpoint:** `/v1/prompt_enhancer`

---

## 3. Components: `components/`

Reusable UI elements for Streamlit.

- **`sidebar.py`**

  - `get_config()`: Renders the sidebar and collects user configuration for image generation, packshot, shadow, and lifestyle shot options.

- **`uploader.py`**

  - `render_uploader()`: Renders an image uploader with file type validation and preview.
  - `is_valid_image()`: Checks if the uploaded file is a valid image using `python-magic`.

- **`image_preview.py`**
  - `render_image_preview(result)`: Displays generated images with download buttons and shows API response details.
  - `download_image(url)`: Downloads images from URLs for preview and download.

---

## 4. Workflows: `workflows/`

High-level orchestration of multiple services for complex tasks.

- **`generate_ad_set.py`**
  - `generate_ad_set()`: Given a configuration, generates a set of product ads by chaining together HD image generation, packshot creation, shadow addition, and lifestyle shot creation as needed.

---

## 5. Utilities: `utils/`

- (Not detailed here; add documentation if utility scripts are present.)

---

## 6. Requirements: `requirements.txt`

Lists all Python dependencies with versions. See the earlier section for a full list.

---

## 7. README.md

- Provides project overview, setup instructions, features, and now, in-depth code documentation.

---

## 8. How Everything Connects

- The **UI** (in `app.py` and `components/`) collects user input and configuration.
- **Service modules** in `services/` handle all communication with Bria AI APIs.
- **Workflows** in `workflows/` combine multiple services for advanced ad generation.
- **Session state** ensures a smooth, persistent user experience.

---

## 9. Extending the Codebase

- To add a new feature:
  1. Implement the logic in a new or existing service in `services/`.
  2. Add UI controls in `app.py` or a component in `components/`.
  3. (Optional) Create a workflow in `workflows/` if the feature combines multiple services.

---

This documentation should give you a clear, high-level and detailed understanding of the AdSnap Studio codebase, its structure, and how each part works together.
