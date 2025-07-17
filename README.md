# AdSnap Studio: AI-Powered Advertisement Generation Platform

## Final Report: NAVTTC Data Science Project Documentation

---

### **Student Information**

**Name:** Arshad Khan  
**Email:** arshadkh507@gmail.com  
**Education:** BS Computer Science  
**Domicile:** Karak

### **Project Details**

**Project Title:** AdSnap Studio - AI-Powered Advertisement Generation Platform  
**Project Repository:** https://github.com/arshadkh507/navttc-data-science-project.git  
**Course:** NAVTTC Data Science Program  
**Duration:** 3 months (13-week AI training course)  
**Focus Area:** Computer Vision with NLP Integration  
**Submission Date:** July 2025

---

### **Personal Introduction**

I am Arshad Khan, a Computer Science graduate from Karak, passionate about leveraging artificial intelligence to solve real-world problems. This project represents the culmination of my 13-week intensive training in the NAVTTC Data Science Program, where I developed expertise in machine learning, deep learning, and AI application development.

Through this comprehensive project, I aimed to demonstrate my ability to design, develop, and deploy end-to-end AI solutions that address practical business challenges. The choice of focusing on advertisement generation stems from my interest in computer vision applications and the growing demand for automated content creation in digital marketing.

---

## Table of Contents

1. [Project Overview](#1-project-overview)
2. [Phase 1: Problem Definition & Data Collection](#2-phase-1-problem-definition--data-collection)
3. [Phase 2: Data Preprocessing & Exploration](#3-phase-2-data-preprocessing--exploration)
4. [Phase 3: Feature Engineering](#4-phase-3-feature-engineering)
5. [Phase 4: Model Selection & Training](#5-phase-4-model-selection--training)
6. [Phase 5: Model Evaluation](#6-phase-5-model-evaluation)
7. [Phase 6: Deployment](#7-phase-6-deployment)
8. [Phase 7: Results & Discussion](#8-phase-7-results--discussion)
9. [Phase 8: Conclusion & Future Work](#9-phase-8-conclusion--future-work)
10. [Appendix: Code & Resources](#10-appendix-code--resources)

---

## 1. Project Overview

This project, **"AdSnap Studio: AI-Powered Advertisement Generation Platform"**, represents my comprehensive capstone project for the NAVTTC Data Science Program. As a Computer Science graduate with a passion for artificial intelligence, I developed this solution to demonstrate the practical application of AI/ML concepts learned during the intensive 13-week training course.

### Personal Project Vision

Having observed the challenges faced by small businesses and marketers in creating professional advertisement content, I identified an opportunity to democratize access to high-quality ad generation through AI technology. This project reflects my commitment to developing solutions that bridge the gap between advanced AI capabilities and practical business needs.

### Project Implementation: AdSnap Studio

**AdSnap Studio** is a Streamlit-based web application that I designed and developed to help users generate professional product advertisements using Bria AI's advanced image generation and manipulation APIs. The platform represents my understanding of modern AI architecture patterns and user-centric design principles.

**Personal Motivation:** As someone from Karak, I understand the challenges faced by local businesses in accessing professional design services. This project aims to democratize advertisement creation by making AI-powered tools accessible to users regardless of their technical background or geographic location.

**Technical Achievement:** The project showcases my ability to integrate external AI services, develop intuitive user interfaces, and create scalable applications that solve real-world problems.

**Expected Impact:** Beyond being an academic project, AdSnap Studio demonstrates how AI can be leveraged to provide practical solutions for marketing and e-commerce, particularly benefiting small businesses and entrepreneurs who may lack extensive design resources.

**Focus Area:** The project emphasizes Computer Vision applications with Natural Language Processing integration, reflecting my interest in multimodal AI systems and their practical applications in creative industries.

---

## 2. Phase 1: Problem Definition & Data Collection

### Problem Statement

The project addresses the critical need for efficient and high-quality generation of product advertisement visuals. Traditional methods are often time-consuming and require significant design expertise. AdSnap Studio provides an AI-powered solution for generating professional product packshots, lifestyle images, and performing image manipulation tasks for advertising purposes.

### Objectives

- Develop an interactive web application for AI-driven image generation and manipulation
- Integrate with external AI APIs (Bria AI) for advanced image processing capabilities
- Provide comprehensive functionalities including:
  - Text-to-image generation
  - Packshot creation
  - Shadow addition
  - Lifestyle shot generation
  - Generative fill
  - Element erasure
- Create a user-friendly interface using Streamlit
- Demonstrate practical application of AI/ML skills in a deployable solution

### Data Sources

AdSnap Studio primarily leverages **Bria AI APIs** for its core functionality. Data input sources include:

- User-provided text prompts (product descriptions)
- Uploaded product images for manipulation tasks
- User interface interactions and configurations

### Data Description

The application processes two main types of data:

1. **Text Data:** User-provided descriptions for image generation and prompt enhancement
2. **Image Data:** User-uploaded image files for product packshots, lifestyle shots, generative fill, and element erasure

File type detection for uploaded images is performed using the `python-magic` library to ensure proper handling and validation.

---

## 3. Phase 2: Data Preprocessing & Exploration

### Data Cleaning

Data cleaning in AdSnap Studio focuses on:

- **Input Validation:** Ensuring uploaded image files are valid image types
- **File Format Verification:** Using `python-magic` for accurate file type detection
- **API Input Preparation:** Formatting user inputs for proper API calls to Bria AI services

### Exploratory Data Analysis (EDA)

As AdSnap Studio functions as an interface utilizing pre-trained models via APIs rather than training new models, traditional EDA on raw datasets is not applicable. Instead, the exploration focuses on:

- Understanding Bria AI API capabilities
- Testing various input configurations
- Analyzing output quality and consistency

### Insights

Key insights are derived from the capabilities of the integrated Bria AI APIs in transforming user inputs into desired visual outputs for advertisement purposes, demonstrating the effectiveness of API-based AI solutions.

---

## 4. Phase 3: Feature Engineering

### Feature Selection

In the context of AdSnap Studio, "features" are represented by configurable options and inputs provided to the Bria AI APIs:

- Prompt enhancement settings
- Background removal options
- Shadow addition parameters
- Lifestyle shot configurations
- Advanced settings (background color, shadow intensity)

### Feature Creation

New features are implicitly created by the Bria AI APIs through:

- **Clean Background Generation:** For professional packshots
- **Contextual Scene Placement:** For lifestyle shots
- **AI-Enhanced Prompts:** Feature augmentation for text input
- **Dynamic Image Manipulation:** Based on user selections

### Dimensionality Considerations

Traditional dimensionality reduction techniques are not explicitly implemented as the project relies on pre-trained models provided by Bria AI, which handle internal feature optimization.

---

## 5. Phase 4: Model Selection & Training

### Model Candidates

The project leverages Bria AI's comprehensive suite of pre-trained models:

- **Text-to-Image Generation Models**
- **Packshot Creation Models**
- **Shadow Addition Models**
- **Generative Fill Models**
- **Foreground Erasure Models**

### Training Process

The underlying AI models (including LSTMs, Transformers, CNNs, ResNets) are trained and maintained by Bria AI. This project focuses on:

- Integration and orchestration of API calls
- Configuration management for different model endpoints
- Optimization of API usage patterns

### Hyperparameter Configuration

While core model hyperparameters are managed by Bria AI, users can configure operational parameters:

- Number of images to generate
- Aspect ratio specifications
- Style preferences
- Quality settings

---

## 6. Phase 5: Model Evaluation

### Evaluation Approach

As AdSnap Studio serves as an interface to Bria AI APIs, evaluation focuses on:

- **Output Quality Assessment:** Visual evaluation of generated images
- **Functionality Testing:** Ensuring all features work as expected
- **User Experience Evaluation:** Interface usability and workflow efficiency
- **Performance Monitoring:** Response times and API reliability

### Results

The application successfully demonstrates:

- **HD Product Image Generation:** High-quality images from text descriptions
- **Professional Packshot Creation:** Clean, marketing-ready product images
- **Lifestyle Shot Generation:** Contextual product placement
- **Advanced Image Manipulation:** Generative fill and element erasure capabilities

### Model Selection Rationale

Bria AI was selected as the primary API provider based on:

- Advanced image generation capabilities
- Comprehensive API coverage
- Reliable performance and quality
- Suitable pricing model for the project scope

---

## 7. Phase 6: Deployment

### Deployment Strategy

AdSnap Studio is deployed as a web application using Streamlit, providing an intuitive interface for users to interact with AI-powered image generation and manipulation services.

### Tools & Technologies

#### Core Framework

- **Streamlit (v1.32.0):** Interactive web application framework
- **Python (100.0%):** Primary programming language

#### Dependencies

- **requests (v2.31.0):** HTTP requests to Bria AI APIs
- **python-dotenv (v1.0.1):** Environment variable management
- **Pillow (PIL) (v10.2.0):** Image processing and manipulation
- **python-magic (v0.4.27):** File type detection
- **streamlit-drawable-canvas:** Interactive drawing capabilities
- **numpy:** Numerical operations for image arrays

#### External Services

- **Bria AI APIs:** Core image generation and manipulation services
- **Git/GitHub:** Version control and project management

### User Guide

The application features an organized interface with dedicated tabs:

- **Generate Image:** Text-to-image generation
- **Lifestyle Shot:** Contextual product placement
- **Generative Fill:** Intelligent image completion
- **Erase Elements:** Selective content removal

**Setup Requirements:**

- Valid `BRIA_API_KEY` configured in `.env` file
- Python environment with required dependencies
- Internet connection for API access

---

## 8. Phase 7: Results & Discussion

### Key Findings

AdSnap Studio effectively demonstrates the power of integrating external AI APIs to create functional, user-friendly applications for creative content generation. The project showcases:

- **Successful API Integration:** Seamless connection with Bria AI services
- **Diverse Visual Generation:** Multiple advertisement formats and styles
- **User-Friendly Interface:** Intuitive Streamlit-based design
- **Modular Architecture:** Maintainable and extensible codebase structure

### Interpretation

The project highlights how advanced AI models, accessed via APIs, can be leveraged to build valuable applications that solve real-world creative problems. The modular structure facilitates future enhancements and maintenance.

### Limitations

- **External API Dependency:** Complete reliance on Bria AI service availability
- **API Key Requirement:** Essential configuration for functionality
- **Computational Cost:** API usage costs (detailed analysis needed)
- **Capability Constraints:** Limited to Bria AI's specific offerings

---

## 9. Phase 8: Conclusion & Future Work

### Conclusion

The **AdSnap Studio: AI-Powered Advertisement Generation Platform** successfully demonstrates my ability to design, develop, and deploy a complete AI solution for practical business applications. As a Computer Science graduate from Karak, this project represents my journey from theoretical learning to practical implementation, showcasing skills acquired during the intensive NAVTTC Data Science Program.

**Personal Achievement:** This project reflects my growth from a computer science student to an AI practitioner capable of building end-to-end solutions that address real-world challenges. The experience of developing AdSnap Studio has strengthened my understanding of AI architecture, API integration, and user experience design.

**Technical Accomplishment:** Successfully integrated external AI services, created an intuitive web interface, and demonstrated practical application of AI/ML concepts in a deployable solution.

**Impact Beyond Academia:** AdSnap Studio serves as a testament to how AI education can be translated into tools that benefit businesses and entrepreneurs, particularly those from underserved regions like my home district of Karak.

**Professional Development:** This project has prepared me for advanced roles in AI development, demonstrating my capability to handle complex technical challenges while maintaining focus on user needs and business value.

**Key Achievements:**

- Complete end-to-end AI application development
- Successful integration of external AI services
- User-friendly web interface implementation
- Practical demonstration of learned AI concepts

### Future Work

#### Immediate Enhancements

- **Additional Image Editing Features:** Implement new services in the `services/` directory
- **UI/UX Improvements:** Enhanced Streamlit interface design
- **Expanded Workflows:** Complex multi-service combinations in `workflows/`

#### Advanced Development

- **MLOps Implementation:**
  - MLFlow integration for experiment tracking
  - GitHub Actions for CI/CD pipelines
  - Real-time performance monitoring
  - Automated testing frameworks

#### Scalability Improvements

- **Performance Optimization:** Caching and response time improvements
- **Multi-API Integration:** Additional AI service providers
- **Advanced Analytics:** Usage patterns and performance metrics

---

## 10. Appendix: Code & Resources

### Code Repository

**GitHub Repository:** https://github.com/arshadkh507/navttc-data-science-project

### Project Structure

```
navttc-data-science-project/
├── app.py                 # Main Streamlit application
├── services/             # API service modules
├── components/           # UI components
├── workflows/            # Complex operation workflows
├── requirements.txt      # Project dependencies
├── .env                 # Environment variables
└── README.md            # Project documentation
```

### References

- **Bria AI APIs:** https://bria.ai - Core external service
- **Streamlit Documentation:** Web application framework
- **Python Imaging Library (PIL/Pillow):** Image processing
- **requests Library:** HTTP request handling

### Acknowledgments

I extend my gratitude to the **NAVTTC Data Science Program** for providing comprehensive training that enabled me to develop this project. Special thanks to the instructors and mentors who guided me through the 13-week intensive course, helping me transform from a Computer Science graduate to a skilled AI practitioner.

As a student from Karak, I appreciate the opportunity to participate in this program and develop skills that will contribute to the growing AI ecosystem in Pakistan.

---

**Document Prepared by:** Arshad Khan (arshadkh507@gmail.com)  
**Academic Qualification:** BS Computer Science  
**Location:** Karak  
**Document Generated:** July 2025  
**Project Status:** Complete  
**Total Development Time:** 3 months  
**Primary Language:** Python (100.0%)

---

_This report represents a comprehensive documentation of my NAVTTC Data Science capstone project, showcasing the complete AI development lifecycle from problem definition to deployment and future planning. The AdSnap Studio platform demonstrates my ability to create practical AI solutions that address real-world business challenges._

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
