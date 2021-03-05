---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 0588929d8f45c04275e2d79823ed86c9db787060
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977773"
---
# <span data-ttu-id="e6e47-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e6e47-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="e6e47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6e47-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e47-103">Aggiorna i criteri di accesso di rete JIT.</span><span class="sxs-lookup"><span data-stu-id="e6e47-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="e6e47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6e47-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6e47-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e6e47-105">DESCRIPTION</span></span>
<span data-ttu-id="e6e47-106">Aggiorna i criteri di accesso di rete JIT.</span><span class="sxs-lookup"><span data-stu-id="e6e47-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="e6e47-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6e47-107">EXAMPLES</span></span>

### <span data-ttu-id="e6e47-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e6e47-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="e6e47-109">Aggiorna un criterio di accesso alla rete JIT con nuove regole per le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="e6e47-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="e6e47-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6e47-110">PARAMETERS</span></span>

### <span data-ttu-id="e6e47-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e47-111">-DefaultProfile</span></span>
<span data-ttu-id="e6e47-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e47-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6e47-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="e6e47-113">-Kind</span></span>
<span data-ttu-id="e6e47-114">Tipo di criteri di accesso di rete Jit.</span><span class="sxs-lookup"><span data-stu-id="e6e47-114">Jit Network Access Policy Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e47-115">-Location</span><span class="sxs-lookup"><span data-stu-id="e6e47-115">-Location</span></span>
<span data-ttu-id="e6e47-116">Posizione.</span><span class="sxs-lookup"><span data-stu-id="e6e47-116">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e47-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e6e47-117">-Name</span></span>
<span data-ttu-id="e6e47-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e6e47-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e47-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6e47-119">-ResourceGroupName</span></span>
<span data-ttu-id="e6e47-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e6e47-120">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e47-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e6e47-121">-VirtualMachine</span></span>
<span data-ttu-id="e6e47-122">Macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="e6e47-122">Virtual Machines.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e47-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6e47-123">-Confirm</span></span>
<span data-ttu-id="e6e47-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6e47-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6e47-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6e47-125">-WhatIf</span></span>
<span data-ttu-id="e6e47-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6e47-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6e47-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6e47-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6e47-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e47-128">CommonParameters</span></span>
<span data-ttu-id="e6e47-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6e47-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e47-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e6e47-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e47-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="e6e47-131">INPUTS</span></span>

### <span data-ttu-id="e6e47-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e6e47-132">None</span></span>

## <span data-ttu-id="e6e47-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6e47-133">OUTPUTS</span></span>

### <span data-ttu-id="e6e47-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e6e47-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="e6e47-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="e6e47-135">NOTES</span></span>

## <span data-ttu-id="e6e47-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6e47-136">RELATED LINKS</span></span>
