# theodore-mma-site
MMA nettside for Theodore Magnus Thalund-Fossen
import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Badge } from "@/components/ui/badge";

const stats = [
  { label: "Navn", value: "Theodore Magnus Thalund-Fossen" },
  { label: "Fødselsdato", value: "4. juni 2008" },
  { label: "Høyde", value: "185 cm" },
  { label: "Vekt", value: "80 kg" },
  { label: "Stilarter", value: "Muay Thai, Boksing, Bryting" },
  { label: "Kjennetegn", value: "Eksplosiv knockout-kraft" },
];

const MMAStatsPage = () => {
  return (
    <div className="min-h-screen bg-gray-950 text-white p-8">
      <div className="max-w-3xl mx-auto">
        <h1 className="text-4xl font-bold mb-6 text-center text-red-600">
          MMA-Profil: Theodore Magnus Thalund-Fossen
        </h1>

        <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
          {stats.map((stat) => (
            <Card key={stat.label} className="bg-gray-900 border border-red-700">
              <CardContent className="p-4">
                <h2 className="text-xl font-semibold text-red-500 mb-2">
                  {stat.label}
                </h2>
                <p className="text-lg text-white">{stat.value}</p>
              </CardContent>
            </Card>
          ))}
        </div>

        <div className="mt-10 text-center">
          <Badge className="bg-red-700 text-white text-lg py-2 px-4 rounded-xl shadow-lg">
            Fremtidig MMA-stjerne i Europa
          </Badge>
        </div>
      </div>
    </div>
  );
};

export default MMAStatsPage;
