import React from 'react';
import { PieChart, Pie, Cell, BarChart, Bar, XAxis, YAxis, CartesianGrid, Tooltip, Legend, ResponsiveContainer } from 'recharts';

const Dashboard = () => {
  // Données pour le graphique de répartition par modalité de formation
  const modaliteData = [
    { name: 'Présentiel', value: 30 },
    { name: 'Dist. Synchrone (Visio)', value: 30 },
    { name: 'Hybride/Multimodal', value: 20 },
    { name: 'Dist. Asynchrone (M@gistère)', value: 15 },
    { name: 'Webinaires', value: 5 }
  ];

  // Données pour le graphique de répartition par thématique
  const thematiqueData = [
    { name: 'Pédagogie & Numérique', value: 45 },
    { name: 'Compétences Transversales', value: 30 },
    { name: 'ENT', value: 15 },
    { name: 'Inclusion & Accessibilité', value: 5 },
    { name: 'Formation de Formateurs', value: 5 }
  ];

  // Données pour les statistiques clés
  const statsData = [
    { name: 'Modules Codifiés', value: 70 },
    { name: 'Outils/Plateformes', value: 20 },
    { name: 'Publics Ciblés', value: 4 },
    { name: 'Modalités de Formation', value: 5 }
  ];

  // Couleurs pour les graphiques
  const COLORS = ['#0088FE', '#00C49F', '#FFBB28', '#FF8042', '#8884d8'];

  return (
    <div className="p-6 bg-gray-100 min-h-screen">
      <div className="max-w-6xl mx-auto">
        {/* En-tête */}
        <div className="bg-blue-600 text-white p-4 rounded-t-lg">
          <h1 className="text-2xl font-bold">Tableau de Bord PAF Numérique 2024-2025</h1>
          <p className="mt-2">Objectif Principal: Développer les compétences numériques des personnels via une offre de formation structurée</p>
        </div>
        
        {/* Statistiques principales */}
        <div className="bg-white p-4 shadow-md mb-6">
          <h2 className="text-xl font-semibold mb-4 text-gray-700">Statistiques Clés</h2>
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
            {statsData.map((item, index) => (
              <div key={index} className="bg-gray-50 p-4 rounded-lg text-center">
                <p className="text-3xl font-bold text-blue-600">{item.value}</p>
                <p className="text-sm text-gray-600">{item.name}</p>
              </div>
            ))}
          </div>
        </div>
        
        {/* Graphiques */}
        <div className="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
          {/* Graphique Modalités */}
          <div className="bg-white p-4 shadow-md rounded-lg">
            <h2 className="text-lg font-semibold mb-4 text-gray-700">Répartition par Modalité de Formation</h2>
            <div className="h-64">
              <ResponsiveContainer width="100%" height="100%">
                <PieChart>
                  <Pie
                    data={modaliteData}
                    cx="50%"
                    cy="50%"
                    labelLine={true}
                    outerRadius={80}
                    fill="#8884d8"
                    dataKey="value"
                    label={({name, percent}) => `${name} ${(percent * 100).toFixed(0)}%`}
                  >
                    {modaliteData.map((entry, index) => (
                      <Cell key={`cell-${index}`} fill={COLORS[index % COLORS.length]} />
                    ))}
                  </Pie>
                  <Tooltip formatter={(value) => `${value}%`} />
                </PieChart>
              </ResponsiveContainer>
            </div>
          </div>
          
          {/* Graphique Thématiques */}
          <div className="bg-white p-4 shadow-md rounded-lg">
            <h2 className="text-lg font-semibold mb-4 text-gray-700">Poids des Grandes Thématiques</h2>
            <div className="h-64">
              <ResponsiveContainer width="100%" height="100%">
                <PieChart>
                  <Pie
                    data={thematiqueData}
                    cx="50%"
                    cy="50%"
                    labelLine={true}
                    outerRadius={80}
                    fill="#8884d8"
                    dataKey="value"
                    label={({name, percent}) => `${name} ${(percent * 100).toFixed(0)}%`}
                  >
                    {thematiqueData.map((entry, index) => (
                      <Cell key={`cell-${index}`} fill={COLORS[index % COLORS.length]} />
                    ))}
                  </Pie>
                  <Tooltip formatter={(value) => `${value}%`} />
                </PieChart>
              </ResponsiveContainer>
            </div>
          </div>
        </div>

        {/* Autres indicateurs clés */}
        <div className="bg-white p-4 shadow-md mb-6 rounded-lg">
          <h2 className="text-xl font-semibold mb-4 text-gray-700">Autres Indicateurs Clés</h2>
          <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
            <div className="border-l-4 border-blue-500 pl-3">
              <h3 className="font-semibold text-lg">Focus Institutionnel</h3>
              <p className="text-gray-600">Forte présence de l'ENT, Pix, Apps.education.fr, M@gistère</p>
            </div>
            <div className="border-l-4 border-green-500 pl-3">
              <h3 className="font-semibold text-lg">Innovation Pédagogique</h3>
              <p className="text-gray-600">Nombreux modules dédiés aux nouvelles pratiques (IA, RV/RA, Escape Games)</p>
            </div>
            <div className="border-l-4 border-yellow-500 pl-3">
              <h3 className="font-semibold text-lg">Demandes Terrain (FEE)</h3>
              <p className="text-gray-600">8+ thématiques distinctes demandées par les établissements (IA étant la plus citée)</p>
            </div>
            <div className="border-l-4 border-purple-500 pl-3">
              <h3 className="font-semibold text-lg">Organisation Logistique</h3>
              <p className="text-gray-600">Formateurs en binôme, calendrier précis sur 2024-2025, multiples lieux identifiés</p>
            </div>
          </div>
        </div>
        
        {/* Conclusion */}
        <div className="bg-gray-50 p-4 rounded-lg border-t-4 border-blue-600">
          <h2 className="text-lg font-semibold mb-2">Conclusion Synthétique</h2>
          <p className="text-gray-600">
            Le PAF Numérique 24-25 apparaît comme une offre dense, diversifiée et bien structurée, avec un fort accent mis sur 
            l'innovation pédagogique et la maîtrise des compétences numériques transversales. La variété des modalités et la prise 
            en compte des besoins locaux (FEE) indiquent une volonté d'adaptation, avec une logistique bien planifiée pour le déploiement.
          </p>
        </div>
      </div>
    </div>
  );
};

export default Dashboard;
