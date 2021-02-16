---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208827"
---
# <span data-ttu-id="7c730-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7c730-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="7c730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c730-102">SYNOPSIS</span></span>
<span data-ttu-id="7c730-103">Rimuovere una regola di routing dallo slot.</span><span class="sxs-lookup"><span data-stu-id="7c730-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="7c730-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c730-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c730-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7c730-105">DESCRIPTION</span></span>
<span data-ttu-id="7c730-106">Il cmdlet **Remove-AzWebAppTrafficRouting** rimuove una regola di routing da uno slot Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7c730-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="7c730-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c730-107">EXAMPLES</span></span>

### <span data-ttu-id="7c730-108">Esempio 1: rimuove la regola di routing specifica dallo slot della webapp</span><span class="sxs-lookup"><span data-stu-id="7c730-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="7c730-109">Questo comando rimuove una regola di routing per un determinato slot webapp.</span><span class="sxs-lookup"><span data-stu-id="7c730-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="7c730-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c730-110">PARAMETERS</span></span>

### <span data-ttu-id="7c730-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c730-111">-DefaultProfile</span></span>
<span data-ttu-id="7c730-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c730-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c730-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c730-113">-ResourceGroupName</span></span>
<span data-ttu-id="7c730-114">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="7c730-114">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c730-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="7c730-115">-RuleName</span></span>
<span data-ttu-id="7c730-116">Nome regola</span><span class="sxs-lookup"><span data-stu-id="7c730-116">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c730-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="7c730-117">-WebAppName</span></span>
<span data-ttu-id="7c730-118">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="7c730-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c730-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c730-119">-PassThru</span></span>
<span data-ttu-id="7c730-120">Restituire l'oggetto configurazione della restrizione di accesso.</span><span class="sxs-lookup"><span data-stu-id="7c730-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="7c730-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c730-121">-Confirm</span></span>
<span data-ttu-id="7c730-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c730-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c730-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c730-123">-WhatIf</span></span>
<span data-ttu-id="7c730-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c730-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c730-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c730-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c730-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c730-126">CommonParameters</span></span>
<span data-ttu-id="7c730-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c730-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c730-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7c730-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c730-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="7c730-129">INPUTS</span></span>

### <span data-ttu-id="7c730-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7c730-130">None</span></span>

## <span data-ttu-id="7c730-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c730-131">OUTPUTS</span></span>

### <span data-ttu-id="7c730-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="7c730-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="7c730-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="7c730-133">NOTES</span></span>

## <span data-ttu-id="7c730-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c730-134">RELATED LINKS</span></span>
[<span data-ttu-id="7c730-135">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7c730-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="7c730-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7c730-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="7c730-137">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7c730-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)