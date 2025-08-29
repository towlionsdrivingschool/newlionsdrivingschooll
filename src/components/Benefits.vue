<script setup lang="ts">
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card";

import {
  Sparkle,
  Tag,
  Paintbrush,
  Blocks,
  LineChart,
  Wallet,
} from "lucide-vue-next";

interface BenefitsProps {
  icon: string;
  title: string;
  description: string;
}

const benefitList: BenefitsProps[] = [
  {
    icon: "blocks",
    title: "RTO Certified",
     description:
      "",
  },
  {
    icon: "lineChart",
    title: "Pick-Up & Drop Services",
     description:
     "",
  },
  {
    icon: "wallet",
    title: "Affordable Fee",
     description:
      "",
  },
  {
    icon: "sparkle",
    title: "Road Test Preparation",
     description:
      "",
  },
];

const iconMap: Record<
  string,
  | typeof Sparkle
  | typeof Tag
  | typeof Paintbrush
  | typeof Blocks
  | typeof LineChart
  | typeof Wallet
> = {
  sparkle: Sparkle,
  tag: Tag,
  paintbrush: Paintbrush,
  blocks: Blocks,
  lineChart: LineChart,
  wallet: Wallet,
};
</script>

<template>
  <section id="benefits" class="container py-24 sm:py-32">
    <div class="grid lg:grid-cols-2 place-items-center lg:gap-24">
      <div>


        <h2 class="text-3xl md:text-4xl font-bold mb-4">
          About us
        </h2>
        <p class="text-xl text-muted-foreground mb-8">
          Welcome to New Lions Driving School, where safety meets excellence in driver education. Our mission is to
          equip students with the knowledge, skills, and confidence they need to become responsible and proficient
          drivers.
        </p>
      </div>

      <div class="grid lg:grid-cols-2 gap-4 w-full">
        <Card v-for="({ icon, title, description }, index) in benefitList" :key="title"
          class="bg-muted/50 dark:bg-card hover:bg-background dark:hover:bg-background transition-all delay-75 group/number">
          <CardHeader>
            <div class="flex justify-between">
              <component class="size-8 mb-6 text-primary" :is="iconMap[icon]" />

              <span
                class="text-5xl text-muted-foreground/15 font-medium transition-all delay-75 group-hover/number:text-muted-foreground/30">0{{
                  index + 1 }}</span>
            </div>

            <CardTitle>{{ title }}</CardTitle>
          </CardHeader>

          <CardContent class="text-muted-foreground">
            {{ description }}
          </CardContent>
        </Card>
      </div>
    </div>
  </section>
</template>
