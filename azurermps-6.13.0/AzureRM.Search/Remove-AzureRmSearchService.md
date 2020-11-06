---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/remove-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
ms.openlocfilehash: c558a5d7228253e0a76b0d47fb21f581b4e06f11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519221"
---
# <span data-ttu-id="73877-101">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="73877-101">Remove-AzureRmSearchService</span></span>

## <span data-ttu-id="73877-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73877-102">SYNOPSIS</span></span>
<span data-ttu-id="73877-103">Rimuovere un servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="73877-103">Remove an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73877-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73877-104">SYNTAX</span></span>

### <span data-ttu-id="73877-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="73877-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73877-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73877-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73877-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73877-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSearchService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73877-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73877-108">DESCRIPTION</span></span>
<span data-ttu-id="73877-109">Il cmdlet **Remove-AzureRmSearchService** rimuove un servizio di ricerca di Azure con parametri specificato.</span><span class="sxs-lookup"><span data-stu-id="73877-109">The **Remove-AzureRmSearchService** cmdlet removes an Azure Search service with specified paramters.</span></span>

## <span data-ttu-id="73877-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73877-110">EXAMPLES</span></span>

### <span data-ttu-id="73877-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="73877-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="73877-112">Nell'esempio viene rimosso un servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="73877-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="73877-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73877-113">PARAMETERS</span></span>

### <span data-ttu-id="73877-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73877-114">-DefaultProfile</span></span>
<span data-ttu-id="73877-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73877-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73877-116">-Force</span><span class="sxs-lookup"><span data-stu-id="73877-116">-Force</span></span>
<span data-ttu-id="73877-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="73877-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="73877-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73877-118">-InputObject</span></span>
<span data-ttu-id="73877-119">Oggetto di input del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="73877-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73877-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="73877-120">-Name</span></span>
<span data-ttu-id="73877-121">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="73877-121">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73877-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73877-122">-PassThru</span></span>
<span data-ttu-id="73877-123">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="73877-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="73877-124">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="73877-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="73877-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73877-125">-ResourceGroupName</span></span>
<span data-ttu-id="73877-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="73877-126">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73877-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73877-127">-ResourceId</span></span>
<span data-ttu-id="73877-128">ID risorsa del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="73877-128">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73877-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="73877-129">-Confirm</span></span>
<span data-ttu-id="73877-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73877-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73877-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73877-131">-WhatIf</span></span>
<span data-ttu-id="73877-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73877-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73877-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73877-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73877-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73877-134">CommonParameters</span></span>
<span data-ttu-id="73877-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73877-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73877-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73877-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73877-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73877-137">INPUTS</span></span>

### <span data-ttu-id="73877-138">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="73877-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="73877-139">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="73877-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="73877-140">System. String</span><span class="sxs-lookup"><span data-stu-id="73877-140">System.String</span></span>

## <span data-ttu-id="73877-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73877-141">OUTPUTS</span></span>

### <span data-ttu-id="73877-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="73877-142">System.Boolean</span></span>

## <span data-ttu-id="73877-143">Note</span><span class="sxs-lookup"><span data-stu-id="73877-143">NOTES</span></span>

## <span data-ttu-id="73877-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73877-144">RELATED LINKS</span></span>

[<span data-ttu-id="73877-145">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="73877-145">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="73877-146">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="73877-146">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="73877-147">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="73877-147">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

