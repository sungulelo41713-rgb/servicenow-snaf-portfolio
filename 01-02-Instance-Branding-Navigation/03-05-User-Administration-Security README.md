### 📊 Database Schema: Solar Inquiry Table (`u_solar_inquiry`)
*   **Parent Table:** Task (Inherits baseline workflow fields)
*   **Custom Fields Configured:**
    | Column Label | DB Name | Type | Reference / Choices |
    |---|---|---|---|
    | Assigned Kit | `u_assigned_kit` | Reference | `cmdb_ci` |
    | Kasi Region | `u_kasi_region` | Choice | Soweto, Alexandria, Tembisa, Diepsloot |
    | Estimated Daily Peak Load (kWh) | `u_est_daily_peak` | Integer | N/A |

    ### 🔐 Security Implementation Notes
*   **Default Behavior:** Leveraged ServiceNow's auto-generated baseline ACL configurations for the custom table.
*   **Role-Based Enforcement:** Updated the `Requires role` related lists to map explicitly to our functional groups (`x_kce_field_agent`, `x_kce_logistics_manager`, `x_kce_director`), ensuring that Field Agents can update records but only Logistics Managers possess Delete permissions.
