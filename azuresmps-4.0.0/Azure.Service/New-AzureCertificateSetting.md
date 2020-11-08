---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023890"
---
# New-AzureCertificateSetting

## Sinossi
Crea un oggetto di impostazione del certificato per un certificato in un servizio.

## SINTASSI

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureCertificateSetting** crea un oggetto di impostazione del certificato per un certificato che si trova in un servizio Azure.

Puoi usare un oggetto di impostazione del certificato per creare un oggetto di configurazione usando il cmdlet **Add-AzureProvisioningConfig** .
Usa un oggetto Configuration per creare una macchina virtuale usando il cmdlet **New-AzureVM** .
Puoi usare un oggetto di impostazione del certificato per creare una macchina virtuale usando il cmdlet **New-AzureQuickVM** .

## ESEMPI

### Esempio 1: creare un oggetto di impostazione del certificato
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

Questo comando crea un oggetto di impostazione del certificato per un certificato esistente.

### Esempio 2: creare una macchina virtuale che usa un oggetto impostazione di configurazione
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

Il primo comando aggiunge il certificato ContosoCert. cer al servizio denominato ContosoService usando il cmdlet **Add-AzureCertificate** .

Il secondo comando crea un oggetto di impostazione del certificato e lo archivia nella variabile $CertificateSetting.

Il terzo comando ottiene un'immagine dal repository di immagini usando il cmdlet **Get-AzureVMImage** .
Questo comando Archivia l'immagine nella variabile $Image.

Il comando finale crea un oggetto di configurazione della macchina virtuale basato sull'immagine in $Image usando il cmdlet **New-AzureVMConfig** .
Il comando passa l'oggetto al cmdlet **Add-AzureProvisioningConfig** usando l'operatore pipeline.
Questo cmdlet aggiunge le informazioni di provisioning alla configurazione.
Il comando passa l'oggetto al cmdlet **New-AzureVM** , che crea la macchina virtuale.

## PARAMETRI

### -InformationAction
Specifica il modo in cui questo cmdlet risponde a un evento informativo.

I valori accettabili per questo parametro sono i seguenti:

- Continuare
- Ignora
- Informarsi
- SilentlyContinue
- Stop
- Sospensione

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifica una variabile di informazioni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StoreName
Specifica l'archivio certificati in cui inserire il certificato.
I valori validi sono: 

- AddressBook
- AuthRoot
- CertificateAuthority
- Non consentiti
- Personale
- Radice
- TrustedPeople
- TrustedPublisher

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identificazione personale
Specifica l'identificazione personale del certificato.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureCertificate](./Add-AzureCertificate.md)

[Add-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[Get-AzureCertificate](./Get-AzureCertificate.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[New-AzureQuickVM](./New-AzureQuickVM.md)

[New-AzureVM](./New-AzureVM.md)

[Remove-AzureCertificate](./Remove-AzureCertificate.md)


