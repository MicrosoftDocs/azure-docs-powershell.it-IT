---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServiceEnvironment.md
ms.openlocfilehash: 9641c55dd25d8f09d1898bdda37fafa840db0a19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983901"
---
# <span data-ttu-id="41af4-101">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="41af4-101">Get-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="41af4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41af4-102">SYNOPSIS</span></span>
<span data-ttu-id="41af4-103">Ottiene l'ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="41af4-103">Gets App Service Environment.</span></span> <span data-ttu-id="41af4-104">Se è specificato solo gruppo di risorse, verrà restituito un elenco di tipi di risorse del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="41af4-104">If only Resource Group is specified, it will return a list of ASE in the Resource Group.</span></span>

## <span data-ttu-id="41af4-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41af4-105">SYNTAX</span></span>

```
Get-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41af4-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="41af4-106">DESCRIPTION</span></span>
<span data-ttu-id="41af4-107">Il cmdlet **Get-AzAppServiceEnvironment** restituisce i file ASE che corrispondono alla query.</span><span class="sxs-lookup"><span data-stu-id="41af4-107">The **Get-AzAppServiceEnvironment** cmdlet return ASE(s) matching the query.</span></span>

## <span data-ttu-id="41af4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41af4-108">EXAMPLES</span></span>

### <span data-ttu-id="41af4-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="41af4-109">Example 1</span></span>
```powershell
PS C:\> Get-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseName
```

<span data-ttu-id="41af4-110">restituisce uno specifico ambiente del servizio app <MyAseName> denominato in <MyResourceGroup></span><span class="sxs-lookup"><span data-stu-id="41af4-110">Returns a specific App Service Environment named <MyAseName> in <MyResourceGroup></span></span>

## <span data-ttu-id="41af4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41af4-111">PARAMETERS</span></span>

### <span data-ttu-id="41af4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41af4-112">-DefaultProfile</span></span>
<span data-ttu-id="41af4-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41af4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41af4-114">-Name</span><span class="sxs-lookup"><span data-stu-id="41af4-114">-Name</span></span>
<span data-ttu-id="41af4-115">Nome dell'ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="41af4-115">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41af4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41af4-116">-ResourceGroupName</span></span>
<span data-ttu-id="41af4-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="41af4-117">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41af4-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41af4-118">-Confirm</span></span>
<span data-ttu-id="41af4-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41af4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41af4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41af4-120">-WhatIf</span></span>
<span data-ttu-id="41af4-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41af4-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41af4-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41af4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41af4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41af4-123">CommonParameters</span></span>
<span data-ttu-id="41af4-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41af4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41af4-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="41af4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41af4-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="41af4-126">INPUTS</span></span>

### <span data-ttu-id="41af4-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="41af4-127">None</span></span>

## <span data-ttu-id="41af4-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41af4-128">OUTPUTS</span></span>

### <span data-ttu-id="41af4-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="41af4-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment</span></span>

## <span data-ttu-id="41af4-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="41af4-130">NOTES</span></span>

## <span data-ttu-id="41af4-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41af4-131">RELATED LINKS</span></span>

[<span data-ttu-id="41af4-132">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="41af4-132">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="41af4-133">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="41af4-133">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)

[<span data-ttu-id="41af4-134">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="41af4-134">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)