---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 676ba76cb4412e03c684be4d166e8707c5652b26
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486448"
---
# <span data-ttu-id="3d6c3-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3d6c3-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="3d6c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d6c3-102">SYNOPSIS</span></span>

<span data-ttu-id="3d6c3-103">Ottiene i punti di ripristino per un elemento di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="3d6c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d6c3-104">SYNTAX</span></span>

### <span data-ttu-id="3d6c3-105">NoFilterParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3d6c3-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d6c3-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="3d6c3-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d6c3-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="3d6c3-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d6c3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d6c3-108">DESCRIPTION</span></span>

<span data-ttu-id="3d6c3-109">Il cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** ottiene i punti di ripristino per un elemento di backup di Azure supportato.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="3d6c3-110">Dopo aver eseguito il backup di un elemento, un oggetto **AzureRmRecoveryServicesBackupRecoveryPoint** ha uno o più punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="3d6c3-111">Imposta il contesto del Vault usando il parametro-VaultId.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="3d6c3-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d6c3-112">EXAMPLES</span></span>

### <span data-ttu-id="3d6c3-113">Esempio 1: ottenere punti di ripristino dall'ultima settimana per un elemento</span><span class="sxs-lookup"><span data-stu-id="3d6c3-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="3d6c3-114">Il primo comando ottiene l'oggetto Vault basato su VAULTNAME.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="3d6c3-115">Il secondo comando ottiene la data di sette giorni fa e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="3d6c3-116">Il terzo comando ottiene la data odierna e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="3d6c3-117">Il quarto comando ottiene i contenitori di backup di AzureVM e li archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="3d6c3-118">Il quinto comando ottiene l'elemento di backup basato su workloadType, vaultId e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="3d6c3-119">L'ultimo comando ottiene una matrice di punti di ripristino per l'elemento in $BackupItem e quindi li archivia nella variabile $RP.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="3d6c3-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d6c3-120">PARAMETERS</span></span>

### <span data-ttu-id="3d6c3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d6c3-121">-DefaultProfile</span></span>

<span data-ttu-id="3d6c3-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d6c3-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="3d6c3-123">-EndDate</span></span>

<span data-ttu-id="3d6c3-124">Specifica la fine dell'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-124">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="3d6c3-125">-Elemento</span><span class="sxs-lookup"><span data-stu-id="3d6c3-125">-Item</span></span>

<span data-ttu-id="3d6c3-126">Specifica l'elemento per cui questo cmdlet ottiene i punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="3d6c3-127">Per ottenere un oggetto **AzureRmRecoveryServicesBackupItem** , usa il cmdlet **Get-AzRecoveryServicesBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="3d6c3-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="3d6c3-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="3d6c3-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="3d6c3-129">Specifica il percorso in cui scaricare il file di input per ripristinare la chiave del Vault per una macchina virtuale crittografata.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="3d6c3-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="3d6c3-130">-RecoveryPointId</span></span>

<span data-ttu-id="3d6c3-131">Specifica l'ID del punto di recupero.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-131">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="3d6c3-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="3d6c3-132">-StartDate</span></span>

<span data-ttu-id="3d6c3-133">Specifica l'inizio dell'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-133">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="3d6c3-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3d6c3-134">-VaultId</span></span>

<span data-ttu-id="3d6c3-135">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3d6c3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6c3-136">CommonParameters</span></span>
<span data-ttu-id="3d6c3-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d6c3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d6c3-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d6c3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6c3-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d6c3-139">INPUTS</span></span>

### <span data-ttu-id="3d6c3-140">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="3d6c3-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="3d6c3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3d6c3-141">System.String</span></span>

## <span data-ttu-id="3d6c3-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d6c3-142">OUTPUTS</span></span>

### <span data-ttu-id="3d6c3-143">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="3d6c3-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="3d6c3-144">Note</span><span class="sxs-lookup"><span data-stu-id="3d6c3-144">NOTES</span></span>

## <span data-ttu-id="3d6c3-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d6c3-145">RELATED LINKS</span></span>

[<span data-ttu-id="3d6c3-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="3d6c3-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="3d6c3-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3d6c3-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
