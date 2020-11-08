---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 4dceb934f5cf746908c289c7662de0dc3dae09a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189778"
---
# <span data-ttu-id="d45aa-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d45aa-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="d45aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d45aa-102">SYNOPSIS</span></span>
<span data-ttu-id="d45aa-103">Rimuove un assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d45aa-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="d45aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d45aa-104">SYNTAX</span></span>

### <span data-ttu-id="d45aa-105">ByIntegrationAccount (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d45aa-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d45aa-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d45aa-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d45aa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d45aa-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d45aa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d45aa-108">DESCRIPTION</span></span>
<span data-ttu-id="d45aa-109">Il cmdlet **Remove-AzIntegrationAccountAssembly** rimuove un assembly da un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d45aa-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="d45aa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d45aa-110">EXAMPLES</span></span>

### <span data-ttu-id="d45aa-111">Esempio 1: rimuovere un assembly in base a parametri</span><span class="sxs-lookup"><span data-stu-id="d45aa-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="d45aa-112">Rimuove l'assembly denominato "sampleAssembly" situato nell'account di integrazione "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="d45aa-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="d45aa-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d45aa-113">PARAMETERS</span></span>

### <span data-ttu-id="d45aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d45aa-114">-DefaultProfile</span></span>
<span data-ttu-id="d45aa-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d45aa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d45aa-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d45aa-116">-InputObject</span></span>
<span data-ttu-id="d45aa-117">Un assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d45aa-117">An integration account assembly.</span></span>

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

### <span data-ttu-id="d45aa-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d45aa-118">-Name</span></span>
<span data-ttu-id="d45aa-119">Nome dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d45aa-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="d45aa-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="d45aa-120">-ParentName</span></span>
<span data-ttu-id="d45aa-121">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d45aa-121">The integration account name.</span></span>

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

### <span data-ttu-id="d45aa-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d45aa-122">-PassThru</span></span>
<span data-ttu-id="d45aa-123">Restituirà se il comando ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d45aa-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="d45aa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d45aa-124">-ResourceGroupName</span></span>
<span data-ttu-id="d45aa-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d45aa-125">The resource group name.</span></span>

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

### <span data-ttu-id="d45aa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d45aa-126">-ResourceId</span></span>
<span data-ttu-id="d45aa-127">ID risorsa dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d45aa-127">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="d45aa-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d45aa-128">-Confirm</span></span>
<span data-ttu-id="d45aa-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d45aa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d45aa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d45aa-130">-WhatIf</span></span>
<span data-ttu-id="d45aa-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d45aa-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d45aa-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d45aa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d45aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d45aa-133">CommonParameters</span></span>
<span data-ttu-id="d45aa-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d45aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d45aa-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d45aa-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d45aa-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d45aa-136">INPUTS</span></span>

### <span data-ttu-id="d45aa-137">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d45aa-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="d45aa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d45aa-138">System.String</span></span>

## <span data-ttu-id="d45aa-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d45aa-139">OUTPUTS</span></span>

### <span data-ttu-id="d45aa-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d45aa-140">System.Boolean</span></span>

## <span data-ttu-id="d45aa-141">Note</span><span class="sxs-lookup"><span data-stu-id="d45aa-141">NOTES</span></span>

## <span data-ttu-id="d45aa-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d45aa-142">RELATED LINKS</span></span>