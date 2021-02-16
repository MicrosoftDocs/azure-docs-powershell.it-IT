---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: ba45ea8d4c1b58290623f7f415f09cdb7663f575
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199447"
---
# <span data-ttu-id="4c006-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4c006-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="4c006-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c006-102">SYNOPSIS</span></span>
<span data-ttu-id="4c006-103">Rimuove un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="4c006-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="4c006-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c006-104">SYNTAX</span></span>

### <span data-ttu-id="4c006-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c006-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c006-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c006-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c006-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4c006-107">DESCRIPTION</span></span>
<span data-ttu-id="4c006-108">Il cmdlet **Remove-AzCdnProfile** rimuove un profilo rete per la distribuzione di contenuti (CDN) di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c006-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="4c006-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c006-109">EXAMPLES</span></span>

## <span data-ttu-id="4c006-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c006-110">PARAMETERS</span></span>

### <span data-ttu-id="4c006-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="4c006-111">-CdnProfile</span></span>
<span data-ttu-id="4c006-112">Specifica il profilo rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c006-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4c006-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c006-113">-DefaultProfile</span></span>
<span data-ttu-id="4c006-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="4c006-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c006-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4c006-115">-Force</span></span>
<span data-ttu-id="4c006-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="4c006-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4c006-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c006-117">-PassThru</span></span>
<span data-ttu-id="4c006-118">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="4c006-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4c006-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="4c006-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4c006-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4c006-120">-ProfileName</span></span>
<span data-ttu-id="4c006-121">Specifica il nome del profilo rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c006-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4c006-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c006-122">-ResourceGroupName</span></span>
<span data-ttu-id="4c006-123">Specifica il nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="4c006-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="4c006-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c006-124">-Confirm</span></span>
<span data-ttu-id="4c006-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c006-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c006-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c006-126">-WhatIf</span></span>
<span data-ttu-id="4c006-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c006-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c006-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c006-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c006-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c006-129">CommonParameters</span></span>
<span data-ttu-id="4c006-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c006-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c006-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4c006-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c006-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="4c006-132">INPUTS</span></span>

### <span data-ttu-id="4c006-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="4c006-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="4c006-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4c006-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4c006-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c006-135">OUTPUTS</span></span>

### <span data-ttu-id="4c006-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4c006-136">System.Boolean</span></span>

## <span data-ttu-id="4c006-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="4c006-137">NOTES</span></span>

## <span data-ttu-id="4c006-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c006-138">RELATED LINKS</span></span>

[<span data-ttu-id="4c006-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4c006-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="4c006-140">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4c006-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="4c006-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4c006-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


