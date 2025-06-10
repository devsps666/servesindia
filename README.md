import React from "react";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { ArrowRight, PhoneCall } from "lucide-react";
import Image from "next/image";

export default function HomePage() {
  return (
    <div className="min-h-screen bg-white text-gray-900 px-6 py-10">
      <header className="text-center mb-10">
        <div className="flex justify-center mb-4">
          <Image
            src="/logo.png"
            alt="ServIndia Logo"
            width={80}
            height={80}
            className="rounded-full"
          />
        </div>
        <h1 className="text-4xl font-bold">ServIndia</h1>
        <p className="text-lg mt-2 text-gray-600 italic">
          "Clean India, Dignified Workers, Trusted Services"
        </p>
      </header>

      <section className="grid gap-6 md:grid-cols-2 lg:grid-cols-3">
        {[
          {
            title: "Street & Drain Cleaning",
            description:
              "Professional cleaning of gullies, drains, open areas, and community bins.",
          },
          {
            title: "Home & Office Cleaning",
            description:
              "From dusting to deep cleaning – hygienic and affordable services for your premises.",
          },
          {
            title: "Vehicle Washing",
            description:
              "Doorstep bike and car cleaning using eco-safe techniques.",
          },
          {
            title: "Restaurant & Commercial",
            description:
              "Kitchen, washroom, and floor cleaning for small businesses and restaurants.",
          },
          {
            title: "Electric & Repair",
            description:
              "Basic electric fittings, fan repairs, and home maintenance support.",
          },
          {
            title: "Custom Cleaning Plans",
            description:
              "Monthly packages for residential societies, businesses, and clinics.",
          },
        ].map((service, index) => (
          <Card key={index} className="rounded-2xl shadow-md">
            <CardContent className="p-6">
              <h3 className="text-xl font-semibold mb-2">{service.title}</h3>
              <p className="text-sm text-gray-700 mb-4">{service.description}</p>
              <Button className="mt-auto" variant="outline">
                Book Now <ArrowRight className="ml-2 h-4 w-4" />
              </Button>
            </CardContent>
          </Card>
        ))}
      </section>

      <section className="mt-16 text-center">
        <h2 className="text-2xl font-bold mb-4">Join as a Worker</h2>
        <p className="text-gray-700 max-w-xl mx-auto mb-4">
          We believe in the dignity of work. If you want to become a part of ServIndia as a trained cleaning or maintenance professional, contact us to get trained and placed in your area.
        </p>
        <Button className="text-white bg-green-600 hover:bg-green-700">
          <PhoneCall className="mr-2 h-4 w-4" /> Call Us: +91-8368681063
        </Button>
      </section>

      <footer className="mt-16 text-center text-gray-600 text-sm">
        &copy; {new Date().getFullYear()} ServIndia. All rights reserved.
      </footer>
    </div>
  );
}
