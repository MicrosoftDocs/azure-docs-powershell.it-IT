---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: 8a0fbc09f9c46bea6ac09d75911ac83b68f0e296
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022691"
---
# <span data-ttu-id="16254-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="16254-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="16254-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16254-102">SYNOPSIS</span></span>
<span data-ttu-id="16254-103">Questo comando elenca i punti iniziali e finali della catena di log non interrotta dell'elemento di backup indicato.</span><span class="sxs-lookup"><span data-stu-id="16254-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="16254-104">Usalo per determinare se il temporizzatore, a cui l'utente vuole che venga ripristinato il DB, sia valido o meno.</span><span class="sxs-lookup"><span data-stu-id="16254-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="16254-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16254-105">SYNTAX</span></span>

### <span data-ttu-id="16254-106">NoFilterParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="16254-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16254-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="16254-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16254-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16254-108">DESCRIPTION</span></span>
<span data-ttu-id="16254-109">Il cmdlet **Get-AzRecoveryServicesBackupRecoveryLogChain** ottiene i punti di ripristino dell'intervallo di tempo in tempo per un elemento di backup di Azure supportato.</span><span class="sxs-lookup"><span data-stu-id="16254-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="16254-110">Dopo aver eseguito il backup di un elemento, un oggetto **AzRecoveryServicesBackupRecoveryLogChain** ha uno o più intervalli di tempo di recupero.</span><span class="sxs-lookup"><span data-stu-id="16254-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="16254-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16254-111">EXAMPLES</span></span>

### <span data-ttu-id="16254-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="16254-112">Example 1</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="16254-113">Il primo comando ottiene la data di sette giorni fa e lo archivia nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="16254-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="16254-114">Il secondo comando ottiene la data odierna e lo archivia nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="16254-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="16254-115">Il terzo comando ottiene i contenitori di backup di AzureWorkload e li archivia nella variabile $Containers.</span><span class="sxs-lookup"><span data-stu-id="16254-115">The third command gets AzureWorkload backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="16254-116">Il quarto comando ottiene l'elemento di backup e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="16254-116">The fourth command gets the backup item, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="16254-117">L'ultimo comando ottiene una matrice di intervalli di tempo del punto di ripristino per l'elemento in $BackupItem e quindi li archivia nella variabile $RP.</span><span class="sxs-lookup"><span data-stu-id="16254-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="16254-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16254-118">PARAMETERS</span></span>

### <span data-ttu-id="16254-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16254-119">-DefaultProfile</span></span>
<span data-ttu-id="16254-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16254-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16254-121">-EndDate</span><span class="sxs-lookup"><span data-stu-id="16254-121">-EndDate</span></span>
<span data-ttu-id="16254-122">Ora di fine dell'intervallo di tempo per il quale il punto di ripristino deve essere recuperato</span><span class="sxs-lookup"><span data-stu-id="16254-122">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="16254-123">-Elemento</span><span class="sxs-lookup"><span data-stu-id="16254-123">-Item</span></span>
<span data-ttu-id="16254-124">Oggetto elemento protetto per il quale deve essere recuperato il punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="16254-124">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="16254-125">-StartDate</span><span class="sxs-lookup"><span data-stu-id="16254-125">-StartDate</span></span>
<span data-ttu-id="16254-126">Ora di inizio dell'intervallo di tempo per il quale il punto di ripristino deve essere recuperato</span><span class="sxs-lookup"><span data-stu-id="16254-126">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="16254-127">-VaultId</span><span class="sxs-lookup"><span data-stu-id="16254-127">-VaultId</span></span>
<span data-ttu-id="16254-128">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="16254-128">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="16254-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16254-129">CommonParameters</span></span>
<span data-ttu-id="16254-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16254-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16254-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16254-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16254-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16254-132">INPUTS</span></span>

### <span data-ttu-id="16254-133">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="16254-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="16254-134">System. String</span><span class="sxs-lookup"><span data-stu-id="16254-134">System.String</span></span>

## <span data-ttu-id="16254-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16254-135">OUTPUTS</span></span>

### <span data-ttu-id="16254-136">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="16254-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="16254-137">Note</span><span class="sxs-lookup"><span data-stu-id="16254-137">NOTES</span></span>

## <span data-ttu-id="16254-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16254-138">RELATED LINKS</span></span>
