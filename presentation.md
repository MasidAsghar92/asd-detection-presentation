---
marp: true
theme: default
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

<!--
_class: lead
_paginate: false
-->

# ASD Detection Using AI and Brain MRI

## A Deep Learning Approach for Early Autism Diagnosis

**Masid Asghar**

---

# Introduction to ASD Detection

## What is ASD?
- **Autism Spectrum Disorder (ASD)** is a brain development condition
- Affects social skills, communication, and behavior

## Why it matters:
- Early detection helps children learn and improves long-term outcomes
- Current tests are slow and often depend on subjective observation

## Project goal:
- Use AI on brain MRI scans to detect ASD faster and more objectively

---

# Literature Review – Key Points

## What researchers found:
- MRI and deep learning models can detect ASD-related brain patterns
- **3D CNNs** work better than 2D slice methods (use whole brain volume)
- Combining sMRI and fMRI can improve accuracy but increases complexity

## Important lessons:
- **Explainable AI** (Grad-CAM, SHAP) is needed for clinician trust
- Multi-site datasets give better generalization than single-site studies
- Lightweight and privacy-preserving models are promising

---

# Existing Systems – Short Summary

## Simple/mobile tools:
- **ASDetect**: parent questionnaire app, ~83% accurate, depends on parent input
- **SenseToKnow**: eye-tracking prototype; needs special hardware
- **Think Autism**: screening questionnaire — not a clinical diagnosis

## MRI-based research systems:
- Some achieve high accuracy (90%+) using fMRI or multimodal data
- **Main problems**: many are black boxes, single-site, or too complex for clinics

## Gap:
Need a practical, interpretable MRI + AI system that works across sites

---

# Proposed Approach

## Data and model:
- Use **T1-weighted structural MRI (sMRI)** from large public datasets
- Train a **3D convolutional neural network (3D-CNN)** to classify ASD vs. control

## Preprocessing and explainability:
- Preprocess scans (skull strip, normalize, register, resample)
- Use **XAI** (Grad-CAM, SHAP) to show which brain areas influenced the decision

## End product:
- A **web app** where clinicians upload an MRI, get a prediction, explanation, and therapy suggestions

---

# System Modules

1. **Data Acquisition**: download and organize MRI files and metadata
2. **Data Loader**: read NIfTI files, preserve affine and voxel info
3. **Preprocessing**: skull stripping, bias correction, registration, intensity norm
4. **Feature Extraction**: optional handcrafted regional/texture features
5. **3D-CNN Model**: train, validate, and infer ASD vs control
6. **XAI Module**: Grad-CAM/SHAP explanations and heatmaps
7. **Therapy Engine**: map predictions/severity to therapy suggestions
8. **Backend & API**: Flask REST API for processing and report creation
9. **Frontend**: React web app for upload, viewing, and downloads
10. **Database & Storage**: store files, predictions, explanations, reports

---

# Functional Requirements

- Upload MRI files (.nii, .nii.gz)
- Validate file format and metadata
- Automatically run preprocessing pipeline
- Convert preprocessed scans to tensors and run 3D-CNN inference
- Produce prediction: **ASD or Control** with confidence score
- Generate XAI outputs: heatmap + short explanation text
- Generate and show a downloadable report (PDF + web view)
- Store records in database for history and audits
- Provide therapy recommendations when prediction = ASD

---

# Non-Functional Requirements

- **Performance**: fast enough for clinic use (preprocess + predict within reasonable time)
- **Reliability**: handle corrupted files, clear error messages, logging
- **Security & privacy**: anonymize patient data, HTTPS, secure file handling
- **Usability**: easy upload flow, clear results, minimal technical steps
- **Scalability**: support multiple simultaneous users; allow model updates
- **Maintainability**: modular code, clear documentation, replaceable model component

---

# Use Case Overview

## Actors:
- Clinician / Researcher
- System (Backend)

## Main use cases (flow):
1. Clinician uploads MRI file
2. System validates file and metadata
3. System preprocesses the MRI
4. System runs prediction (3D-CNN)
5. System generates XAI explanation and therapy suggestions
6. System stores result and creates a report
7. Clinician views or downloads the report

---

# Conclusion

## Summary:
- AI with sMRI can give faster, more objective ASD screening than behavior-only tests
- 3D-CNN + XAI balances accuracy and trust for clinicians
- A web-based tool makes the system usable in clinics

## Next steps / future work:
- Add more sites and multimodal data (fMRI, DTI) to improve accuracy
- Improve personalization of therapy recommendations
- Deploy and test in real clinical settings

---

<!--
_class: lead
_paginate: false
-->

# Thank You

## Questions?

**Contact**: [Your Email Here]