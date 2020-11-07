---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: e0a200bf0930d847ba4a4576700221c4c8023ba9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684862"
---
# <span data-ttu-id="e0e7f-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e0e7f-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="e0e7f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e7f-103">Rimuove un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="e0e7f-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="e0e7f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0e7f-104">SYNTAX</span></span>

### <span data-ttu-id="e0e7f-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0e7f-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e7f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0e7f-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0e7f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0e7f-107">DESCRIPTION</span></span>
<span data-ttu-id="e0e7f-108">Il cmdlet **Remove-AzCdnProfile** consente di rimuovere un profilo CDN (Azure Content delivering Network).</span><span class="sxs-lookup"><span data-stu-id="e0e7f-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="e0e7f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0e7f-109">EXAMPLES</span></span>

## <span data-ttu-id="e0e7f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0e7f-110">PARAMETERS</span></span>

### <span data-ttu-id="e0e7f-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="e0e7f-111">-CdnProfile</span></span>
<span data-ttu-id="e0e7f-112">Specifica il profilo rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e7f-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e0e7f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0e7f-113">-DefaultProfile</span></span>
<span data-ttu-id="e0e7f-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e0e7f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0e7f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e0e7f-115">-Force</span></span>
<span data-ttu-id="e0e7f-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e0e7f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e0e7f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0e7f-117">-PassThru</span></span>
<span data-ttu-id="e0e7f-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e0e7f-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e0e7f-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e0e7f-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e0e7f-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e0e7f-120">-ProfileName</span></span>
<span data-ttu-id="e0e7f-121">Specifica il nome del profilo rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e7f-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e0e7f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0e7f-122">-ResourceGroupName</span></span>
<span data-ttu-id="e0e7f-123">Specifica il nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="e0e7f-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="e0e7f-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e0e7f-124">-Confirm</span></span>
<span data-ttu-id="e0e7f-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e7f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0e7f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0e7f-126">-WhatIf</span></span>
<span data-ttu-id="e0e7f-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0e7f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0e7f-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0e7f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0e7f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e7f-129">CommonParameters</span></span>
<span data-ttu-id="e0e7f-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0e7f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e7f-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0e7f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e7f-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0e7f-132">INPUTS</span></span>

### <span data-ttu-id="e0e7f-133">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="e0e7f-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="e0e7f-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e0e7f-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e0e7f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0e7f-135">OUTPUTS</span></span>

### <span data-ttu-id="e0e7f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e0e7f-136">System.Boolean</span></span>

## <span data-ttu-id="e0e7f-137">Note</span><span class="sxs-lookup"><span data-stu-id="e0e7f-137">NOTES</span></span>

## <span data-ttu-id="e0e7f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0e7f-138">RELATED LINKS</span></span>

[<span data-ttu-id="e0e7f-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e0e7f-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="e0e7f-140">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e0e7f-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="e0e7f-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e0e7f-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


