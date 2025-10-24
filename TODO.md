# TODO: Add Route Name Filter to ViewDriver Page

## Information Gathered
- ViewDriver.js currently fetches drivers from `/getdrivers` endpoint, which returns basic driver info.
- To show route names, we need to join driver table with vehicle and route tables.
- Current table columns: Staff Code, Staff Name, Vehicle ID, Door No, Street Name, City, State, Pincode, Mobile No, Photo.
- Need to add Route Name column and filter dropdown.

## Plan
1. **Backend Changes**:
   - Update `/getdrivers` endpoint in `route.js` to join with vehicle and route tables to include `routename`.
   - Modify the query to use LEFT JOIN to handle drivers without assigned routes.

2. **Frontend Changes**:
   - Add Route Name column to the driver table in ViewDriver.js.
   - Add a Route Name filter dropdown in the filter section.
   - Update the search/filter logic to include route name filtering.
   - Update state management to handle route name filter.

## Dependent Files to Edit
- `Transport_Management_System/tms/src/Backend/routes/route.js` - Update /getdrivers endpoint
- `Transport_Management_System/tms/src/Frontend/pages/DriverAllotment/ViewDriver.js` - Add route filter and table column

## Followup Steps
- Test the updated ViewDriver page to ensure route names display correctly.
- Verify that the route name filter works properly.
- Check that existing functionality (staff code/name filters) still works.
