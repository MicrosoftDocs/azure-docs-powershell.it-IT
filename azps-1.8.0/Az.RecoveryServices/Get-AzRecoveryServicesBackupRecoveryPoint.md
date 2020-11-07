---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 9a5d0f0607692217cf4016a1261f23b725d07e68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677650"
---
# <span data-ttu-id="91ab5-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="91ab5-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="91ab5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="91ab5-103">Ottiene i punti di ripristino per un elemento di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="91ab5-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="91ab5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91ab5-104">SYNTAX</span></span>

### <span data-ttu-id="91ab5-105">NoFilterParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="91ab5-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91ab5-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="91ab5-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91ab5-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="91ab5-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91ab5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91ab5-108">DESCRIPTION</span></span>
<span data-ttu-id="91ab5-109">Il cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** ottiene i punti di ripristino per un elemento di backup di Azure supportato.</span><span class="sxs-lookup"><span data-stu-id="91ab5-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="91ab5-110">Dopo aver eseguito il backup di un elemento, un oggetto **AzureRmRecoveryServicesBackupRecoveryPoint** ha uno o più punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="91ab5-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="91ab5-111">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="91ab5-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="91ab5-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91ab5-112">EXAMPLES</span></span>

### <span data-ttu-id="91ab5-113">Esempio 1: ottenere punti di ripristino dall'ultima settimana per un elemento</span><span class="sxs-lookup"><span data-stu-id="91ab5-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="91ab5-114">Il primo comando ottiene la data di sette giorni fa e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="91ab5-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="91ab5-115">Il secondo comando ottiene la data odierna e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="91ab5-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="91ab5-116">Il terzo comando ottiene i contenitori di backup di AzureVM e li archivia nella variabile $Containers.</span><span class="sxs-lookup"><span data-stu-id="91ab5-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="91ab5-117">Il quarto comando ottiene l'elemento di backup denominato V2VM e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="91ab5-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="91ab5-118">L'ultimo comando ottiene una matrice di punti di ripristino per l'elemento in $BackupItem e quindi li archivia nella variabile $RP.</span><span class="sxs-lookup"><span data-stu-id="91ab5-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="91ab5-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91ab5-119">PARAMETERS</span></span>

### <span data-ttu-id="91ab5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91ab5-120">-DefaultProfile</span></span>
<span data-ttu-id="91ab5-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91ab5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91ab5-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="91ab5-122">-EndDate</span></span>
<span data-ttu-id="91ab5-123">Specifica la fine dell'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="91ab5-123">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="91ab5-124">-Elemento</span><span class="sxs-lookup"><span data-stu-id="91ab5-124">-Item</span></span>
<span data-ttu-id="91ab5-125">Specifica l'elemento per cui questo cmdlet ottiene i punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="91ab5-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="91ab5-126">Per ottenere un oggetto **AzureRmRecoveryServicesBackupItem** , usa il cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="91ab5-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="91ab5-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="91ab5-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="91ab5-128">Specifica il percorso in cui scaricare il file di input per ripristinare la chiave del Vault per una macchina virtuale crittografata.</span><span class="sxs-lookup"><span data-stu-id="91ab5-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="91ab5-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="91ab5-129">-RecoveryPointId</span></span>
<span data-ttu-id="91ab5-130">Specifica l'ID del punto di recupero.</span><span class="sxs-lookup"><span data-stu-id="91ab5-130">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="91ab5-131">-StartDate</span><span class="sxs-lookup"><span data-stu-id="91ab5-131">-StartDate</span></span>
<span data-ttu-id="91ab5-132">Specifica l'inizio dell'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="91ab5-132">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="91ab5-133">-VaultId</span><span class="sxs-lookup"><span data-stu-id="91ab5-133">-VaultId</span></span>
<span data-ttu-id="91ab5-134">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="91ab5-134">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="91ab5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ab5-135">CommonParameters</span></span>
<span data-ttu-id="91ab5-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91ab5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ab5-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91ab5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ab5-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91ab5-138">INPUTS</span></span>

### <span data-ttu-id="91ab5-139">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="91ab5-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="91ab5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="91ab5-140">System.String</span></span>

## <span data-ttu-id="91ab5-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91ab5-141">OUTPUTS</span></span>

### <span data-ttu-id="91ab5-142">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="91ab5-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="91ab5-143">Note</span><span class="sxs-lookup"><span data-stu-id="91ab5-143">NOTES</span></span>

## <span data-ttu-id="91ab5-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91ab5-144">RELATED LINKS</span></span>

[<span data-ttu-id="91ab5-145">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="91ab5-145">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="91ab5-146">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="91ab5-146">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

