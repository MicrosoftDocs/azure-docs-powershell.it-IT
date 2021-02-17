---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 71731c0a6f4f0bb917cb7490c1647add71b9a893
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186614"
---
# <span data-ttu-id="989d3-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="989d3-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="989d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="989d3-102">SYNOPSIS</span></span>
<span data-ttu-id="989d3-103">Interrompe/disabilita la replica per un elemento protetto da replica di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="989d3-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="989d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="989d3-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="989d3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="989d3-105">DESCRIPTION</span></span>
<span data-ttu-id="989d3-106">Il cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItem** disabilita la replica dell'elemento protetto da replica di Azure Site Recovery specificato.</span><span class="sxs-lookup"><span data-stu-id="989d3-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="989d3-107">Questa operazione causa l'interruzione della replica per l'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="989d3-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="989d3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="989d3-108">EXAMPLES</span></span>

### <span data-ttu-id="989d3-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="989d3-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="989d3-110">Avvia l'operazione di disabilitazione della replica per l'elemento protetto da replica specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="989d3-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="989d3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="989d3-111">PARAMETERS</span></span>

### <span data-ttu-id="989d3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="989d3-112">-DefaultProfile</span></span>
<span data-ttu-id="989d3-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="989d3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="989d3-114">-Force</span><span class="sxs-lookup"><span data-stu-id="989d3-114">-Force</span></span>
<span data-ttu-id="989d3-115">Forzare l'esecuzione del comando senza visualizzare altri avvisi.</span><span class="sxs-lookup"><span data-stu-id="989d3-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="989d3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="989d3-116">-InputObject</span></span>
<span data-ttu-id="989d3-117">Oggetto di input per il cmdlet: oggetto elemento protetto da replica ASR corrispondente all'elemento protetto da replica per il quale deve essere disabilitata la replica.</span><span class="sxs-lookup"><span data-stu-id="989d3-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="989d3-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="989d3-118">-WaitForCompletion</span></span>
<span data-ttu-id="989d3-119">Indica che il cmdlet deve attendere il completamento dell'operazione prima di restituire.</span><span class="sxs-lookup"><span data-stu-id="989d3-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="989d3-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="989d3-120">-Confirm</span></span>
<span data-ttu-id="989d3-121">Specificare se è necessaria una conferma.</span><span class="sxs-lookup"><span data-stu-id="989d3-121">Specify if confirmation is required.</span></span> <span data-ttu-id="989d3-122">Impostare il valore del parametro confirm su $false per ignorare la conferma.</span><span class="sxs-lookup"><span data-stu-id="989d3-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="989d3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="989d3-123">-WhatIf</span></span>
<span data-ttu-id="989d3-124">Mostra cosa accadrebbe se il cmdlet viene eseguito senza effettivamente eseguirlo.</span><span class="sxs-lookup"><span data-stu-id="989d3-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="989d3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="989d3-125">CommonParameters</span></span>
<span data-ttu-id="989d3-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="989d3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="989d3-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="989d3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="989d3-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="989d3-128">INPUTS</span></span>

### <span data-ttu-id="989d3-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="989d3-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="989d3-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="989d3-130">OUTPUTS</span></span>

### <span data-ttu-id="989d3-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="989d3-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="989d3-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="989d3-132">NOTES</span></span>

## <span data-ttu-id="989d3-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="989d3-133">RELATED LINKS</span></span>

[<span data-ttu-id="989d3-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="989d3-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="989d3-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="989d3-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="989d3-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="989d3-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
