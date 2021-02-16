---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178991"
---
# <span data-ttu-id="a11af-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="a11af-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="a11af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a11af-102">SYNOPSIS</span></span>
<span data-ttu-id="a11af-103">Questo comando elenca i punti di inizio e di fine della catena di log ininterrotta dell'elemento di backup specificato.</span><span class="sxs-lookup"><span data-stu-id="a11af-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="a11af-104">Consente di determinare se il periodo di tempo in cui l'utente vuole ripristinare il database di database è valido o meno.</span><span class="sxs-lookup"><span data-stu-id="a11af-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="a11af-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a11af-105">SYNTAX</span></span>

### <span data-ttu-id="a11af-106">NoFilterParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a11af-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a11af-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="a11af-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a11af-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a11af-108">DESCRIPTION</span></span>
<span data-ttu-id="a11af-109">Il cmdlet **Get-AzRecoveryServicesBackupRecoveryLogChain** ottiene i punti di ripristino dell'intervallo di tempo per un elemento di backup di Azure di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="a11af-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="a11af-110">Dopo il backup di un elemento, un **oggetto AzRecoveryServicesBackupRecoveryLogChain** include uno o più intervalli di tempo di recupero.</span><span class="sxs-lookup"><span data-stu-id="a11af-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="a11af-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a11af-111">EXAMPLES</span></span>

### <span data-ttu-id="a11af-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a11af-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="a11af-113">Il primo comando recupera la data di sette giorni fa e quindi la archivia nella $StartDate variabile.</span><span class="sxs-lookup"><span data-stu-id="a11af-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="a11af-114">Il secondo comando ottiene la data odierna e la archivia nella $EndDate variabile.</span><span class="sxs-lookup"><span data-stu-id="a11af-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="a11af-115">Il terzo comando recupera i contenitori di backup AzureWorkload e li archivia nella $Container variabile.</span><span class="sxs-lookup"><span data-stu-id="a11af-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="a11af-116">Il quarto comando ottiene l'elemento di backup e quindi lo condivide nel cmdlet piped come oggetto elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="a11af-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="a11af-117">L'ultimo comando ottiene una matrice di intervalli di tempo dei punti di ripristino per l'elemento in $BackupItem e quindi li archivia nella variabile $RP di recupero.</span><span class="sxs-lookup"><span data-stu-id="a11af-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="a11af-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a11af-118">Example 2</span></span>

<span data-ttu-id="a11af-119">Questo comando elenca i punti di inizio e di fine della catena di log ininterrotta dell'elemento di backup specificato.</span><span class="sxs-lookup"><span data-stu-id="a11af-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="a11af-120">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="a11af-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="a11af-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a11af-121">PARAMETERS</span></span>

### <span data-ttu-id="a11af-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a11af-122">-DefaultProfile</span></span>
<span data-ttu-id="a11af-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a11af-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a11af-124">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a11af-124">-EndDate</span></span>
<span data-ttu-id="a11af-125">Ora di fine dell'intervallo di tempo per cui è necessario recuperare il punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="a11af-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="a11af-126">-Item</span><span class="sxs-lookup"><span data-stu-id="a11af-126">-Item</span></span>
<span data-ttu-id="a11af-127">Oggetto Elemento protetto per cui è necessario recuperare il punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="a11af-127">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="a11af-128">-StartDate</span><span class="sxs-lookup"><span data-stu-id="a11af-128">-StartDate</span></span>
<span data-ttu-id="a11af-129">Ora di inizio dell'intervallo di tempo per cui è necessario recuperare il punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="a11af-129">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="a11af-130">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a11af-130">-VaultId</span></span>
<span data-ttu-id="a11af-131">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a11af-131">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a11af-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a11af-132">CommonParameters</span></span>
<span data-ttu-id="a11af-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a11af-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a11af-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a11af-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a11af-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="a11af-135">INPUTS</span></span>

### <span data-ttu-id="a11af-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="a11af-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="a11af-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a11af-137">System.String</span></span>

## <span data-ttu-id="a11af-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a11af-138">OUTPUTS</span></span>

### <span data-ttu-id="a11af-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="a11af-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="a11af-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="a11af-140">NOTES</span></span>

## <span data-ttu-id="a11af-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a11af-141">RELATED LINKS</span></span>
