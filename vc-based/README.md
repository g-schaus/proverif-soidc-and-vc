
# VC-Based Third Party Authentication Protocol

The model...

![MSC of ...](/msc/msc_vc_based.png)

# Results

The following properties...





Query not attacker(check_reach_issuer[]) is false.

Query not attacker(check_reach_user[]) is false.

Query not attacker(check_reach_user_to_pod[]) is false.

Query not attacker(check_reach_pod[]) is false.

Query not attacker(symmetric_key_IU[]) is true.

Query not attacker(symmetric_key_UP[]) is true.

Query inj-event(issuerCompletesProtocol(m_62,m_63,m_64,m_65)) ==> inj-event(userSendsLastMessageToIssuer(m_62,m_63,m_64,m_65)) is true.

Query inj-event(userCompletesProtocol(m_62,m_63,m_64,m_65,m_66)) ==> inj-event(issuerSendsLastMessageToUser(m_62,m_63,m_64,m_65,m_66)) is true.

Query event(userCompletesProtocolFull(m_62,m_63,m_64,m_65,m_66,m_67,m_68,m_69,m_70,m_71,m_72,m_73)) ==> event(issuerSendsLastMessageToUser(m_62,m_63,m_64,m_65,m_66)) && event(podSendsLastMessageToUser(m_67,m_68,m_69,m_70,m_71,m_72,m_73)) is true.

Query inj-event(podCompletesProtocol(m_62,m_63,m_64,m_65,m_66,m_67)) ==> inj-event(userSendsLastMessageToPod(m_62,m_63,m_64,m_65,m_66,m_67)) is true.
