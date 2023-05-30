# Principal Protected Note

A principal protected deposit note consists of zero plus call option and linear amortizing bond floor structure. these models are essentially accrual models, determining the current value of the option due to fee accrual and historical hedge fund performance in accordance with the documentation. 

Zero Plus Call is a CAD denominated principal protected note ($100CDN per note), referencing a basked of USD hedge fund investments. The notes are lodged in the Canadian Depository for Securities Ltd., and ultimately marketed to smaller investors.

The value of the note to the investor (the ‘note value’) has an ultimate floor of the current price of a (CAD) zero coupon bond maturing at the maturity of the option, providing principal protection. The valuation of this structure essentially reduces to the valuation of the Zero plus a leveraged investment in an accreting strike option.

Initially the $100CAD investment is split up into the price of a CAD zero coupon bond Z0 maturing at T (option maturity), and the remainder:
	OV(CAD) = $100 − Z0,

Since Z0 purchases the zero, the seller must put up K0 when the deal is initiated to fund the notional investment in a basket of hedge funds.

To hedge CAD/USD exchange rates, the reference basket will contain not only hedge funds, but also a foreign-exchange hedge (buy CAD, sell USD forward), the value of which depends on changes in interest and exchange rates. So at any time, the total basket value is the sum of the two components:
	BV = FXHedge + HFI,

with BV0 = N0 initially. Every month-end, the value of the Hedge fund component (HFI) of the basket is derived from the value of the underlying hedge funds, and the hedge (FXHedge) and zero (Z) revalued based on the then current market conditions. All fees and valuations are based upon these quantities as of month-end.

To simplify matters somewhat, we will consider all quantities here as ‘per-note’, rather than keeping track of how many notes there are outstanding. Making the translation to compare with AAG reports is straightforward.

The Capital Basis is equal to the notional amount: CB = N0 until a re-/de-leveraging occurs, after which it is the lesser of the new notional amount and the original notional amount. Following such a re-/de-leveraging, there will be a net Additional Capital Balance (from additional investor contributions or hedge fund redemption), 

During the first year there is a setup-fee SetUpFee equal to a pre-specified amount per month, divided equally among all notes sold (that is, it is a transaction-level setup fee rather than a note-level fee). Finally there is a monthly basket Management Fee:

Linear Amortizing bond Floor is similar to the ‘Zero plus Call’ structure in that there is principal protection and there are options embedded in the Basket, however, in this case the ‘bond floor’ accretes linearly in time, and there is no clean interpretation of the option as in investment in a zero coupon bond with a leveraged call option.

At initiation of the deal the client invests an amount BV0 _ $10M, part of which is invested in hedge funds (HFI) and the rest in a hedge for the Bond Floor (BFHedge). At any time there may also be a cash component C.

The bond floor is initially set at some fraction above the price of a Zero coupon bond maturing at option maturity with x ~ 3%. (In fact, x is chosen so that the Leverage Ratio, below, is set equal to a target leverage ration of ~ 3.72.) At the end of every month (n) thereafter the bond floor accretes a constant amount every month (t is an integer representing the number of months since the starting date):

The Capital Basis CBt at every month-end is capped at BV0, but can be less due to capital contributions/withdrawals that occur during the life of the deal: If there are no capital contributions/withdrawals then CBt = CBt−1, if the are then CBt = HFIt + BFHedget. Every month a Principal Protection Fee is charged against the capital basis:

References:

https://finpricing.com/lib/FiBond.html

https://derivatives.hcommons.org/interest-rate-derivatives/
