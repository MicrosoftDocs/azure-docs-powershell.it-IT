---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: cca1cc480f529c49f679930d9d88f39f69f6e966
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983789"
---
# <span data-ttu-id="ea2f4-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ea2f4-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="ea2f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea2f4-102">SYNOPSIS</span></span>

## <span data-ttu-id="ea2f4-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea2f4-103">SYNTAX</span></span>

### <span data-ttu-id="ea2f4-104">S1</span><span class="sxs-lookup"><span data-stu-id="ea2f4-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea2f4-105">S2</span><span class="sxs-lookup"><span data-stu-id="ea2f4-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea2f4-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ea2f4-106">DESCRIPTION</span></span>
<span data-ttu-id="ea2f4-107">Il cmdlet **Remove-AzWebAppSlot rimuove** uno slot di Azure Web App a condizione che il gruppo di risorse e il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="ea2f4-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="ea2f4-108">Questo cmdlet, per impostazione predefinita, rimuove anche tutti gli slot e le metriche.</span><span class="sxs-lookup"><span data-stu-id="ea2f4-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="ea2f4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea2f4-109">EXAMPLES</span></span>

### <span data-ttu-id="ea2f4-110">Esempio 1: Rimuovere uno slot per l'app Web</span><span class="sxs-lookup"><span data-stu-id="ea2f4-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="ea2f4-111">Questo comando rimuove lo slot denominato Slot001 associato a Sito Contoso app Web che appartiene al gruppo di risorse denominato Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="ea2f4-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ea2f4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea2f4-112">PARAMETERS</span></span>

### <span data-ttu-id="ea2f4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea2f4-113">-AsJob</span></span>
<span data-ttu-id="ea2f4-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ea2f4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea2f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea2f4-115">-DefaultProfile</span></span>
<span data-ttu-id="ea2f4-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea2f4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea2f4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ea2f4-117">-Force</span></span>
<span data-ttu-id="ea2f4-118">Opzione Rimuovi forzatamente</span><span class="sxs-lookup"><span data-stu-id="ea2f4-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="ea2f4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ea2f4-119">-Name</span></span>
<span data-ttu-id="ea2f4-120">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="ea2f4-120">WebApp Name</span></span>

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

### <span data-ttu-id="ea2f4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea2f4-121">-ResourceGroupName</span></span>
<span data-ttu-id="ea2f4-122">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ea2f4-122">Resource Group Name</span></span>

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

### <span data-ttu-id="ea2f4-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="ea2f4-123">-Slot</span></span>
<span data-ttu-id="ea2f4-124">Nome slot WebApp</span><span class="sxs-lookup"><span data-stu-id="ea2f4-124">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea2f4-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ea2f4-125">-WebApp</span></span>
<span data-ttu-id="ea2f4-126">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="ea2f4-126">WebApp Object</span></span>

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

### <span data-ttu-id="ea2f4-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea2f4-127">-Confirm</span></span>
<span data-ttu-id="ea2f4-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea2f4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea2f4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea2f4-129">-WhatIf</span></span>
<span data-ttu-id="ea2f4-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea2f4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea2f4-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea2f4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea2f4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea2f4-132">CommonParameters</span></span>
<span data-ttu-id="ea2f4-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea2f4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea2f4-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea2f4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea2f4-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="ea2f4-135">INPUTS</span></span>

### <span data-ttu-id="ea2f4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ea2f4-136">System.String</span></span>

### <span data-ttu-id="ea2f4-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ea2f4-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ea2f4-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea2f4-138">OUTPUTS</span></span>

### <span data-ttu-id="ea2f4-139">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ea2f4-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="ea2f4-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="ea2f4-140">NOTES</span></span>

## <span data-ttu-id="ea2f4-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea2f4-141">RELATED LINKS</span></span>

[<span data-ttu-id="ea2f4-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ea2f4-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="ea2f4-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ea2f4-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="ea2f4-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ea2f4-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="ea2f4-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ea2f4-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="ea2f4-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ea2f4-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="ea2f4-147">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ea2f4-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="ea2f4-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ea2f4-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
