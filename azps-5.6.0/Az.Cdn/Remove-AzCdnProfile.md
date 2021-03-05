---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: 904af1f1d1f6cba7bd0a44ee0811b55fef01e106
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996896"
---
# <span data-ttu-id="54180-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="54180-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="54180-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54180-102">SYNOPSIS</span></span>
<span data-ttu-id="54180-103">Rimuove un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="54180-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="54180-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54180-104">SYNTAX</span></span>

### <span data-ttu-id="54180-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="54180-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54180-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54180-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54180-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="54180-107">DESCRIPTION</span></span>
<span data-ttu-id="54180-108">Il cmdlet **Remove-AzCdnProfile** rimuove un profilo rete per la distribuzione di contenuti (CDN) di Azure.</span><span class="sxs-lookup"><span data-stu-id="54180-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="54180-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54180-109">EXAMPLES</span></span>

## <span data-ttu-id="54180-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54180-110">PARAMETERS</span></span>

### <span data-ttu-id="54180-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="54180-111">-CdnProfile</span></span>
<span data-ttu-id="54180-112">Specifica il profilo rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54180-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54180-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54180-113">-DefaultProfile</span></span>
<span data-ttu-id="54180-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="54180-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54180-115">-Force</span><span class="sxs-lookup"><span data-stu-id="54180-115">-Force</span></span>
<span data-ttu-id="54180-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="54180-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="54180-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54180-117">-PassThru</span></span>
<span data-ttu-id="54180-118">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="54180-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="54180-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="54180-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54180-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="54180-120">-ProfileName</span></span>
<span data-ttu-id="54180-121">Specifica il nome del profilo rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54180-121">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54180-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54180-122">-ResourceGroupName</span></span>
<span data-ttu-id="54180-123">Specifica il nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="54180-123">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54180-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54180-124">-Confirm</span></span>
<span data-ttu-id="54180-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54180-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54180-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54180-126">-WhatIf</span></span>
<span data-ttu-id="54180-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54180-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54180-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54180-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54180-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54180-129">CommonParameters</span></span>
<span data-ttu-id="54180-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54180-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54180-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="54180-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54180-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="54180-132">INPUTS</span></span>

### <span data-ttu-id="54180-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="54180-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="54180-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="54180-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="54180-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54180-135">OUTPUTS</span></span>

### <span data-ttu-id="54180-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="54180-136">System.Boolean</span></span>

## <span data-ttu-id="54180-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="54180-137">NOTES</span></span>

## <span data-ttu-id="54180-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54180-138">RELATED LINKS</span></span>

[<span data-ttu-id="54180-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="54180-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="54180-140">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="54180-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="54180-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="54180-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


