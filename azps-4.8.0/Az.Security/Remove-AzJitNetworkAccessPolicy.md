---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 484fa890f672435d0add2ba7b30325d03dab91f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191932"
---
# <span data-ttu-id="4c247-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4c247-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="4c247-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c247-102">SYNOPSIS</span></span>
<span data-ttu-id="4c247-103">Elimina un criterio di accesso alla rete JIT.</span><span class="sxs-lookup"><span data-stu-id="4c247-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="4c247-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c247-104">SYNTAX</span></span>

### <span data-ttu-id="4c247-105">ResourceGroupLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4c247-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c247-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c247-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c247-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="4c247-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c247-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c247-108">DESCRIPTION</span></span>
<span data-ttu-id="4c247-109">Elimina un criterio di accesso alla rete just in time.</span><span class="sxs-lookup"><span data-stu-id="4c247-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="4c247-110">Dopo questa azione, un utente non sarà in grado di richiedere una connessione di rete temporanea sulle VM configurate all'interno dei criteri eliminati.</span><span class="sxs-lookup"><span data-stu-id="4c247-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="4c247-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c247-111">EXAMPLES</span></span>

### <span data-ttu-id="4c247-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4c247-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="4c247-113">Elimina un criterio di accesso alla rete just in time.</span><span class="sxs-lookup"><span data-stu-id="4c247-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="4c247-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c247-114">PARAMETERS</span></span>

### <span data-ttu-id="4c247-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c247-115">-DefaultProfile</span></span>
<span data-ttu-id="4c247-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c247-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c247-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c247-117">-InputObject</span></span>
<span data-ttu-id="4c247-118">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="4c247-118">Input Object.</span></span>

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

### <span data-ttu-id="4c247-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4c247-119">-Location</span></span>
<span data-ttu-id="4c247-120">Posizione.</span><span class="sxs-lookup"><span data-stu-id="4c247-120">Location.</span></span>

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

### <span data-ttu-id="4c247-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c247-121">-Name</span></span>
<span data-ttu-id="4c247-122">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="4c247-122">Resource name.</span></span>

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

### <span data-ttu-id="4c247-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c247-123">-PassThru</span></span>
<span data-ttu-id="4c247-124">Restituirà se l'operazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="4c247-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="4c247-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c247-125">-ResourceGroupName</span></span>
<span data-ttu-id="4c247-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4c247-126">Resource group name.</span></span>

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

### <span data-ttu-id="4c247-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c247-127">-ResourceId</span></span>
<span data-ttu-id="4c247-128">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="4c247-128">Resource ID.</span></span>

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

### <span data-ttu-id="4c247-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4c247-129">-Confirm</span></span>
<span data-ttu-id="4c247-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c247-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c247-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c247-131">-WhatIf</span></span>
<span data-ttu-id="4c247-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c247-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c247-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c247-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c247-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c247-134">CommonParameters</span></span>
<span data-ttu-id="4c247-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c247-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c247-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c247-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c247-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c247-137">INPUTS</span></span>

### <span data-ttu-id="4c247-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4c247-138">System.String</span></span>

### <span data-ttu-id="4c247-139">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4c247-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="4c247-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c247-140">OUTPUTS</span></span>

### <span data-ttu-id="4c247-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c247-141">System.Boolean</span></span>

## <span data-ttu-id="4c247-142">Note</span><span class="sxs-lookup"><span data-stu-id="4c247-142">NOTES</span></span>

## <span data-ttu-id="4c247-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c247-143">RELATED LINKS</span></span>
