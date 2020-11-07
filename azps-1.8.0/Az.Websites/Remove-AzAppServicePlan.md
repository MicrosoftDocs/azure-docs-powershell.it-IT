---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: f541ac58fe8512d67fab1755cfededc8839388e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676280"
---
# <span data-ttu-id="8fff6-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8fff6-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="8fff6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8fff6-102">SYNOPSIS</span></span>
<span data-ttu-id="8fff6-103">Rimuove un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="8fff6-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="8fff6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8fff6-104">SYNTAX</span></span>

### <span data-ttu-id="8fff6-105">S1</span><span class="sxs-lookup"><span data-stu-id="8fff6-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fff6-106">S2</span><span class="sxs-lookup"><span data-stu-id="8fff6-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fff6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fff6-107">DESCRIPTION</span></span>
<span data-ttu-id="8fff6-108">Il cmdlet **Remove-AzAppServicePlan** rimuove un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="8fff6-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="8fff6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8fff6-109">EXAMPLES</span></span>

### <span data-ttu-id="8fff6-110">Esempio 1: rimuovere un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="8fff6-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="8fff6-111">Questo comando rimuove il piano di servizio app Azure denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="8fff6-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="8fff6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8fff6-112">PARAMETERS</span></span>

### <span data-ttu-id="8fff6-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8fff6-113">-AppServicePlan</span></span>
<span data-ttu-id="8fff6-114">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="8fff6-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="8fff6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8fff6-115">-AsJob</span></span>
<span data-ttu-id="8fff6-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8fff6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8fff6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fff6-117">-DefaultProfile</span></span>
<span data-ttu-id="8fff6-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8fff6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fff6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8fff6-119">-Force</span></span>
<span data-ttu-id="8fff6-120">Opzione Rimuovi con forza</span><span class="sxs-lookup"><span data-stu-id="8fff6-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="8fff6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8fff6-121">-Name</span></span>
<span data-ttu-id="8fff6-122">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="8fff6-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="8fff6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fff6-123">-ResourceGroupName</span></span>
<span data-ttu-id="8fff6-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="8fff6-124">Resource Group Name</span></span>

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

### <span data-ttu-id="8fff6-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8fff6-125">-Confirm</span></span>
<span data-ttu-id="8fff6-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fff6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fff6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fff6-127">-WhatIf</span></span>
<span data-ttu-id="8fff6-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8fff6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fff6-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8fff6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fff6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fff6-130">CommonParameters</span></span>
<span data-ttu-id="8fff6-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fff6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fff6-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fff6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fff6-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8fff6-133">INPUTS</span></span>

### <span data-ttu-id="8fff6-134">Microsoft. Azure. Commands. webapps. Models. Web App. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8fff6-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="8fff6-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8fff6-135">OUTPUTS</span></span>

### <span data-ttu-id="8fff6-136">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8fff6-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="8fff6-137">Note</span><span class="sxs-lookup"><span data-stu-id="8fff6-137">NOTES</span></span>

## <span data-ttu-id="8fff6-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8fff6-138">RELATED LINKS</span></span>

[<span data-ttu-id="8fff6-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8fff6-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="8fff6-140">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8fff6-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="8fff6-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8fff6-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


