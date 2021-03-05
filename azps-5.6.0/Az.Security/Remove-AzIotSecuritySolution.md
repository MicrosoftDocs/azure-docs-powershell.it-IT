---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: da98138060b0c06e09a56b375c64f530ea8e51f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984093"
---
# <span data-ttu-id="e4558-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="e4558-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="e4558-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4558-102">SYNOPSIS</span></span>
<span data-ttu-id="e4558-103">Eliminare la soluzione di sicurezza IoT</span><span class="sxs-lookup"><span data-stu-id="e4558-103">Delete IoT security solution</span></span>

## <span data-ttu-id="e4558-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4558-104">SYNTAX</span></span>

### <span data-ttu-id="e4558-105">ResourceGroupLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4558-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4558-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4558-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4558-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e4558-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4558-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e4558-108">DESCRIPTION</span></span>
<span data-ttu-id="e4558-109">Il Remove-AzIotSecuritySolution cmdlet elimina una soluzione di sicurezza iot specifica.</span><span class="sxs-lookup"><span data-stu-id="e4558-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="e4558-110">La soluzione di sicurezza IoT raccoglie dati di sicurezza ed eventi dai dispositivi iot e dall'hub iot per prevenire e rilevare le minacce.</span><span class="sxs-lookup"><span data-stu-id="e4558-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="e4558-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4558-111">EXAMPLES</span></span>

### <span data-ttu-id="e4558-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e4558-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="e4558-113">Eliminare la soluzione di sicurezza IoT "MySample" con il gruppo di risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="e4558-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="e4558-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4558-114">PARAMETERS</span></span>

### <span data-ttu-id="e4558-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4558-115">-DefaultProfile</span></span>
<span data-ttu-id="e4558-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4558-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4558-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4558-117">-InputObject</span></span>
<span data-ttu-id="e4558-118">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="e4558-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4558-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e4558-119">-Name</span></span>
<span data-ttu-id="e4558-120">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4558-120">Resource name.</span></span>

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

### <span data-ttu-id="e4558-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4558-121">-PassThru</span></span>
<span data-ttu-id="e4558-122">Restituisce se l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="e4558-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="e4558-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4558-123">-ResourceGroupName</span></span>
<span data-ttu-id="e4558-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4558-124">Resource group name.</span></span>

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

### <span data-ttu-id="e4558-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4558-125">-ResourceId</span></span>
<span data-ttu-id="e4558-126">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="e4558-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="e4558-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4558-127">-Confirm</span></span>
<span data-ttu-id="e4558-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4558-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4558-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4558-129">-WhatIf</span></span>
<span data-ttu-id="e4558-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4558-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4558-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4558-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4558-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4558-132">CommonParameters</span></span>
<span data-ttu-id="e4558-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4558-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4558-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e4558-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4558-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="e4558-135">INPUTS</span></span>

### <span data-ttu-id="e4558-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e4558-136">System.String</span></span>

### <span data-ttu-id="e4558-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="e4558-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="e4558-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4558-138">OUTPUTS</span></span>

### <span data-ttu-id="e4558-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e4558-139">System.Boolean</span></span>

## <span data-ttu-id="e4558-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="e4558-140">NOTES</span></span>

## <span data-ttu-id="e4558-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4558-141">RELATED LINKS</span></span>
