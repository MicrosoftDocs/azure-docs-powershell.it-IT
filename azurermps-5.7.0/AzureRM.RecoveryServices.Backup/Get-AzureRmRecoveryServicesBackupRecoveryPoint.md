---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 8223172994eb4fdbea3c887f788c4b0e445e0202
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509736"
---
# <span data-ttu-id="b03c6-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b03c6-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="b03c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b03c6-102">SYNOPSIS</span></span>
<span data-ttu-id="b03c6-103">Ottiene i punti di ripristino per un elemento di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="b03c6-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b03c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b03c6-104">SYNTAX</span></span>

### <span data-ttu-id="b03c6-105">NoFilterParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b03c6-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b03c6-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="b03c6-106">DateTimeFilter</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b03c6-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="b03c6-107">RecoveryPointId</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b03c6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b03c6-108">DESCRIPTION</span></span>
<span data-ttu-id="b03c6-109">Il cmdlet **Get-AzureRmRecoveryServicesBackupRecoveryPoint** ottiene i punti di ripristino per un elemento di backup di Azure supportato.</span><span class="sxs-lookup"><span data-stu-id="b03c6-109">The **Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="b03c6-110">Dopo aver eseguito il backup di un elemento, un oggetto **AzureRmRecoveryServicesBackupRecoveryPoint** ha uno o più punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b03c6-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>

<span data-ttu-id="b03c6-111">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="b03c6-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b03c6-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b03c6-112">EXAMPLES</span></span>

### <span data-ttu-id="b03c6-113">Esempio 1: ottenere punti di ripristino dall'ultima settimana per un elemento</span><span class="sxs-lookup"><span data-stu-id="b03c6-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="b03c6-114">Il primo comando ottiene la data di sette giorni fa e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="b03c6-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="b03c6-115">Il secondo comando ottiene la data odierna e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="b03c6-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="b03c6-116">Il terzo comando ottiene i contenitori di backup di AzureVM e li archivia nella variabile $Containers.</span><span class="sxs-lookup"><span data-stu-id="b03c6-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>

<span data-ttu-id="b03c6-117">Il quarto comando ottiene l'elemento di backup denominato V2VM e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="b03c6-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="b03c6-118">L'ultimo comando ottiene una matrice di punti di ripristino per l'elemento in $BackupItem e quindi li archivia nella variabile $RP.</span><span class="sxs-lookup"><span data-stu-id="b03c6-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="b03c6-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b03c6-119">PARAMETERS</span></span>

### <span data-ttu-id="b03c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03c6-120">-DefaultProfile</span></span>
<span data-ttu-id="b03c6-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b03c6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03c6-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b03c6-122">-EndDate</span></span>
<span data-ttu-id="b03c6-123">Specifica la fine dell'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="b03c6-123">Specifies the end of the date range.</span></span>

```yaml
Type: DateTime
Parameter Sets: DateTimeFilter
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03c6-124">-Elemento</span><span class="sxs-lookup"><span data-stu-id="b03c6-124">-Item</span></span>
<span data-ttu-id="b03c6-125">Specifica l'elemento per cui questo cmdlet ottiene i punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b03c6-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="b03c6-126">Per ottenere un oggetto **AzureRmRecoveryServicesBackupItem** , usa il cmdlet Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="b03c6-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b03c6-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="b03c6-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="b03c6-128">Specifica il percorso in cui scaricare il file di input per ripristinare la chiave del Vault per una macchina virtuale crittografata.</span><span class="sxs-lookup"><span data-stu-id="b03c6-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: RecoveryPointId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03c6-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="b03c6-129">-RecoveryPointId</span></span>
<span data-ttu-id="b03c6-130">Specifica l'ID del punto di recupero.</span><span class="sxs-lookup"><span data-stu-id="b03c6-130">Specifies the recovery point ID.</span></span>

```yaml
Type: String
Parameter Sets: RecoveryPointId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03c6-131">-StartDate</span><span class="sxs-lookup"><span data-stu-id="b03c6-131">-StartDate</span></span>
<span data-ttu-id="b03c6-132">Specifica l'inizio dell'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="b03c6-132">Specifies the start of the date range.</span></span>

```yaml
Type: DateTime
Parameter Sets: DateTimeFilter
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03c6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03c6-133">CommonParameters</span></span>
<span data-ttu-id="b03c6-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b03c6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b03c6-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b03c6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03c6-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b03c6-136">INPUTS</span></span>

### <span data-ttu-id="b03c6-137">ItemBase</span><span class="sxs-lookup"><span data-stu-id="b03c6-137">ItemBase</span></span>
<span data-ttu-id="b03c6-138">Il parametro ' Item ' accetta il valore di tipo ' ItemBase ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b03c6-138">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="b03c6-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b03c6-139">OUTPUTS</span></span>

### <span data-ttu-id="b03c6-140">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="b03c6-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="b03c6-141">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase]</span><span class="sxs-lookup"><span data-stu-id="b03c6-141">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase]</span></span>

## <span data-ttu-id="b03c6-142">Note</span><span class="sxs-lookup"><span data-stu-id="b03c6-142">NOTES</span></span>

## <span data-ttu-id="b03c6-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b03c6-143">RELATED LINKS</span></span>

[<span data-ttu-id="b03c6-144">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b03c6-144">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="b03c6-145">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b03c6-145">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


