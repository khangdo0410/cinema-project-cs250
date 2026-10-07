# Group 13 contribution workflow

The professor requires EACH group member to push at least one commit. Use your own account and make a real, reviewable contribution. Do not create a commit under another person's identity or add an empty change merely to create a commit record.

## Khang Do

Review the architecture, atomic holds and booking lifecycle in Sections 6.3, 6.6 and 6.8. Own the integrated requirements-plus-design report and its export. The initial document upload is made through Khang's authorized GitHub session; Minh and Phu's individual contribution requirements remain separate.

## Minh Nguyen

Read the Account, Movie, Auditorium, Seat and Showtime specifications and the AuthService/CatalogService interfaces. Make any needed corrections in the editable source. Add `review/minh_accounts_catalog.md` with concrete expected outcomes for these cases:

1. Duplicate email, expired recovery token, and role removal while a session is open.
2. Two showtimes in the same auditorium with exactly 20 minutes of turnaround, then 19 minutes and 59 seconds.
3. A catalog/layout edit after a booking exists; verify which saved receipt and show values remain unchanged.

Write your own reasoning, inputs and expected outputs. Commit and push the edits yourself. A suitable message is `Review account and scheduling design with boundary cases`.

## Phu Pham

Read Payment, Refund, Ticket and AdmissionAttempt and the PaymentService/TicketService interfaces. Make any needed corrections in the editable source. Add `review/phu_payment_admission.md` with concrete expected outcomes for:

1. A successful callback arriving after the hold expires, and a replay of a callback that already confirmed successfully.
2. A card refund timeout followed by reconciliation, and a cash refund that has been approved but not handed back.
3. Two concurrent scans with different request IDs, a retry with the same request ID, and admission exactly at the window boundaries.

Write your own reasoning, inputs and expected outputs. Commit and push the edits yourself. A suitable message is `Review payment refunds and admission boundary cases`.

## Simple GitHub workflow

1. Sign in with your own account. Khang must grant repository collaboration access if you cannot edit; use the correct GitHub username.
2. Pull the latest work if using Git, or open the target file in GitHub and select Edit. To create the review file in GitHub, use Add file > Create new file and enter the path shown above.
3. Write your substantive contribution and commit it with a descriptive message. If using Git locally, also push your commit to the group repository. If using a branch, open a pull request for a teammate to review and merge.
4. Check the repository history shows your own commit and that it reached the remote repository. Confirm with the instructor if they specifically require a command-line push rather than a GitHub web commit.
5. Update the Word/PDF report for accepted design changes. Khang checks the combined report, and one group member submits its file link.

These review files are intentionally not prewritten as completed contributions. Each member must actually perform their review and push their own work.
