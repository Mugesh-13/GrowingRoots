# GrowingRoots
Project Title
Growing Roots

Target Audience
Social Activists,Farmers,Biologists.

Team Size
1 (Solo Developer)

Budget
₹0 (Zero)

Timeline
1 Month

Type
Business to Customer (B2C)

✅ Final Feature Order
User Registration
  New users can create accounts.

User Login
  Secure login for returning users.

User Profile Page (Extra Feature)
  Each user can view their requests, planted trees, and suggestions.

Add Trees
  Users or admins can add tree details to the system.

Request Tree Saplings
  Users can request saplings through a simple form.

Types of Species Available
  Display all tree species available with basic info.

Search and Filter Tree Species (Extra Feature)
  Users can quickly find tree types by name or category.

Suggest Suitable Species for User's Land
  Suggest species based on input like soil type and climate.

Species and Their Byproducts
  Information on what each tree species produces (fruits, oils, leaves, etc.).

Learning Hub (Tree Care Tips)
Educational content on tree care and plantation best practices.

----Model class---
public class User {
    private Long id;
    private String name;
    private String email;
    private String password;
    private String location;
    private List<Tree> treesOwned;             // Trees the user added
    private List<SaplingRequest> saplingRequests; // Requests made by this user
    private List<SaplingDonation> saplingDonations; // Saplings ready to donate
}
public class Tree {
    private Long id;
    private String name;
    private List<String> byproducts;           // E.g., ["Fruit", "Oil"]
    private String suitableSoil;               // E.g., Loamy
    private String suitableClimate;            // E.g., Tropical
    private Long ownerId;                      // FK to User who added it
}
public class SaplingRequest {
    private Long id;
    private Long userId;                       // FK to requester
    private String treeName;                   // Type of tree requested
    private Integer quantity;
    private String status;                     // pending/fulfilled
    private String requestDate;
}
public class SaplingDonation {
    private Long id;
    private Long donorId;                      // FK to user
    private String treeName;                   // Type of sapling
    private Integer quantity;
    private String availableFromDate;
}











