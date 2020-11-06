---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: d9c53d550f64b17a7ee821b43322dd974b7b5676
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517355"
---
# <span data-ttu-id="95b03-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="95b03-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="95b03-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95b03-102">SYNOPSIS</span></span>
<span data-ttu-id="95b03-103">Ottiene i punti di ripristino per un elemento di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="95b03-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95b03-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95b03-104">SYNTAX</span></span>

### <span data-ttu-id="95b03-105">NoFilterParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="95b03-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95b03-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="95b03-106">DateTimeFilter</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95b03-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="95b03-107">RecoveryPointId</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95b03-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95b03-108">DESCRIPTION</span></span>
<span data-ttu-id="95b03-109">Il cmdlet **Get-AzureRmRecoveryServicesBackupRecoveryPoint** ottiene i punti di ripristino per un elemento di backup di Azure supportato.</span><span class="sxs-lookup"><span data-stu-id="95b03-109">The **Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="95b03-110">Dopo aver eseguito il backup di un elemento, un oggetto **AzureRmRecoveryServicesBackupRecoveryPoint** ha uno o più punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="95b03-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="95b03-111">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="95b03-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="95b03-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95b03-112">EXAMPLES</span></span>

### <span data-ttu-id="95b03-113">Esempio 1: ottenere punti di ripristino dall'ultima settimana per un elemento</span><span class="sxs-lookup"><span data-stu-id="95b03-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="95b03-114">Il primo comando ottiene la data di sette giorni fa e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="95b03-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="95b03-115">Il secondo comando ottiene la data odierna e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="95b03-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="95b03-116">Il terzo comando ottiene i contenitori di backup di AzureVM e li archivia nella variabile $Containers.</span><span class="sxs-lookup"><span data-stu-id="95b03-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="95b03-117">Il quarto comando ottiene l'elemento di backup denominato V2VM e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="95b03-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="95b03-118">L'ultimo comando ottiene una matrice di punti di ripristino per l'elemento in $BackupItem e quindi li archivia nella variabile $RP.</span><span class="sxs-lookup"><span data-stu-id="95b03-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="95b03-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95b03-119">PARAMETERS</span></span>

### <span data-ttu-id="95b03-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95b03-120">-DefaultProfile</span></span>
<span data-ttu-id="95b03-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95b03-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95b03-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="95b03-122">-EndDate</span></span>
<span data-ttu-id="95b03-123">Specifica la fine dell'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="95b03-123">Specifies the end of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95b03-124">-Elemento</span><span class="sxs-lookup"><span data-stu-id="95b03-124">-Item</span></span>
<span data-ttu-id="95b03-125">Specifica l'elemento per cui questo cmdlet ottiene i punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="95b03-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="95b03-126">Per ottenere un oggetto **AzureRmRecoveryServicesBackupItem** , usa il cmdlet Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="95b03-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95b03-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="95b03-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="95b03-128">Specifica il percorso in cui scaricare il file di input per ripristinare la chiave del Vault per una macchina virtuale crittografata.</span><span class="sxs-lookup"><span data-stu-id="95b03-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95b03-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="95b03-129">-RecoveryPointId</span></span>
<span data-ttu-id="95b03-130">Specifica l'ID del punto di recupero.</span><span class="sxs-lookup"><span data-stu-id="95b03-130">Specifies the recovery point ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95b03-131">-StartDate</span><span class="sxs-lookup"><span data-stu-id="95b03-131">-StartDate</span></span>
<span data-ttu-id="95b03-132">Specifica l'inizio dell'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="95b03-132">Specifies the start of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95b03-133">-VaultId</span><span class="sxs-lookup"><span data-stu-id="95b03-133">-VaultId</span></span>
<span data-ttu-id="95b03-134">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="95b03-134">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95b03-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95b03-135">CommonParameters</span></span>
<span data-ttu-id="95b03-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95b03-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95b03-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95b03-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95b03-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95b03-138">INPUTS</span></span>

### <span data-ttu-id="95b03-139">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="95b03-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="95b03-140">Parameters: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="95b03-140">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="95b03-141">System. String</span><span class="sxs-lookup"><span data-stu-id="95b03-141">System.String</span></span>
<span data-ttu-id="95b03-142">Parametri: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="95b03-142">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="95b03-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95b03-143">OUTPUTS</span></span>

### <span data-ttu-id="95b03-144">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="95b03-144">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="95b03-145">Note</span><span class="sxs-lookup"><span data-stu-id="95b03-145">NOTES</span></span>

## <span data-ttu-id="95b03-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95b03-146">RELATED LINKS</span></span>

[<span data-ttu-id="95b03-147">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="95b03-147">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="95b03-148">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="95b03-148">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


