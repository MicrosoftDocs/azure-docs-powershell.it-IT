---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 4c1739120c024629e68395f34a7f66b4259eb311
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861926"
---
# Get-AzWebAppSSLBinding

## Sinossi
Ottiene un binding SSL certificato di Azure Web App.

## SINTASSI

### S1
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzWebAppSSLBinding** ottiene un binding SSL (Secure Sockets Layer) per una Azure Web App.
I binding SSL vengono usati per associare un'app Web a un certificato caricato.
Le app Web possono essere associate a più certificati.

## ESEMPI

### Esempio 1: ottenere binding SSL per un'app Web
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

Questo comando recupera i binding SSL per l'app Web ContosoWebApp, associato al gruppo di risorse ContosoResourceGroup.

### Esempio 2: usare un riferimento a un oggetto per ottenere binding SSL per un'app Web
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

I comandi in questo esempio ottengono anche i binding SSL per l'app Web ContosoWebApp; in questo caso, tuttavia, viene usato un riferimento a un oggetto al posto del nome dell'app Web e del nome del gruppo di risorse associato.
Questo riferimento all'oggetto viene creato dal primo comando dell'esempio, che usa **Get-AzWebApp** per creare un riferimento a un oggetto all'app Web denominata ContosoWebApp.
Il riferimento a un oggetto viene archiviato in una variabile denominata $WebApp.

Questa variabile e il cmdlet **Get-AzWebAppSSLBinding** vengono quindi usati dal secondo comando per ottenere i binding SSL.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome del binding SSL.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse a cui è assegnato il certificato.

Non è possibile usare il parametro *ResourceGroupName* e il parametro *Web App* nello stesso comando.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Specifica uno slot di distribuzione dell'app Web.
Per ottenere uno slot di distribuzione, usare il cmdlet Get-AzWebAppSlot.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Web App
Specifica un'app Web.
Per ottenere un'app Web, usa il cmdlet Get-AzWebApp.

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Specifica il nome dell'app Web da cui questo cmdlet ottiene i binding SSL.

Non è possibile usare il parametro *WebAppName* e il parametro *Web App* nello stesso comando.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Sito
Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebApp](./Get-AzWebApp.md)


