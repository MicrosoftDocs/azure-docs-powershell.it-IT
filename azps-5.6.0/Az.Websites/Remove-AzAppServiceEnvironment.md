---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServiceEnvironment.md
ms.openlocfilehash: 73c7a7b76f882678612eb6f2a1fb682637705858
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970078"
---
# <span data-ttu-id="ecdc8-101">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="ecdc8-101">Remove-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="ecdc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecdc8-102">SYNOPSIS</span></span>
<span data-ttu-id="ecdc8-103">Rimuovere l'ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="ecdc8-103">Remove App Service Environment.</span></span>

## <span data-ttu-id="ecdc8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecdc8-104">SYNTAX</span></span>

### <span data-ttu-id="ecdc8-105">InputValuesParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecdc8-105">InputValuesParameterSet</span></span>
```
Remove-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecdc8-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecdc8-106">InputObjectParameterSet</span></span>
```
Remove-AzAppServiceEnvironment [-Force] [-PassThru] [-AsJob] -InputObject <PSAppServiceEnvironment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecdc8-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ecdc8-107">DESCRIPTION</span></span>
<span data-ttu-id="ecdc8-108">Il cmdlet **Remove-AzAppServiceEnvironment** rimuove un ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="ecdc8-108">The **Remove-AzAppServiceEnvironment** cmdlet removes an App Service Environment.</span></span> <span data-ttu-id="ecdc8-109">Prima di eliminare AsE, è necessario eliminare qualsiasi piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="ecdc8-109">Any App Service Plan must be deleted prior to deleting the ASE.</span></span>

## <span data-ttu-id="ecdc8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecdc8-110">EXAMPLES</span></span>

### <span data-ttu-id="ecdc8-111">Esempio 1: Eliminare un ambiente del servizio app</span><span class="sxs-lookup"><span data-stu-id="ecdc8-111">Example 1 : Delete an App Service Environment</span></span>
```powershell
PS C:\> Remove-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseName
```

<span data-ttu-id="ecdc8-112">Eliminare un ambiente del servizio app</span><span class="sxs-lookup"><span data-stu-id="ecdc8-112">Delete an App Service Environment</span></span>

## <span data-ttu-id="ecdc8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecdc8-113">PARAMETERS</span></span>

### <span data-ttu-id="ecdc8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecdc8-114">-AsJob</span></span>
<span data-ttu-id="ecdc8-115">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="ecdc8-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ecdc8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecdc8-116">-DefaultProfile</span></span>
<span data-ttu-id="ecdc8-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecdc8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecdc8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ecdc8-118">-Force</span></span>
<span data-ttu-id="ecdc8-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ecdc8-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ecdc8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecdc8-120">-InputObject</span></span>
<span data-ttu-id="ecdc8-121">Oggetto ambiente del servizio app</span><span class="sxs-lookup"><span data-stu-id="ecdc8-121">The app service environment object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecdc8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ecdc8-122">-Name</span></span>
<span data-ttu-id="ecdc8-123">Nome dell'ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="ecdc8-123">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecdc8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecdc8-124">-PassThru</span></span>
<span data-ttu-id="ecdc8-125">Stato reso.</span><span class="sxs-lookup"><span data-stu-id="ecdc8-125">Return status.</span></span>

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

### <span data-ttu-id="ecdc8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecdc8-126">-ResourceGroupName</span></span>
<span data-ttu-id="ecdc8-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ecdc8-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecdc8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecdc8-128">-Confirm</span></span>
<span data-ttu-id="ecdc8-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecdc8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecdc8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecdc8-130">-WhatIf</span></span>
<span data-ttu-id="ecdc8-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecdc8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecdc8-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecdc8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecdc8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecdc8-133">CommonParameters</span></span>
<span data-ttu-id="ecdc8-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecdc8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecdc8-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ecdc8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecdc8-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="ecdc8-136">INPUTS</span></span>

### <span data-ttu-id="ecdc8-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ecdc8-137">None</span></span>

## <span data-ttu-id="ecdc8-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecdc8-138">OUTPUTS</span></span>

### <span data-ttu-id="ecdc8-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="ecdc8-139">System.Object</span></span>
## <span data-ttu-id="ecdc8-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="ecdc8-140">NOTES</span></span>

## <span data-ttu-id="ecdc8-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecdc8-141">RELATED LINKS</span></span>

[<span data-ttu-id="ecdc8-142">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="ecdc8-142">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="ecdc8-143">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="ecdc8-143">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="ecdc8-144">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="ecdc8-144">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)