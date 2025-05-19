<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Devis Travaux de Peinture</title>
    <!-- Firebase App (the core Firebase SDK) -->
    <script src="https://www.gstatic.com/firebasejs/8.10.1/firebase-app.js"></script>
    <!-- Firebase Analytics -->
    <script src="https://www.gstatic.com/firebasejs/8.10.1/firebase-analytics.js"></script>
    <!-- Firebase Database -->
    <script src="https://www.gstatic.com/firebasejs/8.10.1/firebase-database.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 20px;
            background-color: #f5f5f5;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        h1, h2, h3, h4 {
            color: #2c3e50;
        }
        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 4px;
            cursor: pointer;
            margin: 5px 0;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #2980b9;
        }
        .piece {
            background-color: #f9f9f9;
            padding: 15px;
            margin-bottom: 20px;
            border-radius: 5px;
            border-left: 4px solid #3498db;
        }
        .surface {
            background-color: #f2f2f2;
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
            border-left: 3px solid #e74c3c;
        }
        label {
            display: block;
            margin: 10px 0 5px;
            font-weight: bold;
        }
        select, input {
            width: 100%;
            padding: 8px;
            margin-bottom: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            box-sizing: border-box;
        }
        .color-preview {
            display: inline-block;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            margin-left: 10px;
            vertical-align: middle;
            border: 1px solid #ddd;
        }
        .devis-result {
            margin-top: 30px;
            padding: 20px;
            background-color: #ecf0f1;
            border-radius: 5px;
        }
        .devis-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        .devis-table th, .devis-table td {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: left;
        }
        .devis-table th {
            background-color: #3498db;
            color: white;
        }
        .devis-table tr:nth-child(even) {
            background-color: #f2f2f2;
        }
        .photo-upload {
            margin: 10px 0;
        }
        .options {
            background-color: #e8f4fc;
            padding: 15px;
            margin: 15px 0;
            border-radius: 5px;
        }
        .remove-btn {
            background-color: #e74c3c;
        }
        .remove-btn:hover {
            background-color: #c0392b;
        }
        @media print {
            button {
                display: none;
            }
            .container {
                box-shadow: none;
            }
        }
        .progress-bar {
            background-color: #ecf0f1;
            height: 20px;
            width: 100%;
            border-radius: 10px;
            margin-bottom: 20px;
        }
        .progress {
            background-color: #3498db;
            height: 100%;
            border-radius: 10px;
            width: 0%;
            transition: width 0.5s;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Devis Travaux de Peinture</h1>
        
        <div class="progress-bar">
            <div id="progress" class="progress"></div>
        </div>
        
        <div class="options">
            <h3>Options Générales</h3>
            <div>
                <label for="fourniture">Fourniture :</label>
                <select id="fourniture">
                    <option value="client">Fourniture à la charge du client</option>
                    <option value="entreprise">Fourniture à la charge de l'entreprise</option>
                </select>
            </div>
            <div>
                <label for="meubles">Protection des meubles :</label>
                <select id="meubles">
                    <option value="non">Pas de meubles présents</option>
                    <option value="client">Meubles présents - Protection par le client</option>
                    <option value="entreprise">Meubles présents - Protection par l'entreprise</option>
                </select>
            </div>
        </div>
        
        <div id="pieces-container">
            <!-- Les pièces seront ajoutées ici dynamiquement -->
        </div>
        
        <button id="add-piece-btn">Ajouter une pièce</button>
        
        <button id="generate-devis-btn">Générer le devis</button>
        
        <div id="devis-result" class="devis-result" style="display: none;">
            <h2>Devis Estimatif</h2>
            <div id="devis-details"></div>
            <table id="devis-table" class="devis-table">
                <thead>
                    <tr>
                        <th>Pièce</th>
                        <th>Surface</th>
                        <th>Support</th>
                        <th>Revêtement existant</th>
                        <th>Préparation</th>
                        <th>Finition</th>
                        <th>Couleur</th>
                        <th>Surface (m²)</th>
                    </tr>
                </thead>
                <tbody id="devis-body">
                    <!-- Les lignes du devis seront ajoutées ici -->
                </tbody>
            </table>
            <div id="devis-summary" style="margin-top: 20px;">
                <!-- Le résumé du devis sera ajouté ici -->
            </div>
            <button id="print-devis-btn" style="margin-top: 20px;">Imprimer le devis</button>
        </div>
    </div>
    
    <script>
        // Configuration Firebase - À remplacer par vos propres informations
        const firebaseConfig = {
            apiKey: "VOTRE_API_KEY",
            authDomain: "VOTRE_AUTH_DOMAIN",
            databaseURL: "VOTRE_DATABASE_URL",
            projectId: "VOTRE_PROJECT_ID",
            storageBucket: "VOTRE_STORAGE_BUCKET",
            messagingSenderId: "VOTRE_MESSAGING_SENDER_ID",
            appId: "VOTRE_APP_ID",
            measurementId: "VOTRE_MEASUREMENT_ID"
        };
        
        // Initialiser Firebase si les clés sont définies
        let analytics = null;
        let database = null;
        let sessionId = Date.now().toString(36) + Math.random().toString(36).substr(2);
        
        try {
            if (firebaseConfig.apiKey !== "VOTRE_API_KEY") {
                firebase.initializeApp(firebaseConfig);
                analytics = firebase.analytics();
                database = firebase.database();
                console.log("Analytics activé");
            }
        } catch (e) {
            console.log("Firebase non configuré: ", e);
        }
        
        // Fonction pour enregistrer les événements
        function logEvent(eventName, eventData = {}) {
            try {
                if (analytics) {
                    // Enregistrer dans Firebase Analytics
                    analytics.logEvent(eventName, eventData);
                    
                    // Enregistrer dans Firebase Database avec horodatage
                    if (database) {
                        const eventRef = database.ref('form_events/' + sessionId);
                        eventRef.push({
                            timestamp: firebase.database.ServerValue.TIMESTAMP,
                            event: eventName,
                            data: eventData
                        });
                    }
                    console.log("Événement enregistré:", eventName, eventData);
                }
            } catch (e) {
                console.log("Erreur lors de l'enregistrement de l'événement:", e);
            }
        }
        
        // Fonction pour mettre à jour la barre de progression
        function updateProgress() {
            const totalPieces = document.querySelectorAll('.piece').length;
            const totalSurfaces = document.querySelectorAll('.surface').length;
            const formFields = document.querySelectorAll('select, input[type="number"], input[type="color"]');
            let filledFields = 0;
            
            formFields.forEach(field => {
                if (field.tagName === 'SELECT' && field.value !== '' && field.value !== 'default') {
                    filledFields++;
                } else if (field.tagName === 'INPUT' && field.type === 'number' && field.value !== '' && field.value > 0) {
                    filledFields++;
                } else if (field.tagName === 'INPUT' && field.type === 'color' && field.value !== '#ffffff') {
                    filledFields++;
                }
            });
            
            // Le minimum est de 10% (pour montrer qu'on a commencé)
            // On considère que 100% = au moins une pièce avec toutes ses infos
            const totalRequired = 10; // Nombre approximatif de champs à remplir par surface
            const progress = Math.max(10, Math.min(100, Math.round((filledFields / (totalSurfaces * totalRequired)) * 100)));
            
            document.getElementById('progress').style.width = progress + '%';
            
            return {
                progress: progress,
                totalPieces: totalPieces,
                totalSurfaces: totalSurfaces,
                filledFields: filledFields
            };
        }
        
        // Fonction pour enregistrer les changements dans les champs
        function logChange(elementId, fieldType) {
            const element = document.getElementById(elementId);
            if (!element) return;
            
            const value = element.value;
            logEvent('field_changed', {
                elementId: elementId,
                fieldType: fieldType,
                value: value
            });
            
            // Mettre à jour la barre de progression
            const progress = updateProgress();
            logEvent('progress_updated', progress);
        }

        document.addEventListener('DOMContentLoaded', function() {
            const piecesContainer = document.getElementById('pieces-container');
            const addPieceBtn = document.getElementById('add-piece-btn');
            const generateDevisBtn = document.getElementById('generate-devis-btn');
            const printDevisBtn = document.getElementById('print-devis-btn');
            
            // Types de pièces disponibles
            const typesPieces = [
                'Salon', 'Cuisine', 'Salle de bain', 'Toilette', 
                'Chambre 1', 'Chambre 2', 'Chambre 3', 'Chambre 4', 
                'Escalier', 'Couloir', 'Entrée', 'Local', 'Autre'
            ];
            
            // Types de surfaces disponibles
            const typesSurfaces = ['Plafond', 'Murs', 'Portes', 'Fenêtres', 'Sol'];
            
            // Types de supports disponibles
            const typesSupports = ['Béton', 'Placo', 'Bois', 'Métal'];
            
            // Types de revêtements existants
            const typesRevetements = [
                'Aucun', 'Papier peint', 'Toile de verre', 'Gouttelettes', 
                'Crépi', 'Revêtement bois', 'Carrelage au sol', 'Faïence murale', 'Autre'
            ];
            
            // Types de préparations
            const typesPreparations = [
                'Aucune (garder le revêtement existant)', 
                'Retrait du revêtement existant'
            ];
            
            // Types de finitions
            const typesFinitions = [
                'Pose papier peint', 
                'Pose de toile de verre', 
                'Peinture acrylique en 2 couches après préparation en ponçage et enduit',
                'Vernis'
            ];
            
            // Types de finitions pour peinture
            const typesFinitionsPeinture = [
                'Mate', 'Velours', 'Satinée', 'Brillante'
            ];
            
            let pieceCounter = 0;
            
            // Enregistrer que l'utilisateur a ouvert le formulaire
            logEvent('form_opened', {
                timestamp: new Date().toISOString(),
                referrer: document.referrer
            });
            
            // Ajouter les événements de suivi pour les boutons principaux
            addPieceBtn.addEventListener('click', function() {
                logEvent('add_piece_button_clicked', {
                    currentPieceCount: document.querySelectorAll('.piece').length
                });
                addPiece();
            });
            
            generateDevisBtn.addEventListener('click', function() {
                const progressData = updateProgress();
                logEvent('generate_devis_clicked', {
                    pieceCount: progressData.totalPieces,
                    surfaceCount: progressData.totalSurfaces,
                    completionPercentage: progressData.progress
                });
                generateDevis();
            });
            
            printDevisBtn.addEventListener('click', function() {
                logEvent('print_devis_clicked');
                window.print();
            });
            
            // Ajouter des événements pour les options générales
            document.getElementById('fourniture').addEventListener('change', function() {
                logEvent('fourniture_changed', {
                    value: this.value
                });
                updateProgress();
            });
            
            document.getElementById('meubles').addEventListener('change', function() {
                logEvent('meubles_changed', {
                    value: this.value
                });
                updateProgress();
            });
            
            // Fonction pour ajouter une nouvelle pièce
            function addPiece() {
                pieceCounter++;
                const pieceId = `piece-${pieceCounter}`;
                
                const pieceDiv
