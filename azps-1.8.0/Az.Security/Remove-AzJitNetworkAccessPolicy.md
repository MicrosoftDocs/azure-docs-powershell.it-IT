---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: b0414b6fbbd4cdb0211b7dee1f85e172c1329c3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677196"
---
# <span data-ttu-id="e8e41-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e8e41-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="e8e41-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8e41-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e41-103">Elimina un criterio di accesso alla rete JIT.</span><span class="sxs-lookup"><span data-stu-id="e8e41-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="e8e41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8e41-104">SYNTAX</span></span>

### <span data-ttu-id="e8e41-105">ResourceGroupLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e8e41-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8e41-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8e41-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8e41-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e8e41-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8e41-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8e41-108">DESCRIPTION</span></span>
<span data-ttu-id="e8e41-109">Elimina un criterio di accesso alla rete just in time.</span><span class="sxs-lookup"><span data-stu-id="e8e41-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="e8e41-110">Dopo questa azione, un utente non sarà in grado di richiedere una connessione di rete temporanea sulle VM configurate all'interno dei criteri eliminati.</span><span class="sxs-lookup"><span data-stu-id="e8e41-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="e8e41-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8e41-111">EXAMPLES</span></span>

### <span data-ttu-id="e8e41-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e8e41-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="e8e41-113">Elimina un criterio di accesso alla rete just in time.</span><span class="sxs-lookup"><span data-stu-id="e8e41-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="e8e41-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8e41-114">PARAMETERS</span></span>

### <span data-ttu-id="e8e41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8e41-115">-DefaultProfile</span></span>
<span data-ttu-id="e8e41-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8e41-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8e41-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8e41-117">-InputObject</span></span>
<span data-ttu-id="e8e41-118">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="e8e41-118">Input Object.</span></span>

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

### <span data-ttu-id="e8e41-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e8e41-119">-Location</span></span>
<span data-ttu-id="e8e41-120">Posizione.</span><span class="sxs-lookup"><span data-stu-id="e8e41-120">Location.</span></span>

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

### <span data-ttu-id="e8e41-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8e41-121">-Name</span></span>
<span data-ttu-id="e8e41-122">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="e8e41-122">Resource name.</span></span>

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

### <span data-ttu-id="e8e41-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8e41-123">-PassThru</span></span>
<span data-ttu-id="e8e41-124">Restituirà se l'operazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="e8e41-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="e8e41-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8e41-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8e41-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e8e41-126">Resource group name.</span></span>

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

### <span data-ttu-id="e8e41-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8e41-127">-ResourceId</span></span>
<span data-ttu-id="e8e41-128">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e8e41-128">Resource ID.</span></span>

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

### <span data-ttu-id="e8e41-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e8e41-129">-Confirm</span></span>
<span data-ttu-id="e8e41-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8e41-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8e41-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8e41-131">-WhatIf</span></span>
<span data-ttu-id="e8e41-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8e41-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8e41-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8e41-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8e41-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8e41-134">CommonParameters</span></span>
<span data-ttu-id="e8e41-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8e41-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8e41-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8e41-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8e41-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8e41-137">INPUTS</span></span>

### <span data-ttu-id="e8e41-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e8e41-138">System.String</span></span>

### <span data-ttu-id="e8e41-139">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e8e41-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="e8e41-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8e41-140">OUTPUTS</span></span>

### <span data-ttu-id="e8e41-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8e41-141">System.Boolean</span></span>

## <span data-ttu-id="e8e41-142">Note</span><span class="sxs-lookup"><span data-stu-id="e8e41-142">NOTES</span></span>

## <span data-ttu-id="e8e41-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8e41-143">RELATED LINKS</span></span>