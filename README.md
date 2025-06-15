# ai-web-my-college

import { useState } from "react";
import { MessageCircle, GraduationCap, Users, BookOpen, Calendar, Phone, Mail, MapPin, Award, Building2, Wrench } from "lucide-react";
import { Button } from "@/components/ui/button";
import { Card, CardContent, CardDescription, CardHeader, CardTitle } from "@/components/ui/card";
import ChatBot from "@/components/ChatBot";

const Index = () => {
  const [isChatOpen, setIsChatOpen] = useState(false);

  const quickActions = [
    {
      title: "Kemasukan & Syarat",
      description: "Syarat kemasukan, proses permohonan dan tarikh penting",
      icon: GraduationCap,
      color: "bg-blue-500"
    },
    {
      title: "Program DVM",
      description: "6 program Diploma Vokasional Malaysia yang ditawarkan",
      icon: Award,
      color: "bg-green-500"
    },
    {
      title: "Kemudahan Kampus",
      description: "Makmal terkini, asrama, kafeteria dan kemudahan sukan",
      icon: Building2,
      color: "bg-purple-500"
    },
    {
      title: "Kerjaya & Industri",
      description: "Job placement 95%, latihan industri dan rakan korporat",
      icon: Wrench,
      color: "bg-orange-500"
    }
  ];

  const contactInfo = [
    { icon: Phone, label: "Telefon", value: "03-4108 3200" },
    { icon: Mail, label: "E-mel", value: "kvsetapak@mohe.gov.my" },
    { icon: MapPin, label: "Alamat", value: "Jalan Lingkaran Tengah 2, Setapak, 53300 KL" }
  ];

  const programs = [
    "DVM Kejuruteraan Mekanikal",
    "DVM Kejuruteraan Elektrik", 
    "DVM Kejuruteraan Elektronik",
    "DVM Teknologi Maklumat",
    "DVM Hospitaliti",
    "DVM Perniagaan"
  ];

  return (
    <div className="min-h-screen bg-gradient-to-br from-blue-50 via-white to-green-50">
      {/* Header */}
      <header className="bg-white shadow-sm border-b">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4">
          <div className="flex items-center justify-between">
            <div className="flex items-center space-x-3">
              <div className="bg-blue-600 rounded-lg p-2">
                <GraduationCap className="h-8 w-8 text-white" />
              </div>
              <div>
                <h1 className="text-2xl font-bold text-gray-900">Kolej Vokasional Setapak</h1>
                <p className="text-sm text-gray-600">Kementerian Pendidikan Tinggi Malaysia</p>
              </div>
            </div>
            <Button
              onClick={() => setIsChatOpen(true)}
              className="bg-blue-600 hover:bg-blue-700 text-white px-6 py-2 rounded-full shadow-lg hover:shadow-xl transition-all duration-300"
            >
              <MessageCircle className="h-5 w-5 mr-2" />
              Tanya AI Assistant
            </Button>
          </div>
        </div>
      </header>

      {/* Hero Section */}
      <section className="py-20 px-4 sm:px-6 lg:px-8">
        <div className="max-w-4xl mx-auto text-center">
          <h2 className="text-4xl md:text-5xl font-bold text-gray-900 mb-6">
            Pendidikan Vokasional
            <span className="text-blue-600 block">Berkualiti Tinggi</span>
          </h2>
          <p className="text-xl text-gray-600 mb-8 max-w-2xl mx-auto">
            Kolej Vokasional Setapak menawarkan 6 program Diploma Vokasional Malaysia (DVM) dengan kadar penempatan kerja 95%. 
            Pengajian PERCUMA untuk warganegara Malaysia dengan kemudahan terkini dan kerjasama industri yang kukuh.
          </p>
          <div className="flex flex-col sm:flex-row gap-4 justify-center">
            <Button
              onClick={() => setIsChatOpen(true)}
              size="lg"
              className="bg-blue-600 hover:bg-blue-700 text-white px-8 py-4 rounded-full text-lg shadow-lg hover:shadow-xl transition-all duration-300"
            >
              <MessageCircle className="h-6 w-6 mr-2" />
              Tanya Sekarang
            </Button>
            <Button
              variant="outline"
              size="lg"
              className="border-2 border-blue-600 text-blue-600 hover:bg-blue-50 px-8 py-4 rounded-full text-lg transition-all duration-300"
            >
              Lawat Kampus
            </Button>
          </div>
        </div>
      </section>

      {/* Programs Highlight */}
      <section className="py-16 px-4 sm:px-6 lg:px-8 bg-white">
        <div className="max-w-6xl mx-auto">
          <h3 className="text-3xl font-bold text-center text-gray-900 mb-4">
            Program Diploma Vokasional Malaysia (DVM)
          </h3>
          <p className="text-gray-600 text-center mb-12 max-w-3xl mx-auto">
            6 semester • MQF Level 4 • Setaraf Diploma • Boleh sambung Ijazah • PERCUMA*
          </p>
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            {programs.map((program, index) => (
              <Card key={index} className="hover:shadow-lg transition-shadow duration-300 cursor-pointer group">
                <CardHeader className="text-center pb-4">
                  <div className="bg-gradient-to-r from-blue-500 to-green-500 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition-transform duration-300">
                    <Award className="h-8 w-8 text-white" />
                  </div>
                  <CardTitle className="text-lg">{program}</CardTitle>
                </CardHeader>
                <CardContent>
                  <CardDescription className="text-center">
                    Program 6 semester dengan latihan industri dan jaminan penempatan kerja
                  </CardDescription>
                </CardContent>
              </Card>
            ))}
          </div>
          <div className="text-center mt-8">
            <p className="text-sm text-gray-500">*Percuma untuk warganegara Malaysia, kos peralatan dan buku teks ditanggung pelajar</p>
          </div>
        </div>
      </section>

      {/* Quick Actions */}
      <section className="py-16 px-4 sm:px-6 lg:px-8 bg-gray-50">
        <div className="max-w-6xl mx-auto">
          <h3 className="text-3xl font-bold text-center text-gray-900 mb-12">
            Bagaimana Kami Boleh Membantu Anda?
          </h3>
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
            {quickActions.map((action, index) => (
              <Card key={index} className="hover:shadow-lg transition-shadow duration-300 cursor-pointer group">
                <CardHeader className="text-center pb-4">
                  <div className={`${action.color} w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition-transform duration-300`}>
                    <action.icon className="h-8 w-8 text-white" />
                  </div>
                  <CardTitle className="text-lg">{action.title}</CardTitle>
                </CardHeader>
                <CardContent>
                  <CardDescription className="text-center">
                    {action.description}
                  </CardDescription>
                </CardContent>
              </Card>
            ))}
          </div>
        </div>
      </section>

      {/* Key Stats */}
      <section className="py-16 px-4 sm:px-6 lg:px-8 bg-blue-600 text-white">
        <div className="max-w-4xl mx-auto">
          <h3 className="text-3xl font-bold text-center mb-12">Pencapaian Kami</h3>
          <div className="grid grid-cols-1 md:grid-cols-4 gap-8 text-center">
            <div>
              <div className="text-4xl font-bold mb-2">95%</div>
              <div className="text-blue-100">Kadar Penempatan Kerja</div>
            </div>
            <div>
              <div className="text-4xl font-bold mb-2">200+</div>
              <div className="text-blue-100">Rakan Industri</div>
            </div>
            <div>
              <div className="text-4xl font-bold mb-2">15</div>
              <div className="text-blue-100">Ekar Kampus</div>
            </div>
            <div>
              <div className="text-4xl font-bold mb-2">800</div>
              <div className="text-blue-100">Kapasiti Pelajar</div>
            </div>
          </div>
        </div>
      </section>

      {/* Contact Information */}
      <section className="py-16 px-4 sm:px-6 lg:px-8 bg-white">
        <div className="max-w-4xl mx-auto">
          <h3 className="text-3xl font-bold text-center text-gray-900 mb-12">
            Hubungi Kami
          </h3>
          <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
            {contactInfo.map((contact, index) => (
              <div key={index} className="text-center">
                <div className="bg-blue-600 w-12 h-12 rounded-full flex items-center justify-center mx-auto mb-4">
                  <contact.icon className="h-6 w-6 text-white" />
                </div>
                <h4 className="font-semibold text-gray-900 mb-2">{contact.label}</h4>
                <p className="text-gray-600">{contact.value}</p>
              </div>
            ))}
          </div>
          <div className="text-center mt-12">
            <p className="text-gray-600 mb-4">
              <strong>Waktu Pejabat:</strong> Isnin-Khamis 8 pagi-5 petang, Jumaat 8 pagi-4.15 petang
            </p>
            <p className="text-gray-600">
              <strong>Lokasi:</strong> 10 minit dari LRT Wangsa Maju, akses mudah dari DUKE Highway
            </p>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-gray-900 text-white py-12 px-4 sm:px-6 lg:px-8">
        <div className="max-w-6xl mx-auto text-center">
          <div className="flex items-center justify-center space-x-3 mb-6">
            <div className="bg-blue-600 rounded-lg p-2">
              <GraduationCap className="h-6 w-6 text-white" />
            </div>
            <h4 className="text-xl font-bold">Kolej Vokasional Setapak</h4>
          </div>
          <p className="text-gray-400 mb-6">
            Melahirkan tenaga mahir bertauliah untuk memenuhi keperluan industri Malaysia
          </p>
          <p className="text-gray-500 text-sm">
            © 2024 Kolej Vokasional Setapak, Kementerian Pendidikan Tinggi Malaysia. Hak cipta terpelihara.
          </p>
        </div>
      </footer>

      {/* Floating Chat Button */}
      {!isChatOpen && (
        <Button
          onClick={() => setIsChatOpen(true)}
          className="fixed bottom-6 right-6 bg-blue-600 hover:bg-blue-700 text-white w-14 h-14 rounded-full shadow-lg hover:shadow-xl transition-all duration-300 z-40"
        >
          <MessageCircle className="h-6 w-6" />
        </Button>
      )}

      {/* ChatBot Component */}
      <ChatBot isOpen={isChatOpen} onClose={() => setIsChatOpen(false)} />
    </div>
  );
};

export default Index;
