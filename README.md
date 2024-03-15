
# Mento contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Q&A

### Q: On what chains are the smart contracts going to be deployed?
Celo
___

### Q: Which ERC20 tokens do you expect will interact with the smart contracts? 
Mento Token
___

### Q: Which ERC721 tokens do you expect will interact with the smart contracts? 
None
___

### Q: Do you plan to support ERC1155?
No
___

### Q: Which ERC777 tokens do you expect will interact with the smart contracts? 
None
___

### Q: Are there any FEE-ON-TRANSFER tokens interacting with the smart contracts?

No
___

### Q: Are there any REBASING tokens interacting with the smart contracts?

No
___

### Q: Are the admins of the protocols your contracts integrate with (if any) TRUSTED or RESTRICTED?
Trusted
___

### Q: Is the admin/owner of the protocol/contracts TRUSTED or RESTRICTED?
Trusted
___

### Q: Are there any additional protocol roles? If yes, please explain in detail:
Canceller(aka watchdog): can cancel queued proposals(Trusted)

___

### Q: Is the code/contract expected to comply with any EIPs? Are there specific assumptions around adhering to those EIPs that Watsons should be aware of?
No
___

### Q: Please list any known issues/acceptable risks that should not result in a valid finding.
- Users may end up with a less-than-ideal voting power if the total multiplier exceeds 1 in the locking formula.
- Locking with a cliff may have a slight advantage over locking with a slope.
- Any problems on the blockchain that impact the block generations will also affect the locking schedule.
- Lack of address(0) checks, provided they do not introduce any additional issues compared to using any other invalid address.
___

### Q: Please provide links to previous audits (if any).
https://0xmacro.com/library/audits/mento-2
https://0xmacro.com/library/audits/mento-3
___

### Q: Are there any off-chain mechanisms or off-chain procedures for the protocol (keeper bots, input validation expectations, etc)?
We use fractal.id for KYC
___

### Q: In case of external protocol integrations, are the risks of external contracts pausing or executing an emergency withdrawal acceptable? If not, Watsons will submit issues related to these situations that can harm your protocol's functionality.
No
___

### Q: Do you expect to use any of the following tokens with non-standard behaviour with the smart contracts?
No
___

### Q: Add links to relevant protocol resources
https://mentolabs.notion.site/Audit-Contest-Documentation-d8482dcefa754ab39b8ec80755596a09
https://www.mento.org/
___



# Audit scope


[mento-core @ d174c8a9810514e0ea0ddd67463854a2bfe80b32](https://github.com/mento-protocol/mento-core/tree/d174c8a9810514e0ea0ddd67463854a2bfe80b32)
- [mento-core/contracts/governance/Airgrab.sol](mento-core/contracts/governance/Airgrab.sol)
- [mento-core/contracts/governance/Emission.sol](mento-core/contracts/governance/Emission.sol)
- [mento-core/contracts/governance/GovernanceFactory.sol](mento-core/contracts/governance/GovernanceFactory.sol)
- [mento-core/contracts/governance/MentoGovernor.sol](mento-core/contracts/governance/MentoGovernor.sol)
- [mento-core/contracts/governance/MentoToken.sol](mento-core/contracts/governance/MentoToken.sol)
- [mento-core/contracts/governance/TimelockController.sol](mento-core/contracts/governance/TimelockController.sol)
- [mento-core/contracts/governance/deployers/AirgrabDeployerLib.sol](mento-core/contracts/governance/deployers/AirgrabDeployerLib.sol)
- [mento-core/contracts/governance/deployers/EmissionDeployerLib.sol](mento-core/contracts/governance/deployers/EmissionDeployerLib.sol)
- [mento-core/contracts/governance/deployers/LockingDeployerLib.sol](mento-core/contracts/governance/deployers/LockingDeployerLib.sol)
- [mento-core/contracts/governance/deployers/MentoGovernorDeployerLib.sol](mento-core/contracts/governance/deployers/MentoGovernorDeployerLib.sol)
- [mento-core/contracts/governance/deployers/MentoTokenDeployerLib.sol](mento-core/contracts/governance/deployers/MentoTokenDeployerLib.sol)
- [mento-core/contracts/governance/deployers/ProxyDeployerLib.sol](mento-core/contracts/governance/deployers/ProxyDeployerLib.sol)
- [mento-core/contracts/governance/deployers/TimelockControllerDeployerLib.sol](mento-core/contracts/governance/deployers/TimelockControllerDeployerLib.sol)
- [mento-core/contracts/governance/locking/Locking.sol](mento-core/contracts/governance/locking/Locking.sol)
- [mento-core/contracts/governance/locking/LockingBase.sol](mento-core/contracts/governance/locking/LockingBase.sol)
- [mento-core/contracts/governance/locking/LockingRelock.sol](mento-core/contracts/governance/locking/LockingRelock.sol)
- [mento-core/contracts/governance/locking/LockingVotes.sol](mento-core/contracts/governance/locking/LockingVotes.sol)
- [mento-core/contracts/governance/locking/interfaces/ILocking.sol](mento-core/contracts/governance/locking/interfaces/ILocking.sol)
- [mento-core/contracts/governance/locking/libs/LibBrokenLine.sol](mento-core/contracts/governance/locking/libs/LibBrokenLine.sol)
- [mento-core/contracts/governance/locking/libs/LibIntMapping.sol](mento-core/contracts/governance/locking/libs/LibIntMapping.sol)

