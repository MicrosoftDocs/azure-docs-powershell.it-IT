---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: 3fda360369615c28647769e6bc5aeb0af71e0e35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006173"
---
# <span data-ttu-id="aca48-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="aca48-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="aca48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aca48-102">SYNOPSIS</span></span>
<span data-ttu-id="aca48-103">Elimina un Provider SecurityPartnerProvider di Azure.</span><span class="sxs-lookup"><span data-stu-id="aca48-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="aca48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aca48-104">SYNTAX</span></span>

### <span data-ttu-id="aca48-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="aca48-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aca48-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aca48-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aca48-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aca48-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aca48-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aca48-108">DESCRIPTION</span></span>
<span data-ttu-id="aca48-109">Il cmdlet **Remove-AzSecurityPartnerProvider** elimina un provider di sicurezza di Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="aca48-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="aca48-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aca48-110">EXAMPLES</span></span>

### <span data-ttu-id="aca48-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aca48-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="aca48-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aca48-112">PARAMETERS</span></span>

### <span data-ttu-id="aca48-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aca48-113">-AsJob</span></span>
<span data-ttu-id="aca48-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="aca48-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aca48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aca48-115">-DefaultProfile</span></span>
<span data-ttu-id="aca48-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aca48-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aca48-117">-Force</span><span class="sxs-lookup"><span data-stu-id="aca48-117">-Force</span></span>
<span data-ttu-id="aca48-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="aca48-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="aca48-119">-Name</span><span class="sxs-lookup"><span data-stu-id="aca48-119">-Name</span></span>
<span data-ttu-id="aca48-120">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="aca48-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aca48-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aca48-121">-PassThru</span></span>
<span data-ttu-id="aca48-122">Restituisce un oggetto che rappresenta l'elemento su cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="aca48-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="aca48-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aca48-123">-ResourceGroupName</span></span>
<span data-ttu-id="aca48-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aca48-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aca48-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aca48-125">-ResourceId</span></span>
<span data-ttu-id="aca48-126">ID risorsa securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="aca48-126">The securityPartnerProvider resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aca48-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="aca48-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="aca48-128">Oggetto di input securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="aca48-128">The securityPartnerProvider input object.</span></span>

```yaml
Type: PSSecurityPartnerProvider
Parameter Sets: SecurityPartnerProviderInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aca48-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aca48-129">-Confirm</span></span>
<span data-ttu-id="aca48-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aca48-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aca48-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aca48-131">-WhatIf</span></span>
<span data-ttu-id="aca48-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aca48-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aca48-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aca48-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aca48-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aca48-134">CommonParameters</span></span>
<span data-ttu-id="aca48-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aca48-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aca48-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aca48-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aca48-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="aca48-137">INPUTS</span></span>

### <span data-ttu-id="aca48-138">System.String</span><span class="sxs-lookup"><span data-stu-id="aca48-138">System.String</span></span>

### <span data-ttu-id="aca48-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="aca48-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="aca48-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aca48-140">OUTPUTS</span></span>

### <span data-ttu-id="aca48-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aca48-141">System.Boolean</span></span>

## <span data-ttu-id="aca48-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="aca48-142">NOTES</span></span>

## <span data-ttu-id="aca48-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aca48-143">RELATED LINKS</span></span>
