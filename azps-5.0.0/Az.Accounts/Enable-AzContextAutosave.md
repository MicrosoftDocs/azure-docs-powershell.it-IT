---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201728"
---
# Enable-AzContextAutosave

## Sinossi
I contesti di Azure sono oggetti di PowerShell che rappresentano l'abbonamento attivo per eseguire comandi e le informazioni di autenticazione necessarie per connettersi a un cloud di Azure. Con i contesti di Azure, Azure PowerShell non deve riautenticare l'account ogni volta che si cambia abbonamento. Per altre informazioni, Vedi [oggetti Context di Azure PowerShell](https://docs.microsoft.com/powershell/azure/context-persistence).

Questo cmdlet consente di salvare e caricare automaticamente le informazioni sul contesto di Azure quando si avvia un processo di PowerShell. Ad esempio, quando si apre una nuova finestra.

## SINTASSI

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione

Consente di salvare le informazioni di contesto di Azure e caricarle automaticamente all'avvio di un processo di PowerShell. Il contesto viene salvato alla fine dell'esecuzione di qualsiasi cmdlet che influisce sul contesto. Ad esempio, qualsiasi cmdlet di profilo. Se si usa l'autenticazione utente, i token possono essere aggiornati durante l'uso di qualsiasi cmdlet.

## ESEMPI

### Esempio 1: abilitare il salvataggio delle credenziali per l'utente corrente

Attivare il salvataggio automatico delle credenziali per l'utente corrente. Ogni volta che viene aperta una finestra di PowerShell, il contesto corrente viene ricordato senza effettuare l'accesso.

```powershell
Enable-AzContextAutosave
```

### Esempio 2

Consente di salvare e caricare automaticamente le informazioni di credenziali, account e sottoscrizione di Azure quando si apre una finestra di PowerShell in questa sessione di PowerShell. AutoGenerated

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## PARAMETRI

### -DefaultProfile

Credenziali, tenant e abbonamento usati per la comunicazione con Azure

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

### -Ambito

Determina l'ambito delle modifiche al contesto. Ad esempio, se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente. Le modifiche apportate all'ambito `CurrentUser` verranno applicate a tutte le sessioni di PowerShell avviate dall'utente. Se una particolare sessione deve avere impostazioni diverse, usare l'ambito `Process` .

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Parametri comuni

Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings

## Note

## COLLEGAMENTI CORRELATI