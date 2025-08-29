<script setup lang="ts">
import { Button } from "@/components/ui/button";
import {
  Card,
  CardContent,
  CardDescription,
  CardFooter,
  CardHeader,
  CardTitle,
} from "@/components/ui/card";

import { Check } from "lucide-vue-next";

enum PopularPlan {
  NO = 0,
  YES = 1,
}

interface PlanProps {
  title: string;
  popular: PopularPlan;
  price: number;
  description: string;
  buttonText: string;
  benefitList: string[];
}

const plans: PlanProps[] = [
  {
    title: "Basic Package",
    popular: 0,
    price: 11000,
    description:
      "Two Wheeler and Four Wheeler ",
    buttonText: "Start Free Trial",
    benefitList: [
      " Total :25 Days sessions",

      "25 driving sessions (manual car)",
      "10 H Practice ",
      "Road Test Practice",
    ],
  },
  {
    title: " Four Wheeler Package ",
    popular: 1,
    price: 10000,
    description:
      "only Four Wheeler .",
    buttonText: "Get starterd",
    benefitList: [
      "25 driving sessions ",
      "10 H Practice",
      "Road Test Practice",
      // "Upto 6 pages",
      // "Priority support",
      // "AI assistance",
    ],
  },
  {
    title: "Two Wheeler Package",
    popular: 0,
    price: 3500,
    description:
      " Two Wheeler 8 and Two Wheeler Road",
    buttonText: "Contact US",
    benefitList: [
      "150/per Day ",
      "8 Practice ",
      " Two Wheeler Road Test Practice",
      // "Upto 10 pages",
      // "Phone & email support",
      // "AI assistance",
    ],
  },
];
</script>

<template>
  <section class="container py-24 sm:py-32">
    <h2 class="text-lg text-primary text-center mb-2 tracking-wider">
      Pricing
    </h2>

    <h2 class="text-3xl md:text-4xl text-center font-bold mb-4">
      <!-- Get unlimitted access -->
    </h2>

    <h3 class="md:w-1/2 mx-auto text-xl text-center text-muted-foreground pb-14">
      <!-- Lorem ipsum dolor sit amet consectetur adipisicing reiciendis. -->
    </h3>

    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8 lg:gap-4">
      <Card v-for="{
        title,
        popular,
        price,
        description,
        buttonText,
        benefitList,
      } in plans" :key="title" :class="{
        'drop-shadow-xl shadow-black/10 dark:shadow-white/10 border-[1.5px] border-primary lg:scale-[1.1]':
          popular === PopularPlan?.YES,
      }">
        <CardHeader>
          <CardTitle class="pb-2">
            {{ title }}
          </CardTitle>

          <CardDescription class="pb-4">{{ description }}</CardDescription>

          <div>
            <span class="text-3xl font-bold">₹{{ price }}</span>
            <span class="text-muted-foreground"> </span>
          </div>
        </CardHeader>

        <CardContent class="flex">
          <div class="space-y-4">
            <span v-for="benefit in benefitList" :key="benefit" class="flex">
              <Check class="text-primary mr-2" />
              <h3>{{ benefit }}</h3>
            </span>
          </div>
        </CardContent>

        <CardFooter>
          <Button :variant="popular === PopularPlan?.NO ? 'secondary' : 'default'" class="w-full">
            {{ buttonText }}
          </Button>
        </CardFooter>
      </Card>
    </div>
  </section>
</template>
