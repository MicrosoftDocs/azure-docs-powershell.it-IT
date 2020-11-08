---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: a316a59492034f0effd2d233ce386cbd6a256c75
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201468"
---
# <span data-ttu-id="063e1-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="063e1-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="063e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="063e1-102">SYNOPSIS</span></span>
<span data-ttu-id="063e1-103">Aggiorna i criteri di accesso alla rete JIT.</span><span class="sxs-lookup"><span data-stu-id="063e1-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="063e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="063e1-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="063e1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="063e1-105">DESCRIPTION</span></span>
<span data-ttu-id="063e1-106">Aggiorna i criteri di accesso alla rete JIT.</span><span class="sxs-lookup"><span data-stu-id="063e1-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="063e1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="063e1-107">EXAMPLES</span></span>

### <span data-ttu-id="063e1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="063e1-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="063e1-109">Aggiorna un criterio di accesso alla rete JIT con le nuove regole VM.</span><span class="sxs-lookup"><span data-stu-id="063e1-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="063e1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="063e1-110">PARAMETERS</span></span>

### <span data-ttu-id="063e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="063e1-111">-DefaultProfile</span></span>
<span data-ttu-id="063e1-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="063e1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="063e1-113">-Tipo</span><span class="sxs-lookup"><span data-stu-id="063e1-113">-Kind</span></span>
<span data-ttu-id="063e1-114">Tipo.</span><span class="sxs-lookup"><span data-stu-id="063e1-114">Kind.</span></span>

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

### <span data-ttu-id="063e1-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="063e1-115">-Location</span></span>
<span data-ttu-id="063e1-116">Posizione.</span><span class="sxs-lookup"><span data-stu-id="063e1-116">Location.</span></span>

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

### <span data-ttu-id="063e1-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="063e1-117">-Name</span></span>
<span data-ttu-id="063e1-118">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="063e1-118">Resource name.</span></span>

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

### <span data-ttu-id="063e1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="063e1-119">-ResourceGroupName</span></span>
<span data-ttu-id="063e1-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="063e1-120">Resource group name.</span></span>

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

### <span data-ttu-id="063e1-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="063e1-121">-VirtualMachine</span></span>
<span data-ttu-id="063e1-122">Macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="063e1-122">Virtual Machines.</span></span>

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

### <span data-ttu-id="063e1-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="063e1-123">-Confirm</span></span>
<span data-ttu-id="063e1-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="063e1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="063e1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="063e1-125">-WhatIf</span></span>
<span data-ttu-id="063e1-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="063e1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="063e1-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="063e1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="063e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="063e1-128">CommonParameters</span></span>
<span data-ttu-id="063e1-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="063e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="063e1-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="063e1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="063e1-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="063e1-131">INPUTS</span></span>

### <span data-ttu-id="063e1-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="063e1-132">None</span></span>

## <span data-ttu-id="063e1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="063e1-133">OUTPUTS</span></span>

### <span data-ttu-id="063e1-134">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="063e1-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="063e1-135">Note</span><span class="sxs-lookup"><span data-stu-id="063e1-135">NOTES</span></span>

## <span data-ttu-id="063e1-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="063e1-136">RELATED LINKS</span></span>
