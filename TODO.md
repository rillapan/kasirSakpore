# Layout Fix Plan for PointOfSale Application

## Information Gathered
- The application uses AbsoluteLayout in many forms (Form_Penjualan, Form_Pembelian, Form_Barang, Form_DasbordPemilik), which positions components at fixed coordinates.
- This causes misalignment when the window is resized or maximized, as components do not adjust relative to the container size.
- setPreferredSize is set to fixed dimensions (e.g., 960x540), preventing dynamic resizing.
- In Design View, layouts appear centered, but at runtime, components shift left or misalign.

## Plan
- Replace AbsoluteLayout with flexible layouts (e.g., BorderLayout, GridBagLayout) in affected forms.
- Adjust component positioning to use layout constraints instead of absolute coordinates.
- Remove or modify setPreferredSize to allow resizing.
- Ensure components are centered and responsive.

## Dependent Files to Edit
- app/src/Main/Form_Penjualan.java: Change jPanel1 layout from AbsoluteLayout to BorderLayout, adjust component placements.
- app/src/Main/Form_Pembelian.java: Change jPanel2 layout from AbsoluteLayout to BorderLayout, adjust component placements.
- app/src/Master/Form_Barang.java: Change jPanel3 layout from AbsoluteLayout to BorderLayout, adjust component placements.
- app/src/Main/Form_DasbordPemilik.java: Change jPanel1 layout from AbsoluteLayout to BorderLayout, adjust component placements.
- app/src/Main/Menu_Utama.java: Verify and adjust if needed.

## Followup Steps
- Test the application by running and resizing the window to ensure components align properly.
- Check for any compilation errors after changes.
- If issues persist, refine layout constraints.

## Confirmation
Please confirm if this plan addresses the issue. Proceed with edits?
