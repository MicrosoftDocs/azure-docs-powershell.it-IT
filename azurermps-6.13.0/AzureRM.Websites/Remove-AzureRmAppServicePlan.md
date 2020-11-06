---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: b97506b8f104859c54c55ee1a937916623f4201d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508923"
---
# <span data-ttu-id="69930-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="69930-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="69930-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69930-102">SYNOPSIS</span></span>
<span data-ttu-id="69930-103">Rimuove un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="69930-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69930-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69930-104">SYNTAX</span></span>

### <span data-ttu-id="69930-105">S1</span><span class="sxs-lookup"><span data-stu-id="69930-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69930-106">S2</span><span class="sxs-lookup"><span data-stu-id="69930-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69930-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69930-107">DESCRIPTION</span></span>
<span data-ttu-id="69930-108">Il cmdlet **Remove-AzureRmAppServicePlan** rimuove un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="69930-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="69930-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69930-109">EXAMPLES</span></span>

### <span data-ttu-id="69930-110">Esempio 1: rimuovere un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="69930-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="69930-111">Questo comando rimuove il piano di servizio app Azure denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="69930-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="69930-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69930-112">PARAMETERS</span></span>

### <span data-ttu-id="69930-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="69930-113">-AppServicePlan</span></span>
<span data-ttu-id="69930-114">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="69930-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="69930-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69930-115">-AsJob</span></span>
<span data-ttu-id="69930-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="69930-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69930-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69930-117">-DefaultProfile</span></span>
<span data-ttu-id="69930-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69930-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69930-119">-Force</span><span class="sxs-lookup"><span data-stu-id="69930-119">-Force</span></span>
<span data-ttu-id="69930-120">Opzione Rimuovi con forza</span><span class="sxs-lookup"><span data-stu-id="69930-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="69930-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="69930-121">-Name</span></span>
<span data-ttu-id="69930-122">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="69930-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="69930-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69930-123">-ResourceGroupName</span></span>
<span data-ttu-id="69930-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="69930-124">Resource Group Name</span></span>

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

### <span data-ttu-id="69930-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="69930-125">-Confirm</span></span>
<span data-ttu-id="69930-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69930-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69930-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69930-127">-WhatIf</span></span>
<span data-ttu-id="69930-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69930-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69930-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69930-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69930-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69930-130">CommonParameters</span></span>
<span data-ttu-id="69930-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69930-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69930-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69930-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69930-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69930-133">INPUTS</span></span>

### <span data-ttu-id="69930-134">Microsoft. Azure. Management. website. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="69930-134">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="69930-135">Parametri: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="69930-135">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="69930-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69930-136">OUTPUTS</span></span>

### <span data-ttu-id="69930-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="69930-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="69930-138">Note</span><span class="sxs-lookup"><span data-stu-id="69930-138">NOTES</span></span>

## <span data-ttu-id="69930-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69930-139">RELATED LINKS</span></span>

[<span data-ttu-id="69930-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="69930-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="69930-141">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="69930-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="69930-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="69930-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


