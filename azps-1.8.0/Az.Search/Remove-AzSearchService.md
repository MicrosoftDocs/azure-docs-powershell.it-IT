---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 245cbce2516dcb26502313bcac35dd35b957f94d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677230"
---
# <span data-ttu-id="908cf-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="908cf-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="908cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="908cf-102">SYNOPSIS</span></span>
<span data-ttu-id="908cf-103">Rimuovere un servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="908cf-103">Remove an Azure Search service.</span></span>

## <span data-ttu-id="908cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="908cf-104">SYNTAX</span></span>

### <span data-ttu-id="908cf-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="908cf-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="908cf-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="908cf-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="908cf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="908cf-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="908cf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="908cf-108">DESCRIPTION</span></span>
<span data-ttu-id="908cf-109">Il cmdlet **Remove-AzSearchService** rimuove un servizio di ricerca di Azure con parametri specificato.</span><span class="sxs-lookup"><span data-stu-id="908cf-109">The **Remove-AzSearchService** cmdlet removes an Azure Search service with specified paramters.</span></span>

## <span data-ttu-id="908cf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="908cf-110">EXAMPLES</span></span>

### <span data-ttu-id="908cf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="908cf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="908cf-112">Nell'esempio viene rimosso un servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="908cf-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="908cf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="908cf-113">PARAMETERS</span></span>

### <span data-ttu-id="908cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="908cf-114">-DefaultProfile</span></span>
<span data-ttu-id="908cf-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="908cf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="908cf-116">-Force</span><span class="sxs-lookup"><span data-stu-id="908cf-116">-Force</span></span>
<span data-ttu-id="908cf-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="908cf-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="908cf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="908cf-118">-InputObject</span></span>
<span data-ttu-id="908cf-119">Oggetto di input del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="908cf-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="908cf-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="908cf-120">-Name</span></span>
<span data-ttu-id="908cf-121">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="908cf-121">Search Service name.</span></span>

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

### <span data-ttu-id="908cf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="908cf-122">-PassThru</span></span>
<span data-ttu-id="908cf-123">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="908cf-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="908cf-124">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="908cf-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="908cf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="908cf-125">-ResourceGroupName</span></span>
<span data-ttu-id="908cf-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="908cf-126">Resource Group name.</span></span>

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

### <span data-ttu-id="908cf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="908cf-127">-ResourceId</span></span>
<span data-ttu-id="908cf-128">ID risorsa del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="908cf-128">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="908cf-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="908cf-129">-Confirm</span></span>
<span data-ttu-id="908cf-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="908cf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="908cf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="908cf-131">-WhatIf</span></span>
<span data-ttu-id="908cf-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="908cf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="908cf-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="908cf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="908cf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="908cf-134">CommonParameters</span></span>
<span data-ttu-id="908cf-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="908cf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="908cf-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="908cf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="908cf-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="908cf-137">INPUTS</span></span>

### <span data-ttu-id="908cf-138">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="908cf-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="908cf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="908cf-139">System.String</span></span>

## <span data-ttu-id="908cf-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="908cf-140">OUTPUTS</span></span>

### <span data-ttu-id="908cf-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="908cf-141">System.Boolean</span></span>

## <span data-ttu-id="908cf-142">Note</span><span class="sxs-lookup"><span data-stu-id="908cf-142">NOTES</span></span>

## <span data-ttu-id="908cf-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="908cf-143">RELATED LINKS</span></span>

[<span data-ttu-id="908cf-144">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="908cf-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="908cf-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="908cf-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="908cf-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="908cf-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

