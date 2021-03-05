---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: 1f69ba390d0cdf3184b876147984c10e79ed423a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987613"
---
# <span data-ttu-id="34d91-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="34d91-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="34d91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34d91-102">SYNOPSIS</span></span>
<span data-ttu-id="34d91-103">Aggiungere il disco per la protezione per una macchina virtuale di Azure già protetta.</span><span class="sxs-lookup"><span data-stu-id="34d91-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="34d91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34d91-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34d91-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="34d91-105">DESCRIPTION</span></span>
<span data-ttu-id="34d91-106">Il cmdlet **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** aggiunge il disco per la protezione per una macchina virtuale di Azure già protetta.</span><span class="sxs-lookup"><span data-stu-id="34d91-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="34d91-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34d91-107">EXAMPLES</span></span>

### <span data-ttu-id="34d91-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="34d91-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="34d91-109">Avviare l'operazione per aggiungere la configurazione del disco specificata per la protezione.</span><span class="sxs-lookup"><span data-stu-id="34d91-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="34d91-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="34d91-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="34d91-111">Avviare l'operazione per aggiungere la configurazione del disco specificata per la protezione. Elemento protetto da replica di input di piping.</span><span class="sxs-lookup"><span data-stu-id="34d91-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="34d91-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34d91-112">PARAMETERS</span></span>

### <span data-ttu-id="34d91-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="34d91-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="34d91-114">Specifica la configurazione del disco da usare per la protezione del disco per lo scenario di ripristino di emergenza da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="34d91-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d91-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d91-115">-DefaultProfile</span></span>
<span data-ttu-id="34d91-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34d91-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34d91-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34d91-117">-InputObject</span></span>
<span data-ttu-id="34d91-118">Oggetto di input per il cmdlet: oggetto elemento protetto da replica ASR corrispondente al nuovo disco da proteggere.</span><span class="sxs-lookup"><span data-stu-id="34d91-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34d91-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="34d91-119">-WaitForCompletion</span></span>
<span data-ttu-id="34d91-120">Attendi completamento</span><span class="sxs-lookup"><span data-stu-id="34d91-120">Wait For Completion</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d91-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34d91-121">-Confirm</span></span>
<span data-ttu-id="34d91-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34d91-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d91-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34d91-123">-WhatIf</span></span>
<span data-ttu-id="34d91-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34d91-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34d91-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34d91-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d91-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d91-126">CommonParameters</span></span>
<span data-ttu-id="34d91-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34d91-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d91-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34d91-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d91-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="34d91-129">INPUTS</span></span>

### <span data-ttu-id="34d91-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="34d91-130">None</span></span>

## <span data-ttu-id="34d91-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34d91-131">OUTPUTS</span></span>

### <span data-ttu-id="34d91-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="34d91-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="34d91-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="34d91-133">NOTES</span></span>

## <span data-ttu-id="34d91-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34d91-134">RELATED LINKS</span></span>
