---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: acd6b0735cb0ecf38ecef3448d02c4349954f405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987123"
---
# <span data-ttu-id="4dd2c-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4dd2c-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="4dd2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dd2c-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd2c-103">Rimuove un piano di servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd2c-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="4dd2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4dd2c-104">SYNTAX</span></span>

### <span data-ttu-id="4dd2c-105">S1</span><span class="sxs-lookup"><span data-stu-id="4dd2c-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dd2c-106">S2</span><span class="sxs-lookup"><span data-stu-id="4dd2c-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dd2c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4dd2c-107">DESCRIPTION</span></span>
<span data-ttu-id="4dd2c-108">Il cmdlet **Remove-AzAppServicePlan** rimuove un piano di servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd2c-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="4dd2c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4dd2c-109">EXAMPLES</span></span>

### <span data-ttu-id="4dd2c-110">Esempio 1: Rimuovere un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="4dd2c-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="4dd2c-111">Questo comando rimuove il piano di servizio app di Azure denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="4dd2c-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="4dd2c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dd2c-112">PARAMETERS</span></span>

### <span data-ttu-id="4dd2c-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4dd2c-113">-AppServicePlan</span></span>
<span data-ttu-id="4dd2c-114">Oggetto Piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="4dd2c-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="4dd2c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4dd2c-115">-AsJob</span></span>
<span data-ttu-id="4dd2c-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4dd2c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4dd2c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd2c-117">-DefaultProfile</span></span>
<span data-ttu-id="4dd2c-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd2c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dd2c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4dd2c-119">-Force</span></span>
<span data-ttu-id="4dd2c-120">Opzione Rimuovi forzatamente</span><span class="sxs-lookup"><span data-stu-id="4dd2c-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="4dd2c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4dd2c-121">-Name</span></span>
<span data-ttu-id="4dd2c-122">Nome del piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="4dd2c-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="4dd2c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dd2c-123">-ResourceGroupName</span></span>
<span data-ttu-id="4dd2c-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4dd2c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="4dd2c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4dd2c-125">-Confirm</span></span>
<span data-ttu-id="4dd2c-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dd2c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dd2c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dd2c-127">-WhatIf</span></span>
<span data-ttu-id="4dd2c-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4dd2c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dd2c-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4dd2c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dd2c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd2c-130">CommonParameters</span></span>
<span data-ttu-id="4dd2c-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dd2c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd2c-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dd2c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd2c-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="4dd2c-133">INPUTS</span></span>

### <span data-ttu-id="4dd2c-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4dd2c-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="4dd2c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4dd2c-135">OUTPUTS</span></span>

### <span data-ttu-id="4dd2c-136">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4dd2c-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="4dd2c-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="4dd2c-137">NOTES</span></span>

## <span data-ttu-id="4dd2c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4dd2c-138">RELATED LINKS</span></span>

[<span data-ttu-id="4dd2c-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4dd2c-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="4dd2c-140">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4dd2c-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="4dd2c-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4dd2c-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


