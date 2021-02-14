---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: dfd2cfd20ab11e2e70e03dc3e166c83729ef344a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188695"
---
# <span data-ttu-id="14872-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="14872-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="14872-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14872-102">SYNOPSIS</span></span>
<span data-ttu-id="14872-103">Rimuove un piano di servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="14872-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="14872-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14872-104">SYNTAX</span></span>

### <span data-ttu-id="14872-105">S1</span><span class="sxs-lookup"><span data-stu-id="14872-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14872-106">S2</span><span class="sxs-lookup"><span data-stu-id="14872-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14872-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="14872-107">DESCRIPTION</span></span>
<span data-ttu-id="14872-108">Il cmdlet **Remove-AzAppServicePlan** rimuove un piano di servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="14872-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="14872-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14872-109">EXAMPLES</span></span>

### <span data-ttu-id="14872-110">Esempio 1: Rimuovere un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="14872-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="14872-111">Questo comando rimuove il piano di servizio app di Azure denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="14872-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="14872-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14872-112">PARAMETERS</span></span>

### <span data-ttu-id="14872-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="14872-113">-AppServicePlan</span></span>
<span data-ttu-id="14872-114">Oggetto Piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="14872-114">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14872-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14872-115">-AsJob</span></span>
<span data-ttu-id="14872-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="14872-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14872-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14872-117">-DefaultProfile</span></span>
<span data-ttu-id="14872-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14872-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14872-119">-Force</span><span class="sxs-lookup"><span data-stu-id="14872-119">-Force</span></span>
<span data-ttu-id="14872-120">Opzione Rimuovi forzatamente</span><span class="sxs-lookup"><span data-stu-id="14872-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="14872-121">-Name</span><span class="sxs-lookup"><span data-stu-id="14872-121">-Name</span></span>
<span data-ttu-id="14872-122">Nome del piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="14872-122">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14872-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14872-123">-ResourceGroupName</span></span>
<span data-ttu-id="14872-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="14872-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14872-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14872-125">-Confirm</span></span>
<span data-ttu-id="14872-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14872-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14872-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14872-127">-WhatIf</span></span>
<span data-ttu-id="14872-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14872-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14872-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14872-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14872-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14872-130">CommonParameters</span></span>
<span data-ttu-id="14872-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14872-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14872-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14872-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14872-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="14872-133">INPUTS</span></span>

### <span data-ttu-id="14872-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="14872-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="14872-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14872-135">OUTPUTS</span></span>

### <span data-ttu-id="14872-136">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="14872-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="14872-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="14872-137">NOTES</span></span>

## <span data-ttu-id="14872-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14872-138">RELATED LINKS</span></span>

[<span data-ttu-id="14872-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="14872-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="14872-140">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="14872-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="14872-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="14872-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


