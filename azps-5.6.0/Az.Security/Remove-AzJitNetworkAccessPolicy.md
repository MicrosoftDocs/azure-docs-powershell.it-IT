---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 7220304c4dbc234a3513d2dfc35e6d71180159e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003086"
---
# <span data-ttu-id="7b169-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7b169-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="7b169-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b169-102">SYNOPSIS</span></span>
<span data-ttu-id="7b169-103">Elimina i criteri di accesso di rete JIT.</span><span class="sxs-lookup"><span data-stu-id="7b169-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="7b169-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b169-104">SYNTAX</span></span>

### <span data-ttu-id="7b169-105">ResourceGroupLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b169-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b169-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b169-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b169-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7b169-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b169-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7b169-108">DESCRIPTION</span></span>
<span data-ttu-id="7b169-109">Elimina i criteri di accesso di rete Just In Time.</span><span class="sxs-lookup"><span data-stu-id="7b169-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="7b169-110">Dopo questa azione, un utente non sarà in grado di richiedere una connessione di rete temporanea nelle macchine virtuali configurate all'interno dei criteri eliminati.</span><span class="sxs-lookup"><span data-stu-id="7b169-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="7b169-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b169-111">EXAMPLES</span></span>

### <span data-ttu-id="7b169-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7b169-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="7b169-113">Elimina i criteri di accesso di rete Just In Time.</span><span class="sxs-lookup"><span data-stu-id="7b169-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="7b169-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b169-114">PARAMETERS</span></span>

### <span data-ttu-id="7b169-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b169-115">-DefaultProfile</span></span>
<span data-ttu-id="7b169-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b169-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b169-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b169-117">-InputObject</span></span>
<span data-ttu-id="7b169-118">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="7b169-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b169-119">-Location</span><span class="sxs-lookup"><span data-stu-id="7b169-119">-Location</span></span>
<span data-ttu-id="7b169-120">Posizione.</span><span class="sxs-lookup"><span data-stu-id="7b169-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b169-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7b169-121">-Name</span></span>
<span data-ttu-id="7b169-122">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7b169-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b169-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b169-123">-PassThru</span></span>
<span data-ttu-id="7b169-124">Restituisce se l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="7b169-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="7b169-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b169-125">-ResourceGroupName</span></span>
<span data-ttu-id="7b169-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7b169-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b169-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b169-127">-ResourceId</span></span>
<span data-ttu-id="7b169-128">ID risorsa della risorsa Criteri di accesso di rete jit.</span><span class="sxs-lookup"><span data-stu-id="7b169-128">The resource id of the jit Network Access Policy resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b169-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b169-129">-Confirm</span></span>
<span data-ttu-id="7b169-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b169-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b169-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b169-131">-WhatIf</span></span>
<span data-ttu-id="7b169-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b169-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b169-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b169-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b169-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b169-134">CommonParameters</span></span>
<span data-ttu-id="7b169-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b169-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b169-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7b169-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b169-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="7b169-137">INPUTS</span></span>

### <span data-ttu-id="7b169-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7b169-138">System.String</span></span>

### <span data-ttu-id="7b169-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7b169-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="7b169-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b169-140">OUTPUTS</span></span>

### <span data-ttu-id="7b169-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7b169-141">System.Boolean</span></span>

## <span data-ttu-id="7b169-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="7b169-142">NOTES</span></span>

## <span data-ttu-id="7b169-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b169-143">RELATED LINKS</span></span>
