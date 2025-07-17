# Iam-Access-control-Simulation
# 🚀 Secure Access Control in IBM Cloud Object Storage using IAM

This project simulates secure and role-based access to **IBM Cloud Object Storage (COS)** using **Identity and Access Management (IAM)**. It demonstrates how permissions are assigned and validated across different user roles — **Viewer**, **Editor**, and **Manager** — through access groups.

---

## 🎯 Objective

To implement and test IAM roles in IBM Cloud COS using:
- Multiple IBM Cloud accounts
- Access groups
- Service IDs (optional)

This showcases how real-world cloud teams manage secure access to shared resources.

---

## 🛠️ Tools & Services Used

- **IBM Cloud Console**
- **IBM Cloud Object Storage (COS)**
- **IBM IAM (Identity & Access Management)**
- **Access Groups & Resource Groups**
- **Service IDs (Optional)**
- **Multiple IBM Cloud Users**

---

## 🧭 Step-by-Step Procedure

### 1. Create a COS Instance
- Go to **IBM Cloud → Catalog → Cloud Object Storage → Create Instance**

### 2. (Optional) Create a Resource Group
- Navigate to **Manage → Account → Resource Groups → Create Resource Group**

### 3. Create Access Groups
- Go to **IAM → Access Groups → Create**
- Create groups like:
  - `ViewerGroup`
  - `EditorGroup`
  - `AdminGroup`

### 4. Assign IAM Roles to Access Groups
- Assign roles **Viewer**, **Writer**, or **Manager** to the COS instance
- Scope permissions to either the COS instance or resource group

### 5. Invite Users
- Go to **IAM → Users → Invite**
- Add users to the corresponding Access Group

### 6. Create a Bucket
- Inside your COS instance → **Buckets → Create Bucket**
- Example: `test-bucket`

### 7. Log In and Test Roles
- Each user logs in and:
  - Accesses COS instance from **Resource List**
  - Performs tasks based on permissions

### 8. (Optional) Use Service IDs
- Go to **IAM → Service IDs → Create**
- Assign to an Access Group
- Use **API Key** for automated testing

---

## ✅ IAM Role Test Matrix

| Action                        | Viewer | Editor | Manager |
|------------------------------|--------|--------|---------|
| View buckets                 | ✅     | ✅     | ✅      |
| Upload files to bucket       | ❌     | ✅     | ✅      |
| Delete objects               | ❌     | ✅     | ✅      |
| Create/Delete buckets        | ❌     | ❌     | ✅      |
| View lifecycle/CORS settings | ❌     | ❌     | ✅      |

---

## 📸 Outputs

- COS access verified for each user role
- Upload/delete tested by Editor and Manager
- **Access Denied** verified for unauthorized actions
- Lifecycle rules visible/editable only by Manager

---

## 🎓 Key Learnings

- IAM role-based security model in IBM Cloud
- How to configure scoped permissions for COS
- Clear distinction between Viewer, Writer, and Manager roles

---

## 📌 Conclusion

This project showcases how **IBM Cloud IAM** enables secure and structured access to **Cloud Object Storage**. Role-based access control is a key element in collaborative cloud environments and this simulation mirrors real-world setups in cloud teams.

---

## 🌱 Future Scope

- Integrate with **Watson AI services**
- Automate access control with **Service IDs**
- Implement logging and auditing with **Activity Tracker**

---

> Created by: Fatima Anab
