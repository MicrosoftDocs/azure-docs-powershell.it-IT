---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 423d79a1dddc95fb6d9437cbfc14d6157ccf8d90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208290"
---
# <span data-ttu-id="b80bb-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b80bb-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="b80bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b80bb-102">SYNOPSIS</span></span>
<span data-ttu-id="b80bb-103">Elimina i criteri di accesso di rete JIT.</span><span class="sxs-lookup"><span data-stu-id="b80bb-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="b80bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b80bb-104">SYNTAX</span></span>

### <span data-ttu-id="b80bb-105">ResourceGroupLevelResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b80bb-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b80bb-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b80bb-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b80bb-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b80bb-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b80bb-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b80bb-108">DESCRIPTION</span></span>
<span data-ttu-id="b80bb-109">Elimina i criteri di accesso di rete Just In Time.</span><span class="sxs-lookup"><span data-stu-id="b80bb-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="b80bb-110">Dopo questa azione, un utente non sarà in grado di richiedere una connessione di rete temporanea nelle macchine virtuali configurate all'interno dei criteri eliminati.</span><span class="sxs-lookup"><span data-stu-id="b80bb-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="b80bb-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b80bb-111">EXAMPLES</span></span>

### <span data-ttu-id="b80bb-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b80bb-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="b80bb-113">Elimina i criteri di accesso di rete Just In Time.</span><span class="sxs-lookup"><span data-stu-id="b80bb-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="b80bb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b80bb-114">PARAMETERS</span></span>

### <span data-ttu-id="b80bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b80bb-115">-DefaultProfile</span></span>
<span data-ttu-id="b80bb-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b80bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b80bb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b80bb-117">-InputObject</span></span>
<span data-ttu-id="b80bb-118">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="b80bb-118">Input Object.</span></span>

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

### <span data-ttu-id="b80bb-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b80bb-119">-Location</span></span>
<span data-ttu-id="b80bb-120">Posizione.</span><span class="sxs-lookup"><span data-stu-id="b80bb-120">Location.</span></span>

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

### <span data-ttu-id="b80bb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b80bb-121">-Name</span></span>
<span data-ttu-id="b80bb-122">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b80bb-122">Resource name.</span></span>

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

### <span data-ttu-id="b80bb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b80bb-123">-PassThru</span></span>
<span data-ttu-id="b80bb-124">Restituisce se l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="b80bb-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="b80bb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b80bb-125">-ResourceGroupName</span></span>
<span data-ttu-id="b80bb-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b80bb-126">Resource group name.</span></span>

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

### <span data-ttu-id="b80bb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b80bb-127">-ResourceId</span></span>
<span data-ttu-id="b80bb-128">ID risorsa della risorsa Criteri di accesso di rete jit.</span><span class="sxs-lookup"><span data-stu-id="b80bb-128">The resource id of the jit Network Access Policy resource.</span></span>

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

### <span data-ttu-id="b80bb-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b80bb-129">-Confirm</span></span>
<span data-ttu-id="b80bb-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b80bb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b80bb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b80bb-131">-WhatIf</span></span>
<span data-ttu-id="b80bb-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b80bb-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b80bb-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b80bb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b80bb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b80bb-134">CommonParameters</span></span>
<span data-ttu-id="b80bb-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b80bb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b80bb-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b80bb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b80bb-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="b80bb-137">INPUTS</span></span>

### <span data-ttu-id="b80bb-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b80bb-138">System.String</span></span>

### <span data-ttu-id="b80bb-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b80bb-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="b80bb-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b80bb-140">OUTPUTS</span></span>

### <span data-ttu-id="b80bb-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b80bb-141">System.Boolean</span></span>

## <span data-ttu-id="b80bb-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="b80bb-142">NOTES</span></span>

## <span data-ttu-id="b80bb-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b80bb-143">RELATED LINKS</span></span>
