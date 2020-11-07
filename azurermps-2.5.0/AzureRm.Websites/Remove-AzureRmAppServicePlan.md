---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: e8ce0397a59a72e2960a8e0af978c1b5484c53af
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865716"
---
# <span data-ttu-id="93160-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="93160-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="93160-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93160-102">SYNOPSIS</span></span>
<span data-ttu-id="93160-103">Rimuove un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="93160-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93160-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93160-104">SYNTAX</span></span>

### <span data-ttu-id="93160-105">S1</span><span class="sxs-lookup"><span data-stu-id="93160-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93160-106">S2</span><span class="sxs-lookup"><span data-stu-id="93160-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <AppServicePlan> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93160-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93160-107">DESCRIPTION</span></span>
<span data-ttu-id="93160-108">Il cmdlet **Remove-AzureRmAppServicePlan** rimuove un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="93160-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="93160-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93160-109">EXAMPLES</span></span>

### <span data-ttu-id="93160-110">Esempio 1: rimuovere un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="93160-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="93160-111">Questo comando rimuove il piano di servizio app Azure denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="93160-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="93160-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93160-112">PARAMETERS</span></span>

### <span data-ttu-id="93160-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="93160-113">-AppServicePlan</span></span>
<span data-ttu-id="93160-114">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="93160-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93160-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93160-115">-DefaultProfile</span></span>
<span data-ttu-id="93160-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93160-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93160-117">-Force</span><span class="sxs-lookup"><span data-stu-id="93160-117">-Force</span></span>
<span data-ttu-id="93160-118">Opzione Rimuovi con forza</span><span class="sxs-lookup"><span data-stu-id="93160-118">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93160-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="93160-119">-Name</span></span>
<span data-ttu-id="93160-120">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="93160-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93160-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93160-121">-ResourceGroupName</span></span>
<span data-ttu-id="93160-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="93160-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93160-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="93160-123">-Confirm</span></span>
<span data-ttu-id="93160-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93160-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93160-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93160-125">-WhatIf</span></span>
<span data-ttu-id="93160-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93160-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93160-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93160-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93160-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93160-128">-AsJob</span></span>
<span data-ttu-id="93160-129">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="93160-129">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93160-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93160-130">CommonParameters</span></span>
<span data-ttu-id="93160-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93160-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93160-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93160-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93160-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93160-133">INPUTS</span></span>

### <span data-ttu-id="93160-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="93160-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="93160-135">Il parametro ' AppServicePlan ' accetta il valore di tipo ' ServerFarmWithRichSku ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="93160-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="93160-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93160-136">OUTPUTS</span></span>

### <span data-ttu-id="93160-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="93160-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="93160-138">Note</span><span class="sxs-lookup"><span data-stu-id="93160-138">NOTES</span></span>

## <span data-ttu-id="93160-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93160-139">RELATED LINKS</span></span>

[<span data-ttu-id="93160-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="93160-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="93160-141">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="93160-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="93160-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="93160-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


