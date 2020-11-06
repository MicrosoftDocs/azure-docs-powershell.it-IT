---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 72e3cf48f112c5e9bb07a8f7eb57dfe3d4c9ee07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513436"
---
# <span data-ttu-id="5ad09-101">Set-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5ad09-101">Set-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="5ad09-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ad09-102">SYNOPSIS</span></span>
<span data-ttu-id="5ad09-103">Aggiorna i criteri di accesso alla rete JIT.</span><span class="sxs-lookup"><span data-stu-id="5ad09-103">Updates JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ad09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ad09-104">SYNTAX</span></span>

```
Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ad09-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ad09-105">DESCRIPTION</span></span>
<span data-ttu-id="5ad09-106">Aggiorna i criteri di accesso alla rete JIT.</span><span class="sxs-lookup"><span data-stu-id="5ad09-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="5ad09-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ad09-107">EXAMPLES</span></span>

### <span data-ttu-id="5ad09-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5ad09-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="5ad09-109">Aggiorna un criterio di accesso alla rete JIT con le nuove regole VM.</span><span class="sxs-lookup"><span data-stu-id="5ad09-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="5ad09-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ad09-110">PARAMETERS</span></span>

### <span data-ttu-id="5ad09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ad09-111">-DefaultProfile</span></span>
<span data-ttu-id="5ad09-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ad09-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad09-113">-Tipo</span><span class="sxs-lookup"><span data-stu-id="5ad09-113">-Kind</span></span>
<span data-ttu-id="5ad09-114">Tipo.</span><span class="sxs-lookup"><span data-stu-id="5ad09-114">Kind.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad09-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5ad09-115">-Location</span></span>
<span data-ttu-id="5ad09-116">Posizione.</span><span class="sxs-lookup"><span data-stu-id="5ad09-116">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad09-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ad09-117">-Name</span></span>
<span data-ttu-id="5ad09-118">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="5ad09-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad09-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ad09-119">-ResourceGroupName</span></span>
<span data-ttu-id="5ad09-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5ad09-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad09-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5ad09-121">-VirtualMachine</span></span>
<span data-ttu-id="5ad09-122">Macchine virutal.</span><span class="sxs-lookup"><span data-stu-id="5ad09-122">Virutal Machines.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad09-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5ad09-123">-Confirm</span></span>
<span data-ttu-id="5ad09-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ad09-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ad09-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ad09-125">-WhatIf</span></span>
<span data-ttu-id="5ad09-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ad09-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ad09-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ad09-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ad09-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ad09-128">CommonParameters</span></span>
<span data-ttu-id="5ad09-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ad09-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ad09-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ad09-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ad09-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ad09-131">INPUTS</span></span>

### <span data-ttu-id="5ad09-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5ad09-132">System.String</span></span>
<span data-ttu-id="5ad09-133">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyVirtualMachine []</span><span class="sxs-lookup"><span data-stu-id="5ad09-133">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]</span></span>

## <span data-ttu-id="5ad09-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ad09-134">OUTPUTS</span></span>

### <span data-ttu-id="5ad09-135">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5ad09-135">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="5ad09-136">Note</span><span class="sxs-lookup"><span data-stu-id="5ad09-136">NOTES</span></span>

## <span data-ttu-id="5ad09-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ad09-137">RELATED LINKS</span></span>
