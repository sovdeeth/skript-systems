# trading

**Requires: my system message skript**

(i should switch to basic messages but i'm lazy)

A basic two-way trading system. Two players must be within 15 blocks (configurable) and can open up a menu that allows them to trade 11 slots worth of whatever. 
The trade requires the acceptance of both parties and will reset acceptance if the trade contents are modified to prevent scams.

To use it, simply use ``/trade <player>`` to send a trade request to a player. They can either click on the request or use ``/trade-accept`` to accept the request and open the trade gui.

All trades are logged to ``Skript/logs/trade-history.log`` for moderation purposes.
