---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 83aca2353102b85fd138422f249464b59a8666ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208242"
---
# <span data-ttu-id="a760d-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a760d-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="a760d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a760d-102">SYNOPSIS</span></span>
<span data-ttu-id="a760d-103">Aggiorna i criteri di accesso di rete JIT.</span><span class="sxs-lookup"><span data-stu-id="a760d-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="a760d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a760d-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a760d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a760d-105">DESCRIPTION</span></span>
<span data-ttu-id="a760d-106">Aggiorna i criteri di accesso di rete JIT.</span><span class="sxs-lookup"><span data-stu-id="a760d-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="a760d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a760d-107">EXAMPLES</span></span>

### <span data-ttu-id="a760d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a760d-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="a760d-109">Aggiorna un criterio di accesso alla rete JIT con nuove regole per le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="a760d-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="a760d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a760d-110">PARAMETERS</span></span>

### <span data-ttu-id="a760d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a760d-111">-DefaultProfile</span></span>
<span data-ttu-id="a760d-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a760d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a760d-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="a760d-113">-Kind</span></span>
<span data-ttu-id="a760d-114">Tipo di criteri di accesso di rete Jit.</span><span class="sxs-lookup"><span data-stu-id="a760d-114">Jit Network Access Policy Kind.</span></span>

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

### <span data-ttu-id="a760d-115">-Location</span><span class="sxs-lookup"><span data-stu-id="a760d-115">-Location</span></span>
<span data-ttu-id="a760d-116">Posizione.</span><span class="sxs-lookup"><span data-stu-id="a760d-116">Location.</span></span>

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

### <span data-ttu-id="a760d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a760d-117">-Name</span></span>
<span data-ttu-id="a760d-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a760d-118">Resource name.</span></span>

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

### <span data-ttu-id="a760d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a760d-119">-ResourceGroupName</span></span>
<span data-ttu-id="a760d-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a760d-120">Resource group name.</span></span>

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

### <span data-ttu-id="a760d-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a760d-121">-VirtualMachine</span></span>
<span data-ttu-id="a760d-122">Macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="a760d-122">Virtual Machines.</span></span>

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

### <span data-ttu-id="a760d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a760d-123">-Confirm</span></span>
<span data-ttu-id="a760d-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a760d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a760d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a760d-125">-WhatIf</span></span>
<span data-ttu-id="a760d-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a760d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a760d-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a760d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a760d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a760d-128">CommonParameters</span></span>
<span data-ttu-id="a760d-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a760d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a760d-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a760d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a760d-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="a760d-131">INPUTS</span></span>

### <span data-ttu-id="a760d-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a760d-132">None</span></span>

## <span data-ttu-id="a760d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a760d-133">OUTPUTS</span></span>

### <span data-ttu-id="a760d-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a760d-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="a760d-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="a760d-135">NOTES</span></span>

## <span data-ttu-id="a760d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a760d-136">RELATED LINKS</span></span>
