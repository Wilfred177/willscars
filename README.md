import { Button } from "@/components/ui/button"
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card"
import Link from "next/link"
import { ArrowRight, Camera, CheckCircle, Clock, Users } from "lucide-react"

export default function VendrePage() {
  return (
    <div className="container py-12">
      <div className="max-w-4xl mx-auto">
        <h1 className="text-3xl font-bold mb-2">Vendez votre véhicule</h1>
        <p className="text-muted-foreground mb-8">
          Publiez votre annonce en quelques minutes et trouvez rapidement un acheteur
        </p>

        <div className="grid grid-cols-1 md:grid-cols-3 gap-6 mb-12">
          <Card>
            <CardHeader className="text-center">
              <div className="mx-auto mb-4 h-12 w-12 rounded-full bg-rollsroyce/10 flex items-center justify-center">
                <Camera className="h-6 w-6 text-rollsroyce" />
              </div>
              <CardTitle>Créez votre annonce</CardTitle>
            </CardHeader>
            <CardContent className="text-center">
              <p className="text-muted-foreground">Ajoutez des photos et une description détaillée de votre véhicule</p>
            </CardContent>
          </Card>

          <Card>
            <CardHeader className="text-center">
              <div className="mx-auto mb-4 h-12 w-12 rounded-full bg-rollsroyce/10 flex items-center justify-center">
                <Users className="h-6 w-6 text-rollsroyce" />
              </div>
              <CardTitle>Recevez des offres</CardTitle>
            </CardHeader>
            <CardContent className="text-center">
              <p className="text-muted-foreground">Des acheteurs qualifiés vous contactent directement</p>
            </CardContent>
          </Card>

          <Card>
            <CardHeader className="text-center">
              <div className="mx-auto mb-4 h-12 w-12 rounded-full bg-rollsroyce/10 flex items-center justify-center">
                <CheckCircle className="h-6 w-6 text-rollsroyce" />
              </div>
              <CardTitle>Finalisez la vente</CardTitle>
            </CardHeader>
            <CardContent className="text-center">
              <p className="text-muted-foreground">Nous vous accompagnons dans les démarches administratives</p>
            </CardContent>
          </Card>
        </div>

        <Card className="bg-rollsroyce text-white mb-12">
          <CardContent className="p-8">
            <div className="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
              <div>
                <h2 className="text-2xl font-bold mb-4">Pourquoi vendre avec Will's Cars ?</h2>
                <ul className="space-y-3">
                  <li className="flex items-start gap-2">
                    <CheckCircle className="h-5 w-5 mt-0.5 flex-shrink-0" />
                    <span>Visibilité maximale auprès d'acheteurs de véhicules de luxe</span>
                  </li>
                  <li className="flex items-start gap-2">
                    <CheckCircle className="h-5 w-5 mt-0.5 flex-shrink-0" />
                    <span>Estimation gratuite de la valeur de votre véhicule</span>
                  </li>
                  <li className="flex items-start gap-2">
                    <CheckCircle className="h-5 w-5 mt-0.5 flex-shrink-0" />
                    <span>Accompagnement personnalisé tout au long du processus</span>
                  </li>
                  <li className="flex items-start gap-2">
                    <CheckCircle className="h-5 w-5 mt-0.5 flex-shrink-0" />
                    <span>Sécurisation des transactions et des paiements</span>
                  </li>
                </ul>
              </div>
              <div className="text-center">
                <div className="mb-4">
                  <Clock className="h-16 w-16 mx-auto" />
                </div>
                <h3 className="text-xl font-bold mb-2">Vente rapide garantie</h3>
                <p className="mb-4">Vendez votre véhicule en moins de 30 jours ou nous réduisons nos frais</p>
                <Button asChild className="bg-white text-rollsroyce hover:bg-white/90">
                  <Link href="/ajouter-vehicule">
                    Démarrer maintenant <ArrowRight className="ml-2 h-4 w-4" />
                  </Link>
                </Button>
              </div>
            </div>
          </CardContent>
        </Card>

        <div className="text-center">
          <Button asChild size="lg" className="bg-rollsroyce hover:bg-rollsroyce-800">
            <Link href="/ajouter-vehicule">Ajouter mon véhicule</Link>
          </Button>
        </div>
      </div>
    </div>
  )
}
