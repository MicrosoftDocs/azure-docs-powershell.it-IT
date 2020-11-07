---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: 3d0e3ad30df71700eb83938181ed86a97a77528a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861877"
---
# <span data-ttu-id="1a2df-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1a2df-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="1a2df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a2df-102">SYNOPSIS</span></span>
<span data-ttu-id="1a2df-103">Rimuove un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="1a2df-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="1a2df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a2df-104">SYNTAX</span></span>

### <span data-ttu-id="1a2df-105">S1</span><span class="sxs-lookup"><span data-stu-id="1a2df-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a2df-106">S2</span><span class="sxs-lookup"><span data-stu-id="1a2df-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AppServicePlan] <AppServicePlan> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a2df-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a2df-107">DESCRIPTION</span></span>
<span data-ttu-id="1a2df-108">Il cmdlet **Remove-AzAppServicePlan** rimuove un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="1a2df-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="1a2df-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a2df-109">EXAMPLES</span></span>

### <span data-ttu-id="1a2df-110">Esempio 1: rimuovere un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="1a2df-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="1a2df-111">Questo comando rimuove il piano di servizio app Azure denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="1a2df-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="1a2df-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a2df-112">PARAMETERS</span></span>

### <span data-ttu-id="1a2df-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1a2df-113">-AppServicePlan</span></span>
<span data-ttu-id="1a2df-114">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="1a2df-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="1a2df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a2df-115">-DefaultProfile</span></span>
<span data-ttu-id="1a2df-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a2df-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a2df-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1a2df-117">-Force</span></span>
<span data-ttu-id="1a2df-118">Opzione Rimuovi con forza</span><span class="sxs-lookup"><span data-stu-id="1a2df-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="1a2df-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a2df-119">-Name</span></span>
<span data-ttu-id="1a2df-120">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="1a2df-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="1a2df-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a2df-121">-ResourceGroupName</span></span>
<span data-ttu-id="1a2df-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1a2df-122">Resource Group Name</span></span>

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

### <span data-ttu-id="1a2df-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1a2df-123">-Confirm</span></span>
<span data-ttu-id="1a2df-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a2df-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a2df-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a2df-125">-WhatIf</span></span>
<span data-ttu-id="1a2df-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a2df-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a2df-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a2df-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a2df-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a2df-128">-AsJob</span></span>
<span data-ttu-id="1a2df-129">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1a2df-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a2df-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a2df-130">CommonParameters</span></span>
<span data-ttu-id="1a2df-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a2df-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a2df-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a2df-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a2df-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a2df-133">INPUTS</span></span>

### <span data-ttu-id="1a2df-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="1a2df-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="1a2df-135">Il parametro ' AppServicePlan ' accetta il valore di tipo ' ServerFarmWithRichSku ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1a2df-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="1a2df-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a2df-136">OUTPUTS</span></span>

### <span data-ttu-id="1a2df-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1a2df-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="1a2df-138">Note</span><span class="sxs-lookup"><span data-stu-id="1a2df-138">NOTES</span></span>

## <span data-ttu-id="1a2df-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a2df-139">RELATED LINKS</span></span>

[<span data-ttu-id="1a2df-140">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1a2df-140">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="1a2df-141">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1a2df-141">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="1a2df-142">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1a2df-142">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


