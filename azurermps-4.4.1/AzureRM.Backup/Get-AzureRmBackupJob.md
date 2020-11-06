---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 48c1a3c3b7422f76bfbea0fbff8c3df541764606
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510752"
---
# Get-AzureRmBackupJob

## Sinossi
Ottiene i processi di backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### FiltersSet (impostazione predefinita)
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### JobsListFilter
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmBackupJob** ottiene i processi di backup di Azure per un Vault specifico.

## ESEMPI

### Esempio 1: ottenere tutti i processi in un caveau di backup
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet **Get-AzureRmBackupVault** .
Il comando Archivia l'oggetto nella variabile $Vault.

Il secondo comando consente di ottenere tutti i processi per il Vault in $Vault.

### Esempio 2: ottenere processi completati
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

Questo comando ottiene i processi completati dal Vault in $Vault.

### Esempio 3: ottenere processi non riusciti per l'ultima settimana
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

Questo comando restituisce i processi non riusciti dell'ultima settimana dal Vault in $Vault.
Il parametro *from* specifica un periodo di sette giorni nel passato.
Il comando non specifica un valore per il parametro *to* .
Di conseguenza, usa il valore predefinito dell'ora corrente.

### Esempio 4: backup del sondaggio per un processo in corso che termina
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

Questo script esegue il polling del primo processo che è attualmente in corso fino al completamento del processo.

La prima riga dello script consente di ottenere tutti i processi in $Vault in corso e quindi di archiviarli nella variabile di matrice $Jobs.

La seconda riga archivia il primo processo dalla matrice $Jobs nella variabile $Job.

La terza riga avvia un ciclo **while** che controlla lo stato corrente del processo fino al completamento del processo.
Per informazioni sulla parola chiave **while** , digitare `Get-Help about_While` .

Il ciclo **while** scrive un messaggio nella console, dorme per dieci secondi e quindi aggiorna la variabile $job.
Lo script aggiorna la variabile $Job usando il valore esistente di $Job e il cmdlet corrente per ottenere lo stato corrente del processo.
Per informazioni sui cmdlet di Windows PowerShell, digitare `Get-Help Write-Host` e `Get-Help Start-Sleep` .

La riga finale dello script indica che lo script è terminato.

## PARAMETRI

### -Da
Specifica l'inizio, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.
Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.
Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Specifica un processo ottenuto da questo cmdlet.
Per ottenere un oggetto **AzureRmBackupJob** , usa il cmdlet Get-AzureRmBackupJob.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Specifica l'ID di un processo ottenuto da questo cmdlet.
L'ID è la proprietà **InstanceID** di un oggetto **AzureRmBackupJob** .
Per ottenere un oggetto **AzureRmBackupJob** , USA Get-AzureRmBackupJob.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Operazione
Specifica un'operazione dei processi ottenuti da questo cmdlet.
I valori accettabili per questo parametro sono i seguenti:

- Backup 
- ConfigureBackup 
- DeleteBackupData 
- Registrare 
- Ripristinare 
- Rimuovi protezione 
- Unregister

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Stato
Specifica lo stato dei processi ottenuti da questo cmdlet.
I valori accettabili per questo parametro sono i seguenti:

- InProgress
- Fallito
- Annullata
- Annullamento
- Completato
- CompletedWithWarnings 

Puoi specificare questo parametro per trovare tutti i processi in corso o tutti i processi non riusciti.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
Specifica la fine, come oggetto **DateTime** , di un intervallo di tempo per i processi ottenuti da questo cmdlet.
Il valore predefinito è l'ora di sistema corrente.
Se specifichi questo parametro, devi anche specificare il parametro *from* .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Digitare
Specifica il tipo di contenitore per cui questo cmdlet ottiene i processi di backup.
Attualmente, l'unico valore supportato è AzureVM.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vault
Specifica il Vault di backup per cui questo cmdlet ottiene i processi.
Per ottenere un oggetto **AzureRmBackupVault** , usa il cmdlet Get-AzureRmBackupVault.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### AzureRmBackupVault

## OUTPUT

### AzureRmBackupJob[]
Questo cmdlet restituisce uno o più processi di backup.

## Note
* Nessuno

## COLLEGAMENTI CORRELATI

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Stop-AzureRmBackupJob](./Stop-AzureRmBackupJob.md)

[Wait-AzureRmBackupJob](./Wait-AzureRmBackupJob.md)


