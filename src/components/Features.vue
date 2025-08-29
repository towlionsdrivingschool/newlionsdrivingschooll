<script setup lang="ts">
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card";

import {
  Paintbrush,
  MessageCircle,
  TabletSmartphone,
  BadgeCheck,
  Goal,
  PictureInPicture,
  MousePointerClick,
  Newspaper,
  CalendarCheck2,
  HandCoins,
  Check,
  UserRound,
 
  MapPinned ,
} from "lucide-vue-next";


interface FeaturesProps {
  icon: string;
  title: string;
  description: string;
}

const featureList: FeaturesProps[] = [
  {
    icon: "check",
    title: "Safety First",
    description:
      "We prioritize safety in all our lessons, teaching you how to handle various driving situations responsibly.",
  },
  {
    icon: "handCoins",
    title: "Affordable Rates",
    description:
      "Quality driving instruction should be accessible to everyone, which is why we offer competitive pricing and package deals.",
  },
  {
    icon: "calendarCheck2",
    title: "Flexible Scheduling",
    description:
      "We offer a variety of lesson times to fit your busy schedule, including evenings and weekends.",
  },
  {
    icon: "userRound",
    title: "Professional Instructors",
    description:
      "we take pride in our team of professional instructors who are dedicated to providing the highest quality driver education. Our instructors are.",
  },
  {
    icon: "mapPinned",
    title: "Pick And Drop At Your Doorstep",
    description:
      "Our instructors pick you up and drop you off, fitting lessons into your busy schedule for maximum convenience.",
  },
  {
    icon: "newspaper",
    title: "8 and H Test Practice",
    description:
      "Prepare for the essential 8 and H driving tests with our specialized training sessions. Our practice sessions will help you master the skills and techniques needed to pass confidently and successfully.",
  },
];

const iconMap: Record<
  string,
  | typeof TabletSmartphone
  | typeof BadgeCheck
  | typeof Goal
  | typeof PictureInPicture
  | typeof Paintbrush
  | typeof MousePointerClick
  | typeof MessageCircle
  | typeof Newspaper
  | typeof Check
  | typeof CalendarCheck2
  | typeof UserRound
> = {
  tabletSmartphone: TabletSmartphone,
  badgeCheck: BadgeCheck,
  goal: Goal,
  pictureInPicture: PictureInPicture,
  paintbrush: Paintbrush,
  mousePointerClick: MousePointerClick,
  messageCircle: MessageCircle,
  newspaper: Newspaper,
  check: Check,
  handCoins: HandCoins,
  calendarCheck2: CalendarCheck2,
  userRound: UserRound,
  mapPinned  : MapPinned  ,
};
</script>

<template>
  <section id="features" class="container py-24 sm:py-32">
    <h2 class="text-lg text-primary text-center mb-2 tracking-wider">
      Features
    </h2>

    <h2 class="text-3xl md:text-4xl text-center font-bold mb-4">
      Why Choose Us
    </h2>

    <!-- <h3 class="md:w-1/2 mx-auto text-xl text-center text-muted-foreground mb-8">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Voluptatem
      fugiat, odit similique quasi sint reiciendis quidem iure veritatis optio
      facere tenetur.
    </h3> -->

    <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-4">
      <div v-for="{ icon, title, description } in featureList" :key="title">
        <Card class="h-full bg-background border-0 shadow-none">
          <CardHeader class="flex justify-center items-center">
            <div class="bg-primary/20 p-2 rounded-full ring-8 ring-primary/10 mb-4">
              <component :is="iconMap[icon]" class="size-6 text-primary" />
            </div>

            <CardTitle>
              {{ title }}
            </CardTitle>
          </CardHeader>

          <CardContent class="text-muted-foreground text-center">
            {{ description }}
          </CardContent>
        </Card>
      </div>
    </div>
  </section>
</template>

<style lang="less" scoped></style>
