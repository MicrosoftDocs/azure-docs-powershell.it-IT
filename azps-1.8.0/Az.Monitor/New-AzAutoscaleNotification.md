---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 35eeb7aa1482cb04c194f1a0674825bd3a72b187
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835043"
---
# New-AzAutoscaleNotification

## Sinossi
Crea una notifica tramite posta elettronica di scala.

## SINTASSI

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzAutoscaleNotification** crea una notifica tramite posta elettronica per la scalabilità verticale.

## ESEMPI

### Esempio 1: creare una notifica di posta elettronica in scala ridotta
```
PS C:\>New-AzAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

Questo comando crea una notifica di posta elettronica di Autosacale per due indirizzi specificati.

### Esempio 2: creare una notifica di posta elettronica di scalabilità per l'amministratore della sottoscrizione
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

Questo comando crea una notifica di posta elettronica di Autosacale per l'amministratore della sottoscrizione.

## PARAMETRI

### -CustomEmail
Specifica un elenco delimitato da virgole di indirizzi di posta elettronica.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendEmailToSubscriptionAdministrator
Indica che questa operazione invia una notifica tramite posta elettronica all'amministratore della sottoscrizione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SendEmailToSubscriptionCoAdministrator
Indica che questa operazione invia una notifica tramite posta elettronica ai coordinatori dell'abbonamento.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Webhook
Specifica un elenco delimitato da virgole di Webhook di scala.

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Management. monitor. Management. Models. WebhookNotification []

### System. String []

### System. Management. Automation. SwitchParameter

## OUTPUT

### Microsoft. Azure. Management. monitor. Management. Models. AutoscaleNotification

## Note

## COLLEGAMENTI CORRELATI

[New-AzAutoscaleWebhook](./New-AzAutoscaleWebhook.md)


