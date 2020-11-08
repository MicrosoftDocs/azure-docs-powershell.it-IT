---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029916"
---
# Remove-AzureVMImage

## Sinossi
Rimuove un'immagine del sistema operativo dal repository di immagini.

## SINTASSI

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzureVMImage** rimuove un'immagine del sistema operativo dal repository di immagini.
Per impostazione predefinita, questo cmdlet non elimina il BLOB di immagini fisiche associato dall'account di archiviazione.
Per eliminare il disco rigido virtuale associato (VHD), usare il parametro **DeleteVHD** .

## ESEMPI

### Esempio 1: rimuovere un'immagine dal repository di immagini
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

Questo comando rimuove l'immagine denominata Image001 dal repository di immagini.

### Esempio 2: rimuovere un'immagine dal repository di immagini e anche dal VHD
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

Questo comando rimuove l'immagine denominata Image001 dal repository di immagini ed elimina anche l'immagine del VHD fisico dall'account di archiviazione.

### Esempio 3: impostare un contesto di sottoscrizione e quindi rimuovere tutte le immagini
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

Questo comando imposta il contesto di sottoscrizione e quindi rimuove tutte le immagini dal repository di immagini la cui etichetta include il nome beta.

## PARAMETRI

### -DeleteVHD
Indica che questo cmdlet elimina il BLOB di immagine del VHD fisico dall'account di archiviazione.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageName
Specifica il sistema operativo o l'immagine della macchina virtuale da rimuovere dal repository di immagini.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet.
Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

[Add-AzureVMImage](./Add-AzureVMImage.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Salva-AzureVMImage](./Save-AzureVMImage.md)

[Update-AzureVMImage](./Update-AzureVMImage.md)


