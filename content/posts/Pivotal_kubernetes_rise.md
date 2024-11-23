+++
title = "VMware, Pivotal and the rise of Kubernetes"
date = "2024-11-23"
summary = "Building a successful platform, spinning out into something new, and facing big shifts in the industry"
tags = ["pivotal","cloudfoundry","kubernetes"]
+++

## Building a Successful Platform  

When I left Engine Yard, I joined VMware to work on the Cloud Foundry team. The idea behind Cloud Foundry was familiar — a PaaS (Platform as a Service) designed to let engineers focus on writing applications without worrying about infrastructure. Whether it was “cf push” on Cloud Foundry, “ey deploy” at Engine Yard, or “heroku up,” the goal was the same. No need to worry about configurations like DNS or nginx. Developers write code and the platform handles the rest.  

But Cloud Foundry was more ambitious than Engine Yard or Heroku. It aimed to be "Google in a box," providing enterprises with a platform they could control and run anywhere. VMware offered a hosted version, and IBM eventually launched their own hosted version, BlueMix. For those who wanted more control, Cloud Foundry could also be deployed independently on public or private clouds using our secret weapon: BOSH. Originally led by Kent Skaar and Vadim Spivak and later completely owned by Pivotal engineers, BOSH was an orchestration system for the orchestration system. It deployed all of Cloud Foundry, attaching disks and networks seamlessly. Based on Google's BORG, BOSH was powerful, reliable, and instrumental in making Cloud Foundry a flexible, enterprise-ready solution.

Mark Lucovsky, who led engineering, brought a storied past from his days at Microsoft, where he helped develop the NT Kernel. Mark had a reputation for being brutally honest — once telling me and a colleague we were “lucky to have worked at Engine Yard” or we wouldn’t have gotten the jobs on our own merits. His humor was dark and his standards were high. Working with him, and the engineers he trusted, was a real priviledge.  

The rest of the team included legends like Derek Collison (creator of NATS), Peter Noordhuis (a contributor to Redis), Dale Olds (a pioneer of LDAP), and Jerry Chen (later an investor in Docker). I absorbed as much as I could.

Our initial strategy likely came from Mark Lucovsky and VMware’s CEO, Paul Maritz. The idea was to compete with Heroku by offering a hosted PaaS, but with the advantage of being open source. The thinking was that enterprises would gravitate toward a platform they could control, much like how MySQL disrupted Oracle or how Apache displaced IIS. At the same time, VMware saw Cloud Foundry as a way to counter Amazon’s dominance in public cloud. VMware’s core business — virtualized servers in private datacenters — was at risk as more companies moved to public cloud. Cloud Foundry was meant to give VMware a foothold in this new landscape, but their own cloud offerings, like vCloud, struggled to gain traction.

Our initial strategy likely came from Mark Lucovsky and VMware’s CEO, Paul Maritz. The idea was to compete with Heroku by offering a hosted PaaS while also enabling enterprises to deploy Cloud Foundry “in a box” using tools like BOSH. The vision was ambitious: provide the flexibility of a self-managed platform while simultaneously running a hosted service in VMware’s datacenters. In theory, we could serve both worlds—those who wanted a hands-off, fully managed solution and those who needed control over their infrastructure.

In practice, however, the emphasis was heavily skewed toward the hosted PaaS, which consumed nearly all of our resources. The imbalance made it difficult to give equal focus to the self-managed version, even though many on the marketing team — Killian Murphy and James Bayer especially — saw the “Google in a box” concept as a better fit for enterprises. They believed this approach aligned more closely with VMware’s strengths and would resonate with the enterprise audience we were trying to reach.

Their instincts would eventually be proven right, but not before significant upheaval. The shift in strategy caused tension across the team, leading to disagreements, uncertainty, and eventually, a wave of resignations. This struggle between hosted and self-managed models foreshadowed the eventual pivot to “Project Bento,” a turning point in Cloud Foundry’s journey and its ultimate transformation into a self-managed enterprise platform.

## The Big Spin-Out  

After a couple of years, it became clear that the emphasis on the hosted PaaS was misplaced. The costs of running it in VMware’s datacenters were immense, and while we didn’t abandon the hosted model entirely, its role began to shift. It became more of a testbed — a place to experiment — rather than a core product we actively sold. Meanwhile, the self-managed model, which allowed enterprises to deploy Cloud Foundry on their own infrastructure, started to gain traction.

This shift coincided with a broader realization within VMware and EMC. Cloud Foundry wasn’t just a product — it was part of a larger vision for enabling developers and modernizing enterprise software practices. Alongside other open-source projects like RabbitMQ and the Spring Java framework, it represented a developer-focused portfolio with the potential to make a much bigger impact if it could operate outside VMware’s core business. This led to the creation of Pivotal: a standalone company backed by EMC that combined these technologies with the agile expertise of Pivotal Labs, a consulting group EMC had previously acquired.

The spin-out wasn’t just a strategic move — it was a cultural transformation. Pivotal Labs, with its emphasis on extreme programming and agile methodologies, brought a dynamic, startup-like energy to the table. Their culture meshed with the open-source ethos of Cloud Foundry, Spring, and RabbitMQ, and created this rare blend of enterprise credibility with developer-first thinking. For many of us, it felt like an exciting new chapter, even though it introduced a period of upheaval.

When Pivotal officially launched, it set out with a bold mission: to help enterprises transform both their technology and their development practices for the digital age. The focus shifted firmly to self-managed solutions, helping companies deploy Cloud Foundry “in a box” while leveraging Pivotal Labs’ expertise to guide their digital transformation.

This redefined Cloud Foundry’s trajectory and laid the groundwork for Pivotal to become a leader in the emerging cloud-native space. A key figure was James Watters, who I believe coined the term "Cloud Native." Originally a business development guy on the original Cloud Foundry team at VMware, James bridged the technical and business worlds. His drive felt authentic — he wasn’t just hustling for himself; he was accelerating the company, the product, and the mission.

James was also a renaissance man. He could discuss the future of containers, predict the struggles of companies like Docker (he was right — they never figured out how to make money), and weave in references to classic literature or Greek mythology. He’s a brilliant guy and still leads the Cloud Foundry (now Tanzu) team today.

James also mastered the early days of Twitter, back when it was still new and very much a place for tech people. It hadn’t caught on with the mainstream yet — it was our space, and many of us had been there since the beginning (my account dates back to 2008). James gained tens of thousands of followers by authentically engaging with influential people, flipping conversations in his favor with just the right mix of humor and conviction. When I once asked him how he did it, he gave a simple answer: "I have one rule on Twitter. Have fun."

As exciting as the spin-out was, it wasn’t without its challenges. It came at a cost — resignations, reorgs, and the loss of some of the original Cloud Foundry team. It marked the beginning of a new era for everyone involved.

## Facing the Unstoppable Shift  

For a time, Pivotal thrived. Cloud Foundry became central to "digital transformation" strategies for enterprises. Companies like Ford invested heavily in Pivotal to adopt agile practices and become “the Google of their industry.” Combining Spring, Cloud Foundry, and Pivotal Labs’ methodologies gave enterprises a way to innovate faster and compete with startups that were disrupting traditional industries.

Of course, it wasn’t all smooth sailing. Internally, our engineering teams faced challenges delivering features quickly. Some of the Pivotal Labs engineers were incredible — on par with the top talent I worked with at VMware. But others were relatively new to programming. While everyone was undeniably smart and empathetic (two qualities Pivotal prioritized when hiring to ensure people could pair program effectively), the lack of experience made tackling complex systems problems difficult. Code refactoring became a constant topic of debate, and balancing flexibility with usability was an ongoing challenge.

Externally, the competition was heating up. Red Hat’s OpenShift began gaining traction, and its pivot to a Kubernetes-based architecture positioned it as a strong alternative to Cloud Foundry. 

Kubernetes itself was becoming the industry standard for container orchestration. It wasn’t as user-friendly as Cloud Foundry, but it had significant mindshare, and cloud providers started offering Kubernetes as a managed service. At Pivotal, we considered replacing Cloud Foundry’s scheduler, Diego, with Kubernetes but ultimately decided against it. The decision was both politically and technically complex, and our customers were demanding other features. In hindsight, this was a critical moment where we began to lose ground to the Kubernetes ecosystem.

Ironically, Diego itself was already a massive improvement over Cloud Foundry’s original scheduler, Cloud Controller, which had been written in Ruby at VMware. Diego was built in Go, a newer language we were excited about, and led by Onsi Fakhouri, our head of engineering. Onsi and others on the team even contributed to Go’s ecosystem, creating the widely used testing framework Ginkgo. This kind of contribution was common at Cloud Foundry — we had a culture of deep engagement with open-source communities. Many of the Pivotal engineers were active contributors to numerous other projects, and the team’s collective talent was undeniable.

Despite all of this, the Kubernetes ecosystem was accelerating quickly. Its open API and the growing support from cloud providers made it hard to ignore, and our decision to stick with Diego, while understandable at the time, left us increasingly isolated as the industry moved toward Kubernetes.

I left Pivotal in 2016, just before the company went public. It was a missed financial opportunity, but I was ready for something new. My father’s passing and a promotion to director — a role where I realized I preferred building things to managing people  accelerated my departure. Still, Pivotal’s story continued.

After going public, Pivotal faced scrutiny over its reliance on a small number of large customers. As Kubernetes gained dominance, Pivotal’s growth slowed. Eventually, the company was reacquired by VMware and folded into its Tanzu product line. Today, Cloud Foundry still has a loyal following, but Kubernetes has firmly established itself as the “operating system of the cloud.”  

Cloud Foundry continues to power thousands of critical applications today, standing as a testament to its impact. Its integration with Spring and the adoption of agile methodologies helped redefine how enterprises approached software development. However, the rise of Kubernetes served as a familiar reminder that great platforms must evolve — or risk being left behind.