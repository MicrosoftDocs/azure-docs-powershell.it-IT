---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 6041973d4bab91310ed213d461cf97db9cc5e720
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993494"
---
# <span data-ttu-id="22dc0-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="22dc0-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="22dc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="22dc0-103">Aggiorna il mapping di rete di Azure Site Recovery specificato.</span><span class="sxs-lookup"><span data-stu-id="22dc0-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="22dc0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22dc0-104">SYNTAX</span></span>

### <span data-ttu-id="22dc0-105">ByNetworkObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22dc0-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22dc0-106">ById</span><span class="sxs-lookup"><span data-stu-id="22dc0-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22dc0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="22dc0-107">DESCRIPTION</span></span>
<span data-ttu-id="22dc0-108">Il cmdlet **Update-AzRecoveryServicesAsrNetworkMapping aggiorna** il mapping di rete di Azure Site Recovery specificato.</span><span class="sxs-lookup"><span data-stu-id="22dc0-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="22dc0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22dc0-109">EXAMPLES</span></span>

### <span data-ttu-id="22dc0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22dc0-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="22dc0-111">Avvia l'operazione di aggiornamento della mappatura di rete usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="22dc0-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="22dc0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22dc0-112">PARAMETERS</span></span>

### <span data-ttu-id="22dc0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22dc0-113">-DefaultProfile</span></span>
<span data-ttu-id="22dc0-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22dc0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="22dc0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22dc0-115">-InputObject</span></span>
<span data-ttu-id="22dc0-116">Oggetto di input: specifica l'oggetto mapping di rete ASR corrispondente alla mappatura di rete ASR da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="22dc0-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="22dc0-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="22dc0-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="22dc0-118">Specifica l'ID di rete Azure di ripristino per il mapping di rete.</span><span class="sxs-lookup"><span data-stu-id="22dc0-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc0-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="22dc0-119">-RecoveryNetwork</span></span>
<span data-ttu-id="22dc0-120">Specifica l'oggetto di rete di recupero per il mapping di rete.</span><span class="sxs-lookup"><span data-stu-id="22dc0-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22dc0-121">-Confirm</span></span>
<span data-ttu-id="22dc0-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22dc0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22dc0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22dc0-123">-WhatIf</span></span>
<span data-ttu-id="22dc0-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22dc0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22dc0-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22dc0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22dc0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22dc0-126">CommonParameters</span></span>
<span data-ttu-id="22dc0-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22dc0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22dc0-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="22dc0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22dc0-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="22dc0-129">INPUTS</span></span>

### <span data-ttu-id="22dc0-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="22dc0-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="22dc0-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22dc0-131">OUTPUTS</span></span>

### <span data-ttu-id="22dc0-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="22dc0-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="22dc0-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="22dc0-133">NOTES</span></span>

## <span data-ttu-id="22dc0-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22dc0-134">RELATED LINKS</span></span>
