---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486456"
---
# <span data-ttu-id="2c8b5-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="2c8b5-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="2c8b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c8b5-102">SYNOPSIS</span></span>
<span data-ttu-id="2c8b5-103">Questo comando elenca i punti iniziali e finali della catena di log non interrotta dell'elemento di backup indicato.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="2c8b5-104">Usalo per determinare se il temporizzatore, a cui l'utente vuole che venga ripristinato il DB, sia valido o meno.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="2c8b5-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c8b5-105">SYNTAX</span></span>

### <span data-ttu-id="2c8b5-106">NoFilterParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2c8b5-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c8b5-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="2c8b5-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c8b5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c8b5-108">DESCRIPTION</span></span>
<span data-ttu-id="2c8b5-109">Il cmdlet **Get-AzRecoveryServicesBackupRecoveryLogChain** ottiene i punti di ripristino dell'intervallo di tempo in tempo per un elemento di backup di Azure supportato.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="2c8b5-110">Dopo aver eseguito il backup di un elemento, un oggetto **AzRecoveryServicesBackupRecoveryLogChain** ha uno o più intervalli di tempo di recupero.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="2c8b5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c8b5-111">EXAMPLES</span></span>

### <span data-ttu-id="2c8b5-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2c8b5-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="2c8b5-113">Il primo comando ottiene la data di sette giorni fa e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="2c8b5-114">Il secondo comando ottiene la data odierna e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="2c8b5-115">Il terzo comando ottiene i contenitori di backup di AzureWorkload e li archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="2c8b5-116">Il quarto comando ottiene l'elemento di backup e lo condivide attraverso il cmdlet piped come oggetto elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="2c8b5-117">L'ultimo comando ottiene una matrice di intervalli di tempo del punto di ripristino per l'elemento in $BackupItem e quindi li archivia nella variabile $RP.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="2c8b5-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2c8b5-118">Example 2</span></span>

<span data-ttu-id="2c8b5-119">Questo comando elenca i punti iniziali e finali della catena di log non interrotta dell'elemento di backup indicato.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="2c8b5-120">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="2c8b5-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="2c8b5-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c8b5-121">PARAMETERS</span></span>

### <span data-ttu-id="2c8b5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c8b5-122">-DefaultProfile</span></span>
<span data-ttu-id="2c8b5-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c8b5-124">-EndDate</span><span class="sxs-lookup"><span data-stu-id="2c8b5-124">-EndDate</span></span>
<span data-ttu-id="2c8b5-125">Ora di fine dell'intervallo di tempo per il quale il punto di ripristino deve essere recuperato</span><span class="sxs-lookup"><span data-stu-id="2c8b5-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2c8b5-126">-Elemento</span><span class="sxs-lookup"><span data-stu-id="2c8b5-126">-Item</span></span>
<span data-ttu-id="2c8b5-127">Oggetto elemento protetto per il quale deve essere recuperato il punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="2c8b5-127">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2c8b5-128">-StartDate</span><span class="sxs-lookup"><span data-stu-id="2c8b5-128">-StartDate</span></span>
<span data-ttu-id="2c8b5-129">Ora di inizio dell'intervallo di tempo per il quale il punto di ripristino deve essere recuperato</span><span class="sxs-lookup"><span data-stu-id="2c8b5-129">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2c8b5-130">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2c8b5-130">-VaultId</span></span>
<span data-ttu-id="2c8b5-131">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-131">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2c8b5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c8b5-132">CommonParameters</span></span>
<span data-ttu-id="2c8b5-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c8b5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c8b5-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c8b5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c8b5-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c8b5-135">INPUTS</span></span>

### <span data-ttu-id="2c8b5-136">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="2c8b5-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="2c8b5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2c8b5-137">System.String</span></span>

## <span data-ttu-id="2c8b5-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c8b5-138">OUTPUTS</span></span>

### <span data-ttu-id="2c8b5-139">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="2c8b5-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="2c8b5-140">Note</span><span class="sxs-lookup"><span data-stu-id="2c8b5-140">NOTES</span></span>

## <span data-ttu-id="2c8b5-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c8b5-141">RELATED LINKS</span></span>
