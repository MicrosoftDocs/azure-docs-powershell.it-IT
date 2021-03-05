---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 1ce172ea2f1851f2f75a95a3037798ca3b3a2bf4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961069"
---
# <span data-ttu-id="ae185-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ae185-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="ae185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae185-102">SYNOPSIS</span></span>
<span data-ttu-id="ae185-103">Rimuove un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="ae185-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="ae185-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae185-104">SYNTAX</span></span>

### <span data-ttu-id="ae185-105">S1</span><span class="sxs-lookup"><span data-stu-id="ae185-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae185-106">S2</span><span class="sxs-lookup"><span data-stu-id="ae185-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae185-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ae185-107">DESCRIPTION</span></span>
<span data-ttu-id="ae185-108">Il cmdlet **Remove-AzWebApp** rimuove un'app Web di Azure fornita dal gruppo di risorse e dal nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="ae185-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="ae185-109">Questo cmdlet, per impostazione predefinita, rimuove anche tutti gli slot e le metriche.</span><span class="sxs-lookup"><span data-stu-id="ae185-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="ae185-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae185-110">EXAMPLES</span></span>

### <span data-ttu-id="ae185-111">Esempio 1: Rimuovere un'app Web</span><span class="sxs-lookup"><span data-stu-id="ae185-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="ae185-112">Questo comando rimuove l'app Web di Azure denominata ContosoSite che appartiene al gruppo di risorse denominato Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="ae185-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ae185-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae185-113">PARAMETERS</span></span>

### <span data-ttu-id="ae185-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae185-114">-AsJob</span></span>
<span data-ttu-id="ae185-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ae185-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae185-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae185-116">-DefaultProfile</span></span>
<span data-ttu-id="ae185-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae185-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae185-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ae185-118">-Force</span></span>
<span data-ttu-id="ae185-119">Opzione Rimuovi forzatamente</span><span class="sxs-lookup"><span data-stu-id="ae185-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="ae185-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ae185-120">-Name</span></span>
<span data-ttu-id="ae185-121">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="ae185-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae185-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae185-122">-ResourceGroupName</span></span>
<span data-ttu-id="ae185-123">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ae185-123">Resource Group Name</span></span>

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

### <span data-ttu-id="ae185-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ae185-124">-WebApp</span></span>
<span data-ttu-id="ae185-125">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="ae185-125">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae185-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae185-126">-Confirm</span></span>
<span data-ttu-id="ae185-127">Chiede conferma prima di eseguire il cmdlet. Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae185-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae185-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae185-128">-WhatIf</span></span>
<span data-ttu-id="ae185-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae185-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae185-130">Il cmdlet non viene eseguito. Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae185-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae185-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae185-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae185-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae185-132">CommonParameters</span></span>
<span data-ttu-id="ae185-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae185-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae185-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae185-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae185-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="ae185-135">INPUTS</span></span>

### <span data-ttu-id="ae185-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ae185-136">System.String</span></span>

### <span data-ttu-id="ae185-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ae185-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ae185-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae185-138">OUTPUTS</span></span>

### <span data-ttu-id="ae185-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="ae185-139">System.Void</span></span>

## <span data-ttu-id="ae185-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="ae185-140">NOTES</span></span>

## <span data-ttu-id="ae185-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae185-141">RELATED LINKS</span></span>

[<span data-ttu-id="ae185-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ae185-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="ae185-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ae185-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="ae185-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ae185-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="ae185-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ae185-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="ae185-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ae185-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


