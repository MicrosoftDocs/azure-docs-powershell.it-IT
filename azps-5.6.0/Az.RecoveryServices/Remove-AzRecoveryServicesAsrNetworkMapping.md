---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: bb80bebc8c1a5dccbeedf4abd277891c3b2e9de7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953278"
---
# <span data-ttu-id="9d10e-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9d10e-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="9d10e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d10e-102">SYNOPSIS</span></span>
<span data-ttu-id="9d10e-103">Elimina il mapping di rete ASR specificato dal vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9d10e-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="9d10e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d10e-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d10e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9d10e-105">DESCRIPTION</span></span>
<span data-ttu-id="9d10e-106">Il cmdlet **Remove-AzRecoveryServicesAsrNetworkMapping** elimina il mapping di rete ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="9d10e-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="9d10e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d10e-107">EXAMPLES</span></span>

### <span data-ttu-id="9d10e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9d10e-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="9d10e-109">Avvia l'eliminazione del mapping di rete ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9d10e-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9d10e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d10e-110">PARAMETERS</span></span>

### <span data-ttu-id="9d10e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d10e-111">-DefaultProfile</span></span>
<span data-ttu-id="9d10e-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d10e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9d10e-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d10e-113">-InputObject</span></span>
<span data-ttu-id="9d10e-114">Oggetto di input per il cmdlet: oggetto di mapping di rete ASR corrispondente al mapping di rete ASR da eliminare.</span><span class="sxs-lookup"><span data-stu-id="9d10e-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d10e-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d10e-115">-Confirm</span></span>
<span data-ttu-id="9d10e-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d10e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d10e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d10e-117">-WhatIf</span></span>
<span data-ttu-id="9d10e-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d10e-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d10e-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d10e-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d10e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d10e-120">CommonParameters</span></span>
<span data-ttu-id="9d10e-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d10e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d10e-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9d10e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d10e-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="9d10e-123">INPUTS</span></span>

### <span data-ttu-id="9d10e-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9d10e-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="9d10e-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d10e-125">OUTPUTS</span></span>

### <span data-ttu-id="9d10e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="9d10e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9d10e-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="9d10e-127">NOTES</span></span>

## <span data-ttu-id="9d10e-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d10e-128">RELATED LINKS</span></span>

[<span data-ttu-id="9d10e-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9d10e-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="9d10e-130">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9d10e-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
