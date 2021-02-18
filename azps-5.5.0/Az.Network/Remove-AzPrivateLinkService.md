---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 4b95610996aad93144ccaa749c41319cf513ff7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206571"
---
# <span data-ttu-id="476f1-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="476f1-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="476f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="476f1-102">SYNOPSIS</span></span>
<span data-ttu-id="476f1-103">Rimuove un servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="476f1-103">Removes a private link service</span></span>

## <span data-ttu-id="476f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="476f1-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="476f1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="476f1-105">DESCRIPTION</span></span>
<span data-ttu-id="476f1-106">Il cmdlet **Remove-AzPrivateLinkService** rimuove un servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="476f1-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="476f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="476f1-107">EXAMPLES</span></span>

### <span data-ttu-id="476f1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="476f1-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="476f1-109">Questo esempio rimuove un servizio di collegamento privato denominato TestPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="476f1-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="476f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="476f1-110">PARAMETERS</span></span>

### <span data-ttu-id="476f1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="476f1-111">-AsJob</span></span>
<span data-ttu-id="476f1-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="476f1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="476f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="476f1-113">-DefaultProfile</span></span>
<span data-ttu-id="476f1-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="476f1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="476f1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="476f1-115">-Force</span></span>
<span data-ttu-id="476f1-116">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="476f1-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="476f1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="476f1-117">-Name</span></span>
<span data-ttu-id="476f1-118">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="476f1-118">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476f1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="476f1-119">-PassThru</span></span>
<span data-ttu-id="476f1-120">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="476f1-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="476f1-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="476f1-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="476f1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="476f1-122">-ResourceGroupName</span></span>
<span data-ttu-id="476f1-123">Nome del gruppo di risorse del servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="476f1-123">The resource group name of the private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476f1-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="476f1-124">-Confirm</span></span>
<span data-ttu-id="476f1-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="476f1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="476f1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="476f1-126">-WhatIf</span></span>
<span data-ttu-id="476f1-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="476f1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="476f1-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="476f1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="476f1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="476f1-129">CommonParameters</span></span>
<span data-ttu-id="476f1-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="476f1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="476f1-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="476f1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="476f1-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="476f1-132">INPUTS</span></span>

### <span data-ttu-id="476f1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="476f1-133">System.String</span></span>

## <span data-ttu-id="476f1-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="476f1-134">OUTPUTS</span></span>

### <span data-ttu-id="476f1-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="476f1-135">System.Boolean</span></span>

## <span data-ttu-id="476f1-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="476f1-136">NOTES</span></span>

## <span data-ttu-id="476f1-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="476f1-137">RELATED LINKS</span></span>

[<span data-ttu-id="476f1-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="476f1-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="476f1-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="476f1-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)