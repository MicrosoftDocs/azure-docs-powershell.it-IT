---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: a5ac137692c8945ba58e848ccca530bd4bc99ed2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020593"
---
# <span data-ttu-id="beac2-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="beac2-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="beac2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="beac2-102">SYNOPSIS</span></span>
<span data-ttu-id="beac2-103">Rimuove i dischi in elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="beac2-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="beac2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="beac2-104">SYNTAX</span></span>

### <span data-ttu-id="beac2-105">AzureToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="beac2-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="beac2-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="beac2-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="beac2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="beac2-107">DESCRIPTION</span></span>
<span data-ttu-id="beac2-108">Il cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** rimuove il disco dall'elemento protetto da replica ASR.</span><span class="sxs-lookup"><span data-stu-id="beac2-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="beac2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="beac2-109">EXAMPLES</span></span>

### <span data-ttu-id="beac2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="beac2-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="beac2-111">Avviare l'operazione per rimuovere il disco specificato dalla protezione VM per il disco non gestito.</span><span class="sxs-lookup"><span data-stu-id="beac2-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="beac2-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="beac2-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="beac2-113">Avviare l'operazione per rimuovere il disco specificato dalla protezione VM per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="beac2-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="beac2-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="beac2-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="beac2-115">Avvia l'operazione per rimuovere il disco specificato e restituisce il processo ASR usato per tenere traccia dell'operazione Rimuovi disco protetto.</span><span class="sxs-lookup"><span data-stu-id="beac2-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="beac2-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="beac2-116">PARAMETERS</span></span>

### <span data-ttu-id="beac2-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="beac2-117">-Confirm</span></span>
<span data-ttu-id="beac2-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="beac2-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beac2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beac2-119">-DefaultProfile</span></span>
<span data-ttu-id="beac2-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="beac2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beac2-121">-DiskID</span><span class="sxs-lookup"><span data-stu-id="beac2-121">-DiskId</span></span>
<span data-ttu-id="beac2-122">Specifica l'elenco di ID disco gestiti.</span><span class="sxs-lookup"><span data-stu-id="beac2-122">Specifies the list of managed disk Ids.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beac2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="beac2-123">-InputObject</span></span>
<span data-ttu-id="beac2-124">L'oggetto di input per il cmdlet: l'oggetto elemento protetto della replica ASR che corrisponde al disco da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="beac2-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="beac2-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="beac2-125">-VhdUri</span></span>
<span data-ttu-id="beac2-126">Specifica l'elenco di URI VHD.</span><span class="sxs-lookup"><span data-stu-id="beac2-126">Specifies the list of vhd Uri's.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beac2-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="beac2-127">-WaitForCompletion</span></span>
<span data-ttu-id="beac2-128">Attendere il completamento</span><span class="sxs-lookup"><span data-stu-id="beac2-128">Wait For Completion</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beac2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beac2-129">-WhatIf</span></span>
<span data-ttu-id="beac2-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="beac2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beac2-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="beac2-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beac2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beac2-132">CommonParameters</span></span>
<span data-ttu-id="beac2-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beac2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beac2-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="beac2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beac2-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="beac2-135">INPUTS</span></span>

### <span data-ttu-id="beac2-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="beac2-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="beac2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="beac2-137">OUTPUTS</span></span>

### <span data-ttu-id="beac2-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="beac2-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="beac2-139">Note</span><span class="sxs-lookup"><span data-stu-id="beac2-139">NOTES</span></span>

## <span data-ttu-id="beac2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="beac2-140">RELATED LINKS</span></span>
