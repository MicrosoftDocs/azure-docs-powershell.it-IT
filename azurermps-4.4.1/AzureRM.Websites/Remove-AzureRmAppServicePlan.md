---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: d1d07e27a7ad6fb6059cbfc8e4c972b1cedaf7e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521495"
---
# <span data-ttu-id="340de-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="340de-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="340de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="340de-102">SYNOPSIS</span></span>
<span data-ttu-id="340de-103">Rimuove un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="340de-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="340de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="340de-104">SYNTAX</span></span>

### <span data-ttu-id="340de-105">S1</span><span class="sxs-lookup"><span data-stu-id="340de-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="340de-106">S2</span><span class="sxs-lookup"><span data-stu-id="340de-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <ServerFarmWithRichSku>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="340de-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="340de-107">DESCRIPTION</span></span>
<span data-ttu-id="340de-108">Il cmdlet **Remove-AzureRmAppServicePlan** rimuove un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="340de-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="340de-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="340de-109">EXAMPLES</span></span>

### <span data-ttu-id="340de-110">Esempio 1: rimuovere un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="340de-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="340de-111">Questo comando rimuove il piano di servizio app Azure denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="340de-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="340de-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="340de-112">PARAMETERS</span></span>

### <span data-ttu-id="340de-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="340de-113">-AppServicePlan</span></span>
<span data-ttu-id="340de-114">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="340de-114">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="340de-115">-Force</span><span class="sxs-lookup"><span data-stu-id="340de-115">-Force</span></span>
<span data-ttu-id="340de-116">Opzione Rimuovi con forza</span><span class="sxs-lookup"><span data-stu-id="340de-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="340de-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="340de-117">-Name</span></span>
<span data-ttu-id="340de-118">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="340de-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="340de-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="340de-119">-ResourceGroupName</span></span>
<span data-ttu-id="340de-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="340de-120">Resource Group Name</span></span>

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

### <span data-ttu-id="340de-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="340de-121">-Confirm</span></span>
<span data-ttu-id="340de-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="340de-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="340de-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="340de-123">-WhatIf</span></span>
<span data-ttu-id="340de-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="340de-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="340de-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="340de-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="340de-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="340de-126">-DefaultProfile</span></span>
<span data-ttu-id="340de-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="340de-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="340de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="340de-128">CommonParameters</span></span>
<span data-ttu-id="340de-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="340de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="340de-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="340de-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="340de-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="340de-131">INPUTS</span></span>

### <span data-ttu-id="340de-132">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="340de-132">ServerFarmWithRichSku</span></span>
<span data-ttu-id="340de-133">Il parametro ' AppServicePlan ' accetta il valore di tipo ' ServerFarmWithRichSku ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="340de-133">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="340de-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="340de-134">OUTPUTS</span></span>

### <span data-ttu-id="340de-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="340de-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="340de-136">Note</span><span class="sxs-lookup"><span data-stu-id="340de-136">NOTES</span></span>

## <span data-ttu-id="340de-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="340de-137">RELATED LINKS</span></span>

[<span data-ttu-id="340de-138">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="340de-138">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="340de-139">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="340de-139">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="340de-140">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="340de-140">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


