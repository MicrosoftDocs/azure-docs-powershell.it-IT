---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: d1c61a611b3e2a90c1aa0b0cd21eebdff99ed04b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965854"
---
# <span data-ttu-id="c7723-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c7723-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="c7723-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7723-102">SYNOPSIS</span></span>
<span data-ttu-id="c7723-103">Rimuove un assembly di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c7723-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="c7723-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7723-104">SYNTAX</span></span>

### <span data-ttu-id="c7723-105">ByIntegrationAccount (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c7723-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7723-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c7723-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7723-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7723-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7723-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c7723-108">DESCRIPTION</span></span>
<span data-ttu-id="c7723-109">Il cmdlet **Remove-AzIntegrationAccountAccountAccount rimuove** un assembly da un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c7723-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="c7723-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7723-110">EXAMPLES</span></span>

### <span data-ttu-id="c7723-111">Esempio 1: Rimuovere un assembly in base ai parametri</span><span class="sxs-lookup"><span data-stu-id="c7723-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="c7723-112">Rimuove l'assembly denominato "sampleAccount" che si trova nell'account di integrazione "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="c7723-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="c7723-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7723-113">PARAMETERS</span></span>

### <span data-ttu-id="c7723-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7723-114">-DefaultProfile</span></span>
<span data-ttu-id="c7723-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7723-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7723-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7723-116">-InputObject</span></span>
<span data-ttu-id="c7723-117">Assembly di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c7723-117">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7723-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c7723-118">-Name</span></span>
<span data-ttu-id="c7723-119">Nome assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c7723-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7723-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="c7723-120">-ParentName</span></span>
<span data-ttu-id="c7723-121">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c7723-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7723-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7723-122">-PassThru</span></span>
<span data-ttu-id="c7723-123">Indica se il comando ha avuto esito positivo o meno.</span><span class="sxs-lookup"><span data-stu-id="c7723-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="c7723-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7723-124">-ResourceGroupName</span></span>
<span data-ttu-id="c7723-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c7723-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7723-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7723-126">-ResourceId</span></span>
<span data-ttu-id="c7723-127">ID di risorsa assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c7723-127">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7723-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7723-128">-Confirm</span></span>
<span data-ttu-id="c7723-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7723-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7723-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7723-130">-WhatIf</span></span>
<span data-ttu-id="c7723-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7723-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7723-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7723-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7723-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7723-133">CommonParameters</span></span>
<span data-ttu-id="c7723-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7723-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7723-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7723-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7723-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="c7723-136">INPUTS</span></span>

### <span data-ttu-id="c7723-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAccount</span><span class="sxs-lookup"><span data-stu-id="c7723-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="c7723-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c7723-138">System.String</span></span>

## <span data-ttu-id="c7723-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7723-139">OUTPUTS</span></span>

### <span data-ttu-id="c7723-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c7723-140">System.Boolean</span></span>

## <span data-ttu-id="c7723-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="c7723-141">NOTES</span></span>

## <span data-ttu-id="c7723-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7723-142">RELATED LINKS</span></span>
