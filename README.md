# Learning Methods in Humans, Animals, and Computers
This is an overview of different learning mechanisms used by humans and animals along with machine learning that try to replicate them.
Humans regularly use a combination of these methods to learn new things and most humans are capable of using all of them. From what we know, many animals can also use several of these techniques, while many others mostly rely on evolution.

Many machine learning (ML) methods have been developed to mimic these processes. For a long time, ML often only used one of these techniques, but recently - especially since the popularity of large language models (LLMs) - there has been a trend towards combining multiple techniques to achieve better results. For example, many current LLMs are first trained to imitate human writing using supervised learning, before being fine-tuned using reinforcement learning. Once trained, system prompts instruct the models to act in a certain way, demonstrating basic in-context learning. A slightly better example of in-context learning is few-shot prompting, where the model is given a few examples of the desired output format before having to produce its own output. This has repeatedly been shown to improve the model's performance on tasks.

| Learning method       | Animals | Humans | Computer (Machine Learning) |
|-----------------------|---------|--------|-----------------------------|
| **Evolution**             | genetic evolution                             | genetic evolution | genetic algorithms (e.g. NEAT) |
| **Trial & Error**         | Conditioning                                  | Conditioning      | Reinforcement learning |
| **Imitation**             | Orcas teaching hunting methods & language     | Learning language | Supervised learning, </br> Imitation learning |
| **Abstract Instructions** | Bee dance to describe location of food        | Most of school / higher education,  baking recipes | In-context learning in LLMs |
| **Mental Simulation**     | Birds cracking nuts using cars, </br> tool use | Dreams, </br> pondering other's reactions | World models (e.g. DreamerV3) |

## 1. Evolution
Evolution is different from the other learning methods in that it is not a learning method of an individual, but of a species, requiring the existence of multiple individuals. Each individual is mostly static and does not learn during its lifetime. Instead, the learning happens on a species level, evolving its individuals over time by creating modified copies. By selecting good individuals, the species can, over time, improve on a given task.

There are multiple ways to implement this modification of individuals observed in nature, including:
- random mutation (e.g. asexual reproduction)
- crossover between multiple individuals (e.g. sexual reproduction)
- selection of the best individuals (e.g. natural selection by competition, artificial selection by humans)

Nature has proven that evolution is a very capable learning method, but, compared to the others, is usually very slow. Computational recreations of this process tend to suffer from frequently getting stuck in local optima.
- Complex problems often require a very large number of individuals is to achieve good results. If there are too few individuals, special care needs to be taken to ensure performance does not degrade too quickly when a new generation performs worse than the previous ones.
- Lifetime of individuals needs to be balanced: Too long lifetime leads to slower learning if worse performing individuals keep producing offspring, taking resources away from better performing individuals (too much exploration). Too short lifetimes tends to overcommit to small gains, leaving not enough diversity in the population to explore new solutions (too much exploitation). This problem is known as the exploration-exploitation trade-off.

## 2. Trial & Error
Learning by exploring various actions and receiving feedback on their outcomes is a very common learning method observed in both humans and many other animals. Feedback can be positive or negative.

Trial & Error learning can suffer in scenarios with very sparse feedback.
For example, a mouse exploring a very large maze to find a single piece of food may run out of energy before it ever finds the food, thus (in extreme cases) being unable to learn anything useful.

Additionally, there is the reward allocation problem: Particularly when feedback is delayed or only rewards specific action sequences, it can be difficult to assess which action(s) led to the rewarded outcome.

## 3. Imitation
Imitation can be a very fast way to transfer skills between individuals. It is often used by humans or animals to transfer complex skills such as language or hunting techniques that benefit from coordination between individuals or to pass on skills before the end of the teacher's lifetime. To use this method effectively, the learner needs the ability to judge their own success, which can be difficult and prone to biases and other errors.

However, pure imitation struggles to produce new skills or to adapt existing skills to new requirements. Those require modification of the teacher's skills.
Imitation is also more difficult if the teacher's actions are not fully observable. For example: Teaching thought techniques without an effective communication tool like language is very difficult as the thoughts cannot be directly observed.
This method can only work if an agent has the ability to sense/ observe its environment sufficiently well. Lack of sensory capabilities makes it difficult to attribute teacher's or even learners actions to outcomes. This leads to poor feedback on the performance of the learner.

## 4. Abstract Instructions
While imitation aims to copy a teacher's actions by observing them, abstract instructions rely on active cooperation between teacher and student, thus requiring a suitable method of communication.
If those conditions are met, learning from instructions can be a highly effective and, depending on the communication method, efficient way to acquire new skills. For example, instructions can be given to dozens of students at the same time or documented for later use, allowing for a long delay between teaching and learning.

Disadvantages of this method are similar to imitation learning:
- It relies on the existence and capability of a teacher.
- Therefore, this method is not suitable for acquiring new skills or adapting existing skills to completely new requirements.
- While direct observation of the teacher's actions is not required and even unobservable actions can be communicated (improving on imitation learning), this method instead relies on the existence of sufficient communication abilities.
- If the teacher can directly observe the learner, they can provide specific feedback on the learner's performance, which can greatly improve the learning efficiency compared to imitation learning by ensuring high-quality feedback.

## 5. Mental Simulation
Mental simulation is a learning method that relies on the ability to mentally simulate actions and their outcomes. This can be used to plan actions, predict outcomes, or even learn new skills without direct experience. This is particularly useful in scenarios where direct exploration might be too costly or dangerous to the learning individual.

This method requires that the learner has access to an accurate model of the environment to predict the outcomes of actions. If the model is not accurate enough, transferring learnings from that model to the real world can be difficult or even impossible.