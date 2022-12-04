---
code:QTC301-R
---

Title: How quantum key distribution and entanglement impact cloud security

그냥 quantum entanglement를 이용해서 node간에 Key distribution 을 하는 방법을 설명함

qubit은 관측되면 상태가 결정되어버리니까, channel evasedropping같은 security vulnerablilty를 물리학적으로 원천 차단
노드간에 미리 회선을 셋업하고 entanglement 상태를 만들어야해서, spoofing도 안 됨

- 노드간에 직접 fiber를 깔수도 있고, repeater를 둬서 더 멀리있는 노드 간에 network를 형성할수도 있다
- 밀리초에서 초 단위정도 까지밖에 qubit 상태를 유지할수 있다


## between two nodes
QKD용 망과 기존 classical 망을 복합해서 사용.
classical 망은 MACSec, IPSec같은 전통적인 암호 알고리즘으로 보호 (AES같은 블록알고리즘 등)
AES에 먹일 secret key를 QKD로 교환하자

제 3자가 엿들으면 qubit 상태가 정해지니까, 채널이 tampering됬다는걸 바로 알 수 있음 (그래도 DoS는 못 막을듯?)

## between 3 nodes

A-B, B-C 간 QKD 망을 구축하고, A에서 C로 secret을 전달하고 싶으면, 그냥 xor을 한다

## within networks
network graph상에 tampered된 edge가 있으면 다른 경로를 사용한다

# Reference

 - https://aws.amazon.com/blogs/quantum-computing/new-research-from-harvard-and-aws-will-enable-higher-temperature-operation-of-quantum-communications-networks/
 - https://aws.amazon.com/blogs/quantum-computing/an-illustrated-introduction-to-quantum-networks-and-quantum-repeaters/
 - https://aws.amazon.com/blogs/quantum-computing/announcing-a-research-alliance-between-aws-and-harvard-university/
 - https://aws.amazon.com/blogs/quantum-computing/announcing-the-aws-center-for-quantum-networking/
 - ETSI GS QKD 014, protocol spec drift https://www.etsi.org/deliver/etsi_gs/QKD/001_099/014/01.01.01_60/gs_qkd014v010101p.pdf

# Prerequisite
- MACSec: https://en.wikipedia.org/wiki/IEEE_802.1AE
- IPSec: https://en.wikipedia.org/wiki/IPsec
- Diffie hellman key distribution

- https://en.wikipedia.org/wiki/Quantum_logic_gate
- https://en.wikipedia.org/wiki/Quantum_network#Quantum_networks_for_communication
- https://en.wikipedia.org/wiki/Quantum_error_correction
- https://en.wikipedia.org/wiki/Quantum_decoherence
- https://en.wikipedia.org/wiki/Quantum_noise
- https://en.wikipedia.org/wiki/Quantum_entanglement#Meaning_of_entanglement
- https://en.wikipedia.org/wiki/Bell_state

# Related
- https://en.wikipedia.org/wiki/Homomorphic_encryption
- https://arxiv.org/ftp/arxiv/papers/2012/2012.14396.pdf

# Questions
- https://quantumcomputing.stackexchange.com/questions/4219/what-do-they-mean-by-qubit-cant-be-copied
- coherence in physics: https://en.wikipedia.org/wiki/Coherence_(physics)#Mathematical_definition
- How quantum networks deal with transient disconnection?
- qubit이 tampered된 상태인지 어케암??