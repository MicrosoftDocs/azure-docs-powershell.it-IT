---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 9e9aab3a71e976d9c41694702dae7a8087da9a36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970381"
---
# <span data-ttu-id="e6b61-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e6b61-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="e6b61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6b61-102">SYNOPSIS</span></span>

<span data-ttu-id="e6b61-103">Recupera i punti di ripristino per un elemento di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="e6b61-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="e6b61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6b61-104">SYNTAX</span></span>

### <span data-ttu-id="e6b61-105">NoFilterParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e6b61-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-UseSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b61-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="e6b61-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b61-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="e6b61-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6b61-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e6b61-108">DESCRIPTION</span></span>

<span data-ttu-id="e6b61-109">Il cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** ottiene i punti di ripristino per un elemento di backup di Azure di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="e6b61-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="e6b61-110">Dopo il backup di un elemento, un **oggetto AzureRmRecoveryServicesBackupRecoveryPoint** include uno o più punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e6b61-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="e6b61-111">Impostare il contesto del vault usando il parametro -VaultId.</span><span class="sxs-lookup"><span data-stu-id="e6b61-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="e6b61-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6b61-112">EXAMPLES</span></span>

### <span data-ttu-id="e6b61-113">Esempio 1: Ottenere punti di ripristino dell'ultima settimana per un elemento</span><span class="sxs-lookup"><span data-stu-id="e6b61-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="e6b61-114">Il primo comando recupera l'oggetto vault in base a vaultName.</span><span class="sxs-lookup"><span data-stu-id="e6b61-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="e6b61-115">Il secondo comando recupera la data di sette giorni fa e quindi la archivia nella $StartDate variabile.</span><span class="sxs-lookup"><span data-stu-id="e6b61-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="e6b61-116">Il terzo comando ottiene la data odierna e la archivia nella $EndDate variabile.</span><span class="sxs-lookup"><span data-stu-id="e6b61-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="e6b61-117">Il quarto comando ottiene i contenitori di backup AzureVM e li archivia nella $Container variabile.</span><span class="sxs-lookup"><span data-stu-id="e6b61-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="e6b61-118">Il quinto comando ottiene l'elemento di backup in base a workloadType, vaultId e quindi lo archivia nella $BackupItem variabile.</span><span class="sxs-lookup"><span data-stu-id="e6b61-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="e6b61-119">L'ultimo comando ottiene una matrice di punti di ripristino per l'elemento in $BackupItem e quindi li archivia nella $RP variabile.</span><span class="sxs-lookup"><span data-stu-id="e6b61-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="e6b61-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6b61-120">PARAMETERS</span></span>

### <span data-ttu-id="e6b61-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b61-121">-DefaultProfile</span></span>

<span data-ttu-id="e6b61-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6b61-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6b61-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="e6b61-123">-EndDate</span></span>

<span data-ttu-id="e6b61-124">Specifica la fine dell'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="e6b61-124">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="e6b61-125">-Item</span><span class="sxs-lookup"><span data-stu-id="e6b61-125">-Item</span></span>

<span data-ttu-id="e6b61-126">Specifica l'elemento per cui questo cmdlet ottiene i punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e6b61-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="e6b61-127">Per ottenere un **oggetto AzureRmRecoveryServicesBackupItem,** usare il cmdlet **Get-AzRecoveryServicesBackupItem.**</span><span class="sxs-lookup"><span data-stu-id="e6b61-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="e6b61-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="e6b61-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="e6b61-129">Specifica il percorso in cui scaricare il file di input per ripristinare la chiave KeyVault per una macchina virtuale crittografata.</span><span class="sxs-lookup"><span data-stu-id="e6b61-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="e6b61-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="e6b61-130">-RecoveryPointId</span></span>

<span data-ttu-id="e6b61-131">Specifica l'ID del punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e6b61-131">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="e6b61-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="e6b61-132">-StartDate</span></span>

<span data-ttu-id="e6b61-133">Specifica l'inizio dell'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="e6b61-133">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="e6b61-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e6b61-134">-VaultId</span></span>

<span data-ttu-id="e6b61-135">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e6b61-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e6b61-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b61-136">CommonParameters</span></span>
<span data-ttu-id="e6b61-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6b61-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b61-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e6b61-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b61-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="e6b61-139">INPUTS</span></span>

### <span data-ttu-id="e6b61-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="e6b61-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="e6b61-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e6b61-141">System.String</span></span>

## <span data-ttu-id="e6b61-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6b61-142">OUTPUTS</span></span>

### <span data-ttu-id="e6b61-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="e6b61-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="e6b61-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="e6b61-144">NOTES</span></span>

## <span data-ttu-id="e6b61-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6b61-145">RELATED LINKS</span></span>

[<span data-ttu-id="e6b61-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e6b61-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="e6b61-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e6b61-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
