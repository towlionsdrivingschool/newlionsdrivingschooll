<script setup lang="ts">
import {
  Accordion,
  AccordionContent,
  AccordionItem,
  AccordionTrigger,
} from "@/components/ui/accordion";

interface FAQProps {
  question: string;
  answer: string;
  value: string;
}

const FAQList: FAQProps[] = [
  {
    question: "What is the minimum age to join a driving school",
    answer: "You must be at least 18 years old to enroll for a four-wheeler driving course.",
    value: "item-1",
  },
  {
    question: "What is the total cost of the course?",
    answer:
      "Fees vary by package, but typically range from ₹10,000 to ₹12,000. Contact us for current rates.",
    value: "item-2",
  },
  {
    question:
      "Do you offer classes on weekends or holidays?",
    answer:
      "Yes, weekend and holiday classes are available on request.",
    value: "item-3",
  },
  {
    question: "Do you offer pickup and drop services?",
    answer: "Yes, we offer pickup and drop within city limits ",
    value: "item-4",
  },
  {
    question:
      "Do you provide the car for the driving test?",
    answer: "Yes, we provide our training vehicle for the driving test.",
    value: "item-5",
  },
];
</script>

<template>
  <section id="faq" class="container md:w-[700px] py-24 sm:py-32">
    <div class="text-center mb-8">
      <h2 class="text-lg text-primary text-center mb-2 tracking-wider">FAQS</h2>

      <h2 class="text-3xl md:text-4xl text-center font-bold">
        Common Questions
      </h2>
    </div>

    <Accordion type="single" collapsible class="AccordionRoot">
      <AccordionItem v-for="{ question, answer, value } in FAQList" :key="value" :value="value">
        <AccordionTrigger class="text-left"> {{ question }} </AccordionTrigger>

        <AccordionContent>{{ answer }}</AccordionContent>
      </AccordionItem>
    </Accordion>

    <!-- <h3 class="font-medium mt-4">
      Still have questions?
      <a
        href="#"
        class="text-muted-foreground"
      >
        <a
          href="#"
          class="underline"
          >Contact us</a
        >
      </a>
    </h3> -->
  </section>
</template>
