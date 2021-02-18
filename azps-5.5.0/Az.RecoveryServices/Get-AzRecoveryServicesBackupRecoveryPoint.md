---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 8e102b6542e2e9b262224e73af7b0eb0ed49236a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192974"
---
# <span data-ttu-id="6de41-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="6de41-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="6de41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6de41-102">SYNOPSIS</span></span>

<span data-ttu-id="6de41-103">Recupera i punti di ripristino per un elemento di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="6de41-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="6de41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6de41-104">SYNTAX</span></span>

### <span data-ttu-id="6de41-105">NoFilterParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6de41-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-UseSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6de41-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="6de41-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6de41-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="6de41-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6de41-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6de41-108">DESCRIPTION</span></span>

<span data-ttu-id="6de41-109">Il cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** ottiene i punti di ripristino per un elemento di backup di Azure di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="6de41-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="6de41-110">Dopo il backup di un elemento, un **oggetto AzureRmRecoveryServicesBackupRecoveryPoint** include uno o più punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6de41-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="6de41-111">Impostare il contesto del vault usando il parametro -VaultId.</span><span class="sxs-lookup"><span data-stu-id="6de41-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="6de41-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6de41-112">EXAMPLES</span></span>

### <span data-ttu-id="6de41-113">Esempio 1: Ottenere punti di ripristino dell'ultima settimana per un elemento</span><span class="sxs-lookup"><span data-stu-id="6de41-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="6de41-114">Il primo comando recupera l'oggetto vault in base a vaultName.</span><span class="sxs-lookup"><span data-stu-id="6de41-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="6de41-115">Il secondo comando recupera la data di sette giorni fa e quindi la archivia nella variabile $StartDate locale.</span><span class="sxs-lookup"><span data-stu-id="6de41-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="6de41-116">Il terzo comando ottiene la data odierna e la archivia nella $EndDate variabile.</span><span class="sxs-lookup"><span data-stu-id="6de41-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="6de41-117">Il quarto comando ottiene i contenitori di backup AzureVM e li archivia nella $Container variabile.</span><span class="sxs-lookup"><span data-stu-id="6de41-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="6de41-118">Il quinto comando ottiene l'elemento di backup in base a workloadType, vaultId e quindi lo archivia nella $BackupItem variabile.</span><span class="sxs-lookup"><span data-stu-id="6de41-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="6de41-119">L'ultimo comando ottiene una matrice di punti di ripristino per l'elemento in $BackupItem e quindi li archivia nella $RP variabile.</span><span class="sxs-lookup"><span data-stu-id="6de41-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="6de41-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6de41-120">PARAMETERS</span></span>

### <span data-ttu-id="6de41-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de41-121">-DefaultProfile</span></span>

<span data-ttu-id="6de41-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6de41-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6de41-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="6de41-123">-EndDate</span></span>

<span data-ttu-id="6de41-124">Specifica la fine dell'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="6de41-124">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="6de41-125">-Item</span><span class="sxs-lookup"><span data-stu-id="6de41-125">-Item</span></span>

<span data-ttu-id="6de41-126">Specifica l'elemento per cui questo cmdlet ottiene i punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6de41-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="6de41-127">Per ottenere un **oggetto AzureRmRecoveryServicesBackupItem,** usare il cmdlet **Get-AzRecoveryServicesBackupItem.**</span><span class="sxs-lookup"><span data-stu-id="6de41-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="6de41-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="6de41-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="6de41-129">Specifica il percorso in cui scaricare il file di input per ripristinare la chiave KeyVault per una macchina virtuale crittografata.</span><span class="sxs-lookup"><span data-stu-id="6de41-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="6de41-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="6de41-130">-RecoveryPointId</span></span>

<span data-ttu-id="6de41-131">Specifica l'ID del punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6de41-131">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="6de41-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="6de41-132">-StartDate</span></span>

<span data-ttu-id="6de41-133">Specifica l'inizio dell'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="6de41-133">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="6de41-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6de41-134">-VaultId</span></span>

<span data-ttu-id="6de41-135">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6de41-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6de41-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de41-136">CommonParameters</span></span>
<span data-ttu-id="6de41-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de41-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de41-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6de41-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de41-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="6de41-139">INPUTS</span></span>

### <span data-ttu-id="6de41-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="6de41-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="6de41-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6de41-141">System.String</span></span>

## <span data-ttu-id="6de41-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6de41-142">OUTPUTS</span></span>

### <span data-ttu-id="6de41-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="6de41-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="6de41-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="6de41-144">NOTES</span></span>

## <span data-ttu-id="6de41-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6de41-145">RELATED LINKS</span></span>

[<span data-ttu-id="6de41-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="6de41-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="6de41-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="6de41-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
