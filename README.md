# Off grid mesh communications research

This research covers decentralized mesh communications that is suitable for use in off grid scenarios where no existing infrastructure is available. A number of commercial products and open source products exist in this space already. The goal of this research is to investigate the existing solutions, projects and technologies for use in off-grid mesh network communications.

*This is intended as a living paper. Contributions are encouraged, especially if you have experience in the field*

## Contents

- [Off grid mesh communications research](#Off-grid-mesh-communications-research)
  - [Contents](#Contents)
  - [Motivation](#Motivation)
  - [Scope](#Scope)
  - [Commercial Products](#Commercial-Products)
    - [GoTenna](#GoTenna)
  - [Open Source Projects](#Open-Source-Projects)
  - [Technology](#Technology)
  - [Discussion](#Discussion)
  - [Conclusion](#Conclusion)

## Motivation

In December 2018, while on family holiday in Namibia my mother went for for what was supposed to be a 5km trail run in a rough desert mountain range early one morning. It was supposed to take less than an hour, yet after 2 hours she had not returned. Fearing that she possibly got lost and injured we mounted a search, which was seriously hampered by the lack of proper communication. There was no cell service in the area and we were stuck trying to use department store "walkie talkies", which became useless the moment there was a hill separating two people. Which is serious issue when the entire area consists only of steep hills and valleys.

My mother ended up reappearing 4 hours later, unhurt, having accidentally ended up on a longer 20km route. But the experience remained with me and I started brainstorming some possible low cost solutions for communications in similar scenarios, especially for non line of sight. Normal two way radio repeaters can be expensive or complicated to setup in these ad-hoc situations. Satellite comms is a good option but not exactly cheap. Having played with LORA and other RF modules that work in the license free band, I figured this could work well when interfaced with a smartphone via Bluetooth or Wi-Fi. After a some google searches I came across a number of commercial products and open source products that do exactly that.

## Scope

This research focuses on technology with the following requirements:

- Does not rely on existing infrastructure (cell networks/ satellite / permanent repeaters)
- Works in the license free (ISM) bands
- Can be deployed on a ad-hoc basis
- Makes use of mesh networking
- Can send text as a minimum
- Does not need mains power
- Should have a line of sight range of >1km

## Commercial Products
There is a number of commercial products available, that have various levels of adoption

### [GoTenna](https://gotenna.com/)
Of all the products or projects encountered in this research, GoTenna is the most successful, both as a commercial company and a and in terms of adoption level. They offer a consumer version (GoTenna Mesh) and a professional version (GoTenna Pro).

| Spec          | GoTenna Mesh  | GoTenna Pro |
| ------------- | ------------- | -----       |
| Frequencies   | 868/900 Mhz   | 142-175 MHz / 445-480 MHz|
| Output power | 0.5-1W | 0.5-5W |
| Modulation | GFSK | 4GFSK |
| Mesh Networking Protocol | Aspen Grove (Proprietary) | Aspen Grove (Proprietary) |
| Interface | BLE 4.0+ & 5.0 | BLE 4.0+ & 5.0 |
| Payload | 235 Bytes Max | 235 Bytes Max |

GoTenna allows secure mesh communications using other GoTenna devices as relays even if the users do no know each other. A [node map](https://imeshyou.gotennamesh.com/) shows locations of voluntarily registered nodes, whic is quite extensive across the US.

*Note to self: I think GoTenna is doing everything right EXCEPT for keeping everything closes source. This is understandable since they are a commercial company dependant on hardware sales for revenue.

## Open Source Projects

## Technology
Narrow band GFSK modulation  would be ideal due to the amount of available transceivers. 
The LORA is nice but takes up excessive frequency spectrum coverage. The ICs for LORA all come from Semtech

## Discussion

## Conclusion

# Notes (Unedited)
The network should be 
- hardware agnostic
- defined protocol 
- end to end encrypted
- decentralized (not dependant on any central servers
- group chats
- traffic should be able to route via the internet where applicable
- basically a open source and system
