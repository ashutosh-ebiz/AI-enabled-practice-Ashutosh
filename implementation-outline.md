# implementation outline

#BACKEND

- Add the new column is_non_negotiable of boolean type into the events schema. Update the create and the update API to accept this field from the user and Update the GET events API for return this field in response.

#FRONTEND

- Check the isNonNegotiable flag is true or not. If true then show the black dot right to the date and also re-renders the dot conditionally when the user change the status of the meeting from negotiable to non-negotiable or vice-versa.

#INTEGRATION

- Change the existing get events api response type and add the isNonNegotiable boolean type and destructure this on the EventCard.tsx component.

#Testing

- Verify that indicator is appearing for the non-negotiable event which is confirmed by the isNonNegotiable flag coming from the get API. Also check the placement of the dot into the montly and weekly card.
