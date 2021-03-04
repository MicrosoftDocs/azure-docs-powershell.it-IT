---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: ed06852e2ce0342502d01bd7f5ae17c0c3b8f4e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953293"
---
# <span data-ttu-id="d87c7-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d87c7-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="d87c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d87c7-102">SYNOPSIS</span></span>
<span data-ttu-id="d87c7-103">Elimina l'istanza di Azure Site Recovery Fabric specificata dal vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d87c7-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="d87c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d87c7-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d87c7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d87c7-105">DESCRIPTION</span></span>
<span data-ttu-id="d87c7-106">Il cmdlet **Remove-AzRecoveryServicesAsrFabric** rimuove l'infrastruttura Azure Site Recovery specificata dal vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d87c7-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="d87c7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d87c7-107">EXAMPLES</span></span>

### <span data-ttu-id="d87c7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d87c7-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="d87c7-109">Avvia l'eliminazione di tessuto specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d87c7-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d87c7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d87c7-110">PARAMETERS</span></span>

### <span data-ttu-id="d87c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d87c7-111">-DefaultProfile</span></span>
<span data-ttu-id="d87c7-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d87c7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d87c7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d87c7-113">-Force</span></span>
<span data-ttu-id="d87c7-114">Forzare l'esecuzione del comando senza visualizzare altri avvisi.</span><span class="sxs-lookup"><span data-stu-id="d87c7-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="d87c7-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d87c7-115">-InputObject</span></span>
<span data-ttu-id="d87c7-116">Oggetto di input per il cmdlet: oggetto tessuto ASR corrispondente alla tessuto da eliminare.</span><span class="sxs-lookup"><span data-stu-id="d87c7-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d87c7-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d87c7-117">-Confirm</span></span>
<span data-ttu-id="d87c7-118">Specificare se è necessaria una conferma.</span><span class="sxs-lookup"><span data-stu-id="d87c7-118">Specify if confirmation is required.</span></span> <span data-ttu-id="d87c7-119">Impostare il valore del parametro confirm su $false per ignorare la conferma.</span><span class="sxs-lookup"><span data-stu-id="d87c7-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="d87c7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d87c7-120">-WhatIf</span></span>
<span data-ttu-id="d87c7-121">Mostra cosa accadrebbe se il cmdlet viene eseguito senza effettivamente eseguirlo.</span><span class="sxs-lookup"><span data-stu-id="d87c7-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="d87c7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d87c7-122">CommonParameters</span></span>
<span data-ttu-id="d87c7-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d87c7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d87c7-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d87c7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d87c7-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="d87c7-125">INPUTS</span></span>

### <span data-ttu-id="d87c7-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d87c7-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="d87c7-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d87c7-127">OUTPUTS</span></span>

### <span data-ttu-id="d87c7-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="d87c7-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d87c7-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="d87c7-129">NOTES</span></span>

## <span data-ttu-id="d87c7-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d87c7-130">RELATED LINKS</span></span>

[<span data-ttu-id="d87c7-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d87c7-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="d87c7-132">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d87c7-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
