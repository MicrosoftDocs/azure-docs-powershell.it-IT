---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 553a9561939ffcef3337b0c13d384c5f5f47340e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688205"
---
# Remove-AzureRmWebAppSSLBinding

## Sinossi
Rimuove un binding SSL da un certificato caricato.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### S1
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzureRmWebAppSSLBinding** rimuove un binding SSL (Secure Sockets Layer) da un'app Web di Azure.
I binding SSL vengono usati per associare un'app Web a un certificato.

## ESEMPI

### Esempio 1: rimuovere un binding SSL per un'app Web
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

Questo comando rimuove il binding SSL per l'app Web ContosoWebApp.
Dato che il parametro *DeleteCertificate* non è incluso, il certificato verrà eliminato se non ha più binding SSL.

### Esempio 2: rimuovere un binding SSL senza rimuovere il certificato
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Analogamente all'esempio 1, questo comando rimuove anche il binding SSL per l'app Web ContosoWebApp.
In questo caso, tuttavia, il parametro *DeleteCertificate* è incluso e il valore del parametro è impostato su $false.
Ciò significa che il certificato non verrà eliminato indipendentemente dal fatto che disponga di binding SSL o meno.

### Esempio 3: usare un riferimento a un oggetto per rimuovere un binding SSL
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzureRmWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

In questo esempio viene usato un riferimento a un oggetto al sito Web dell'app per rimuovere il binding SSL per un'app Web.

Il primo comando usa il cmdlet Get-AzureRmWebApp per creare un riferimento a un oggetto all'app Web denominata ContosoWebApp.
Il riferimento a un oggetto viene archiviato in una variabile denominata $WebApp.

Il secondo comando usa il riferimento oggetto e il cmdlet **Remove-AzureRmWebAppSSLBinding** per rimuovere il binding SSL.

## PARAMETRI

### -DeleteCertificate
Specifica l'azione da eseguire se il binding SSL da rimuovere è l'unico binding usato dal certificato.
Se *DeleteCertificate* è impostato su $false, il certificato non verrà eliminato quando l'associazione viene eliminata.
Se *DeleteCertificate* è impostato su $true o non è incluso nel comando, il certificato verrà eliminato insieme al binding SSL.

Il certificato verrà eliminato solo se il binding SSL da rimuovere è l'unico binding usato dal certificato.
Se il certificato contiene più di un binding, il certificato non verrà rimosso indipendentemente dal valore del parametro *DeleteCertificate* .

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Impone l'esecuzione del comando senza richiedere la conferma dell'utente.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome dell'app Web.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse a cui è assegnato il certificato.

Non è possibile usare il parametro *ResourceGroupName* e il parametro *Web App* nello stesso comando.

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Specifica lo slot di distribuzione dell'app Web.
Per ottenere uno slot di distribuzione, usare il cmdlet Get-AzureRMWebAppSlot.

```yaml
Type: System.String
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
Per ottenere un'app Web, usa il cmdlet Get-AzureRmWebApp.

Non è possibile usare il parametro *Web App* nello stesso comando del parametro *ResourceGroupName* e/o *WebAppName*.

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Specifica il nome dell'app Web.

Non è possibile usare il parametro *WebAppName* e il parametro *Web App* nello stesso comando.

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Sito
Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmWebAppSSLBinding](./Get-AzureRmWebAppSSLBinding.md)

[New-AzureRmWebAppSSLBinding](./New-AzureRmWebAppSSLBinding.md)

[Get-AzureRMWebAppSlot](./Get-AzureRMWebAppSlot.md)

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)


